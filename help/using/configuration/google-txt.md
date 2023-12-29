---
solution: Journey Optimizer
product: journey optimizer
title: 하위 도메인에 Google TXT 레코드 추가
description: 하위 도메인에 Google TXT 레코드를 추가하는 방법 알아보기
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 하위 도메인, google, txt, 레코드, gmail, 게재 기능
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 30%

---

# 하위 도메인에 Google TXT 레코드 추가 {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Google TXT 레코드"
>abstract="이메일이 Gmail 주소에 성공적으로 게재될 수 있도록 특별한 Google 사이트 확인 TXT 레코드를 하위 도메인에 추가하여 이를 확인해야 합니다."

TXT 레코드는 외부 소스에서 읽을 수 있는 도메인에 대한 텍스트 정보를 제공하는 데 사용되는 DNS 레코드 유형입니다.

최적의 전달성과 Gmail 주소로 이메일의 성공적인 전달을 보장하기 위해, [!DNL Journey Optimizer] 에서는 하위 도메인에 특수 Google 사이트 확인 TXT 레코드를 추가하여 확인되었는지 확인할 수 있습니다.

>[!CAUTION]
>
> 이 작업은 하위 도메인에 **[!UICONTROL 성공]** 상태. 하위 도메인 상태에 대한 자세한 내용은 [이 섹션](about-subdomain-delegation.md#access-delegated-subdomains).

하위 도메인에 Google TXT 레코드를 추가하려면 다음 단계를 수행합니다.

1. 에서 하위 도메인을 엽니다. **[!UICONTROL 채널]** / **[!UICONTROL 하위 도메인]** 메뉴 아래의 제품에서 사용할 수 있습니다.

1. 다음에서 **[!UICONTROL Google txt 레코드]** 섹션에서 생성된 확인 코드를 입력합니다. [Google 작업 공간](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->을 클릭한 다음 을 클릭합니다 **[!UICONTROL 저장]**.

   ![](assets/subdomain-google-txt.png)

1. 추가한 TXT 레코드는 Google에서 확인해야 합니다. 이렇게 하려면 다음으로 이동합니다. [Google 작업 공간](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->을 클릭한 다음 확인 단계를 시작합니다.
