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
source-git-commit: 0cc119d3e4c1ffa676f00fcedb93d8818f176689
workflow-type: tm+mt
source-wordcount: '2665'
ht-degree: 1%

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

+++ HTML 조각이 이메일에 올바르게 표시되지 않는 이유는 무엇입니까?

HTML 조각이 전자 메일에서 제대로 렌더링되지 않을 수 있으며 실제 콘텐츠가 아닌 **조각 ID**(으)로 표시되는 경우가 많습니다. 시각적 조각과 달리 HTML 조각은 세심한 구성이 필요합니다. 이 문제를 해결하려면 이메일 캠페인에서 **시각적 및 HTML 표현식 조각**&#x200B;을 모두 사용하는 모범 사례를 따르십시오.

이 문제를 해결하는 방법은 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-25441){target="_blank"}를 참조하세요.

HTML 조각 [에 대해 자세히 알아보세요](../content-management/fragments.md).

+++

+++ 이메일 템플릿과 컨텐츠가 게시되지 않은 여정에서 사라지는 이유는 무엇입니까?

게시되지 않은 여정에서 이메일 템플릿을 편집할 때 특정 이메일의 콘텐츠와 템플릿이 예기치 않게 사라질 수 있습니다. 이로 인해 재작업과 지연이 발생할 수 있습니다. 이 문제의 위험을 줄이려면 동시 편집을 방지하고, 열려 있는 탭 수를 제한하고, 변경 내용을 자주 저장하십시오.

이 문제를 해결하는 방법은 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"}를 참조하세요.

[ 서식 파일에 대해 자세히 알아보세요](../email/use-email-templates.md).

+++

+++ 이메일 프리헤더 필드가 &#39;자신의 코드 작성&#39; 모드로 표시되지 않는 이유는 무엇입니까? 

**전자 메일 본문 편집** 기능 아래의 **&#39;자신의 코드 작성&#39;** 모드에서는 사전 머리글 입력 필드가 표시되지 않습니다. 사전 머리글 텍스트를 포함하려면 사용자가 사용자 지정 HTML 콘텐츠 내에서 사전 헤더를 **수동으로 코딩해야 합니다**.

이 문제를 해결하는 방법은 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26174){target="_blank"}를 참조하세요.

전자 메일 사전 머리글 구성 [에 대한 자세한 내용은 이 페이지](../email/header-parameters.md)를 참조하세요.

+++

+++ 이메일 템플릿에서 HTML 구성 요소를 사용할 때 링크 비헤이비어가 일치하지 않는 이유는 무엇입니까?  

이메일 템플릿에 **HTML 구성 요소**&#x200B;를 추가할 때 링크는 **이메일 클라이언트**, **보기 모드** 또는 **장치/브라우저**&#x200B;에 따라 다르게 작동할 수 있습니다. 예를 들어 앵커 링크는 전체 화면 보기와 **Outlook의 나란히 보기**&#x200B;에서 다르게 작동할 수 있습니다. 이메일 템플릿을 디자인하고 여러 클라이언트 및 장치에서 테스트할 때 이러한 변형을 숙지하십시오.

이 문제를 해결하는 방법은 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26221){target="_blank"}를 참조하세요.

이 페이지의 전자 메일 디자인 모범 사례 [도 참조하세요](../email/get-started-email-design.md).

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



## 인앱 채널

+++ Customer Journey Analytics의 인앱 채널에서 보고할 수 없는 이유는 무엇입니까?

Adobe Customer Journey Analytics의 **인앱 채널**&#x200B;에 대한 보고는 종종 잘못 구성된 **데이터 보기**, **데이터 세트** 또는 **스키마 업데이트**&#x200B;로 인해 발생합니다. 이러한 구성이 이 문제를 해결하기 위해 올바르게 적용되는지 확인하십시오.

이 문제에 대한 자세한 내용은 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26206){target="_blank"}를 참조하세요.

Customer Journey Analytics에서 Journey Optimizer 분석 데이터를 통합하는 방법에 대해 자세히 알아보세요. [이 페이지](https://experienceleague.adobe.com/en/docs/analytics-platform/using/integrations/ajo?lang=en#automatically-configure-journey-optimizer-integration){target="_blank"}.

[Journey Optimizer 전체 보고서 설명서](../reports/report-gs-cja.md)도 참조하세요.

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

+++ 참여 가능 프로필 수가 단기간에 크게 증가한 이유는 무엇입니까? 

**참여 가능한 프로필** 지표는 지난 12개월 동안 여정 또는 캠페인에 의해 참여된 고유한 프로필의 수를 반영합니다. 갑작스러운 증가는 대규모 대상이 타겟팅되거나 데이터 세트가 변경되어 발생할 수 있습니다. 이를 관리하려면 **프로필 계산 논리**&#x200B;를 검토하고, 큰 대상을 타겟팅하는 여정을 조사하고, 여정 수준에서 대상을 **필터링하고**&#x200B;하고, **대응 가능 대상 크기**&#x200B;를 줄이고, **데이터 집합 변경 사항을 모니터링하고**&#x200B;하십시오.

이 문제를 해결하는 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26161){target="_blank"}를 참조하세요.

[라이선스 사용 대시보드](../audience/license-usage.md)를 사용하여 조직의 라이선스 사용 및 참여 가능한 프로필 모니터링

[Adobe Experience Platform 쿼리 서비스 개요](https://experienceleague.adobe.com/en/docs/experience-platform/query/home?lang=en){target="_blank"}도 참조하세요.

+++

+++ 날짜 기능을 기반으로 의도한 대상 외부의 개인에게 이메일이 전송되는 이유는 무엇입니까?

**지정된 대상 기준을 충족하지 않는 받는 사람**&#x200B;에게 전자 메일을 보낼 수 있습니다. 예를 들어, 상환 날짜가 **2025년 7월 4일**&#x200B;인 구성원은 해당 날짜 이후의 구성원에게만 이메일을 받을 수 있습니다. 이 동작은 **잘못 구성된 대상 세분화** 또는 **프로필 자격 논리의 예기치 않은 변경** 때문일 수 있습니다.

이 문제를 해결하는 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26173){target="_blank"}를 참조하세요.

이 페이지의 [날짜 함수](../../rp_landing_pages/date-landing-page.md)에 대해 자세히 알아보세요.

+++

+++ 여정을 저장할 때 대상자 선택 문제 및 Chrome 오류를 해결하려면 어떻게 합니까?

여정 조건에 대상을 추가하면 경우에 따라 Chrome에서 **응용 프로그램 충돌**&#x200B;이 발생하거나 여정 저장 시 오류를 포함한 **Aw Snap 오류**&#x200B;이 표시될 수 있습니다. 이러한 문제는 종종 **Chromium 서비스**&#x200B;와 관련이 있습니다. 이 문제를 해결하려면 **브라우저 업데이트**&#x200B;를 적용하거나 적절한 **해결 방법**&#x200B;을 사용하십시오.

이 문제를 해결하는 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26145){target="_blank"}를 참조하세요.

+++

## 여정 {#ajo-troubleshooting-journeys}

### 여정 버전 {#ajo-troubleshooting-journey-versions}

+++ 새 여정 버전을 만들 때 표현식이 손실되는 이유는 무엇입니까?  

새 버전의 여정을 만들 때 특정 단계&#x200B;**의**&#x200B;식이 손실되어 오류가 발생하고 수동으로 다시 입력해야 할 수 있습니다. 이 문제를 해결하려면 **여정을 복제**&#x200B;하고, 재현성을 테스트하고, **브라우저 다시 로드를 피하고**&#x200B;이전 여정의 경우 **업데이트된 캔버스**&#x200B;를 사용하십시오.

이 문제를 해결하는 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26152){target="_blank"}를 참조하세요.

[ 여정을 이 페이지에서](../building-journeys/journey-ui.md#duplicate-a-journey)에 복제하는 방법을 알아보세요.

+++

### 시작 및 종료 {#ajo-troubleshooting-journeys-exit}

+++ 프로필이 여정을 조기에 종료하는 이유는 무엇입니까? 

보낸 메시지의 **상태 확인 피드백 상태**&#x200B;가 잘못 구성된 경우 프로필이 지정된 노드를 거치지 않고 예기치 않게 여정을 종료할 수 있습니다. 이 문제를 해결하려면 **조건 논리**&#x200B;를 검토하거나 **대체 논리**&#x200B;를 구현하거나 **구현 팀**&#x200B;에 문의하십시오.

이 문제를 해결하는 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26127){target="_blank"}를 참조하세요.

[여정 디자인 지침](../building-journeys/using-the-journey-designer.md)도 참조하세요.

+++


+++ 프로필이 예기치 않게 여정을 종료하는 이유는 무엇입니까?

**이벤트 제한**&#x200B;이 발생할 때 프로필이 예기치 않게 여정을 종료할 수 있으므로 처리된 이벤트 수가 시스템 용량을 초과할 경우 일부 프로필이 삭제됩니다. 프로필 종료를 줄이려면 **시스템 제한**&#x200B;을 이해하고, **이벤트 스파이크**&#x200B;를 모니터링하며, 임계값을 초과하지 않도록 **데이터 흐름**&#x200B;을 최적화하십시오.

이 문제를 해결하는 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26018){target="_blank"}를 참조하세요.

[여정 보호](../start/guardrails.md#journey-guardrails)도 참조하세요.

+++

### 이벤트 {#ajo-troubleshooting-journey-events}

+++ 내 이벤트가 의도한 여정을 트리거하지 않는 이유는 무엇입니까?  

이벤트가 **DCCS(Data Collection Core Service)**&#x200B;로 스트리밍되지 않고 **쿼리 서비스를 통해 만들어진**&#x200B;에서 모든 기준이 충족되는 경우에도 여정을 트리거하지 못할 수 있습니다. 이 문제를 해결하려면 이벤트 구성을 검토하고 이벤트가 **DCCS로 직접 스트리밍되는지**&#x200B;확인한 다음 **테스트 모드**&#x200B;를 사용하여 기능을 확인하십시오.

이 문제를 해결하는 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26031){target="_blank"}를 참조하세요.

[ 이벤트에 대해 자세히 알아보세요](../event/about-events.md).

[여정 이벤트 보호](../start/guardrails.md#events)도 참조하세요.

+++


+++ Adobe Journey Optimizer에서 대상자 변경 후 여정 트리거 문제를 해결하려면 어떻게 합니까? 

병합 여정의 변경과 같이 연결된 대상을 수정한 후 정책이 트리거를 중지하면 흐름이 중단될 수 있습니다. 이 문제를 해결하려면 트리거가 올바르게 작동하도록 업데이트된 대상 설정으로 **여정을 복제하고**&#x200B;다시 게시합니다.

이 문제를 해결하는 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26224){target="_blank"}를 참조하세요.

[ 여정을 이 페이지에서](../building-journeys/journey-ui.md#duplicate-a-journey)에 복제하는 방법을 알아보세요.

+++

### 사용자 지정 작업 {#ajo-troubleshooting-journeys-actions}

+++ 외부 타사 엔드포인트를 호출하는 사용자 지정 작업이 시간 초과된 이유는 무엇입니까?

**사용자 지정 작업**&#x200B;에서 외부 타사 끝점을 호출할 때 시간 초과 오류가 발생할 수 있습니다. 이 문제를 해결하려면 **끝점에 액세스할 수 있는지 확인**&#x200B;하고, **서버 로그**&#x200B;를 확인하고, **Adobe에서 차단이 없는지 확인**&#x200B;하고, 필요에 따라 끝점 구성을 업데이트하고, **업데이트 후 테스트**&#x200B;합니다. 또한 **API 호출 시간 제한 사양**&#x200B;을 염두에 두십시오.

이 문제를 해결하는 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26156){target="_blank"}를 참조하세요.

이 페이지[에서 여정 조절 API ](../configuration/throttling.md)에 대해 자세히 알아보세요.

[외부 시스템과 통합](../configuration/external-systems.md)도 참조하세요.

+++

## 규칙 {#ajo-troubleshooting-rules}

+++ 최대 가용량 규칙 드롭다운이 작동하지 않는 이유는 무엇입니까?

규칙 집합이 **잘못 구성됨** 또는 **액세스할 수 없음**&#x200B;일 때 **최대 가용량 규칙 드롭다운**&#x200B;에 문제가 발생하는 경우가 많습니다. 모든 규칙 세트가 올바르게 구성되고 문제를 해결할 수 있는지 확인하십시오.

자세한 내용은 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26204){target="_blank"}를 참조하세요.

최대 가용량 규칙 [을(를) 적용하는 방법은 이 섹션](../conflict-prioritization/rule-sets.md)을 참조하세요.

+++

## 결정 {#ajo-troubleshooting-decisioning}

+++ 오퍼 컬렉션을 만들 때 문제를 해결하려면 어떻게 합니까?

조직에 대해 **카탈로그가 프로비저닝되지 않은 경우**&#x200B;오퍼 컬렉션을 만드는 데 문제가 발생하는 경우가 많습니다. 이 문제를 해결하려면 오퍼 컬렉션을 만들기 전에 필요한 모든 카탈로그가 올바르게 프로비저닝되었는지 확인하십시오.

이 문제를 해결하는 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26265){target="_blank"}를 참조하세요.

오퍼 컬렉션 [에 대해 자세히 알아보세요](../offers/offer-library/creating-collections.md).

+++

+++ Offer Decisioning에 액세스할 수 없는 이유는 무엇입니까?  

Adobe Journey Optimizer을 사용하여 Adobe Target을 응용 프로그램에 통합하는 경우 데이터 스트림 구성 내에서 **Offer Decisioning** 옵션에 액세스할 수 없습니다. 이 문제는 일반적으로 **권한 설정** 또는 **프로비저닝 제약 조건** 때문에 발생합니다. 이 문제를 해결하려면 사용자 권한을 확인하고 필요한 프로비저닝이 제대로 되어 있는지 확인합니다.

이 문제를 해결하는 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26175){target="_blank"}를 참조하세요.

이 페이지[에서 Offer Decisioning ](../offers/get-started/starting-offer-decisioning.md#granting-acess-to-decision-management)에 필요한 권한에 대해 자세히 알아보세요.

+++



## 다국어 {#ajo-troubleshooting-multilingual}

+++ `Message validation error (CJMMAS - 1069-500)` 문제를 해결하는 방법

Adobe Journey Optimizer에서 다국어 기능에 연결된 메시지 유효성 검사 오류(CJMMAS - 1069-500)로 인해 여정이 테스트 모드 또는 게시됨으로 설정되지 않습니다.

이 문제를 해결하는 방법에 대해 알아보려면 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26168){target="_blank"}를 참조하세요.

이 페이지에서 [다국어 콘텐츠에 대해 자세히 알아보세요](../content-management/multilingual-gs.md).

+++


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

+++

## API {#ajo-troubleshooting-apis}

+++ 쿼리 서비스 API의 액세스 문제를 해결하려면 어떻게 합니까?  

Postman 또는 유사한 도구를 통해 **쿼리 서비스 API**&#x200B;를 사용할 때 발생하는 액세스 오류는 일반적으로 **권한 부족**&#x200B;으로 인해 발생합니다. 이 문제를 해결하려면 사용자 권한을 확인하고 API 자격 증명을 확인한 다음 필요한 경우 지원할 세부 정보를 제공합니다.

자세한 내용은 [이 문제 해결 문서](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26196){target="_blank"}를 참조하세요.

[API 자격 증명 관리 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions?lang=en#manage-api-credentials-for-role){target="_blank"}도 참조하세요.

+++

