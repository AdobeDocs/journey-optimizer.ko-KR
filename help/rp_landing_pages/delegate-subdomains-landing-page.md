---
solution: Journey Optimizer
product: Journey Optimizer
title: 이메일 하위 도메인 위임
description: 이메일 하위 도메인 위임
redpen-status: CREATED_||_2025-08-11_21-07-51
exl-id: 7df9b8e2-136a-4ffc-9243-53c7be026d81
source-git-commit: 2b907a3be8b11ac6308d0b563e122c88478d1d37
workflow-type: ht
source-wordcount: '244'
ht-degree: 100%

---

# 이메일 하위 도메인 위임{#section-overview}

Adobe Journey Optimizer에서 이메일 하위 도메인을 위임하면 관리자가 이메일 전달성을 개선하고, 도메인 평판을 보호하며, 캠페인 관리를 간소화할 수 있습니다. 하위 도메인을 설정하여 마케팅 및 트랜잭션 메시지와 같은 다양한 유형의 이메일 트래픽을 분리하는 동시에 업계 표준을 준수할 수 있습니다. 이 섹션에서는 전체 위임 및 CNAME 설정과 같은 주요 구성 방법을 소개하고 각 방법이 요구하는 노력과 제공하는 제어 수준에서 어떻게 다른지 살펴봅니다. 또한 DMARC 및 PTR과 같은 필수 DNS 레코드를 관리하고, Google TXT 레코드로 Gmail 전달성을 향상시키며, IP 풀을 사용하여 IP를 그룹화하는 방법에 대해 알아봅니다. 보안이나 평판 최적화 여부에 관계없이 이 안내서를 통해 프로세스를 접근 가능하고 효과적으로 수행할 수 있습니다.

## 이메일 하위 도메인 위임

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

하위 도메인 위임 시작

Adobe Journey Optimizer에서 하위 도메인을 위임할 때의 이점, 구성 방법 및 고려 사항에 대해 알아봅니다.

[하위 도메인 위임 시작](../using/configuration/about-subdomain-delegation.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

하위 도메인 위임

전체 위임 및 CNAME 설정을 포함하여 하위 도메인을 Adobe으로 위임하기 위한 단계별 지침입니다.

[위임 방법 알아보기](../using/configuration/delegate-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

DMARC 레코드 설정

위임된 하위 도메인에 대한 이메일 보안 및 전달성을 높이기 위해 DMARC 레코드를 구성합니다.

[DMARC 레코드 바로 설정](../using/configuration/dmarc-record.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

Google TXT 레코드 추가

Adobe Journey Optimizer에서 Google TXT 레코드를 추가하여 Gmail의 메시지 전달성에 대한 하위 도메인을 확인합니다.

[Google TXT 레코드 추가](../using/configuration/google-txt.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

PTR 레코드 액세스 및 편집

업데이트 상태를 편집하고 의미 파악을 포함하여 위임된 하위 도메인의 PTR 레코드를 관리합니다.

[PTR 레코드 편집](../using/configuration/ptr-records.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

IP 풀 만들기

이메일 전달성의 개선을 위해 IP 주소를 그룹화하고 하위 도메인 평판을 효과적으로 관리합니다.

[IP 풀 만들기](../using/configuration/ip-pools.md)
:::

::::
