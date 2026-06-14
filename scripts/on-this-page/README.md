---
source-git-commit: f59dc265b0de732b52e9d26b6ee510733d0d760e
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---
# &quot;이 페이지에서&quot; 상자 도구

상단의 표준 **&quot;이 페이지에서&quot;** 음영 상자를 추가하고 확인하는 도구
AJO 설명서 페이지. `.cursor/rules/on-this-page-box.mdc`에서 세부 항목을 참조하십시오.
롤아웃은 epic **DOCAC-14936**(최상위 폴더당 하나의 작업)에서 추적됩니다.

## 상자 모양

```text
# Page Title {#anchor}

>[!BEGINSHADEBOX]

**On this page:** <one clear sentence describing the page's purpose>

>[!ENDSHADEBOX]
```

## 권장 워크플로우(폴더/Jira 작업당)

저장소 루트(`journey-optimizer.en/`)에서 실행합니다.

1. **상자 삽입**(각 페이지의 앞부분에서 첫 번째 초안 문장 시드 중)
   `description`). 기계적, idempotent, 결코 프론트매스에 닿지 않음:

   ```bash
   python scripts/on-this-page/add_on_this_page.py help/using/reports --seed-from-description
   ```

   먼저 `--dry-run`(으)로 미리 봅니다.

2. **단어 세분화** 시드가 시작점입니다. 각 문장을 편집하십시오.
는 목적문 (한 문장, 일반 텍스트, 미국 영어)으로 읽습니다. **리드
이유**: 독자의 결과/이점(&quot;...을 기술하십시오. <outcome>&quot;), 아님
이 페이지가 다루는 항목의 목록입니다. 하우스 스타일 피쳐 이름 일치(예:
&quot;조정된 캠페인&quot;, &quot;인앱&quot;). `.cursor/rules/on-this-page-box.mdc`을(를) 참조하십시오. 다음을 수행하는 경우
`--seed-from-description`을(를) 건너뛰고 대신 `{{TODO...}}` 자리 표시자가 삽입되었습니다.
유효성 검사기는 남아 있는 모든 항목에 플래그를 지정합니다.

3. PR을 열기 전에 **유효성 검사**:

   ```bash
   python scripts/on-this-page/validate_on_this_page.py help/using/reports --require
   ```

   종료 코드는 모든 실패에서 0이 아니므로 CI를 게이트할 수 있습니다.

## 범위 / 제외

참조 및 구문 페이지는 기본적으로 제외됩니다(경로 부분 `api-reference`,
`expression`, `functions`). 필요한 경우 `--exclude ...`(으)로 재정의합니다.

## 보고서 전체 진행 상황 확인

```bash
python scripts/on-this-page/validate_on_this_page.py help
```

`--require`이(가) 없어도 상자가 없는 페이지는 `pending`(이)로 보고됩니다.
따라서 안내서에서 롤아웃 진행 상황을 추적할 수 있습니다.
