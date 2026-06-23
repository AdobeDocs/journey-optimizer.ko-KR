---
name: ajo-ai-accordion
description: 각 Markdown 파일의 끝에 추가된 AI Assistant 아코디언 섹션을 통해 Adobe Journey Optimizer 설명서 페이지를 강화합니다. 각 페이지를 읽고, 페이지 주제를 기반으로 관련 AI Assistant 콘텐츠를 자동 생성한 다음 축소 가능한 아코디언으로 삽입합니다. 사용자가 AJO 문서에 AI 정보를 추가하거나, AI 콘텐츠가 있는 AJO Markdown 페이지를 보강하거나, AI 아코디언 섹션이 있는 Markdown 파일의 파일 또는 폴더를 처리하려는 경우 사용합니다.
disable-model-invocation: true
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 1%

---


# AJO AI 아코디언 강화

Journey Optimizer 설명서 저장소에 있는 하나 이상의 Markdown 파일 끝에 자동 생성된 AI Assistant 아코디언을 추가합니다.

## 대상 저장소

`/Users/sauviat/GitHub/GHEC/journey-optimizer.en/help/using/`

## 아코디언 구문(Experience League)

```markdown
+++Title of the accordion

Content here — any standard markdown is valid.

+++
```

**규칙:**
- 한 줄에 `+++Title` — `+++` 바로 뒤에 제목이 있으며 그 사이에 공백이 없습니다.
- 한 줄에 `+++`만 있으면 아코디언이 닫힙니다.
- `+++` 열기 전과 `+++` 닫기 후 빈 줄

&#x200B;---

## 워크플로

### 1단계 — 대상 요청

사용자에게 묻기:

> 보강할 파일 또는 폴더를 선택하십시오.
> - 단일 파일: 저장소 루트에 상대적인 경로(예: `help/using/email/get-started-email.md`)
> - 폴더: 내의 모든 `.md`개 파일을 재귀적으로 처리합니다(예: `help/using/email`).
> - 파일/폴더 목록

가능한 경우 `AskQuestion`을(를) 사용하고, 그렇지 않은 경우 대화로 질문하십시오.

폴더를 지정한 경우 처리하기 전에 찾은 모든 `.md`개 파일을 나열하고 사용자에게 확인하십시오.

### 2단계 — 각 파일에 대해 읽기 및 생성

모든 대상 파일에 대해:

1. **전체 파일 읽기**.
2. **페이지 주제 이해** — 어떤 기능, 개념 또는 작업을 다루고 있습니까?
3. 아래 콘텐츠 생성 규칙을 사용하여 **아코디언 콘텐츠를 생성**&#x200B;합니다.
4. **AI 아코디언이 파일의 끝에 이미 있는지 확인**(끝 근처에 `+++`이(가) 있는지 확인). 있는 경우 교체할지 또는 건너뛸 것인지 사용자에게 묻습니다.

### 3단계 — 아코디언 추가

파일의 맨 끝에 를 추가합니다.

```markdown
+++[ACCORDION_TITLE]

[GENERATED_CONTENT]

+++
```

파일의 다른 콘텐츠는 수정할 수 없습니다.

### 4단계 — 보고서

모든 파일이 처리된 후:
- 수정된 목록 파일 ✓
- 건너뛴 파일 및 이유 목록(이미 아코디언이 있음, 빈 파일, 관련 없음 등)

&#x200B;---

## 컨텐츠 생성 규칙

Markdown 페이지를 분석하여 아코디언 콘텐츠를 생성합니다. Markdown 글머리 기호 목록으로 서식이 지정된 다음 섹션 **순서대로**&#x200B;을 생성합니다. 페이지에서 의미 있는 컨텐츠를 추출할 수 없는 섹션은 건너뜁니다.

&#x200B;---

### 어코디언 제목

사용: `+++AI Assistant — Page context`

&#x200B;---

### 생성할 섹션(순서대로)

**1. TL;DR**

한 문장. 이 페이지에서는 무엇을 가르치거나 활성화합니까?

```markdown
- **TL;DR:** [one sentence summary]
```

&#x200B;---

**2. 의도**

사용자가 이 페이지를 읽은 후 수행할 수 있는 작업(3~6개 항목)의 글머리 기호 목록입니다.

```markdown
**Intents:**
- [action the user can perform]
- [action the user can perform]
```

&#x200B;---

**3. 용어집**

짧은 정의가 있는 이 페이지/기능에 관련된 주요 용어입니다. 제품별 용어에 플래그를 지정합니다.

```markdown
**Glossary:**
- **[Term]**: [definition] *(product-specific)*
- **[Term]**: [definition]
```

이 페이지의 주제와 관련된 용어만 포함합니다. 일반적인 마케팅 용어로 패딩하지 마십시오.

&#x200B;---

**4. 보호 기능**

페이지에 언급된 제한 사항, 사전 요구 사항, 권한 또는 제한 사항.

```markdown
**Guardrails:**
- [guardrail or prerequisite]
- [guardrail or prerequisite]
```

&#x200B;---

**5. 용어**

정식 제품 이름, 약어, 허용된 변형, 동의어 및 명확화 힌트. 이 섹션은 주로 AI 파이프라인 표준화에 사용됩니다.

```markdown
**Terminology:**
- Canonical name: [e.g. Adobe Journey Optimizer]
- Acronym: [e.g. AJO] — variants: [e.g. Journey Optimizer, A-JO]
- Synonyms: [e.g. "brand guidelines" = "brand rules", "branding standards"]
- Do not confuse: [e.g. "AI Assistant" ≠ "Adobe Sensei"]
```

페이지에 있거나 암시된 항목만 포함합니다.

&#x200B;---

**6. FAQ**

3-6 사용자가 이 페이지의 콘텐츠에 대해 물어볼 수 있는 질문과 간단한 답변을 제공합니다.

```markdown
**FAQ:**
- **Q: [question]** — [short answer]
- **Q: [question]** — [short answer]
```

&#x200B;---

### 포함하지 않을 항목

- 페이지의 본문 내용(이미 있음)을 **다시 작성하거나 요약하지**&#x200B;마십시오.
- **not**&#x200B;에 단계별 지침(페이지에 있음)을 포함하십시오.
- 페이지에서 지원하지 않는 콘텐츠를 **만들 수 없습니다**.

&#x200B;---

### 전체 아코디언 템플릿

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
- [guardrail]

**Terminology:**
- Canonical name: [name]
- Acronym: [acronym] — variants: [variants]

**FAQ:**
- **Q: [question]** — [short answer]

+++
```

&#x200B;---

## 참고

- 파일을 일괄적으로 처리하지 않고 하나씩 처리하여 생성 품질을 높입니다.
- 페이지가 매우 짧거나 순전히 리디렉션/인덱스 페이지인 경우 플래그를 지정하고 사용자에게 건너뛸 것인지 묻습니다.
- 새 파일을 만들지 않습니다. 기존 `.md`개 파일만 편집하십시오.
