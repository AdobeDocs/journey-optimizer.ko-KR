---
source-git-commit: c81615909e033d52fbed56f0195467a3e346a4be
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 1%

---
# 증강된 AIContent

Journey Optimizer 설명서 저장소에 있는 하나 이상의 Markdown 파일 끝에 자동 생성된 AI Assistant 아코디언을 추가합니다.

## 대상 저장소

`help/using/`(저장소 루트에 상대적)

## 아코디언 구문(Experience League)

```
+++Title of the accordion

Content here — any standard markdown is valid.

+++
```

**규칙:**
- 한 줄에 `+++Title` — 제목은 `+++` 바로 뒤에 옵니다.
- 한 줄에 `+++`만 있으면 아코디언이 닫힙니다.
- `+++` 열기 전과 `+++` 닫기 후 빈 줄

&#x200B;---

## 워크플로

### 1단계 — 대상 요청

사용자에게 묻기:
> 보강할 파일 또는 폴더를 선택하십시오.
> - 단일 파일: 저장소 루트에 상대적인 경로(예: `help/using/email/get-started-email.md`)
> - 폴더: 모든 `.md`개 파일이 반복적으로 사용됩니다(예: `help/using/email`).
> - 파일/폴더 목록

폴더를 지정한 경우 처리하기 전에 찾은 `.md`개 파일을 나열하고 확인하십시오.

### 2단계 — 각 파일에 대해 읽기 및 생성

1. **전체 파일 읽기**.
2. **페이지 주제 이해** — 어떤 기능, 개념 또는 작업을 다루고 있습니까?
3. 아래 콘텐츠 생성 규칙을 사용하여 **아코디언 콘텐츠를 생성**&#x200B;합니다.
4. **생성 후 유효성 검사 목록 실행**(아래 참조) — 건너뛰지 마십시오.
5. **AI 아코디언이 끝에 이미 있는지 확인**(끝 근처에 `+++AI Knowledge Reference`이(가) 있는지 확인). 그렇다면 사용자에게 바꾸기 또는 건너뛰기를 요청하시겠습니까?

### 3단계 — 아코디언 추가

아래 **콘텐츠 생성 규칙**&#x200B;에 정의된 고정 시작 블록과 전체 템플릿을 사용하십시오. 파일의 맨 끝에 을 추가한 다음 동기화 주석을 즉시 추가합니다.

```
<!-- ai-accordion-version: 1 | source-hash: [first 8 chars of MD5 of file content before accordion] -->
```

이 주석을 사용하면 향후 도구 및 작성자가 페이지 본문이 아코디언에서 이동된 시기를 감지할 수 있습니다. 다른 콘텐츠는 수정하지 마십시오.

### 4단계 — 보고서

- 수정된 파일 ✓
- 건너뛴 파일 + 이유(이미 아코디언/빈/인덱스 페이지가 있음)
- 2단계 동안 발생한 모든 유효성 검사 경고

&#x200B;---

## 컨텐츠 생성 규칙

페이지를 분석하고 **다음** 아래 섹션을 Markdown 글머리 기호 목록으로 생성합니다. 의미 있는 컨텐츠를 추출할 수 없는 섹션을 건너뜁니다.

### 아코디언 제목 및 고정 열기 — 축어(수정하지 않음)

모든 아코디언은 이 정확한 블록으로 시작해야 합니다. 그대로 복사하십시오. 다음을 의역하거나 응축하거나 재정렬하지 마십시오.

```
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

이 두 단락 바로 뒤에 생성된 콘텐츠 섹션이 옵니다.

### 1. TL;DR

페이지에서 가르치거나 사용할 수 있는 내용에 대한 한 문장 요약입니다.

```
- **TL;DR:** [one sentence]
```

### &#x200B;2. 의도

3-6 사용자가 이 페이지를 읽고 수행할 수 있는 작업.

```
**Intents:**
- [action]
- [action]
```

### &#x200B;3. 용어집

짧은 정의가 있는 이 페이지/기능에 관련된 주요 용어입니다. 제품별 용어에 플래그를 지정합니다.

```
**Glossary:**
- **[Term]**: [definition] *(product-specific)*
```

이 페이지와 관련된 용어만 포함합니다. 일반적인 마케팅 용어로 패딩하지 마십시오.

**유효성 검사 모드 정밀도 규칙 — 필수:**
이 페이지에서 테스트, 미리 보기 또는 시뮬레이션 실행 형식을 다루는 경우에는 페이지가 실제로 설명하는 모든 모드를 구분해야 합니다. 개별 모드를 하나의 축약 항목으로 축소하지 마십시오.
- **시뮬레이션** — 보내지 않고 메시지 콘텐츠를 렌더링하고 실제 프로필을 사용합니다.
- **테스트 모드** — 지정된 테스트 프로필에만 전송하고, 영구 AEP 테스트 프로필(합성 프로필 또는 가짜 프로필 아님)을 사용합니다.
- **시험 실행** — 작업을 활성화하지 않고 전체 여정 논리를 실행하고 실제 대상 데이터를 사용합니다.

페이지에 있는 모드만 포함합니다. 페이지 본문에서 제품 정확성 용어를 복사합니다. 이러한 용어에 대해 &quot;합성 프로필&quot;, &quot;가짜 데이터&quot; 또는 &quot;실제 데이터 없음&quot;을 대체하지 마십시오.

### &#x200B;4. 가드레일

페이지에 언급된 제한 사항, 사전 요구 사항, 권한 또는 제한 사항.

```
**Guardrails:**
- [guardrail]
```

**보호 정밀도 규칙 — 필수:**

- **모든 숫자 제한을 정규화합니다**. 예: &quot;최대 10개의 데이터 세트 조회&quot;가 아닌 &quot;메시지당 최대 10개의 데이터 세트 조회(엄격한 제한)&quot;.
- **해당 범위를 사용하여 모든 처리량 또는 속도 도형**&#x200B;을(를) 검증합니다. 예: &quot;150,000개의 메시지/시간 상한&quot;이 아닌 &quot;150,000개의 메시지/시간 상한(샌드박스당)&quot;.
- **페이지 본문에 대해 모든 가드레일을 상호 확인**&#x200B;한 후 포함하십시오. 페이지에 10이라고 표시되고 아코디언에 5라고 표시되면 아코디언이 잘못된 것입니다. 페이지 본문은 신뢰할 수 있습니다.
- **페이지에 명시되지 않은 가드레일을 유추하지 마십시오**. 제약조건이 존재하지만 페이지에 제약조건이 명시되지 않은 경우 이를 생략합니다.

### &#x200B;5. 용어

정식 이름, 두문자어, 허용된 변형, 동의어, 명확화. 주로 AI 파이프라인 표준화에 사용됩니다.

```
**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [list]
- Synonyms: "[term A]" = "[term B]"
- Do not confuse: "[term]" ≠ "[other term]"
```

**상태 및 라이프사이클 정밀도 규칙:**
페이지가 라이프사이클(여정 상태, 메시지 상태, 캠페인 상태 등)을 설명하는 경우 페이지 본문에서 정확한 상태 레이블을 복사합니다. 의역하지 마십시오. &quot;혼동하지 마십시오&quot; 항목을 사용하여 루트 단어를 공유하지만 고유한 의미를 갖는 상태를 명확히 합니다. 예:

```
- Do not confuse: "Stop" (user-initiated action) ≠ "Stopped" (resulting status) ≠ "Close" (action on Live journey allowing in-progress profiles to finish) ≠ "Closed" (resulting status)
```

### 6. FAQ

사용자가 질문할 수 있는 3~6개의 질문과 짧은 답변을 제공합니다.

```
**FAQ:**
- **Q: [question]** — [short answer]
```

**FAQ 정밀도 규칙:**
답변은 페이지 본문과 동일한 동사와 명사 선택 사항을 사용해야 합니다. 페이지에서 &quot;되돌리기&quot;, &quot;재설정&quot; 또는 &quot;롤백&quot;과 같은 동사를 사용하지 마십시오. 전환이 세션을 종료하는 경우(예: 테스트 모드를 종료하면 여정이 이전 상태로 돌아감) &quot;여정이 초안으로 되돌아감&quot;을 말하지 마십시오.

### 포함하지 않을 항목

- 본문 내용을 **다시 작성하거나 요약하지 마십시오(**)(이미 페이지에 있음).
- **not**&#x200B;에 단계별 지침 포함
- 페이지에서 지원하지 않는 콘텐츠를 **만들 수 없음**
- 페이지 본문에 &quot;합성&quot;, &quot;가짜 데이터&quot;, &quot;실제 데이터 없음&quot;, &quot;되돌리기&quot;, &quot;롤백&quot;(제품 상태 전환을 설명할 때)과 같은 잘못된 용어가 버바텀 방식으로 표시되지 않는 한 **not**&#x200B;에서 사용하지 마십시오.

&#x200B;---

## 생성 후 유효성 검사 목록

추가하기 전에 모든 아코디언에서 이 체크리스트를 실행하십시오. 계속하기 전에 사용자에게 모든 실패를 플래그로 표시합니다.

### 가드레일 점검
- [ ] 아코디언에 있는 모든 숫자 값은 축어 또는 페이지 본문에서 파생될 수 있습니다.
- [ ] 모든 제한이 권장 또는 하드 제한에 적합함
- [ ] 모든 처리량 수치에는 해당 범위(샌드박스/조직/인스턴스)가 포함됩니다.

### 용어 확인
- [ ] 페이지에 있는 모든 유효성 검사 모드(시뮬레이션, 테스트 모드, 시험 실행)가 포함되어 있으며 페이지 정확성 용어로 이름이 지정됩니다.
- [ ] 모든 라이프사이클 상태는 페이지 본문의 정확한 레이블을 사용합니다
- [ ] 페이지에 존재하지 않는 한 FAQ 답변에 정확하지 않은 동사(&quot;되돌리기&quot;, &quot;합성&quot;, &quot;가짜 데이터&quot;, &quot;실제 데이터 없음&quot;)가 없습니다

### 범위 확인
- [ ] 용어집에 페이지와 관련이 없는 일반 마케팅 용어가 포함되어 있지 않습니다.
- [ ]개의 FAQ 답변에 페이지에 없는 정보가 포함되어 있지 않습니다.

검사에 실패한 경우 추가하기 전에 아코디언을 수정하십시오. 4단계 보고서에 수정 사항을 기록합니다.

&#x200B;---

## 동기화 권한

아코디언은 특정 시점의 페이지 본문을 미분한 것입니다. 페이지의 일부로 처리되어야 합니다.

**페이지 본문을 업데이트할 때(PR 릴리스, 수정 등):**
- 업데이트로 인해 아코디언에 설명된 보호, 제한, 상태 레이블 또는 유효성 검사 모드가 변경되면 동일한 PR에서 아코디언을 재생성하거나 수동으로 업데이트할 → 있습니다.
- 업데이트가 아코디언 콘텐츠와 관련이 없는 경우(예: 절차 단계, 스크린샷 업데이트) → 아코디언은 변경되지 않고 간단하게 검토할 수 있습니다.

아코디언(`<!-- ai-accordion-version -->`) 뒤에 추가된 동기화 주석은 신호입니다. 해당 해시가 작성된 이후 아코디언 앞의 파일 콘텐츠가 변경된 경우 아코디언은 검토 대상입니다.

&#x200B;---

## 전체 템플릿

```markdown
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.

- **TL;DR:** [one sentence]

**Intents:**
- [intent]

**Glossary:**
- **[Term]**: [definition]

**Guardrails:**
- [guardrail — type: recommended|hard — scope: sandbox|org]

**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [variants]
- Synonyms: "[a]" = "[b]"
- Do not confuse: "[x]" ≠ "[y]"

**FAQ:**
- **Q: [question]** — [short answer]

+++
<!-- ai-accordion-version: 1 | source-hash: [hash] -->
```

&#x200B;---

## 참고

- 품질을 위해 파일을 하나씩 처리합니다.
- 매우 짧은 페이지 또는 인덱스 전용 페이지에 플래그를 지정하고 건너뛸 것인지 여부를 사용자에게 묻습니다.
- 새 파일을 만들지 않습니다. 기존 `.md`개 파일만 편집하십시오.
- 사후 생성 유효성 검사 목록은 선택 사항이 아닙니다. 대량 작업을 포함하여 모든 파일에 대해 실행합니다.
