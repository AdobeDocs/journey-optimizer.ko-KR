---
title: 하위 도메인 위임
description: 하위 도메인을 위임하는 방법 알아보기
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: bbc2adabac63ffb813ea2630f29aec552fc3f4df
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 29%

---

# 하위 도메인에 Google TXT 레코드 추가 {#google-txt-record}

TXT 레코드는 외부 소스에서 읽을 수 있는 도메인 관련 텍스트 정보를 제공하는 데 사용되는 DNS 레코드 유형입니다.

Gmail 주소로 이메일이 배달되고 성공적으로 배달되도록 하려면, [!DNL Journey Optimizer] 에서는 하위 도메인에 특수 Google 사이트 확인 TXT 레코드를 추가하여 확인하는지 확인할 수 있습니다.

>[!CAUTION]
>
> 이 작업은 하위 도메인에 **[!UICONTROL Success]** 상태. 하위 도메인 상태에 대한 자세한 내용은 [이 섹션](access-subdomains.md).

하위 도메인에 Google TXT 레코드를 추가하려면 다음 단계를 수행합니다.

1. 에서 하위 도메인을 엽니다. **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** 메뉴 아래의 제품에서 사용할 수 있습니다.

1. 에서 **[!UICONTROL Google txt record]** 섹션에서 생성된 확인 코드를 입력합니다. [Google 작업 공간](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->를 클릭한 다음 **[!UICONTROL Save]**.

   ![](../assets/subdomain-google-txt.png)

1. 추가한 TXT 레코드는 Google에서 확인해야 합니다. 이렇게 하려면 로 이동합니다. [Google 작업 공간](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->그런 다음 확인 단계를 시작합니다.
