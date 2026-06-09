---
source-git-commit: 80e67d5a60b6427ff87e106e37bf6794ac76a210
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 3%

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
3. 아래 규칙을 사용하여 **아코디언 콘텐츠를 생성**&#x200B;합니다.
4. **AI 아코디언이 끝에 이미 있는지 확인**(끝 근처에 `+++AI Assistant`이(가) 있는지 확인). 그렇다면 사용자에게 바꾸기 또는 건너뛰기를 요청하시겠습니까?

### 3단계 — 아코디언 추가

파일의 맨 끝에 를 추가합니다. 다른 콘텐츠는 수정하지 마십시오.

### 4단계 — 보고서

- 수정된 파일 ✓
- 건너뛴 파일 + 이유(이미 아코디언/빈/인덱스 페이지가 있음)

&#x200B;---

## 컨텐츠 생성 규칙

페이지를 분석하고 **다음** 아래 섹션을 Markdown 글머리 기호 목록으로 생성합니다. 의미 있는 컨텐츠를 추출할 수 없는 섹션을 건너뜁니다.

### 어코디언 제목

`+++AI Assistant — Page context`

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

### &#x200B;4. 가드레일

페이지에 언급된 제한 사항, 사전 요구 사항, 권한 또는 제한 사항.

```
**Guardrails:**
- [guardrail]
```

### &#x200B;5. 용어

정식 이름, 두문자어, 허용된 변형, 동의어, 명확화. 주로 AI 파이프라인 표준화에 사용됩니다.

```
**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [list]
- Synonyms: "[term A]" = "[term B]"
- Do not confuse: "[term]" ≠ "[other term]"
```

### 6. FAQ

사용자가 질문할 수 있는 3~6개의 질문과 짧은 답변을 제공합니다.

```
**FAQ:**
- **Q: [question]** — [short answer]
```

### 포함하지 않을 항목

- 본문 내용을 **다시 작성하거나 요약하지 마십시오(**)(이미 페이지에 있음).
- **not**&#x200B;에 단계별 지침 포함
- 페이지에서 지원하지 않는 콘텐츠를 **만들 수 없음**

### 전체 템플릿

```markdown
+++AI Assistant — Page context

- **TL;DR:** [one sentence]

**Intents:**
- [intent]

**Glossary:**
- **[Term]**: [definition]

**Guardrails:**
- [guardrail]

**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [variants]
- Synonyms: "[a]" = "[b]"
- Do not confuse: "[x]" ≠ "[y]"

**FAQ:**
- **Q: [question]** — [short answer]

+++
```

&#x200B;---

## 참고

- 품질을 위해 파일을 하나씩 처리합니다.
- 매우 짧은 페이지 또는 인덱스 전용 페이지에 플래그를 지정하고 건너뛸 것인지 여부를 사용자에게 묻습니다.
- 새 파일을 만들지 않습니다. 기존 `.md`개 파일만 편집하십시오.
