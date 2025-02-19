---
solution: Journey Optimizer
product: journey optimizer
title: 브랜드 관리
description: 브랜드 지침을 만들고 관리하는 방법 알아보기
badge: label="Beta" type="Informative"
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: 6c99d733b973efd790f8727bf867fbf0a952f6d9
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 24%

---

# 브랜드 생성 및 관리 {#brands}

>[!AVAILABILITY]
>
>이 기능은 비공개 베타로 출시됩니다. 향후 릴리스에서 모든 고객에게 점진적으로 제공될 예정입니다.

브랜드 지침은 브랜드의 시각적 및 언어적 정체성을 확립하는 상세한 규칙 및 표준 세트입니다. 모든 마케팅 및 커뮤니케이션 플랫폼에서 일관된 브랜드 표현을 유지하는 참조 역할을 합니다.

<!--Upload feature currently behind feature flag--

In [!DNL Journey Optimizer], you now have the option to manually input and organize your brand details or upload brand guideline documents for automatic information extraction.-->

## 브랜드 액세스 {#generative-access}

[!DNL Adobe Journey Optimizer]에서 **[!UICONTROL 브랜드]** 메뉴에 액세스하려면 사용자에게 **[!UICONTROL 관리 브랜드 키트]** 또는 **[!UICONTROL AI 도우미 사용]** 권한을 부여해야 합니다. [자세히 알아보기](../administration/permissions.md)

+++  브랜드 관련 권한을 할당하는 방법을 알아봅니다.

1. **권한** 제품에서 **역할** 탭으로 이동하여 원하는 **역할**&#x200B;을 선택하십시오.

1. 권한을 수정하려면 **편집**&#x200B;을 클릭하십시오.

1. **AI Assistant** 리소스를 추가한 다음 드롭다운 메뉴에서 **관리 브랜드 키트** 또는 **[!UICONTROL Ai Assistant 사용]**&#x200B;을 선택합니다.

   **[!UICONTROL Ai Assistant 사용]** 권한은 **[!UICONTROL 브랜드]** 메뉴에 대한 읽기 전용 액세스를 제공합니다.

   ![](assets/brands-permission.png){zoomable="yes"}

1. 변경 내용을 적용하려면 **저장**&#x200B;을 클릭하십시오.

   이 역할에 이미 할당된 모든 사용자의 권한은 자동으로 업데이트됩니다.

1. 새 사용자에게 이 역할을 할당하려면 **역할** 대시보드의 **사용자** 탭으로 이동하여 **사용자 추가**&#x200B;를 클릭하십시오.

1. 사용자 이름, 이메일 주소를 입력하거나 목록에서 선택한 다음 **저장**&#x200B;을 클릭합니다.

1. 이전에 사용자를 생성하지 않은 경우 [이 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/access-control/abac/permissions-ui/users)를 참조하십시오.

+++

## 브랜드 만들기 {#create-brand-kit}

브랜드 지침을 만들고 관리하려면 아래 단계를 따르십시오.

<!--Upload feature currently behind feature flag--

To create and manage your Brand guideline, you can either enter the details yourself, or upload your brand guidelines document to have the information extracted automatically:-->

1. **[!UICONTROL 브랜드]** 메뉴에서 **[!UICONTROL 브랜드 만들기]**&#x200B;를 클릭합니다.

   ![](assets/brands-1.png)

1. 브랜드의 **[!UICONTROL 이름]**&#x200B;을(를) 입력하십시오<!--and a **[!UICONTROL Description]** to your brand guideline-->.

   ![](assets/brands-2-temp.png)

<!--Upload feature currently behind feature flag so hidden from doc - should be available again by EOM (Feb)--

1. Drag and drop or select your file to upload your brand guidelines and extract automatically relevant brand information. Click **[!UICONTROL Create brand]**.

    The information extraction process now begins. Note that it may take several minutes to complete.

    ![](assets/brands-2.png)

1. Your Content and visual creation standards are now automatically populated. Browse through the different tabs to adapt the information as needed.

-->

1. **[!UICONTROL 작성 스타일]** 탭에서 ![](assets/do-not-localize/Smock_Add_18_N.svg)을(를) 클릭하여 예제를 포함한 지침 또는 제외를 추가합니다.

   ![](assets/brands-3.png)

1. **[!UICONTROL 시각적 콘텐츠]** 탭에서 ![](assets/do-not-localize/Smock_Add_18_N.svg)을(를) 클릭하여 다른 지침이나 제외를 추가합니다.

1. 올바른 사용을 표시하는 이미지를 추가하려면 **[!UICONTROL 예제]**&#x200B;를 선택하고 **[!UICONTROL 이미지 선택]**&#x200B;을 클릭합니다. 제외 예로서 잘못된 사용을 보여주는 이미지를 추가할 수도 있습니다.

   ![](assets/brands-4.png)

1. 구성이 완료되면 **[!UICONTROL 저장]**&#x200B;을 클릭한 다음 **[!UICONTROL 게시]**&#x200B;을 클릭하여 브랜드 지침을 AI 도우미에서 사용할 수 있도록 합니다.

1. 게시된 브랜드를 수정하려면 **[!UICONTROL 브랜드 편집]**&#x200B;을 클릭하세요.

   >[!NOTE]
   >
   >이렇게 하면 편집 모드에 임시 복사본이 만들어지고 게시 후 라이브 버전이 대체됩니다.

   ![](assets/brands-8.png)

1. **[!UICONTROL 브랜드]** 대시보드에서 ![](assets/do-not-localize/Smock_More_18_N.svg) 아이콘을 클릭하여 고급 메뉴를 열어 다음 작업을 수행합니다.

   * 브랜드 보기
   * 편집
   * 복제
   * 게시
   * 게시 취소
   * 삭제

   ![](assets/brands-6.png)

이제 AI 도우미 메뉴의 **[!UICONTROL Brand]** 드롭다운에서 브랜드 지침에 액세스할 수 있으므로 사양에 맞게 콘텐츠 및 에셋을 생성할 수 있습니다. [AI Assistant에 대해 자세히 알아보기](gs-generative.md)

![](assets/brands-7.png)
