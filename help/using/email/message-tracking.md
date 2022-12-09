---
solution: Journey Optimizer
product: journey optimizer
title: 메시지 추적
description: 링크를 추가하고 보낸 메시지를 추적하는 방법을 알아봅니다
feature: Monitoring
topic: Content Management
role: User
level: Intermediate
exl-id: 689e630a-00ca-4893-8bf5-6d1ec60c52e7
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# 링크 추가 및 메시지 추적 {#tracking}

사용 [!DNL Journey Optimizer] 수신자의 동작을 모니터링하기 위해 컨텐츠에 링크를 추가하고 전송된 메시지를 추적하려면

## 추적 활성화 {#enable-tracking}

이메일 메시지 수준에서 을(를) 확인하여 추적을 활성화할 수 있습니다 **[!UICONTROL Email opens]** 및/또는 **[!UICONTROL Click on email]** 선택 사항 을 사용할 수 있습니다.

>[!BEGINTABS]

>[!TAB 여정에서 추적 활성화]

![](assets/message-tracking-journey.png)

>[!TAB 캠페인에서 추적 활성화]

![](assets/message-tracking-campaign.png)

>[!ENDTABS]

>[!NOTE]
>
>두 옵션 모두 기본적으로 활성화되어 있습니다.

이를 통해 수신자의 동작을 추적할 수 있습니다.

* **[!UICONTROL Email opens]**: 열린 메시지.
* **[!UICONTROL Click on email]**: 이메일의 링크에 대한 클릭 수.

## 링크 삽입 {#insert-links}

메시지를 디자인할 때 콘텐츠에 링크를 추가할 수 있습니다.

>[!NOTE]
>
>When [추적이 활성화됨](#enable-tracking)를 입력하면 메시지 콘텐츠에 포함된 모든 링크가 추적됩니다.

이메일 콘텐츠에 링크를 삽입하려면 아래 단계를 수행하십시오.

1. 요소를 선택하고 를 클릭합니다 **[!UICONTROL Insert link]** 상황별 도구 모음

   ![](assets/message-tracking-insert-link.png)

1. 만들 링크 유형을 선택합니다.

   * **[!UICONTROL External link]**: 외부 URL에 대한 링크를 삽입합니다.

   * **[!UICONTROL Landing page]**: 랜딩 페이지에 대한 링크를 삽입합니다. 추가 정보 [이 섹션](../landing-pages/get-started-lp.md)

   * **[!UICONTROL One click Opt-out]**: 옵트아웃을 확인하지 않고 사용자가 커뮤니케이션에서 빠르게 가입을 해지할 수 있는 링크를 삽입합니다. 추가 정보 [이 섹션](../privacy/opt-out.md#one-click-opt-out).

   * **[!UICONTROL External Opt-in/Subscription]**: 브랜드로부터 받는 커뮤니케이션을 수락하려면 링크를 삽입합니다.

   * **[!UICONTROL External Opt-out/Unsubscription]**: 브랜드의 커뮤니케이션 수신을 취소할 링크를 삽입합니다. 의 옵트아웃 관리에 대해 자세히 알아보십시오 [이 섹션](../privacy/opt-out.md#opt-out-management).

   * **[!UICONTROL Mirror page]**: 웹 브라우저에 이메일 콘텐츠를 표시할 링크를 삽입합니다. 추가 정보 [이 섹션](#mirror-page).

   ![](assets/message-tracking-links.png)

1. 링크를 개인화할 수 있습니다. 의 개인화된 URL에 대해 자세히 알아보십시오 [이 섹션](../personalization/personalization-syntax.md#perso-urls).

1. 변경 사항을 저장합니다.

1. 링크가 만들어지더라도 **[!UICONTROL Component settings]** 오른쪽 창입니다.

   * 링크를 편집하고 유형을 변경할 수 있습니다.
   * 해당 옵션을 선택하여 링크에 밑줄을 긋도록 선택할 수 있습니다.

   ![](assets/message-tracking-link-settings.png)

>[!NOTE]
>
>마케팅 유형 이메일 메시지에는 [옵트아웃 링크](../privacy/opt-out.md#opt-out-management): 트랜잭션 메시지에 필요하지 않습니다. 메시지 카테고리(**[!UICONTROL Marketing]** 또는 **[!UICONTROL Transactional]**)가에 정의되어 있습니다. [채널 표면](../configuration/channel-surfaces.md#email-type) (즉, 메시지 사전 설정) 수준 및 메시지를 만들 때 사용됩니다.

## 미러 페이지에 대한 링크 {#mirror-page}

미러 페이지는 웹 브라우저를 통해 온라인으로 액세스할 수 있는 HTML 페이지입니다. 콘텐츠는 전자 메일의 콘텐츠와 동일합니다.

이메일에 미러 페이지에 대한 링크를 추가하려면 [링크 삽입](#insert-links) 을(를) 선택합니다. **[!UICONTROL Mirror page]** 를 링크 유형으로 사용할 수 있습니다.

![](assets/message-tracking-mirror-page.png)

미러 페이지가 자동으로 생성됩니다.

>[!IMPORTANT]
>
>미러 페이지 링크는 자동으로 생성되므로 편집할 수 없습니다. 여기에는 원본 이메일을 렌더링하는 데 필요한 암호화된 개인화된 데이터가 모두 포함됩니다. 따라서 값이 큰 개인화된 속성을 사용하면 긴 미러 페이지 URL이 생성되므로 링크가 최대 URL 길이를 갖는 웹 브라우저에서 작동하지 않을 수 있습니다.

전자 메일이 전송되면 수신자가 미러 페이지 링크를 클릭하면 전자 메일의 컨텐츠가 기본 웹 브라우저에 표시됩니다.

>[!NOTE]
>
>에서 [증명](preview.md#send-proofs) 테스트 프로필로 전송되면 미러 페이지에 대한 링크가 활성화되지 않습니다. 최종 메시지에서만 활성화됩니다.

미러 페이지의 보존 기간은 60일입니다. 이후 미러 페이지는 더 이상 사용할 수 없습니다.

## 추적 관리 {#manage-tracking}

다음 [이메일 디자이너](content-from-scratch.md) 각 링크에 대한 추적 유형 편집과 같이 추적된 URL을 관리할 수 있습니다.

1. 을(를) 클릭합니다. **[!UICONTROL Links]** 아이콘을 클릭하여 추적할 컨텐츠의 모든 URL 목록을 표시합니다.

   이 목록을 사용하면 중앙 집중식 보기를 사용하고 이메일 콘텐츠에서 각 URL을 찾을 수 있습니다.

1. 링크를 편집하려면 해당 연필 아이콘을 클릭합니다.

   ![](assets/message-tracking-edit-links.png)

1. 을 수정할 수 있습니다 **[!UICONTROL Tracking Type]** 필요한 경우:

   ![](assets/message-tracking-edit-a-link.png)

   추적된 각 URL에 대해 추적 모드를 다음 값 중 하나로 설정할 수 있습니다.

   * **[!UICONTROL Tracked]**: 이 URL에서 추적을 활성화합니다.
   * **[!UICONTROL Opt out]**: 이 URL을 옵트아웃 또는 구독 취소 URL로 간주합니다.
   * **[!UICONTROL Mirror page]**: 이 URL이 미러 페이지 URL인 것으로 간주합니다.
   * **[!UICONTROL Never]**: 이 URL의 추적을 활성화하지 않습니다. <!--This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.-->

시작 및 클릭에 대한 보고는 [라이브 보고서](../reports/live-report.md) 그리고 [글로벌 보고서](../reports/global-report.md).
