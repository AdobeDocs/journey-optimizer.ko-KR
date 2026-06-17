---
source-git-commit: a281a4d244279a6a1fce6968e4636b86414c4400
workflow-type: tm+mt
source-wordcount: '1029'
ht-degree: 6%

---
파일이 이 저장소에 없고 쓰기 권한이 승인되지 않았으므로 요청에 따라 업데이트된 전체 마크다운 파일은 다음과 같습니다.

&#x200B;---
제목: 브랜드 정렬
description: 브랜드 점수를 사용하여 브랜드 내 콘텐츠를 생성, 유효성 검사 및 관리하는 방법을 학습합니다.
topic: 콘텐츠 관리 , Artificial Intelligence
역할: 사용자
level: 초급, 중급
exl-id: 01e74670-7431-4791-b98c-12278e6d3332
TQID: https://experienceleague.adobe.com/hs1F6tz-XHYH6u8jO4kspRcX-ftY-SwilqMfcaLhTfg
product_v2:
- id: cb954087-f4fc-4456-afb9-e939cabcdc79
내부 레이블: Journey Optimizer
feature_v2:
- id: dc22c819-3f29-4e91-8b7d-5c6719831141
내부 레이블: 컨텐츠 관리
- id: fe338112-e2ce-4876-8989-fc4d497613f1
내부 레이블: 이메일
subfeature_v2:
- id: ea4139d9-3405-4b34-ad6e-c3ca120cc269
내부 레이블: 다국어 컨텐츠
- id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
내부 레이블: 이메일 디자인
- id: fb9a80eb-bebc-492f-a0e9-584595621ebb
내부 레이블: 게시
role_v2:
- id: b69b2659-1057-424e-8fc5-ed9e016dc554
내부 레이블: 사용자
level_v2:
- id: b5a62a22-46f7-4f0d-b151-3fc640bef588
내부 레이블: 중간
- id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
내부 레이블: 초보자
topic_v2:
- id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
내부 레이블: 인공 지능
- id: e1e0219c-f879-479f-8427-888ed2a6e9c2
내부 레이블: Insights
---
# 브랜드 정렬 {#brands-score}

>[!BEGINSHADEBOX]

**이 페이지에서:** 브랜드 지침에 따라 이메일 콘텐츠의 유효성을 검사하고 Adobe Journey Optimizer의 브랜드 정렬 점수를 사용하여 전반적인 콘텐츠 품질을 평가하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_brand_score"
>title="브랜드 정렬 점수"
>abstract="브랜드 정렬 점수는 콘텐츠가 브랜드의 지침을 얼마나 잘 준수하는지 측정하여 색상, 글꼴, 로고, 이미지 및 작성 스타일에서의 일관성을 보장합니다."

>[!CONTEXTUALHELP]
>id="ajo_brand_colors"
>title="색상 점수"
>abstract="색상 점수"

>[!CONTEXTUALHELP]
>id="ajo_brand_fonts"
>title="글꼴 점수"
>abstract="글꼴 점수"

>[!CONTEXTUALHELP]
>id="ajo_brand_logos"
>title="로고 점수"
>abstract="로고 점수"

>[!CONTEXTUALHELP]
>id="ajo_brand_suggestions"
>title="AI 생성 제안"
>abstract="브랜드 정렬 또는 품질 평가 중에 콘텐츠에 플래그가 지정되면 AI Assistant는 사용자가 검토하고 인라인으로 적용할 수 있는 수정된 대체 요소를 자동으로 생성합니다."

>[!AVAILABILITY]
>
>Adobe Journey Optimizer에서 AI 도우미를 사용하려면 먼저 [사용자 동의](https://www.adobe.com/kr/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}에 동의해야 합니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.

브랜드 정렬 기능은 브랜드 지침을 준수하는 콘텐츠를 만들고, 검토하고, 관리하는 데 도움이 됩니다. 이메일 캠페인 전반에 걸쳐 톤, 메시징 및 시각적 ID의 일관성을 보장하는 동시에 콘텐츠가 라이브로 전환되기 전에 품질을 확인하는 역할을 합니다.

## 브랜드 정렬을 사용하여 콘텐츠 유효성 검사 {#validate-content}

[브랜드를 설정하고 게시하면](brands.md), 이메일 캠페인 내에서 직접 브랜드 정렬 점수를 평가하여 콘텐츠가 브랜드 지침에 맞게 조정되도록 합니다.

1. [전자 메일 캠페인](../campaigns/create-campaign.md)을 만듭니다.

1. 이메일 Designer에서 **[!UICONTROL 브랜드 정렬]** 메뉴를 엽니다.

   콘텐츠는 기본 브랜드에 대해 자동으로 평가됩니다. [기본 브랜드를 할당하는 방법을 알아보세요](brands.md).

   ![](assets/brand-score-1.png)

1. 다른 브랜드를 사용하여 평가하려면 **[!UICONTROL 브랜드]** 드롭다운 메뉴에서 브랜드를 선택하고 **[!UICONTROL 점수 평가]**&#x200B;를 클릭하십시오.

   ![](assets/brand-score-2.png)

1. **[!UICONTROL 작성 스타일]** 또는 **[!UICONTROL 시각적 콘텐츠]**&#x200B;를 탐색하여 점수에 대한 더 많은 통찰력을 확인합니다.

   ![](assets/brand-score-3.png)

1. 점수에 대한 자세한 인사이트를 보려면 ![전체 화면 아이콘을 클릭하세요](assets/do-not-localize/Smock_FullScreen_18_N.svg "전체 화면").

   ![](assets/brand-score-5.png)

1. 특정 피드백 및 AI가 생성한 제안을 보려면 플래그가 지정된 지침을 선택하십시오. 브랜드 정렬은 다음 범주를 평가합니다.

   &#x200B;* **[!UICONTROL 작성 스타일]**:
      &#x200B;* **[!UICONTROL 브랜드 커뮤니케이션 스타일]**: 모든 채널에서 일관된 브랜드 음성을 제공하기 위해 개성과 감정적인 톤을 정의합니다.
      &#x200B;* **[!UICONTROL 브랜드 메시지 표준]**: 효과적인 마케팅 및 홍보 텍스트에 대한 구조적 및 서식 규칙입니다.
      &#x200B;* **[!UICONTROL 법적 준수 표준]**: 모든 커뮤니케이션이 텍스트 배치 및 준수 확인 목록을 비롯한 법적 요구 사항을 준수하도록 합니다.

   &#x200B;* **[!UICONTROL 시각적 콘텐츠]**:
      &#x200B;* **[!UICONTROL 사진 표준]**: 해상도, 컴포지션, 조명 및 파일 형식을 포함한 사진 콘텐츠에 대한 요구 사항.
      &#x200B;* **[!UICONTROL 일러스트레이션 표준]**: 일러스트레이션의 스타일 매개 변수, 선 두께, 색상 사용 및 파일 형식 요구 사항입니다.
      &#x200B;* **[!UICONTROL 아이콘 표준]**: 격자 시스템, 획 두께 및 균일성을 위한 크기 조정을 포함한 아이콘 디자인을 위한 사양입니다.
      &#x200B;* **[!UICONTROL 사용 지침]**: 브랜드 정체성을 유지하기 위한 이미지 선택, 배치 및 컨텍스트에 대한 모범 사례입니다.



   ![](assets/brand-score-4.png)

1. 플래그가 지정된 쓰기 스타일 문제의 경우 각 위반 아래에 표시된 AI 생성 제안을 검토한 다음 **[!UICONTROL 적용]**&#x200B;을 클릭하여 플래그가 지정된 콘텐츠를 인라인으로 바꾸거나 무시하여 원래 텍스트를 유지하십시오. [AI가 생성한 제안 적용에 대해 자세히 알아보세요](#apply-suggestions).

1. 정렬 점수를 새로 고치기 위해 변경 후 콘텐츠를 수동으로 다시 평가합니다.

## 콘텐츠 품질 유효성 검사 {#validate-quality}

>[!NOTE]
>
>콘텐츠 품질 평가는 브랜드 지침과 독립적입니다. 드롭다운 메뉴에서 브랜드를 선택하더라도 해당 지침은 품질 검사에 적용되지 않습니다. 브랜드 선택은 브랜드 정렬 점수에만 관련이 있습니다.

브랜드 정렬 외에도 브랜드 지침과 관계없이 가독성, 콘텐츠 응집성 및 효과성과 관련된 잠재적 문제를 식별하기 위해 일반적인 콘텐츠 품질을 평가할 수 있습니다.

콘텐츠 품질을 평가하려면 다음을 수행하십시오.

1. [전자 메일 캠페인](../campaigns/create-campaign.md)을 만듭니다.

1. 이메일 Designer에서 **[!UICONTROL 브랜드 정렬]** 메뉴를 엽니다.

   ![](assets/brand-score-1.png)

1. 브랜드 맞춤 점수와 콘텐츠 품질 점수를 모두 생성하려면 **[!UICONTROL 점수 평가]**&#x200B;를 클릭하십시오.

   ![](assets/brand-score-2.png)

1. 콘텐츠 품질 인사이트 및 권장 사항을 검토하려면 **[!UICONTROL 전체 품질]** 탭으로 이동하십시오.

   ![](assets/brand-score-6.png)

1. 품질 점수에 대한 자세한 보기를 보려면 ![전체 화면 아이콘을 클릭하십시오.](assets/do-not-localize/Smock_FullScreen_18_N.svg "전체 화면") 아이콘을 클릭하십시오.

   ![](assets/brand-score-7.png)

1. 특정 피드백 및 AI가 생성한 개선 사항을 보려면 플래그가 지정된 항목을 선택하십시오. 점수는 다음 카테고리를 기반으로 합니다.

   &#x200B;* **[!UICONTROL CTA 효율성]**: call-to-action이 독자에게 원하는 행동을 취하도록 동기를 부여하는 정도를 평가합니다.
   &#x200B;* **[!UICONTROL 제목 줄]**: 명확성, 관련성 및 주의를 끄는 품질을 평가하여 이메일 열기를 유도합니다.
   &#x200B;* **[!UICONTROL 가독성]**: 독자가 이해할 수 있는 컨텐츠의 용이성과 참여도를 측정합니다.
   &#x200B;* **[!UICONTROL 스팸 확인]**: 전달성에 영향을 줄 수 있는 일반적인 스팸 트리거를 식별합니다.
   &#x200B;* **[!UICONTROL 컨텐츠 응집력]**: 컨텐츠가 원활하게 흐르고 주제를 벗어나지 않도록 합니다.
   &#x200B;* **[!UICONTROL 교정]**: 맞춤법, 문법 및 명확성 문제가 있는지 확인합니다.

   ![](assets/brand-score-8.png)

1. 플래그가 지정된 텍스트 항목의 경우 각 문제 아래에 표시된 AI 생성 제안을 검토한 다음 **[!UICONTROL 적용]**&#x200B;을 클릭하여 콘텐츠를 인라인으로 바꾸거나 무시할 경우 원래 텍스트를 유지합니다. [AI가 생성한 제안 적용에 대해 자세히 알아보세요](#apply-suggestions).

1. 품질 점수를 새로 고치려면 변경한 후 **[!UICONTROL 점수 다시 평가]**&#x200B;를 클릭하십시오.

## AI가 생성한 제안 적용 {#apply-suggestions}

브랜드 정렬 또는 품질 평가 중에 콘텐츠에 플래그가 지정되면 AI Assistant는 자동으로 피드백 패널에서 수정 또는 향상된 대체 요소를 직접 생성합니다. 이 워크플로는 편집기를 종료하지 않고 위반을 해결하는 데 도움이 되며, 수동 편집 작업을 줄이고 콘텐츠 제작을 가속화합니다.

AI에서 생성한 제안은 지원되는 모든 콘텐츠 유형(이메일, SMS, 푸시 및 웹)에서 텍스트 기반 위반에 사용할 수 있습니다.

AI 생성 제안을 적용하려면

1. 브랜드 정렬 또는 품질 평가를 실행한 다음 플래그가 지정된 지침 또는 품질 항목을 선택하여 피드백 패널을 확장합니다.

1. 플래그가 지정된 콘텐츠 아래에 표시된 AI 생성 제안을 검토합니다.

1. 플래그가 지정된 콘텐츠를 제안 대체 요소로 바꾸려면 **[!UICONTROL 적용]**&#x200B;을(를) 클릭하십시오.

   원본 텍스트를 유지하려면 **[!UICONTROL 취소]**&#x200B;를 클릭하세요.

1. 플래그가 지정된 나머지 항목에 대해 이 작업을 반복합니다.

1. 점수를 다시 평가하여 모든 개선 사항이 적용되었는지 확인합니다.

## 사용 방법 비디오 {#video}

아래 비디오에서는 고유한 브랜드를 만들고 사용자 정의하여 커뮤니케이션 전반에 걸쳐 시각적 및 언어적 정체성을 명확하게 정의하는 방법을 보여줍니다.

+++ 비디오 보기

>[!VIDEO](https://video.tv.adobe.com/v/3470544/?learn=on)

+++
