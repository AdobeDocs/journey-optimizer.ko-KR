---
solution: Journey Optimizer
product: journey optimizer
title: 오류 코드 참조
description: Adobe Journey Optimizer의 일반적인 오류 코드 및 문제 해결 방법에 대해 알아봅니다
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
keywords: 오류, 코드, 문제 해결, 여정, 캠페인, 메시지
source-git-commit: bf6cc008acba9df44b239e8ac2425c9ffe700229
workflow-type: tm+mt
source-wordcount: '1513'
ht-degree: 1%

---


# 오류 코드 참조 {#error-codes}

Adobe Journey Optimizer은 표준화된 오류 코드를 사용하여 여정, 캠페인 및 메시지 구성 전반에서 문제를 빠르게 식별하고 해결하는 데 도움이 됩니다. 이러한 오류 코드를 이해하면 문제 해결 시간을 크게 줄이고 최적의 캠페인 성능을 유지하는 데 도움이 됩니다.

## 오류 코드 구조 이해 {#error-code-structure}

Adobe Journey Optimizer 오류 코드는 구성 요소 및 문제 유형을 식별하는 데 도움이 되는 일관된 이름 지정 패턴을 따릅니다.

* **서비스 접두사**: 오류를 생성한 Adobe Journey Optimizer 서비스를 나타냅니다(예: 푸시/전송 서비스용 CJMPTS, 여정 런타임용 CJMRT, 메시지 작성 서비스용 CJMMAS).
* **오류 번호**: 특정 오류 조건에 대한 고유 식별자
* **HTTP 상태 코드**: 표준 HTTP 상태 코드(예: 400, 403, 422, 500)

예: `CJMRT-030012-422`은(는) 오류 번호가 030012이고 HTTP 상태가 422(처리할 수 없는 엔터티)인 CJMRT(여정 런타임 오류)를 나타냅니다.

## 오류 코드를 찾을 수 있는 위치 {#find-error-codes}

오류 코드는 Adobe Journey Optimizer 내 여러 위치에 나타납니다.

* 여정 실행 보고서 및 로그
* Campaign 활성화 화면
* 메시지 유효성 검사 경고
* 시스템 알림 및 경고
* API 응답(REST API 사용 시)

오류가 발생하면 전체 오류 코드와 함께 제공되는 요청 ID를 참고하십시오. 이러한 ID는 문제 해결 및 지원 에스컬레이션에 필요합니다.

## 서비스별 일반 오류 코드 {#error-codes-by-service}

### CJMPTS: 푸시 및 전송 서비스 오류 {#cjmpts-errors}

이러한 오류는 푸시 알림 게재 및 메시지 전송 작업 중에 발생합니다.

| 오류 코드 | 설명 | 근본 원인 | 해결 방법 |
|------------|-------------|-----------|-----------|
| **CJMPTS-1510-500** | 푸시 채널 전송 시 내부 서버 오류 | 백엔드 푸시/전송 오작동, 공급자 또는 인프라 오류 | &#x200B;1. 채널 프로비저닝 설정<br/>2을 확인합니다. 푸시 자격 증명이 유효한지 확인<br/>3. <br/>4 작업을 다시 시도하십시오. 영구적인 경우 Adobe 지원 팀에 요청 ID <br/><br/>**관련 설명서**&#x200B;로 문의하십시오. [푸시 구성](../push/push-configuration.md) |
| **CJMPTS-1023-500** | 푸시 전송/프로세스 중 내부 서버 오류(타사 게이트웨이) | 일시적인 클라우드 오작동 또는 알 수 없는 서비스 오류 | &#x200B;1. 공급자/채널 구성 확인<br/>2. 타사 게이트웨이 상태 확인<br/>3. 몇 분 후 다시 시도하십시오<br/>4. 추가 컨텍스트에 대한 로그 검토&#x200B;<br/><br/>**관련 설명서**: [푸시 알림](../push/create-push.md) |
| **CJMPTS-1310-500** | 렌더링 서비스의 내부 오류(미리 보기 또는 라이브 보내기) | 다운스트림 템플릿 렌더러가 실패했습니다. 일반적으로 JSON/템플릿 구문 문제 | &#x200B;1. 템플릿 구문 및 구조의 유효성을 검사합니다<br/>2. 모든 개인화 변수가 유효한지 확인<br/>3. 테스트 페이로드를 사용하여 문제를 식별하십시오<br/>4. 필요한 경우 템플릿 복잡성 단순화&#x200B;<br/><br/>**관련 설명서**: [메시지 템플릿](../content-management/content-templates.md), [Personalization 구문](../personalization/personalization-syntax.md) |

### CJMRT: 여정 런타임 및 API 오류 {#cjmrt-errors}

이러한 오류는 여정 실행, 이벤트 처리 및 API 작업 중에 발생합니다.

| 오류 코드 | 설명 | 근본 원인 | 해결 방법 |
|------------|-------------|-----------|-----------|
| **CJMRT-030012-422** | 처리할 수 없는 엔티티 - 액션 실패, 잘못된 이벤트 또는 잘못된 페이로드 | 잘못된 입력 데이터(예: 존재하지 않는 대상, 이벤트 또는 속성) | &#x200B;1. 입력/이벤트 페이로드 구조 <br/>2을(를) 다시 확인합니다. 참조된 개체(대상, 데이터 세트)가 있고 활성 상태인지 확인하십시오<br/>3. 모든 필수 필드가 있는지 확인합니다<br/>4. 정상 작동이 확인된 페이로드로 테스트&#x200B;<br/><br/>**관련 설명서**: [여정 문제 해결](troubleshooting.md), [이벤트 구성](../event/about-events.md) |
| **CJMRT-130004-400** | 잘못된 요청 - 여정 노드 또는 채널 구성에서 잘못된 입력 | 여정 페이로드 또는 구성 참조가 제거됨/잘못된 리소스 | &#x200B;1. 여정 노드 구성 검토<br/>2. 참조된 모든 리소스(메시지, 대상, 작업)가 있는지 확인하십시오<br/>3. 끊어진 참조를 수정하거나 업데이트하십시오<br/>4. 필요한 경우 여정 구성을 다시 빌드합니다&#x200B;<br/><br/>**관련 설명서**: [여정 만들기](journey-gs.md), [사용자 지정 작업](../action/about-custom-action-configuration.md) |
| **CJMRT-000032-409** | 충돌 - 리소스가 이미 있음 | 중복 ID 또는 이름으로 리소스 만들기 시도 | &#x200B;1. 모든 리소스에 고유 ID 및 이름을 사용합니다<br/>2. 같은 식별자<br/>3을(를) 가진 기존 리소스를 확인하십시오. 충돌하는 개체를 삭제하거나 이름을 바꾸십시오<br/>4. 이름 지정 규칙 검토&#x200B;<br/><br/>**관련 설명서**: [여정 버전](journey-gs.md#journey-versions) |
| **CJMRT-170016-400** | 여정 구성/미리보기 중 잘못된 요청 | 페이로드에 필수 종속성이 없거나 템플릿 링크가 끊어졌습니다. | &#x200B;1. 필요한 모든 리소스가 활성 상태인지 확인합니다<br/>2. 템플릿 및 콘텐츠 블록이 게시되었는지 확인<br/>3. 모든 종속성이 올바르게 연결되어 있는지 확인합니다<br/>4. 여정 테스트 모드 결과 검토&#x200B;<br/><br/>**관련 설명서**: [여정 테스트](testing-the-journey.md), [여정 종속성](journey-gs.md) |
| **CJMRT-080608-400** | 도메인/채널/위임에 잘못된 요청이 있음 | 필수 DNS 레코드 또는 이메일/SMS 구성 누락 | &#x200B;1. 전자 메일 도메인에 대한 DNS 구성을 완료합니다<br/>2. 하위 도메인 위임이 완료되었는지 확인<br/>3. 구성 마법사를 다시 실행하십시오<br/>4. DNS 전파 허용 시간(최대 72시간)<br/><br/>**관련 설명서**: [채널 표면](../configuration/channel-surfaces.md), [하위 도메인 위임](../configuration/delegate-subdomain.md) |
| **CJMRT-110100-500** | 페이로드 내부 오류 | 백엔드 데이터/구성 버그 또는 지원되지 않는 구성 | &#x200B;1. <br/>2 작업을 다시 시도하십시오. 고급 기능을 사용하는 경우 구성을 단순화합니다<br/>3. 요청 ID 및 정확한 페이로드를 사용하여 Adobe 지원 센터로 에스컬레이션합니다<br/>4. 릴리스 정보에서 알려진 문제를 확인합니다&#x200B;<br/><br/>**관련 설명서**: [여정 문제 해결](troubleshooting.md) |

### CJMMAS: 메시지 작성 서비스 오류 {#cjmmas-errors}

메시지, 사전 설정 및 콘텐츠를 작성, 편집 또는 게시할 때 이러한 오류가 발생합니다.

| 오류 코드 | 설명 | 근본 원인 | 해결 방법 |
|------------|-------------|-----------|-----------|
| **CJMMAS-1149-400** | 메시지, 사전 설정 또는 변형을 저장할 때 잘못된 요청 | 메시지에 필수 필드가 누락되었거나 구성이 잘못되었습니다. | &#x200B;1. 모든 필수 필드(별표로 표시)를 작성합니다<br/>2. 메시지/사전 설정 구성의 유효성을 검사합니다<br/>3. 필드 값 형식 및 제약 조건을 확인하십시오<br/>4. UI에서 유효성 검사 메시지 검토&#x200B;<br/><br/>**관련 설명서**: [전자 메일 채널](../email/get-started-email.md), [채널 표면](../configuration/channel-surfaces.md) |
| **CJMMAS-2073-422** | 메시지 사전 설정 편집에서 처리할 수 없는 엔티티 | 유효성 검사 오류, 지원되지 않는 필드 또는 잘못된 구문 | &#x200B;1. 표시된 대로 구문/필드 오류를 수정합니다<br/>2. 정상 작동이 확인된 구성과 비교<br/>3. 저장하기 전에 메시지 UI 유효성 검사 사용<br/>4. 설명서에서 필드 요구 사항 검토&#x200B;<br/><br/>**관련 설명서**: [메시지 사전 설정](../configuration/channel-surfaces.md), [전자 메일 설정](../email/email-settings.md) |
| **CJMMAS-1300-500** | 메시지 작성의 내부 오류 | 인프라 문제, 대용량 콘텐츠 또는 서비스 다운타임으로 인한 백엔드 충돌 | &#x200B;1. 템플릿/콘텐츠를 단순화합니다(크기/복잡성 감소)<br/>2. <br/>3 작업을 다시 시도하십시오. 작업을 증분 저장<br/>4. 영구적인 경우 Adobe 지원&#x200B;<br/><br/>**관련 설명서**: [콘텐츠 템플릿](../content-management/content-templates.md)(으)로 에스컬레이션 |
| **CJMMAS-2001-200** | 성공 상태이지만 오류 배너: 옵트아웃 링크가 누락됨 | 이메일 변형에 필수 구독 취소 링크가 없음 | &#x200B;1. 모든 이메일 변형에 옵트아웃/구독 취소 링크를 추가합니다<br/>2. 모든 언어 버전<br/>3에 링크가 있는지 확인하십시오. 개인화 도우미를 사용하여 옵트아웃 링크<br/>4을(를) 삽입하십시오. 게시하기 전에 모든 변형을 테스트합니다&#x200B;<br/><br/>**관련 설명서**: [옵트아웃 관리](../privacy/opt-out.md), [전자 메일 디자인](../email/content-from-scratch.md) |
| **CJMMAS-1603-403** | 템플릿 또는 사전 설정을 업데이트/게시할 때 사용할 수 없음 | 사용자에게 필요한 권한/역할이 없거나 현재 상태에서 허용되지 않는 작업입니다. | &#x200B;1. 사용자에게 적절한 권한이 있는지 확인합니다(메시지 관리자, 작성자 등).<br/>2. 사전 설정/템플릿 상태(초안, 게시됨, 보관됨)<br/>3 확인 필요한 경우 관리자에게 액세스 권한을 요청하십시오<br/>4. 제품 프로필 할당 검토&#x200B;<br/><br/>**관련 설명서**: [권한](../administration/permissions.md), [액세스 제어](../administration/permissions-overview.md) |

### CJMCMP: 캠페인 오류 {#cjmcmp-errors}

이러한 오류는 캠페인 생성, 구성 및 활성화 중에 발생합니다.

| 오류 코드 | 설명 | 근본 원인 | 해결 방법 |
|------------|-------------|-----------|-----------|
| **CJMCMP-2050-400** | 캠페인 활성화 또는 승인의 잘못된 요청 | 캠페인이 유효하지 않거나 누락된 정책 또는 세그먼트를 참조합니다. | &#x200B;1. 모든 캠페인 노드 구성을 감사<br/>2. 정책/세그먼트 링크가 최신 링크이고 유효한지 확인<br/>3. 올바른 구성으로 업데이트하십시오<br/>4. 활성화 전에 캠페인 다시 테스트&#x200B;<br/><br/>**관련 설명서**: [캠페인 만들기](../campaigns/create-campaign.md), [캠페인 승인](../test-approve/gs-approval.md) |

## 일반적인 문제 해결 방법 {#troubleshooting-approach}

오류 코드가 나타나면 다음 체계적인 방법을 따르십시오.

1. **오류 식별**: 전체 오류 코드, HTTP 상태 및 함께 제공되는 메시지나 요청 ID를 참고하십시오.

2. **서비스 찾기**: 영향을 받는 구성 요소를 식별하려면 서비스 접두사(CJMPTS, CJMRT, CJMMAS, CJMCMP)를 사용하십시오.

3. **상태 코드 확인**:
   * **400(잘못된 요청)**: 입력 데이터 및 구성 검토
   * **403(사용할 수 없음)**: 권한 및 액세스 권한 확인
   * **409(충돌)**: 중복되거나 충돌하는 리소스를 찾습니다
   * **422(처리할 수 없는 엔터티)**: 스키마 요구 사항에 대한 데이터 유효성 검사
   * **500(내부 서버 오류)**: 다시 시도하여 지원을 위해 에스컬레이션할 수 있습니다.

4. **최근 변경 내용 검토**: 최근에 수정된 내용(여정 업데이트, 새 캠페인, 구성 변경 등)을 고려합니다.

5. **설명서를 참조하세요**: 이 안내서에 제공된 링크를 사용하여 영향을 받는 기능에 대한 자세한 설명서에 액세스합니다.

6. **필요한 경우 다시 시도**: 500 계열 오류의 경우 몇 분 후에 간단히 다시 시도하면 일시적인 문제가 해결됩니다.

7. **필요한 경우 에스컬레이션**: 해결 단계를 수행한 후에도 오류가 지속되면 Adobe 지원 센터에 다음 방법으로 문의하십시오.
   * 전체 오류 코드
   * 요청 ID(가능한 경우)
   * 재현 단계
   * 관련 구성 세부 정보

## 일반적인 오류를 방지하는 모범 사례 {#best-practices}

### 여정 활성화 전 {#journey-best-practices}

* **모든 리소스의 유효성을 검사합니다**: 참조된 모든 대상, 데이터 원본 및 사용자 지정 작업이 활성 상태인지 확인하세요.
* **철저하게 테스트**: 게시하기 전에 테스트 모드를 사용하여 문제를 식별합니다([자세히 알아보기](testing-the-journey.md))
* **권한 확인**: 모든 구성 요소에 필요한 액세스 권한이 있는지 확인하십시오.
* **종속성 검토**: 연결된 모든 메시지와 콘텐츠가 게시되었는지 확인

### 메시지를 만들 때 {#message-best-practices}

* **필수 필드 완료**: 저장하기 전에 항상 모든 필수 필드를 입력하십시오.
* **옵트아웃 링크 포함**: 모든 이메일 변형에 구독 취소 링크 추가([자세히 알아보기](../privacy/opt-out.md))
* **개인화 확인**: 샘플 프로필로 모든 다이내믹 콘텐츠를 테스트합니다([자세히 알아보기](../personalization/personalization-build-expressions.md)).
* **관리 가능한 템플릿 유지**: 렌더링 문제를 일으킬 수 있는 너무 복잡한 템플릿을 사용하지 마십시오

### 캠페인 관리용 {#campaign-best-practices}

* **대상 데이터 확인**: 대상 대상이 올바르게 구성 및 채워졌는지 확인하십시오.
* **승인 상태 확인**: 활성화하기 전에 승인 요구 사항을 이해합니다([자세히 알아보기](../test-approve/gs-approval.md)).
* **구성 모니터링**: 채널 표면 및 사전 설정의 유효성을 정기적으로 검토합니다.
* **DNS 변경 계획**: 도메인을 업데이트할 때 DNS 전파에 충분한 시간을 허용합니다.

## 추가 리소스 {#additional-resources}

* [여정 문제 해결](troubleshooting.md)
* [실행 문제 해결](troubleshooting-execution.md)
* [인바운드 활동 문제 해결](troubleshooting-inbound.md)
* [사용자 지정 작업 문제 해결](../action/troubleshoot-custom-action.md)
* [여정 FAQ](journey-faq.md)
* [가드레일 및 제한 사항](limitations.md)

## 지원 받기 {#getting-support}

이 안내서를 사용하여 해결할 수 없는 지속적인 오류가 발생하는 경우:

1. **정보 수집**: 오류 코드, 요청 ID, 타임스탬프 및 재현 단계를 수집합니다.
2. **시스템 상태 확인**: 알려진 서비스 문제에 대해서는 [Adobe 상태](https://status.adobe.com/){target="_blank"}를 방문하세요.
3. **설명서 검색**: 솔루션에 대한 [Adobe Experience League](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=ko){target="_blank"} 검토
4. **커뮤니티 참여**: [Adobe Journey Optimizer 커뮤니티](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}에 질문 게시
5. **Adobe 지원에 문의**: 모든 관련 세부 정보를 포함한 지원 티켓을 제출합니다.

>[!NOTE]
>
>이 오류 코드 참조는 새 코드가 식별되고 문서화됨에 따라 계속 업데이트됩니다. 최신 정보는 [Adobe Journey Optimizer 커뮤니티 블로그](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/bg-p/journey-optimizer-blogs){target="_blank"}를 정기적으로 확인하십시오.

**관련 항목**

* [Adobe Journey Optimizer 오류 코드 식별: 1부](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/ba-p/760884){target="_blank"}
* [Adobe Journey Optimizer 오류 코드 식별: Part 2](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/bc-p/782661){target="_blank"}

