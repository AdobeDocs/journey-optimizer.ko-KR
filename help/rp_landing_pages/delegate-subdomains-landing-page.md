---
solution: Journey Optimizer
product: Journey Optimizer
title: 이메일 하위 도메인 위임
description: 이메일 하위 도메인 위임
redpen-status: CREATED_||_2025-08-11_21-07-51
exl-id: 7df9b8e2-136a-4ffc-9243-53c7be026d81
source-git-commit: bb50d06e86f9399dfd295b8091aa637abcaea4a8
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 41%

---

# 이메일 하위 도메인 위임{#section-overview}

전자 메일 하위 도메인 위임은 [채널 구성](../using/configuration/get-started-configuration.md)의 핵심 단계입니다. Journey Optimizer에서 전자 메일을 보내려면 먼저 필수 단계입니다. 하위 도메인을 사용하면 트래픽 유형(예: 마케팅 및 트랜잭션)을 격리하고 주 도메인의 평판을 보호하며 [IP 준비](../using/configuration/ip-warmup-gs.md) 속도를 높일 수 있습니다. [전자 메일 채널 구성](../using/email/get-started-email-config.md) 및 [게재 가능성 모니터링](../using/reports/deliverability.md)과 함께 작동하여 메시지가 받은 편지함에 도달하는지 확인합니다.

**전체 위임**(Adobe에서 DNS 관리), **CNAME 설정** 또는 **사용자 지정 위임**(사용자가 인증서 및 DNS 소유) 중 선택할 수 있습니다. CNAME으로 시작하는 경우, 나중에 보안을 강화하기 위해 [사용자 지정 위임으로 마이그레이션](../using/configuration/custom-subdomain-migration.md)할 수 있습니다. 이 섹션에서는 DMARC 및 PTR 레코드, Gmail용 Google TXT 레코드 및 IP 풀도 다룹니다. 더 광범위한 전달성 지침은 [전달성 시작](../using/reports/deliverability.md) 및 [전자 메일 주소 모니터링](monitor-reputation-landing-page.md)을 참조하세요.

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
![icon](https://cdn.experienceleague.adobe.com/icons/screwdriver-wrench.svg)

사용자 정의 하위 도메인 설정

사용자 지정 위임을 사용하여 하위 도메인의 전체 소유권을 확보하고 고유한 SSL 인증서를 업로드하며 도메인 구성에 대한 모든 권한을 유지합니다.

[사용자 정의 하위 도메인 설정](../using/configuration/delegate-custom-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

CNAME에서 사용자 지정 위임으로 마이그레이션

기존 CNAME 구성 하위 도메인을 사용자 지정 위임으로 마이그레이션하여 보안 정책을 충족하고 인증서에 대한 모든 권한을 얻습니다.

[하위 도메인 마이그레이션](../using/configuration/custom-subdomain-migration.md)
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

## 추가 리소스

- **[랜딩 페이지 하위 도메인 구성](../using/landing-pages/lp-subdomains.md)** - 랜딩 페이지 및 구독 양식에 대한 하위 도메인을 설정합니다.
- **[웹 하위 도메인을 구성](../using/web/web-delegated-subdomains.md)** - 웹 경험 및 추적을 위한 하위 도메인을 위임합니다.
- **[채널 구성 시작](../using/configuration/get-started-configuration.md)** - 하위 도메인 위임을 포함하여 모든 채널 설정 단계에 대한 개요입니다.
