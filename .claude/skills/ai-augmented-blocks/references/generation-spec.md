---
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 4%

---
# 생성 사양 — AI 기술 자료 블록

AI 참조 블록에 포함된 내용과 그 방식에 대한 단일 소스
작성됨. 모든 페이지에 대해 정확하게 따르십시오. (기존 미러링됨)
`.claude/commands/augmentedAIContent.md`; 기술은 표준 버전입니다.)

## 황금률

블록에 **자체 페이지 본문에서 파생할 수 있는 항목만 포함될 수 있습니다.** 다른 페이지 아님, 아님
HTML 주석 처리/주석 처리된 컨텐츠가 아닌 일반 제품 지식입니다. 페이지에
블록도 마찬가지입니다.

## 아코디언 + 포함 구문

```
+++ AI Knowledge Reference

Content here — standard markdown.

+++
```

- `+++ AI Knowledge Reference`이(가) 열립니다(`+++` 뒤에 한 칸). `+++`만 닫힙니다.
- 여는 `+++` 앞과 닫는 `+++` 뒤에 빈 줄이 있습니다.
- 제목은 항상 정확히 `AI Knowledge Reference`입니다.
- 현지화하지 않음(do-not-localize)에 있는 전체 아코디언이며 와 함께 가져옵니다.
  `{{$include /help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md}}`. 아래에 콘텐츠
  `help/_includes/do-not-localize/`은(는) 지역화에서 제외됩니다. 이렇게 하면 블록이 유지됩니다.
  번역되지 않았습니다.

## 파일 구조 포함

```
---
title: AI Knowledge Reference
---
# AI Knowledge Reference

+++ AI Knowledge Reference

[fixed opening — verbatim]

[the six sections in order]

+++

<!-- ai-section-version: 1 | source-hash: <first 8 chars of md5 of page body> -->
```

- **파일 이름:**&#x200B;은(는) 최상위 수준의 페이지 경로에서 파생됩니다. `help/using/<folder>/`
섹션: `.md`을(를) 제거하고 나머지 `/`을(를) `-`(으)로 바꾸고 접두사를 `ai-augmented-`(으)로 바꿉니다.
  - `help/using/building-journeys/end-journey.md` → `ai-augmented-end-journey.md`
  - `help/using/building-journeys/expression/journey-properties.md` →
    `ai-augmented-expression-journey-properties.md`
- 최상위 수준 섹션당 하나의 하위 폴더(`building-journeys/`, `email/`, `data/`, ...).

## 고정 열기 — 수직적, 수정 안 함

모든 블록은 정확하게 이 두 단락에서 시작됩니다. 바이트 단위로 복사. 의역하지 않음,
압축 또는 순서 바꾸기:

```
This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

## 순서대로 여섯 개의 섹션

페이지에서 의미 있는 콘텐츠를 생성하지 않는 경우에만 섹션을 건너뜁니다.

### 1. TL;DR
한 문장: 페이지에서 가르치거나 사용할 수 있는 문장. `* **TL;DR:** [one sentence]`

### &#x200B;2. 의도
3-6 사용자가 페이지를 읽은 후 수행할 수 있는 작업.

### &#x200B;3. 용어집
짧은 정의가 있는 주요 페이지별 용어, 다음으로 제품별 용어 플래그 지정
`*(product-specific)*`. 일반 마케팅 패딩 없음.

**유효성 검사 모드 전체 자릿수(필수):** 페이지가 테스트/미리 보기/시뮬레이션을 다루는 경우
실행, 페이지에서 실제로 이름을 지정하는 모든 모드를 구분합니다. 축소하지 마십시오. 답변을 읽을 때마다
페이지의 정확한 용어(예: `Simulate content`, `Simulate content (AEP profiles)`,
`Send proof`, `Test mode`, `Dry run`, `Simulation`, `test profile`, `sample input`). 사용 안 함
모든 프로필에 대해 &quot;합성 프로필&quot;, &quot;가짜 데이터&quot; 또는 &quot;실제 데이터 없음&quot;을 대체합니다.

### &#x200B;4. 가드레일
페이지에 명시된 제한, 사전 요구 사항, 권한, 제한.

- **모든 숫자 제한을 `(hard limit)` 또는 `(recommended)`(으)로 한정합니다**. 하지만&#x200B;**&#x200B;**
페이지에서 강제 적용 문구를 사용합니다(오류/거부됨/최대값/다음을 초과할 수 없음/만 지원됨).
또는 추천 단어(최상의 성능을 위해/권장됨)입니다. 페이지에 이 표시되지 않는 경우
한정자를 지정하지 않습니다. **상승 가능, 기본 또는 구성 가능한 값에 하드 레이블을 지정하지 마십시오.**
&quot;Adobe 담당자에게 연락하여&quot; 또는 API를 통해 제기할 수 있는 값은 다음과 같습니다
  `(default)`, 어렵지 않음.
- **모든 처리량/속도 수치를 해당 범위로 한정합니다**(샌드박스/조직/인스턴스 당).
- **페이지 본문에 대해 모든 숫자를 상호 확인합니다.** 페이지 본문은 신뢰할 수 있습니다.
- **유추하지 마십시오** 페이지에서 설명하지 않는 보호 기능. 메타 설명 없음(&quot;페이지가 표시되지 않음
지정...&quot;).

### &#x200B;5. 용어
정식 이름, 약어, 변형, 동의어, 명확화

- **동의어**(`"A" = "B"`)은(는) **true 해당 항목**&#x200B;에만 해당됩니다. 두 양식은 모두 페이지에 표시되어야 합니다.
같은 뜻이야 *대비*&#x200B;인 모든 항목이 **혼동하지 마십시오.**
(`"X" ≠ "Y"`), 동의어가 아닙니다.
- **상태/라이프사이클 정밀도:** 페이지 본문에서 정확한 상태 레이블을 복사합니다.
의역하십시오. 루트 단어를 공유하는 상태를 구분하려면 &quot;혼동하지 마십시오&quot;를 사용하십시오.

### 6. FAQ
3-6개의 질문에 짧은 대답을 제공합니다. 답변에서는 페이지와 같은 **동사와 명사를 사용합니다.
body**. 페이지에서 &quot;되돌리기&quot;, &quot;재설정&quot; 또는 &quot;롤백&quot;을 사용하지 마십시오.

## 포함하지 않을 항목

- 본문 내용을 다시 작성하거나 요약하지 않거나 단계별 지침을 제공하지 않습니다.
- 페이지에서 지원하지 않는 콘텐츠를 만들지 마십시오.
- 이 부정확한 용어는 페이지에 **축어**&#x200B;로 표시되지 않는 한 사용하지 마십시오.
&quot;합성&quot;, &quot;가짜 데이터&quot;, &quot;실제 데이터 없음&quot;, &quot;되돌리기&quot;, &quot;롤백&quot;.
- **수축하지 않음** 블록 산문에서 &quot;is not&quot;, &quot;does not&quot;, &quot;cannot&quot;,
&quot;다음과 같습니다.&quot; 등(유일한 예외는 다음과 같은 축어 제품 UI 문자열입니다.
  `[!UICONTROL configuration doesn't exist]`(정확히 유지됨)

## 3단계 — 모든 클레임 확인(자체 점검, 게이트 1)

포함을 작성하기 전에 클레임별로 생성된 콘텐츠 클레임을 다시 읽으십시오. 필수, 해당
짧은 페이지입니다. 쓰기 전에 오류를 수정하고 보고서에 수정 내용을 기록합니다.

- 블록의 모든 용어/레이블/UI 이름이 페이지 본문에 표시됩니다.
- 두 양식이 페이지에 나타나지 않으면 동의어가 없습니다. 모든 &quot;혼동하지 마십시오&quot;는 참조만 합니다.
이 페이지의 개념
- 모든 숫자 값은 페이지 본문과 정확히 일치합니다. 모든 제한 한정자는
페이지의 문구. 한정자를 발명하지 않았습니다.
- 다른 페이지 또는 일반 지식에서 가져온 용어집/FAQ 세부 정보가 없습니다.
- 페이지에서 축어하지 않는 한 금지된 부정확한 용어는 없으며, 수축도 없습니다.

## 세대 후 체크리스트(게이트 1, 계속)

- [ ] 모든 숫자 값이 축어 형식으로 존재하거나 페이지 본문에서 파생될 수 있습니다.
- [ ] 모든 제한이 올바르게 정규화되었습니다(하드 및 권장 대 없음). 기본값/상승 가능 값 없음
 딱딱한 것으로 잘못 표시됨.
- [ ] 모든 처리량 수치에는 해당 범위가 있습니다.
- [ ] 페이지에 있는 모든 유효성 검사 모드의 이름은 페이지 정확성 용어로 지정됩니다.
- [ ] 모든 주기 상태는 정확한 페이지 레이블을 사용합니다.
- [ ] 동의어는 true와 같습니다. 대비는 &quot;혼동 안 함&quot; 아래에 있습니다.
- [ ] 금기 단어 없음/수축 없음(축어 UI 문자열 외부).
- [ ] 용어집에는 일반 용어가 없습니다. FAQ에 페이지에 없는 내용이 없습니다.

게이트 1은 자신의 작품을 점검하는 블록 작성자입니다. **바꾸기**&#x200B;하지 않습니다.
`verification-round.md`의 독립 인증 라운드(게이트 2).
