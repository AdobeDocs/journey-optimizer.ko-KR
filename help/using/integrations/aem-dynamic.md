---
solution: Journey Optimizer
product: journey optimizer
title: 다이내믹 미디어
description: Journey Optimizer에서 Dynamic Media 사용
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: ccfc0870a8d59d16c7f5b6b02856785aa28dd307
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Dynamic Media 작업 {#aem-dynamic}

>[!AVAILABILITY]
>
>이 통합은 Dynamic Media Manager as a Cloud Service을 사용하는 고객에게만 제공됩니다.

이제 에셋 선택기가 Dynamic Media를 지원하므로 Journey Optimizer 내에서 승인된 Dynamic Media 렌디션을 원활하게 선택하고 사용할 수 있습니다. Adobe Experience Manager의 자산에 대한 변경 사항은 즉시 Journey Optimizer 콘텐츠에 반영되므로 수동으로 업데이트하지 않아도 최신 버전을 항상 사용할 수 있습니다.

Adobe Experience Manager as a Cloud Service의 Dynamic Media에 대한 자세한 내용은 [Experience Manager 설명서](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media)를 참조하세요.

## Dynamic Media 추가 및 관리

Adobe Experience Manager as a Cloud Service의 Dynamic Media를 Journey Optimizer 콘텐츠에 직접 삽입하여 화면 또는 브라우저에 맞게 콘텐츠를 개선하고 최적화합니다.  그런 다음 필요에 따라 크기를 조정하고, 자르고, 강화하고, 기타 조정할 수 있습니다.

1. **[!UICONTROL HTML 구성 요소]**&#x200B;를 콘텐츠로 끌어서 놓습니다.

1. **[!UICONTROL 소스 코드 표시]**&#x200B;를 선택합니다.

   ![](assets/dynamic-media-1.png)

1. **[!UICONTROL HTML 편집]** 메뉴에서 **[!UICONTROL Assets]**(으)로 이동한 다음 **[!UICONTROL 자산 선택기 열기]**&#x200B;를 클릭합니다.

   또는 에셋의 URL을 복사하여 붙여넣을 수 있습니다.

   ![](assets/dynamic-media-2.png)

1. AEM 에셋을 검색하고 콘텐츠에 추가하려는 에셋을 선택합니다.

1. 자산 요구 사항에 맞게 필요에 따라 이미지 매개 변수(예: 높이, 너비)를 조정합니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

이제 콘텐츠에 Dynamic Media가 포함됩니다. Experience Manager에서 수행하는 모든 업데이트는 Journey Optimizer에 자동으로 표시됩니다.

## 텍스트 오버레이가 있는 이미지를 사용하는 Personalization

텍스트 오버레이가 있는 이미지를 사용하여 컨텐츠를 쉽게 개인화할 수 있습니다.
텍스트는 위와 같이 URL의 AJO 변경 시 변경될 수 있습니다

1. **[!UICONTROL HTML 구성 요소]**&#x200B;를 콘텐츠로 끌어다 놓습니다.

1. **[!UICONTROL 소스 코드 표시]**&#x200B;를 선택합니다.

1. **[!UICONTROL HTML 편집]** 메뉴에서 **[!UICONTROL Assets]**&#x200B;에 액세스한 다음 **[!UICONTROL 자산 선택기 열기]**&#x200B;에 액세스합니다.

   에셋 URL을 복사하여 붙여넣을 수도 있습니다.

1. AEM 에셋을 탐색하고 콘텐츠에 추가할 에셋을 선택합니다.

## 전송 시간 개인화

WYSIWYG 작성자의 도움을 받아 DM 레이어 템플릿을 매개 변수화하여 콘텐츠 개인화
AJO 개인화 편집기를 사용한 프로필/컨텍스트 속성 매핑

1. **[!UICONTROL HTML 구성 요소]**&#x200B;를 콘텐츠로 끌어다 놓습니다.

1. **[!UICONTROL 소스 코드 표시]**&#x200B;를 선택합니다.

1. **[!UICONTROL HTML 편집]** 메뉴에서 **[!UICONTROL Assets]**&#x200B;에 액세스한 다음 **[!UICONTROL 자산 선택기 열기]**&#x200B;에 액세스합니다.

   에셋 URL을 복사하여 붙여넣을 수도 있습니다.

1. AEM 에셋을 탐색하고 콘텐츠에 추가할 에셋을 선택합니다.