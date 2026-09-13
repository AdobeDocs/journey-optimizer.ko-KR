---
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 2%

---
# Git, PR 및 JIRA 추적

변경 사항을 안전하게 랜딩하고 추적하는 방법. 작성자의 두 가지 엄격한 규칙:

1. **PR을 열기 전에 묻기** 상관없이 블록을 생성하고 검증하되 풀만 엽니다.
작성자가 예라고 하면 요청합니다.
2. **병합 안 함.** 이러한 PR은 사람의 검토를 위해 존재합니다. 병합은 항상 저자의 결정입니다.

## 구조적 스윕(커밋하기 전에 실행)

폴더에서 처리된 모든 페이지에 대해:

```bash
cd <repo>
for p in <page1> <page2> ...; do
  f="help/_includes/do-not-localize/<folder>/ai-augmented-$p.md"
  inc="help/using/<folder>/$p.md"
  [ -f "$f" ] || echo "MISSING BLOCK: $f"
  grep -q '^# AI Knowledge Reference' "$f"            || echo "$p: missing H1"
  grep -q '^+++ AI Knowledge Reference' "$f"          || echo "$p: missing accordion open"
  grep -q 'This section contains structured knowledge' "$f" || echo "$p: missing opening para 1"
  grep -q 'ai-section-version' "$f"                   || echo "$p: missing sync comment"
  grep -nEi "\b(isn't|aren't|don't|doesn't|didn't|can't|won't|wouldn't|couldn't|shouldn't|it's|we've|we're|you're|they're|that's|there's|haven't|hasn't|wasn't|weren't)\b" "$f" \
    | grep -vi 'UICONTROL' && echo "  ^ $p contraction"
  grep -q "do-not-localize/<folder>/ai-augmented-$p.md" "$inc" || echo "$p: MISSING include in page"
done
echo "=== sweep done ==="
git status --short
```

인쇄된 줄(&quot;스윕 완료&quot; 및 `git status` 목록 제외)은 이전에 수정해야 할 결함입니다
커밋하고 있습니다.

## 분기 및 커밋(본에서 커밋 안 함)

```bash
git checkout main -q && git pull -q origin main
git checkout -q -b DOCAC-<key> origin/main    # branch name = the JIRA task key
# ... generate + verify + sweep ...
git add help/_includes/do-not-localize/<folder>/ help/using/<folder>/*.md
git commit -q -m "DOCAC-<key> Add AI Knowledge Reference blocks (<folder>)

<one-line what + the verification result>

Co-Authored-By: Claude <model> <noreply@anthropic.com>"
```

**커밋이`main`**이 아닌 분기에 도착했는지 확인(전환한 경우)
`main` 페이지를 검사하려면 나중에 커밋할 수 있습니다.):

```bash
git rev-parse --abbrev-ref HEAD                    # must print DOCAC-<key>
git rev-list --left-right --count origin/main...DOCAC-<key>   # must show  0<TAB>1
```

커밋이 `main`에 실수로 랜딩한 경우 `git branch -f DOCAC-<key> <sha>`이(가) 분기를 가리킵니다.
`git checkout DOCAC-<key>`을(를) 시작한 다음 `git branch -f main origin/main`을(를) 클릭하여 로컬 주 항목을 재설정합니다.
`origin/main`은(는) 로컬 오류의 영향을 받지 않습니다.

푸시: `git push -u origin DOCAC-<key>`(분기가 이미 있는 경우 `--force-with-lease` 사용)
이전 커밋에서 원격으로 사용).

## PR에 대해 묻기

작성자에게 명확하게 질문하십시오(예: `<folder>`에 대해 생성 및 확인된 *&quot; 블록). 원하세요?
검토할 PR을 열까요?&quot;* 예인 경우에만:

```bash
gh pr create --base main --head DOCAC-<key> \
  --title "DOCAC-<key> Add AI Knowledge Reference blocks (<folder>)" \
  --body-file <pr-body>.md
```

PR 본문은 필수 속성 라인으로 끝납니다
(`🤖 Generated with [Claude Code](https://claude.com/claude-code)`). **병합 안 함** — 나가기
검토를 위해 PR이 열립니다.

## JIRA 추적

DOCAC 작업의 모든 변경 내용을 추적합니다(롤아웃 서사: `DOCAC-15582`). 폴더 찾기 또는 만들기
작업, 다음:

1. 변경 내용 및 확인 결과(적용/건너뛴 페이지, 확인자)가 포함된 **댓글**
정리/수정됨, 주목할 만한 하드 및 기본 호출). 열려 있는 경우 PR 링크를 포함합니다.
2. **수정 버전을 설정**(이 프로그램은 `AJO26.9`을 사용함).
3. 워크플로우에 따라 **전환**진행 중인 새 → 문제→ 해결되었습니다(해결 방법 &quot;수정됨&quot;). 이 항목
프로젝트 전환 id가 `4`(시작 진행률)인 다음 `5`(해결 방법 포함)입니다.
   `{"name":"Fixed"}`); &quot;새로 만들기&quot;에 있는 작업은 먼저 시작해야 해결할 수 있습니다.

회사 JIRA MCP 도구 사용(`fixVersions`에 대해 `add_jira_comment`, `update_jira_issue`,
`bulk_transition_jira_issues`) 또는 JIRA UI입니다. JIRA 액세스가 부족한 경우 이 단계를
누가 가져와서 보고서에 기록합니다.

## 폴더 1개 = 분기 1개 = 작업 1개

관련 없는 폴더를 단일 분기 또는 PR에서 혼합하지 마십시오. 나중에 추가된 새 페이지는 크기가 작습니다.
팀이 원하는 대로 폴더 작업을 공유하거나 가져올 수 있습니다(만들기 모드).
