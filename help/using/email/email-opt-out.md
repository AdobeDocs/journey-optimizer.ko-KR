---
solution: Journey Optimizer
product: journey optimizer
title: 이메일 옵트아웃 관리
description: 이메일을 사용하여 옵트아웃을 관리하는 방법 알아보기
feature: Email Design, Privacy
topic: Content Management
role: User
level: Intermediate
keywords: 옵트아웃, 이메일, 링크, 구독 취소
exl-id: 4bb51bef-5dab-4a72-8511-1a5e528f4b95
source-git-commit: 9c095df4c8cab4cae8f5f3a5e000dfc5872b1a8b
workflow-type: tm+mt
source-wordcount: '1350'
ht-degree: 26%

---

# 이메일 옵트아웃 관리 {#email-opt-out}

여정 또는 캠페인에서 메시지를 보낼 때 고객이 향후 커뮤니케이션에서 구독을 취소할 수 있도록 항상 확인해야 합니다. 구독을 취소하면 향후 마케팅 메시지 대상자에서 프로필이 자동으로 제거됩니다.  [개인 정보 및 옵트아웃 관리에 대해 자세히 알아보기](../privacy/opt-out.md)

>[!NOTE]
>
>모든 마케팅 메시지에는 옵트아웃 링크가 포함되어야 합니다. 트랜잭션 메시지에는 필요하지 않습니다. 메시지 범주 - **[!UICONTROL 마케팅]** 또는 **[!UICONTROL 트랜잭션]** - 는에서 정의됩니다. [채널 표면](../configuration/channel-surfaces.md#email-type) 레벨 및 메시지를 만들 때.

이메일 콘텐츠에 구독 취소 링크를 삽입하려면 다음을 수행할 수 있습니다.

* 이메일 헤더에 한 번의 클릭으로 구독 취소 URL을 추가합니다. 활성화 **[!UICONTROL 목록-구독 취소 헤더]** 채널 표면 수준의 옵션은 이메일 헤더에 옵트아웃 링크를 추가합니다. [이메일 헤더의 옵트아웃에 대해 자세히 알아보기](#unsubscribe-header)

* 활성화 **원클릭 옵트아웃 링크** 이메일.  [원클릭 옵트아웃 링크를 추가하는 방법 알아보기](#one-click-opt-out)

* 삽입 **랜딩 페이지 링크**. [옵트아웃 랜딩 페이지를 추가하는 방법 알아보기](#opt-out-external-lp)


## 1단계 옵트아웃 {#opt-out-one-step}

### 이메일 헤더의 구독 취소 URL 한 번 클릭 {#unsubscribe-header}

<!--Do not modify - Legal Review Done -->

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="이메일 헤더에 구독 취소 URL 추가"
>abstract="List-Unsubscribe Header를 활성화하여 이메일 헤더에 구독 취소 URL을 추가합니다. 구독 취소 URL을 설정하려면 원클릭 옵트아웃 링크를 이메일 콘텐츠에 삽입합니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=ko#one-click-opt-out" text="원클릭 옵트아웃"

원클릭 목록 구독 취소 URL은 이메일 발신자 정보 옆에 표시되는 구독 취소 링크 또는 단추이며 한 번의 클릭으로 수신자가 메일링 목록에서 즉시 옵트아웃할 수 있습니다. Adobe Journey Optimizer에서 **목록 구독 취소 활성화** 옵션이 켜지면 이메일 헤더에 기본적으로 수신자가 메일링 목록에서 구독을 취소하는 데 사용할 수 있는 mailto 및/또는 URL이 모두 포함됩니다.

다음 [목록 구독 취소 활성화](email-settings.md#list-unsubscribe) 토글을 채널 표면 수준에서 활성화해야 이 표면을 사용하는 이메일에 이메일 헤더에 한 번 클릭 구독 취소 URL이 포함됩니다.

>[!NOTE]
>
>이메일 헤더에 원클릭 구독 취소 URL을 표시하려면 수신자의 이메일 클라이언트가 이 기능을 지원해야 합니다.


예를 들어 한 번의 클릭으로 구독 취소 URL에 다음과 같은 구독 취소 링크가 Gmail에 표시됩니다.

![](assets/unsubscribe-header.png)


Adobe Journey Optimizer을 사용하면 이메일 헤더에 자동 생성된 원클릭 구독 취소 URL 및 mailto 주소로 이메일 표면 설정을 구성하거나 이메일 본문에 원클릭 옵트아웃 URL을 포함할 수 있습니다. 수신자가 원클릭 옵트아웃 링크를 클릭하면 수신자의 구독 취소 요청이 그에 따라 처리됩니다.

>[!AVAILABILITY]
>
>원클릭 구독 취소 URL 헤더 는 2024년 6월 3일부터 Adobe Journey Optimizer에서 사용할 수 있습니다.
>

이메일 클라이언트에 따라 및 [이메일 표면 구독 취소 설정](email-settings.md#list-unsubscribe)이메일 헤더에서 구독 취소 링크를 클릭하면 다음과 같은 영향을 받을 수 있습니다.

* 다음의 경우 **Mailto(구독 취소)** 이 기능은 사용자가 활성화하면 사용자가 만든 하위 도메인을 기반으로 기본 구독 취소 주소로 구독 취소 요청이 전송됩니다.
* 다음의 경우 **한 번의 클릭으로 구독 취소 URL** 사용자가 기능을 활성화하거나 이메일 본문 콘텐츠에 구독 취소 URL을 삽입한 경우 수신자가 사용자가 만든 하위 도메인을 기반으로 하는 한 번의 클릭으로 구독 취소 URL을 클릭하면 수신자가 채널 수준이나 ID 수준(동의 설정 방법에 따라 다름)에서 직접 옵트아웃됩니다.

두 경우 모두 수신자에 대한 해당 프로필이 즉시 옵트아웃되고 이 선택이 Experience Platform에서 업데이트됩니다. 다음에서 자세히 알아보기 [Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=ko#getting-started){target="_blank"}.

목록 구독 취소 헤더에 대해 활성화 기능을 토글한 경우 Mailto 및 One-Click&amp; 구독 취소 URL이라는 featuresmethod를 모두 포함하는 것이 좋습니다. 모든 이메일 클라이언트가 HTTP 메서드를 지원하는 것은 아닙니다. Mailto 목록 구독 취소 기능은 다른 방법을 선택할 수 있는 기능으로 제공되므로 발신자의 평판을 보다 잘 보호할 수 있고 모든 수신자가 구독 취소 기능을 사용할 수 있는 액세스 권한을 가질 수 있습니다. [자세히 알아보기](email-settings.md#list-unsubscribe)


### 이메일 콘텐츠에서 원클릭 옵트아웃 {#one-click-opt-out}

개인화된 구독 취소 URL을 설정하려면 원클릭 옵트아웃 링크를 이메일 메시지 콘텐츠에 삽입하고 아래에 설명된 대로 원하는 URL을 입력합니다.

1. 이메일 콘텐츠에 액세스하고 [링크 삽입](../email/message-tracking.md#insert-links).
1. 선택 **[!UICONTROL 한 번의 클릭으로 옵트아웃]** 를 링크의 유형으로 사용하십시오.

   ![](assets/message-tracking-opt-out.png)

1. 사용자가 가입 해지되면 리디렉션되는 랜딩 페이지의 URL을 입력합니다. 이 페이지는 옵트아웃이 성공했는지 확인하기 위해 여기에 있습니다.

   >[!NOTE]
   >
   >을 활성화한 경우 **[!UICONTROL 목록-구독 취소]** 옵션: [채널 표면 레벨](email-settings.md#list-unsubscribe) 및 기본 원클릭 옵트아웃 URL 옵션이 선택 취소되어 있는 경우, 사용자가 이메일 헤더의 구독 취소 링크를 클릭할 때 이 URL이 사용됩니다. [자세히 알아보기](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   링크를 개인화할 수 있습니다. [이 섹션](../personalization/personalization-syntax.md)에서 URL 개인화에 대해 자세히 알아보십시오.

1. 채널, 신원 또는 구독 등 어느 수준에 옵트아웃을 적용할지 선택합니다.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL 채널]**: 옵트아웃은 현재 채널의 프로필 대상(즉, 이메일 주소)으로 전송된 이후 메시지에 적용됩니다. 여러 대상이 프로필과 연결되어 있는 경우 옵트아웃은 해당 채널에 대한 프로필의 모든 타겟(즉, 이메일 주소)에 적용됩니다.
   * **[!UICONTROL ID]**: 옵트아웃은 현재 메시지에 사용 중인 특정 대상(즉, 이메일 주소)에 전송된 이후 메시지에 적용됩니다.
   * **[!UICONTROL 구독]**: 옵트아웃은 특정 구독 목록과 연관된 이후 메시지에 적용됩니다. 이 옵션은 현재 메시지가 구독 목록과 연결된 경우에만 선택할 수 있습니다.

1. 변경 내용을 저장합니다.



## 2단계 옵트아웃 {#opt-out-external-lp}

표준 옵트아웃 메커니즘은 두 단계에 따라 다릅니다. 구독자는 이메일에서 옵트아웃 링크를 클릭한 다음 옵트아웃 랜딩 페이지로 리디렉션되어 구독 취소를 확인합니다.

이 구독 취소 모드를 구현하려면 옵트아웃 랜딩 페이지를 만들어 게시하고 랜딩 페이지 링크가 있는 구독 취소 링크를 이메일 메시지에 추가해야 합니다. 이러한 단계는 아래에 요약되어 있습니다.


### 전제 조건 {#prereq-lp}

2단계 옵트아웃 메커니즘을 설정하려면 고유한 구독 취소 랜딩 페이지를 만들어야 합니다. 첫 번째 랜딩 페이지는 메시지에서 연결되며 콜 투 액션 버튼을 포함해야 합니다. 사용자가 버튼을 클릭하면 확인 메시지가 표시됩니다.

Adobe Journey Optimizer에서 랜딩 페이지를 만들어 구독 취소를 관리하는 방법을 알아봅니다. [이 페이지](../landing-pages/lp-use-cases.md#opt-out).

외부 랜딩 페이지를 사용할 수도 있습니다. 이 경우 수신자가 구독을 취소한 경우 Adobe Journey Optimizer에 정보를 보내도록 API를 구성합니다.

+++ 옵트아웃 API 호출을 구현하는 방법 알아보기

수신자가 랜딩 페이지에서 선택한 항목을 제출할 때 옵트아웃하도록 하려면 다음을 구현해야 합니다. **구독 API 호출** 에서 [Adobe Developer](https://developer.adobe.com){target="_blank"} 를 클릭하여 해당 프로필의 기본 설정을 업데이트합니다.

이 POST 호출은 다음과 같습니다.

엔드포인트: https://platform.adobe.io/journey/imp/consent/preferences

쿼리 매개 변수:

* **params**: 암호화된 페이로드 포함
* **pid**: 암호화된 프로필 ID

이 세 매개 변수는 수신자에게 전송된 타사 랜딩 페이지 URL에 포함됩니다.

![](assets/opt-out-parameters.png)

헤더 요구 사항:

* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* 인증(기술 계정의 사용자 토큰)

요청 본문:

```
{
   "marketing": [
       {
            "type": "email",           
            "choice": "no",          
            "scope": "channel"       
        }
    ],
 
}
```

[!DNL Journey Optimizer] 에서는 이러한 매개 변수를 사용하여 다음을 통해 해당 프로필의 선택을 업데이트합니다. [Adobe Developer](https://developer.adobe.com){target="_blank"} API 호출.

+++


### 구독 취소 링크 추가 {#add-unsubscribe-link}

먼저 메시지에 구독 취소 링크를 추가해야 합니다. 이렇게 하려면 아래 단계를 수행합니다:

1. 메시지 만들기 및 [링크 삽입](../email/message-tracking.md#insert-links) 상황별 도구 모음 사용.

   ![](assets/opt-out-insert-link.png)

1. 다음 항목 선택 **[!UICONTROL 랜딩 페이지]** 다음에서 **[!UICONTROL 유형]** 드롭다운 목록에서 옵트아웃 랜딩 페이지를 선택합니다. **[!UICONTROL 랜딩 페이지]** 필드.

   외부 랜딩 페이지를 사용하는 경우 다음을 선택합니다. **[!UICONTROL 외부 옵트아웃/구독 취소]** 다음에서 **[!UICONTROL 유형]** 드롭다운 목록입니다.

   ![](assets/opt-out-link-type.png)

   **[!UICONTROL 링크]** 필드에 타사 랜딩 페이지 링크를 붙여넣습니다.

   ![](assets/opt-out-link-url.png)

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.


### 구독 취소 링크가 있는 메시지 보내기 {#send-message-unsubscribe-link}

랜딩 페이지에 대한 구독 취소 링크를 구성했으면 메시지를 만들고 보낼 수 있습니다.

1. 구독 취소 링크를 사용하여 메시지를 구성하고 구독자에게 보냅니다.

1. 메시지가 수신되면 수신자가 구독 취소 링크를 클릭하면 랜딩 페이지가 표시됩니다.

   ![](assets/opt-out-lp-example.png)

1. 수신자가 양식을 제출하는 경우 - 여기에서 **[!UICONTROL 구독 취소]** 랜딩 페이지의 단추 - 프로필 데이터는 API 호출을 통해 업데이트됩니다.

1. 옵트아웃 수신자는 옵트아웃에 성공했음을 나타내는 확인 메시지 화면으로 리디렉션됩니다.

   ![](assets/opt-out-confirmation-example.png)

   따라서 이 사용자는 다시 구독하지 않으면 브랜드에서 보내는 커뮤니케이션을 받지 않습니다.

1. 해당 프로필의 선택 사항이 업데이트되었는지 확인하려면 Experience Platform으로 이동하여 ID 네임스페이스 및 해당 ID 값을 선택하여 프로필에 액세스합니다. 다음에서 자세히 알아보기 [Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=ko#getting-started){target="_blank"}.

   ![](assets/opt-out-profile-choice.png)

   **[!UICONTROL 속성]** 탭에서 **[!UICONTROL 선택]** 값이 **[!UICONTROL 아니요]**&#x200B;로 변경되었음을 확인할 수 있습니다.

