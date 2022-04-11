---
title: 하위 도메인에 Google TXT 레코드 추가
description: 하위 도메인에 Google TXT 레코드를 추가하는 방법을 알아봅니다
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: d568480005d9b4aad5982c26184a5add0be6c83a
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 21%

---

# 하위 도메인에 Google TXT 레코드 추가 {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Google TXT 레코드"
>abstract="Gmail 주소로 이메일을 성공적으로 게재하기 위해 하위 도메인에 특수 Google 사이트 확인 TXT 레코드를 확인용으로 추가할 수 있습니다."

TXT 레코드는 외부 소스에서 읽을 수 있는 도메인 관련 텍스트 정보를 제공하는 데 사용되는 DNS 레코드 유형입니다.

Gmail 주소로 이메일을 게재하는 것을 최적화하기 위해 [!DNL Journey Optimizer] 에서는 하위 도메인에 특수 Google 사이트 확인 TXT 레코드를 추가하여 확인되었는지 확인할 수 있습니다.

>[!CAUTION]
>
> 이 작업은 하위 도메인에 **[!UICONTROL Success]** 상태. 하위 도메인 상태에 대한 자세한 내용은 [이 섹션](access-subdomains.md).

하위 도메인에 Google TXT 레코드를 추가하려면 다음 단계를 수행합니다.

1. 에서 하위 도메인을 엽니다. **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** 메뉴 아래의 제품에서 사용할 수 있습니다.

1. 에서 **[!UICONTROL Google txt record]** 섹션에서 생성된 확인 코드를 입력합니다. [Google 작업 공간](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->를 클릭한 다음 **[!UICONTROL Save]**.

   ![](assets/subdomain-google-txt.png)

1. 추가한 TXT 레코드는 Google에서 확인해야 합니다. 이렇게 하려면 로 이동합니다. [Google 작업 공간](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->그런 다음 확인 단계를 시작합니다.
