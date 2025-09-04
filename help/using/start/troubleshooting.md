---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 문제 해결
description: Journey Optimizer 문제 해결 질문
feature: Get Started
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 3ab8957d0aec6f30853de5537e03f0e7bec2017c
workflow-type: tm+mt
source-wordcount: '1663'
ht-degree: 2%

---

# 문제 해결 {#ajo-troubleshooting}


다음은 Adobe Journey Optimizer 문제 해결 문서 목록입니다. 각 문제 해결 섹션은 FAQ에 대한 답변과 문제에 대한 솔루션을 제공합니다.

[Adobe Experience Platform FAQ 및 문제 해결 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/landing/troubleshooting#service-troubleshooting-directory){target="_blank"}도 참조하세요.

## 이메일 채널 {#ajo-troubleshooting-email}

### 이메일 디자인 {#ajo-troubleshooting-design}

+++ 테마를 사용하여 Adobe Journey Optimizer에서 이메일 서식 문제를 방지하는 방법

Adobe Journey Optimizer(AJO)에서 이메일 헤더의 기본 CSS 블록을 수정하면 예기치 않은 형식 문제가 발생할 수 있습니다(특히 콘텐츠 조각을 제거한 후). 이러한 문제는 모바일 디바이스에서 더 눈에 띄며 레이아웃 변경 또는 스타일 불일치를 초래할 수 있습니다. 이를 방지하려면 테마 기능을 사용하여 시스템에서 생성한 CSS 스타일을 변경하지 않고 사용자 지정 CSS를 안전하게 적용하십시오.

이 문제를 해결하는 방법은 [이 문제 해결 문서](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-27252){target="_blank"}를 참조하세요.

전자 메일 서식 [에 대한 자세한 내용은 이 페이지](../email/get-started-email-design.md)를 참조하세요.

+++


+++ 편집 가능한 필드가 있는 조각이 작동하지 않는 이유는 무엇입니까?

Adobe Journey Optimizer에서 편집 가능한 필드가 있는 조각이 템플릿에 추가될 때 올바르게 로드되지 않거나 예기치 않게 복제될 수 있습니다. 이 문제는 일반적으로 여러 환경에서 특정 조각에 영향을 줍니다.

이 문제를 해결하는 방법은 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26908){target="_blank"}를 참조하세요.

사용자 지정 가능한 조각에 대해 자세히 알아보세요[이 페이지의](../content-management/customizable-fragments.md).

+++

+++ 이메일 템플릿과 컨텐츠가 게시되지 않은 여정에서 사라지는 이유는 무엇입니까?

게시되지 않은 여정에서 이메일 템플릿을 편집할 때 특정 이메일의 콘텐츠와 템플릿이 예기치 않게 사라질 수 있습니다. 이로 인해 재작업과 지연이 발생할 수 있습니다. 이 문제의 위험을 줄이려면 동시 편집을 방지하고, 열려 있는 탭 수를 제한하고, 변경 내용을 자주 저장하십시오.

이 문제를 해결하는 방법은 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"}를 참조하세요.

[ 서식 파일에 대해 자세히 알아보세요](../email/use-email-templates.md).

+++

+++ Adobe Journey Optimizer에서 프로필에 여러 개의 푸시 토큰이 있을 수 있습니까?

Journey Optimizer에서 푸시 알림을 구현할 때 단일 프로필에 실제로 여러 디바이스와 연결된 여러 푸시 토큰이 있을 수 있습니다. 푸시 알림 캠페인 동안 Journey Optimizer은 이러한 토큰을 관리하고 모든 관련 장치에서 타겟팅된 프로필에 연결할 수 있도록 설계되었습니다.

푸시 토큰 관리에 대한 자세한 내용은 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"}를 참조하세요.

푸시 구성 [에 대한 자세한 내용은 이 페이지](../push/push-configuration.md)를 참조하세요.

+++

### 이메일 추적 및 보고 {#ajo-troubleshooting-tracking}

+++ 보고에서 이메일 추적 링크가 누락되지 않도록 하는 방법

이메일 URL이 동적 변수를 사용하고 http로 시작하지 않거나 논리 문이 URL 필드에 배치된 경우 Adobe Journey Optimizer에서 링크 추적이 누락됩니다. 이 문제를 해결하려면 모든 URL이 http로 시작하는지 확인하고, URL 필드에 논리를 사용하지 말고, 복잡한 개인화 논리를 HTML 콘텐츠 또는 사전 처리된 속성으로 이동하십시오.


이 문제를 해결하는 방법은 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26932){target="_blank"}를 참조하세요.

이 페이지의 [전자 메일 추적에 대해 자세히 알아보세요](../email/message-tracking.md).

+++

### 이메일 전송 {#ajo-troubleshooting-sending}

+++ API에서 트리거된 트랜잭션 이메일 캠페인을 설정할 때 메일 교환기 오류를 해결하려면 어떻게 합니까? 

Adobe Journey Optimizer에서 API 트리거 트랜잭션 전자 메일 캠페인에 대한 채널 구성을 만드는 동안 메일 교환기(MX) 오류가 발생하는 경우 **DNS 잘못된 구성** 또는 **DMARC 정책 제한** 때문일 수 있습니다. 이 문제를 해결하려면 DNS가 올바르게 구성되었는지 확인하고 도메인이 **도메인 기반 메시지 인증, 보고 및 준수(DMARC)** 요구 사항을 준수하는지 확인하십시오.

이 문제를 해결하는 방법은 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26200){target="_blank"}를 참조하세요.

이 페이지에서 [이메일 DMARC 정책에 대해 자세히 알아보세요](../configuration/dmarc-record-update.md).

[API 트리거 캠페인 설명서](../campaigns/api-triggered-campaigns.md)도 참조하세요.
+++

## 푸시 채널 {#ajo-troubleshooting-push}

+++ Adobe Journey Optimizer에서 프로필에 여러 개의 푸시 토큰이 있을 수 있습니까?

Journey Optimizer에서 푸시 알림을 구현할 때 단일 프로필에 실제로 여러 디바이스와 연결된 여러 푸시 토큰이 있을 수 있습니다. 푸시 알림 캠페인 동안 Journey Optimizer은 이러한 토큰을 관리하고 모든 관련 장치에서 타겟팅된 프로필에 연결할 수 있도록 설계되었습니다.

푸시 토큰 관리에 대한 자세한 내용은 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"}를 참조하세요.

푸시 구성 [에 대한 자세한 내용은 이 페이지](../push/push-configuration.md)를 참조하세요.

+++

+++ 푸시 메시지를 클릭해도 구성된 웹 URL로 리디렉션되지 않는 이유는 무엇입니까?  

푸시 메시지가 의도한 웹 URL로 리디렉션되지 않는 경우 올바르지 않은 클릭 동작 구성 또는 비활성화된 푸시 알림 설정 때문일 수 있습니다. 푸시 메시지에 대한 **클릭 동작**&#x200B;이 올바르게 설정되어 있고 이 문제를 해결하기 위해 푸시 알림의 **자동 표시 및 추적**&#x200B;이 활성화되어 있는지 확인하십시오.

이 문제에 대한 자세한 내용은 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26226){target="_blank"}를 참조하세요.

푸시 구성 [에 대한 자세한 내용은 이 페이지](../push/push-configuration.md)를 참조하세요.

+++


## SMS 채널 {#ajo-troubleshooting-sms}

+++ 동의가 `marketing.sms.value=y`(으)로 설정되어 있어도 트랜잭션 SMS가 전달되지 않는 이유는 무엇입니까?

받는 사람이 SMS에 **STOP**&#x200B;에 응답하면 트랜잭션 메시지를 포함하여 앞으로 해당 단수에서 오는 모든 메시지가 차단됩니다. 트랜잭션 SMS의 중단 없는 전달을 보장하려면 수신자가 이전에 옵트아웃하지 않은 **별도의 짧은 번호**&#x200B;을(를) 통해 구성 및 전송하십시오.

이 문제에 대한 자세한 내용은 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26258){target="_blank"}를 참조하세요.

SMS 옵트아웃 구성 [에 대해 자세히 알아보세요](../sms/sms-opt-out.md).

+++


## 데이터 관리 {#ajo-troubleshooting-data-management}

+++ 새 샌드박스를 만들 때 프로필 및 데이터 레이크 데이터 세트에 TTL(Time-to-Live) 설정이 어떻게 적용됩니까?

Adobe Journey Optimizer에서 새 샌드박스를 프로비저닝하는 조직에서 TTL(Time-to-Live) 설정이 프로필 및 데이터 레이크 데이터 세트에 적용되는 방법에 대해 의문을 제기했습니다. 이 문서에서는 TTL 설정이 기존 샌드박스에 영향을 주지 않으며 새로 제공된 샌드박스에만 자동으로 적용됨을 명확히 설명합니다.

TTL 처리 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"}를 참조하세요.

이 페이지의 [ 데이터 집합 Time-to-Live에 대해 자세히 알아보세요](../data/datasets-ttl.md).

+++


## 프로필 및 대상자 관리 {#ajo-troubleshooting-audiences}

+++ 대상자 수 불일치를 해결하는 방법

Adobe Journey Optimizer의 **대상자 읽기** 기능에서 처리된 항목 수는 예상 대상자 수보다 적을 수 있습니다. 이 문제는 잘못된 네임스페이스 구성으로 인해 프로필이 여정에서 제외되는 경우가 많습니다. 이 해결 방법에는 네임스페이스 구성 확인 및 수정, 관련 설명서 검토 및 Adobe Journey Optimizer에서의 원활한 작업을 위한 우선 순위 조정이 포함됩니다.

이 문제를 해결하는 방법은 [이 문제 해결 문서](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"}를 참조하세요.

오래된 대상 수에 대한 [이 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26166){target="_blank"}도 참조하세요.

이 페이지의 **여정**&#x200B;에서 [대상자 읽기](../building-journeys/read-audience.md) 활동에 대해 자세히 알아보세요.

+++

+++ 프로필 업데이트가 실패한 이유는 무엇입니까?

Adobe Journey Optimizer에서 여정에서 **프로필 업데이트** 활동을 실행한 후 특정 필드 값이 올바르게 업데이트되지 않을 수 있습니다. 경우에 따라 업데이트된 필드가 사라지거나 이전 상태로 돌아갈 수 있습니다. 이를 해결하려면 충돌하는 규칙이나 조건을 확인하고 권한 설정을 검토하며 **프로필 업데이트** 활동에 고유한 데이터 세트를 사용하고 다른 수집 프로세스가 같은 프로필에 동시에 기록되고 있지 않은지 확인하십시오.

이 문제를 해결하는 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26352){target="_blank"}를 참조하세요.

이 페이지의 **** 여정에서 [프로필 업데이트](../building-journeys/update-profiles.md) 활동에 대해 자세히 알아보세요.

데이터 수집에 대한 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/tutorials/ingest-batch-data?lang=en#dataset-activity){target="_blank"}도 참조하세요.

+++

+++ 여정 입력 시 프로필 수와 관련 대상 수가 일치하지 않는 이유는 무엇입니까?

여정 실행 시 현재 날짜의 스냅샷을 사용할 수 없는 경우 여정이 이전 날짜의 프로필 스냅샷을 사용할 때 불일치가 발생할 수 있습니다.

이 문제를 해결하는 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26253){target="_blank"}를 참조하세요.

[이 Journey Optimizer 커뮤니티 게시물](https://experienceleaguecommunities.adobe.com/t5/real-time-customer-data-platform/profile-snapshot-and-segment-qualification-troubleshooting/ba-p/698998){target="_blank"}에서 자세히 알아보세요.

매일 작업이 예약된 시간을 확인하려면 [Adobe Experience Platform 일정 API 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/api/schedules?lang=en){target="_blank"}를 참조하십시오.

+++


+++ 대상자 모집단 문제를 해결하는 방법

종종 권한 부여, 프로비저닝 또는 권한 구성 오류로 인해 구성 요소 또는 리소스가 누락된 경우 대상자 채우기 문제가 발생할 수 있습니다. 이러한 문제를 해결하려면 먼저 권한을 확인하고 올바른 프로비저닝을 보장하며 권한을 검토하십시오. 문제가 지속되면 사례를 에스컬레이션하고 지원 팀과 조정하여 문제를 완전히 해결합니다.

이 문제를 해결하는 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26333){target="_blank"}를 참조하세요.

이 페이지의 **** 여정에서 [프로필 업데이트](../building-journeys/update-profiles.md) 활동에 대해 자세히 알아보세요.

[Adobe Real-Time CDP 프로필 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide?lang=en#profile-detail){target="_blank"}도 참조하세요.

+++

+++ Adobe Journey Optimizer에서 대상자 변경 후 여정 트리거 문제를 해결하려면 어떻게 합니까? 

병합 여정의 변경과 같이 연결된 대상자가 수정된 후 캠페인이 중지되면 캠페인 흐름이 중단될 수 있습니다. 이 문제를 해결하려면 트리거가 올바르게 작동하도록 업데이트된 대상 설정으로 **여정을 복제하고**&#x200B;다시 게시합니다.

이 문제를 해결하는 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26224){target="_blank"}를 참조하세요.

[ 여정을 이 페이지에서](../building-journeys/journey-ui.md#duplicate-a-journey)에 복제하는 방법을 알아보세요.

+++


## 여정

### 이벤트

+++ 내 이벤트가 의도한 여정을 트리거하지 않는 이유는 무엇입니까?  

이벤트가 **DCCS(Data Collection Core Service)**&#x200B;로 스트리밍되지 않고 **쿼리 서비스를 통해 만들어진**&#x200B;에서 모든 기준이 충족되는 경우에도 여정을 트리거하지 못할 수 있습니다. 이 문제를 해결하려면 이벤트 구성을 검토하고 이벤트가 **DCCS로 직접 스트리밍되는지**&#x200B;확인한 다음 **테스트 모드**&#x200B;를 사용하여 기능을 확인하십시오.

이 문제를 해결하는 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26031){target="_blank"}를 참조하세요.

[ 이벤트에 대해 자세히 알아보세요](../event/about-events.md).

[여정 이벤트 보호](../start/guardrails.md#events)도 참조하세요.

+++

## 결정 {#ajo-troubleshooting-decisioning}

+++ 오퍼 컬렉션을 만들 때 문제를 해결하려면 어떻게 합니까?

조직에 대해 **카탈로그가 프로비저닝되지 않은 경우**&#x200B;오퍼 컬렉션을 만드는 데 문제가 발생하는 경우가 많습니다. 이 문제를 해결하려면 오퍼 컬렉션을 만들기 전에 필요한 모든 카탈로그가 올바르게 프로비저닝되었는지 확인하십시오.

이 문제를 해결하는 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26265){target="_blank"}를 참조하세요.

오퍼 컬렉션 [에 대해 자세히 알아보세요](../offers/offer-library/creating-collections.md).

+++


## 다국어 {#ajo-troubleshooting-multilingual}

+++ `Message validation error (CJMMAS - 1069-500)` 문제를 해결하는 방법

Adobe Journey Optimizer에서 다국어 기능에 연결된 메시지 유효성 검사 오류(CJMMAS - 1069-500)로 인해 여정이 테스트 모드 또는 게시됨으로 설정되지 않습니다.

이 문제를 해결하는 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26168){target="_blank"}를 참조하세요.

이 페이지에서 [다국어 콘텐츠에 대해 자세히 알아보세요](../content-management/multilingual-gs.md).

++


## 구성 {#ajo-troubleshooting-config}

### 보안 {#ajo-troubleshooting-security}

+++ 사용자 지정 작업에 대해 TLS v1.3을 활성화하려면 어떻게 합니까?  

타사 시스템에 연결할 때 **데이터 무결성 및 보안을 유지**&#x200B;하려면 사용자 지정 작업에 대해 전송 계층 보안(**TLS**) v1.3이 활성화되어 있는지 확인하십시오. 이를 통해 통신을 보호하고 잠재적인 보안 취약점을 방지할 수 있습니다.


자세한 내용은 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26223){target="_blank"}를 참조하세요.

이 페이지에서 [다국어 콘텐츠에 대해 자세히 알아보세요](../action/about-custom-action-configuration.md).

+++

### 대시보드 {#ajo-troubleshooting-dashboards}

+++ Adobe Journey Optimizer의 쿼리에서 직접 대시보드를 만들 수 없는 이유는 무엇입니까? 

Adobe Journey Optimizer의 경우 쿼리에서 직접 대시보드를 생성할 수 없습니다. 대시보드를 작성하려면 Adobe Experience Platform 내에서 사용 가능한 **대시보드 만들기 기능**&#x200B;을 사용하십시오. 이 기능을 사용하면 쿼리 데이터를 효과적으로 시각화하고 분석할 수 있습니다.

자세한 내용은 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26201){target="_blank"}를 참조하세요.

++