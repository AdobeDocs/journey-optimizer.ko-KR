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
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 30%

---

# 하위 도메인에 Google TXT 레코드 추가 {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Google TXT 레코드"
>abstract="이메일이 Gmail 주소에 성공적으로 게재될 수 있도록 특별한 Google 사이트 확인 TXT 레코드를 하위 도메인에 추가하여 이를 확인해야 합니다."

TXT 레코드는 외부 소스에서 읽을 수 있는 도메인에 대한 텍스트 정보를 제공하는 데 사용되는 DNS 레코드 유형입니다.

이메일이 Gmail 주소로 최적으로 전달되고 성공적으로 전달될 수 있도록 [!DNL Journey Optimizer]을(를) 사용하면 하위 도메인에 특수 Google 사이트 확인 TXT 레코드를 추가하여 확인되었는지 확인할 수 있습니다.

>[!CAUTION]
>
> 이 작업은 하위 도메인이 **[!UICONTROL 성공]** 상태인 경우에만 수행할 수 있습니다. 하위 도메인 상태에 대한 자세한 내용은 [이 섹션](about-subdomain-delegation.md#access-delegated-subdomains)을 참조하세요.

하위 도메인에 Google TXT 레코드를 추가하려면 다음 단계를 수행합니다.

1. **[!UICONTROL 채널]** > **[!UICONTROL 전자 메일 설정]** > **[!UICONTROL 하위 도메인]** 메뉴에서 하위 도메인을 엽니다.

1. **[!UICONTROL Google txt 레코드]** 섹션에서 [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->에서 생성된 확인 코드를 입력한 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   ![](assets/subdomain-google-txt.png)

1. 추가한 TXT 레코드는 Google에서 확인해야 합니다. 이렇게 하려면 [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->(으)로 이동한 다음 확인 단계를 시작합니다.
