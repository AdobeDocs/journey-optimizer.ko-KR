---
solution: Journey Optimizer
product: journey optimizer
title: AI Assistant의 C2PA 메타데이터
description: Adobe Journey Optimizer에서 AI Assistant를 사용하여 생성 또는 편집한 이미지에 C2PA 메타데이터를 자동으로 적용하는 방법과 이것이 귀하의 콘텐츠에 미치는 영향에 대해 알아봅니다.
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
hide: true
source-git-commit: eeea63d195527451e3ce40481b2ff4657aa76d3b
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 3%

---

# AI Assistant의 C2PA 메타데이터 {#generative-content-credentials}

>[!BEGINSHADEBOX]

**이 페이지에서:** C2PA 메타데이터를 첨부하는 AI Assistant 작업, 여러 생성 AI 소스를 결합하는 이미지에 대한 의미, 콘텐츠가 앱 간에 이동할 때 전달되는 것에 대해 알아봅니다.

>[!ENDSHADEBOX]

>[!INFO]
>
>생성 AI 투명성을 중심으로 새로운 법이 등장하고 있으며, Adobe은 관할권 전반에서 적용 가능한 요구 사항을 충족하기 위해 노력하고 있습니다. C2PA 메타데이터는 Adobe이 이러한 법률의 요구 사항을 충족하기 위해 사용하는 증명 도구입니다.

C2PA 메타데이터는 콘텐츠의 한 부분이 생성되거나 편집되는 방식을 기록하는 보이지 않는 내구성 있는 메타데이터입니다. Adobe Journey Optimizer의 AI Assistant를 사용하여 생성 AI 도구로 이미지를 생성하거나 편집할 때 C2PA 메타데이터가 해당 이미지에 자동으로 첨부되므로 별도의 작업이 필요하지 않습니다.

## C2PA 메타데이터를 첨부하는 작업 {#cc-workflows}

다음 표는 AI Assistant에서 수행된 이미지 작업을 기반으로 C2PA 메타데이터가 첨부되는 시기를 요약합니다.

| 작업 | 설명 | C2PA 메타데이터가 첨부되었습니까? | 사용 사례 예 |
| --- | --- | --- | --- |
| **이미지 생성** | 텍스트 프롬프트, 참조 이미지 또는 유사한 이미지에서 새 이미지 생성 | 항상 이미지는 생성 AI에 의해 생성되므로 항상 새로운 C2PA 메타데이터를 전달합니다. | 이메일 캠페인에 대한 배너 이미지는 원하는 시각적 개체를 설명하는 텍스트 프롬프트에서 생성됩니다. |
| **이미지 자르기**(가운데 또는 스마트 자르기) | 이미지를 요청된 치수로 조정 | 소스 이미지에 이미 C2PA 메타데이터가 있는 경우에만 해당합니다. 자르기는 이미지의 픽셀을 다시 만듭니다. 이렇게 하면 일반적으로 해당 C2PA 메타데이터가 지워지므로 AI 도우미는 자르기 전에 소스 이미지에서 이미지를 읽은 다음 자른 결과에 다시 빌드하고 다시 첨부합니다. 자르기 자체로는 새로운 생성 AI 작업이 추가되지 않으며 기존 AI 작업을 유지합니다. | 생성된 배너 이미지는 웹 페이지에 맞게 잘립니다. C2PA 메타데이터는 자르기를 통해 유지됩니다. </br> 푸시 알림 배경으로 사용되는 업로드된 스톡 사진은 화면에 맞게 잘립니다. 스톡 사진은 생성 AI 작업을 수행하지 않으므로 C2PA 메타데이터가 생성되지 않습니다. |
| **텍스트 오버레이 추가** | 배경 이미지 위에 생성된 텍스트 렌더링 | 배경 이미지에 이미 C2PA 메타데이터가 있는 경우에만 해당합니다. 오버레이를 렌더링하면 배경과 텍스트에서 새 이미지가 생성되며, 이 이미지는 일반적으로 해당 C2PA 메타데이터를 지웁니다. 따라서 AI 길잡이가 배경 이미지에서 미리 읽은 다음 다시 빌드하고 결과에 다시 첨부합니다. 오버레이 단계는 새로운 생성 AI 작업을 추가하지 않습니다. | 홍보 헤드라인은 랜딩 페이지에 대해 생성된 배경 이미지에 텍스트 오버레이로 렌더링됩니다. 배경 이미지의 C2PA 메타데이터는 유지됩니다. |
| **오버레이 이미지** | 두 개 이상의 이미지를 함께 합성 | 소스 이미지에 C2PA 메타데이터가 있으면 결합된 이미지가 모든 이미지를 전달하여 단일 C2PA 메타데이터로 병합됩니다. 합성은 일반적으로 이러한 C2PA 메타데이터를 지우는 소스에서 새 이미지를 생성하므로 AI Assistant는 합성하기 전에 각 이미지를 읽은 다음 생성 AI 작업에 기여한 모든 소스를 나열하는 단일 결합 C2PA 메타데이터를 빌드합니다. | 생성된 제품 이미지는 이메일 헤더에 대해 생성된 배경과 합성됩니다. 이 결과는 생성된 AI 소스를 모두 반영하는 C2PA 메타데이터를 전달합니다. <br> 업로드된 두 개의 브랜드 사진은 하나의 콜라주에 합성됩니다. 두 소스 모두 생성 AI 작업을 수행하지 않으므로 C2PA 메타데이터가 생성되지 않습니다. |

## 컨텐츠 유형 및 해당 범위 {#cc-content-types}

* **이미지**: 적용됨. C2PA 메타데이터는 생성 AI로 이미지가 생성될 때 첨부되며 AI 어시스턴트가 수행하는 자르기, 텍스트 오버레이, 이미지 오버레이 작업 등을 통해 보존된다.
* **텍스트**: 적용할 수 없습니다. 복사 생성, 번역 및 브랜드 정렬 제안과 같은 AI Assistant의 텍스트 전용 출력은 C2PA 메타데이터가 필요하지 않습니다.

## 콘텐츠가 이동할 때 수행되는 작업 {#cc-content-moves}

C2PA 메타데이터는 이미지 파일과 함께 이동합니다. 생성 AI로 생성 또는 편집한 이미지를 Adobe Journey Optimizer에서 다운로드하거나 내보내면 해당 C2PA 메타데이터가 보존됩니다. [C2PA 메타데이터에 대해 자세히 알아보세요](https://helpx.adobe.com/kr/firefly/using/content-credentials.html){target="_blank"}.

PDF 또는 임베드된(base64) 소스에서 이미지를 추출하는 것과 같이 이미지를 콘텐츠로 가져오는 일부 방법은 원래 C2PA 메타데이터를 보존하지 않을 수 있습니다. 이러한 경우 소스에서 C2PA 메타데이터를 읽을 수 없으며 결과에 대해 아무것도 만들어지지 않습니다.

## 추가 리소스

* [Adobe C2PA 메타데이터](https://helpx.adobe.com/kr/firefly/using/content-credentials.html){target="_blank"}: Adobe 제품에서 C2PA 메타데이터가 작동하는 방식에 대해 자세히 알아보세요.
* [Adobe Experience Cloud Generative AI 사용자 지침](https://www.adobe.com/kr/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}
* [가드레일 및 제한 사항](gs-generative.md#generative-guardrails)
