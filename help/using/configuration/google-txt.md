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
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 26%

---

# 하위 도메인에 Google TXT 레코드 추가

TXT 레코드는 외부 소스에서 읽을 수 있는 도메인 관련 텍스트 정보를 제공하는 데 사용되는 DNS 레코드 유형입니다.

고객 여정 관리에서 이메일 배달 가능성을 높여 Gmail 주소로 이메일이 올바르게 배달되도록 하기 위해 하위 도메인에 특수 Google 사이트 확인 TXT 레코드를 확인용으로 추가할 수 있습니다.

>[!NOTE]
>
> 이 작업은 하위 도메인에 **[!UICONTROL Success]** 상태. 하위 도메인 상태에 대한 자세한 내용은 [이 섹션](access-subdomains.md).

하위 도메인에 Google TXT 레코드를 추가하려면 다음 단계를 수행합니다.

1. 에서 하위 도메인을 엽니다. **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** 메뉴 아래의 제품에서 사용할 수 있습니다.

1. Google txt 레코드 섹션에서 [G Suite 관리 도구](https://support.google.com/a/answer/183895)를 클릭한 다음 **[!UICONTROL Save]**.

   ![](../assets/subdomain-google-txt.png)

1. 추가한 TXT 레코드는 Google에서 확인해야 합니다. 이렇게 하려면 G Suite 관리 도구로 이동한 다음 확인 단계를 시작합니다.
