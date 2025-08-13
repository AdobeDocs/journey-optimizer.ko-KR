---
solution: Journey Optimizer
product: Journey Optimizer
title: 이메일 하위 도메인 위임
description: 이메일 하위 도메인 위임
redpen-status: CREATED_||_2025-08-11_21-07-51
source-git-commit: 5a8ef88cba254241933607ca59156d35e0e92926
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 3%

---


# 이메일 하위 도메인 위임{#section-overview}

Adobe Journey Optimizer에서 이메일 하위 도메인을 위임하면 관리자가 이메일 전달성을 향상시키고, 도메인 평판을 보호하며, 캠페인 관리를 간소화할 수 있습니다. 하위 도메인을 설정하여 마케팅 및 트랜잭션 메시지와 같은 다양한 유형의 이메일 트래픽을 격리하는 동시에 업계 표준을 준수할 수 있습니다. 이 섹션에서는 전체 위임 및 CNAME 설정과 같은 주요 구성 방법을 소개하고 이들이 노력과 제어에서 어떻게 다른지 살펴봅니다. 또한 DMARC 및 PTR과 같은 필수 DNS 레코드를 관리하고, Google TXT 레코드로 Gmail 전달성을 향상시키며, IP 풀을 사용하여 IP를 그룹화하는 방법에 대해 알아봅니다. 보안 또는 평판 최적화 여부에 관계없이 이 안내서를 통해 프로세스를 접근 가능하고 효과적으로 수행할 수 있습니다.

## 이메일 하위 도메인 위임

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=ko)

하위 도메인 위임 시작

Adobe Journey Optimizer에서 하위 도메인을 위임할 때의 이점, 구성 방법 및 고려 사항에 대해 알아봅니다.

[하위 도메인 위임 시작](../using/configuration/about-subdomain-delegation.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=ko)

하위 도메인 위임

전체 위임 및 CNAME 설정을 포함하여 하위 도메인을 Adobe으로 위임하기 위한 단계별 지침입니다.

[위임 방법 알아보기](../using/configuration/delegate-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=ko)

DMARC 레코드 설정

위임된 하위 도메인에 대한 이메일 보안 및 전달성을 향상하도록 DMARC 레코드를 구성합니다.

[지금 DMARC 설정](../using/configuration/dmarc-record.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=ko)

Google TXT 레코드 추가

Adobe Journey Optimizer에서 Google TXT 레코드를 추가하여 Gmail 전달의 하위 도메인을 확인합니다.

[Google TXT 레코드 추가](../using/configuration/google-txt.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=ko)

PTR 레코드 액세스 및 편집

업데이트 상태 편집 및 이해를 포함하여 위임된 하위 도메인의 PTR 레코드를 관리합니다.

[PTR 레코드 편집](../using/configuration/ptr-records.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=ko)

IP 풀 만들기

IP 주소를 그룹화하여 이메일 전달성을 개선하고 하위 도메인 평판을 효과적으로 관리합니다.

[IP 풀 만들기](../using/configuration/ip-pools.md)
:::

::::
