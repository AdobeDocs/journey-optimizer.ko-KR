---
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---
# 검증 라운드 — 필수 최종 품질 게이트

2번 게이트 2번이며 각 블록이 **유효하고 true이며 무료임을 보장하는 단계입니다.
모호성**. 단일 페이지 업데이트를 포함하여 **선택 사항이 아니며 건너뛸 수 없습니다**.

## 별개인 이유

블록 작성자(게이트 1)가 블록에 너무 가까워서 자신의 접지 오류를 catch할 수 없습니다. 게이트 2
은(는) **독립적인 적대적 다시 확인**입니다. 블록이 잘못되었을 수 있다고 가정하는 새로운 검토자입니다.
및 은(는) 페이지 본문을 사실로 사용하여 **only**&#x200B;을(를) 증명하려고 합니다. **별도의 하위 에이전트로 실행**
그것은 그 블록이 어떻게 쓰여졌는지를 보지 않았는데, 이 독립은 그것을 유효하게 만드는 것입니다. 대상
한 묶음의 페이지, 하나의 확인 프로그램 하위 에이전트가 전체 폴더를 처리할 수 있습니다.

## 페이지당 검증자의 작업

1. **전체 원본 페이지** `help/using/<folder>/<page>.md`을(를) 읽습니다. HTML-comment /
주석 처리된 콘텐츠는 **not** 올바른 소스입니다.
2. **블록** `help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md`을(를) 읽습니다.
3. **every** 클레임을 페이지 본문에 대해 접지됨/부정확함/접지되지 않음으로 분류합니다.
4. **블록 파일만 편집하여 모든 문제를 해결합니다** — 두 개의 고정된 열기 유지
단락, `+++ … +++` 펜스 및 동기화 설명. 소스 페이지는 수정하지 않습니다.
5. 페이지당 보고서: `clean` 또는 `N issues` + 적용된 정확한 수정 사항.

## 적대적 체크리스트(최고 위험 항목 먼저)

- **숫자 및 제한** 모든 값이 정확합니다. 제한은 페이지가 다음을 사용하는 경우에만 `(hard limit)`입니다.
적용/최대 단어; `(default)`(저장 가능/기본/구성 가능한 경우)(&quot;request&quot; 포함)
Adobe 담당자를 통해 추가 정보&quot; 또는 &quot;API를 통해 수집 가능&quot;); 조언을 위해 `(recommended)`; 아니요
페이지에 아무 것도 제공되지 않는 경우 한정자입니다. **하드 레이블이 지정된 생성기를 다운그레이드합니다.**
모든 처리량/속도 수치에는 그 범위가 적용됩니다.
- **날짜, ID, 제품/필드 이름, SQL 식별자, 상태 열거형, 오류 문자열** — 축어
을 클릭합니다. 규정 준수/법적 기간에 대한 완벽한 허용: SLA, 보존,
또는 시행 날짜; 페이지에서 날짜를 명시하고 페이지로 레이블이 지정된 대로 날짜를 유지합니다.
프레임을 지정합니다.
- **동의어와 혼동하지 않음** 동의어(`"A" = "B"`)에는 페이지에 두 양식이 모두 필요합니다
같은 뜻이야 모든 대비(`"X" ≠ "Y"`)는 &quot;혼동하지 마십시오&quot; 아래에 속합니다. 이동
잘못된 레이블.
- **확인/테스트 모드**이(가) 페이지의 정확한 용어로 이름이 지정되었으며, 해당 용어가 일치하지 않습니다.
클래식 및 재디자인 환경 또는 다양한 채널에서 사용할 수 있습니다.
- **접지를 연결하는 중.** 다른 페이지, 일반 제품 지식 또는 HTML에서 가져온 것이 없습니다.
댓글. 페이지 본문에서 지원하지 않는 모든 항목을 제거합니다.
- **스타일.** 축약 없음(축약 `[!UICONTROL ...]`/`[!DNL ...]` 문자열 외부). 없음
금지된 단어(&quot;합성&quot;, &quot;가짜 데이터&quot;, &quot;실제 데이터 없음&quot;, &quot;되돌리기&quot;, &quot;롤백&quot;) 중
페이지에서 버바텀하지 않는 한. UI 문자열이 정확하게 유지되었습니다.
- **구조.** 고정 열기 단락 2개가 그대로 있고 축어 적음, 6개 섹션이 있고
페이지가 지원하는 순서. 댓글이 표시됩니다.

## 재사용 가능한 검증자 하위 에이전트 프롬프트

폴더 및 페이지 목록을 입력합니다. 독립적인 범용 하위 에이전트로 실행합니다.

```
You are an ADVERSARIAL fact-checker for Adobe Journey Optimizer doc "AI Knowledge Reference"
blocks. Repo: <repo path>. Assume each block MAY contain errors; try hard to find them. This is
the final accuracy gate.

PAGES (basenames): <p1> <p2> ...
SOURCE: help/using/<folder>/<p>.md   BLOCK: help/_includes/do-not-localize/<folder>/ai-augmented-<p>.md

For EACH page:
1. Read the FULL source page body (HTML-comment / commented-out content is NOT valid source).
2. Read the block.
3. Classify EVERY claim GROUNDED / INACCURATE / NOT-GROUNDED against the page body. Scrutinize:
   numeric limits (hard only if the page uses enforcement/maximum wording; downgrade any
   raisable/default/configurable value the block marked hard; every rate figure needs its
   scope); dates/IDs/field names/SQL identifiers/status enums/error strings verbatim and no
   invented SLA/legal timeframes; Synonyms are true equivalents (mislabels -> Do not confuse);
   validation/test modes named with the page's exact terms and not conflated; nothing imported
   from other pages or HTML comments; no contractions (outside verbatim [!UICONTROL ...]); no
   banned words (synthetic / fake data / without real data / revert / roll back) unless verbatim.
4. FIX every issue by editing ONLY the block file. Preserve the two fixed opening paragraphs,
   the +++ ... +++ fences, and the sync comment. Do NOT modify source pages.

Report per page: "<p>: clean" or "<p>: N issues" + the exact fixes applied.
```

## 종료 기준

검증자가 모든 페이지를 `clean`(찾은 페이지)로 보고할 때만 폴더가 게이트 2를 전달합니다.
아무 것도 없거나, 수정 사항이 적용되었으며 블록이 깨끗해졌습니다). 수정을 적용한 경우 이미 다음과 같습니다
블록 파일에서 — 최종 보고서에 이를 포함하고 스윕 및 커밋을 수행합니다.
