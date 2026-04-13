---
solution: Journey Optimizer
product: journey optimizer
title: 통합에 대해 자주 묻는 질문
description: 메시지의 외부 데이터 및 컨텐츠를 위한 Journey Optimizer 통합에 대한 FAQ입니다.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
keywords: 통합, FAQ, 외부 데이터, 개인화
hide: true
source-git-commit: 8a2c90b22dbe68de57bbdbe06123a957e54648a6
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 1%

---

# 통합에 대해 자주 묻는 질문 {#vendor-integration-faq}

>[!BEGINSHADEBOX]

목차:

* [통합 작업](external-sources.md)
* [공급업체 통합 시작](vendor-integration-gs.md)
* [사용 가능한 공급업체](vendor-integration.md)
* **[FAQ](vendor-integration-faq.md)**

>[!ENDSHADEBOX]

다음은 Adobe Journey Optimizer의 **통합**&#x200B;에 대한 FAQ입니다.

## 시작하기

+++ Journey Optimizer에서 통합은 어떤 작업을 수행합니까?

외부 데이터 소스를 Journey Optimizer에 연결하므로 서드파티 시스템의 컨텐츠 및 데이터를 캠페인과 여정으로 가져오고 해당 데이터를 사용하여 메시지를 개인화할 수 있습니다.

➡️ [통합 개요에 대해 자세히 알아보기](external-sources.md)

+++

+++ 누가 통합을 구성하고 누가 콘텐츠에 이를 사용합니까?

관리자는 기술 구성을 만들고 활성화합니다(**[!UICONTROL 구성]** > **[!UICONTROL 통합]** > **[!UICONTROL 관리]** > **[!UICONTROL 통합 만들기]**). 마케터는 텍스트 또는 HTML 구성 요소에서 **[!UICONTROL 개인화 추가]**&#x200B;를 사용하고 **[!UICONTROL 통합]**&#x200B;을 열고 활성 통합을 선택하고 특성을 매핑합니다.

➡️ [관리자 및 마케터 워크플로에 대해 자세히 알아보기](external-sources.md)

+++

+++ 관리자 자격으로 UI에서 통합을 만들거나 관리하려면 어디로 해야 합니까?

왼쪽 메뉴에서 **[!UICONTROL 구성]** 섹션으로 이동하고 **[!UICONTROL 통합]** 카드에서 **[!UICONTROL 관리]**&#x200B;를 연 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

➡️ [통합 만들기에 대한 자세한 정보](external-sources.md#configure)

+++

+++ 통합에 대한 일반적인 사용 사례는 무엇입니까?

예를 들어 충성도 시스템의 보상 포인트, 제품 가격 정보, 추천 엔진의 추천, 배송 상태와 같은 물류 업데이트 등이 있습니다.

➡️ [타사 시스템의 예제 데이터에 대해 자세히 알아보기](external-sources.md)

➡️ [공급업체 통합 예제에 대해 자세히 알아보기](vendor-integration.md)

+++

## 구성

+++ 높은 수준에서 관리자 권한으로 통합을 구성하려면 어떻게 해야 합니까?

이름 및 설명, API 끝점 URL(경로 변수 포함), 경로 템플릿 값, **[!UICONTROL GET]** 또는 **[!UICONTROL POST]**, 선택적 헤더 및 쿼리 매개 변수, 인증 방법, 정책 설정(시간 초과 및 선택적 캐시 또는 다시 시도 등), 필드 매핑에 대한 샘플 JSON 응답, 유효한 경우 **[!UICONTROL 테스트 연결 보내기]** 및 **[!UICONTROL 활성화]**&#x200B;를 실행합니다.

➡️ [통합 구성에 대해 자세히 알아보기](external-sources.md#configure)

+++

+++ 지원되는 인증 유형은 무엇입니까?

다음 인증 유형을 사용할 수 있습니다. **[!UICONTROL 인증 없음]**, **[!UICONTROL API 키]**, **[!UICONTROL 기본 인증]** 및 **[!UICONTROL OAuth 2.0]**(해당되는 경우 OAuth에 대한 페이로드 구성 포함).

➡️ [인증 유형에 대해 자세히 알아보기](external-sources.md#configure)

+++

+++ 응답 페이로드 단계는 무엇에 사용됩니까?

샘플 JSON 응답을 붙여 넣으면 시스템에서 데이터 유형을 감지하고 메시지에 개인화를 위해 노출되는 필드를 선택할 수 있습니다. 작성 중에 마케터가 사용할 수 있는 필드를 제한할 수 있습니다.

➡️ [응답 페이로드 매핑에 대해 자세히 알아보기](external-sources.md#configure)

+++

+++ 마케터는 메시지에 통합을 어떻게 추가합니까?

캠페인 또는 여정 콘텐츠에서 텍스트 또는 HTML 구성 요소에 대해 **[!UICONTROL 개인화 추가]**&#x200B;를 사용하고 **[!UICONTROL 통합]**(으)로 이동하여 통합을 선택하고 저장합니다. 개인화 편집기의 알약 모드에서는 값을 구성의 변수(예: 헤더 또는 쿼리 매개 변수 또는 URL의 경로 변수)에 매핑할 수 있습니다.

➡️ [통합을 사용한 개인화에 대해 자세히 알아보기](external-sources.md#personalization)

+++

## 기능 및 사용 사례

+++ 여정 및 캠페인에서 통합을 사용할 수 있습니까?

예. 이 기능은 현재 제품 제한 내에서 **아웃바운드** 채널(예: 이메일, SMS 및 푸시)의 여정 및 캠페인 모두에 사용할 수 있습니다.

➡️ [여정 및 캠페인에 대해 자세히 알아보기](external-sources.md#limitations)

+++

+++ 재사용 가능한 조각에서 통합을 사용할 수 있습니까?

통합 기능은 조각에서 **지원되지 않습니다**. 제품이 지원하는 캠페인 및 여정 메시지 콘텐츠에서 통합을 사용합니다.

➡️ [조각 및 베타 제한에 대해 자세히 알아보기](external-sources.md#limitations)

+++

## 제한 사항

+++ 어떤 채널이 통합을 지원합니까?

**아웃바운드** 채널이 지원됩니다(예: 이메일, SMS, 푸시).

➡️ [지원되는 채널에 대해 자세히 알아보기](external-sources.md#limitations)

+++

+++ 지원되는 API 응답 형식은 무엇입니까?

API 호출 응답의 경우 필드 매핑에 대해 **JSON**&#x200B;이(가) 지원됩니다. JSON이 아닌 원시 바이너리 이미지 출력 및 형식은 이 워크플로우에서 사용할 수 없습니다.

➡️ [JSON 및 응답 형식에 대해 자세히 알아보기](external-sources.md#limitations)

+++

+++ 연결할 수 있는 API 패턴은 무엇입니까?

특정 콘텐츠를 대상으로 하는 **검색** API가 지원됩니다. **목록**&#x200B;개의 API(광범위한 목록 또는 페이지 매김 패턴)는 이 통합 모델에 대해 지원되지 않습니다.

➡️ [검색 및 목록 API에 대해 자세히 알아보기](external-sources.md#limitations)

+++

## 권한 및 관련 기능

+++ 통합을 구성하는 데 필요한 권한은 무엇입니까?

구성은 **[!UICONTROL 구성]** > **[!UICONTROL 통합]**&#x200B;에서 관리자 워크플로입니다. 정확한 권한 이름은 조직의 Admin Console 및 Journey Optimizer 제품 프로필에 따라 다릅니다. 관리자 또는 Adobe 담당자에게 확인합니다.

➡️ [통합이 구성된 위치에 대해 자세히 알아보기](external-sources.md#configure)

+++

+++ 통합이 Adobe Journey Optimizer 커넥터를 Experience Platform 소스로 대체합니까?

아니요. **통합**&#x200B;은(는) API에서 가져오는 메시지 콘텐츠의 개인화 필드를 위한 것입니다. **소스** 및 기타 데이터 수집 기능은 서로 다른 용도로 사용됩니다(예: 일괄 데이터 수집 및 프로필 보강). 각 기능을 원하는 범위에 사용합니다.

➡️ [통합 기능 자세히 알아보기](external-sources.md)

➡️ [Experience Platform 소스에 대해 자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=ko){target="_blank"}

+++

## 문제 해결

+++ 테스트 연결이 실패하거나 잘못된 상태로 유지되는 이유는 무엇입니까?

끝점 URL, HTTP 메서드, 경로 템플릿, 헤더 및 쿼리 매개 변수, 인증 및 정책 시간 제한을 확인합니다. 조정 후 **[!UICONTROL 테스트 연결 보내기]**&#x200B;를 사용합니다. 페이로드 문제의 경우 샘플이 유효한 JSON을 반영하고 선택한 필드가 API가 반환하는 필드와 일치하는지 확인하십시오.

➡️ [테스트 연결 및 페이로드 유효성 검사에 대해 자세히 알아보기](external-sources.md#configure)

+++

+++ 마케터가 선택기에서 내 통합을 보지 않는 이유는 무엇입니까?

테스트가 성공적으로 완료되면 통합이 **활성화**&#x200B;되어야 합니다. 마케터가 **[!UICONTROL 통합]**&#x200B;을 여는 경우에만 활성 통합이 표시됩니다. 통합이 아직 초안 상태이거나 비활성 상태인 경우 먼저 활성화를 완료하십시오.

➡️ [테스트 연결 및 활성화에 대해 자세히 알아보기](external-sources.md#configure)

+++

## 타사 공급업체

+++ 어떤 공급업체 예제를 사용할 수 있으며 API를 누가 보호합니까?

호환되는 API 엔드포인트를 노출하는 서드파티 플랫폼과 통합할 수 있습니다. **실례가 되는** 공급업체 패턴 및 구성 예제를 통해 호환되는 API를 모델링할 수 있습니다. 엔드포인트 보호에 대한 책임은 타사 플랫폼 및 팀에 있습니다.

➡️ [공급업체 통합 절차에 대해 자세히 알아보기](vendor-integration.md)

+++
