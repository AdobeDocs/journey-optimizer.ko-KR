---
solution: Journey Optimizer
product: journey optimizer
title: 이메일 옵트아웃 관리
description: 이메일을 통해 옵트아웃을 관리하는 방법 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 옵트아웃, 이메일, 링크, 구독 취소
exl-id: 4bb51bef-5dab-4a72-8511-1a5e528f4b95
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 81%

---

# 이메일 옵트아웃 관리 {#email-opt-out}

수신자가 이메일 커뮤니케이션 수신을 취소할 수 있는 기능을 제공하려면 항상 을 포함해야 합니다 **구독 취소 링크** 수신자에게 보내는 모든 이메일에서 [개인 정보 및 옵트아웃 관리에 대해 자세히 알아보십시오](../privacy/opt-out.md)

이렇게 하려면 다음을 수행할 수 있습니다.

* 삽입 **외부 랜딩 페이지에 연결** 이메일 을 통해 사용자가 브랜드로부터 커뮤니케이션 수신을 취소할 수 있도록 합니다. [외부 옵트아웃 링크를 추가하는 방법 알아보기](#opt-out-external-lp)

* 추가 **옵트아웃 링크 1회 클릭** 이메일 콘텐츠로 변경 이 링크를 사용하면 수신자가 랜딩 페이지로 리디렉션되어 옵트아웃을 확인할 필요 없이 커뮤니케이션에서 빠르게 구독을 취소할 수 있습니다. [원클릭 옵트아웃 링크를 추가하는 방법을 알아봅니다](#one-click-opt-out)

또한 **[!UICONTROL 목록 가입 해지]** 선택 사항이 채널 표면 수준에서 활성화되면 Journey Optimizer과 함께 전송되는 해당 이메일에 이메일 헤더에 가입 해지 링크가 포함됩니다. [이메일 헤더의 옵트아웃에 대해 자세히 알아보기](#unsubscribe-header)

>[!NOTE]
>
>마케팅 유형 이메일 메시지에는 옵트아웃 링크가 포함되어야 합니다. 옵트아웃 링크는 트랜잭션 메시지에는 필요 없습니다. 메시지 카테고리(**[!UICONTROL 마케팅]** 또는 **[!UICONTROL 트랜잭션]**)는 [채널 표면](../configuration/channel-surfaces.md#email-type)(예: 메시지 사전 설정) 수준에서 메시지를 만들 때 정의됩니다).

## 외부 옵트아웃 {#opt-out-external-lp}

### 구독 취소 링크 추가 {#add-unsubscribe-link}

먼저 메시지에 구독 취소 링크를 추가해야 합니다. 이렇게 하려면 아래 단계를 수행합니다:

1. 구독 취소 랜딩 페이지를 빌드합니다.

1. 원하는 서드파티 시스템에 호스팅합니다.

1. 여정에 메시지를 만듭니다.

1. 콘텐츠에서 텍스트를 선택하고 상황별 도구 모음을 사용하여 [링크를 삽입합니다](../email/message-tracking.md#insert-links).

   ![](assets/opt-out-insert-link.png)

1. **[!UICONTROL 링크 유형]** 드롭다운 목록에서 **[!UICONTROL 외부 옵트아웃/구독 취소]**&#x200B;를 선택합니다.

   ![](assets/opt-out-link-type.png)

1. **[!UICONTROL 링크]** 필드에 타사 랜딩 페이지 링크를 붙여넣습니다.

   ![](assets/opt-out-link-url.png)

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

### 옵트아웃에 대한 API 호출 구현 {#opt-out-api}

수신자가 랜딩 페이지에서 선택한 항목을 제출할 때 옵트아웃하도록 하려면 **구독 API 호출** through [Adobe Developer](https://developer.adobe.com){target="_blank"} 해당 프로필의 환경 설정을 업데이트하려면

이 POST 호출은 다음과 같습니다.

엔드포인트: platform.adobe.io/journey/imp/consent/preferences

쿼리 매개 변수:

* **params**: 암호화된 페이로드 포함
* **sig**: 서명
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

[!DNL Journey Optimizer] 에서는 다음 매개 변수를 사용하여 [Adobe Developer](https://developer.adobe.com){target="_blank"} API 호출.

### 구독 취소 링크가 있는 메시지 보내기 {#send-message-unsubscribe-link}

랜딩 페이지에 대한 구독 취소 링크를 구성하고 API 호출을 구현하면 메시지를 전송할 준비가 되었습니다.

1. 링크를 포함하는 메시지를 [여정](../building-journeys/journey.md)을 통해서 보냅니다.

1. 메시지가 수신되면 수신자가 구독 취소 링크를 클릭하면 랜딩 페이지가 표시됩니다.

   ![](assets/opt-out-lp-example.png)

1. 수신자가 양식을 제출하는 경우(여기에서는 랜딩 페이지의 **구독 취소** 버튼을 누르는 경우), 프로필 데이터는 [API 호출](#opt-out-api)을 통해 업데이트됩니다.

1. 옵트아웃 수신자는 옵트아웃에 성공했음을 나타내는 확인 메시지 화면으로 리디렉션됩니다.

   ![](assets/opt-out-confirmation-example.png)

   따라서 이 사용자는 다시 구독하지 않으면 브랜드에서 보내는 커뮤니케이션을 받지 않습니다.

1. 해당 프로필의 선택 사항이 업데이트되었는지 확인하려면 Experience Platform으로 이동하여 ID 네임스페이스 및 해당 ID 값을 선택하여 프로필에 액세스합니다. 자세한 내용은 [Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=ko#getting-started){target="_blank"}.

   ![](assets/opt-out-profile-choice.png)

   **[!UICONTROL 속성]** 탭에서 **[!UICONTROL 선택]** 값이 **[!UICONTROL 아니요]**&#x200B;로 변경되었음을 확인할 수 있습니다.

## 원클릭 옵트아웃 {#one-click-opt-out}

이메일에 옵트아웃 링크를 추가하려면 아래 단계를 따르십시오.

1. [링크를 삽입](../email/message-tracking.md#insert-links)하고 **[!UICONTROL 원클릭 옵트아웃]**&#x200B;을 선택합니다.

   ![](assets/message-tracking-opt-out.png)

1. 채널, 신원 또는 구독 등 어느 수준에 옵트아웃을 적용할지 선택합니다.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL 채널]**: 옵트아웃은 현재 채널의 프로필 대상(즉, 이메일 주소)으로 전송된 이후 메시지에 적용됩니다. 여러 대상이 프로필과 연결되어 있는 경우 옵트아웃은 해당 채널에 대한 프로필의 모든 타겟(즉, 이메일 주소)에 적용됩니다.
   * **[!UICONTROL ID]**: 옵트아웃은 현재 메시지에 사용 중인 특정 대상(즉, 이메일 주소)에 전송된 이후 메시지에 적용됩니다.
   * **[!UICONTROL 구독]**: 옵트아웃은 특정 구독 목록과 연관된 이후 메시지에 적용됩니다. 이 옵션은 현재 메시지가 구독 목록과 연결된 경우에만 선택할 수 있습니다.

1. 사용자가 가입 해지되면 리디렉션될 랜딩 페이지의 URL을 입력합니다. 이 페이지는 옵트아웃이 성공했는지 확인하기 위한 것입니다.

   >[!NOTE]
   >
   >채널 표면 수준에서 **목록 구독 취소** 옵션을 사용하도록 설정한 경우 이 URL이 사용자가 이메일 헤더의 구독 취소 링크를 클릭할 때도 사용됩니다. [자세히 알아보기](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   링크를 개인화할 수 있습니다. [이 섹션](../personalization/personalization-syntax.md)에서 URL 개인화에 대해 자세히 알아보십시오.

1. 변경 내용을 저장합니다.

[여정](../building-journeys/journey.md)을 통해 메시지를 보낸 이후 수신자가 옵트아웃 링크를 클릭하면 수신자의 프로필이 즉시 옵트아웃됩니다.

## 이메일 헤더의 구독 취소 링크 {#unsubscribe-header}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="이메일 헤더에 구독 취소 링크 추가"
>abstract="[목록 구독 취소]를 활성화하여 이메일 헤더에 구독 취소 링크를 추가합니다. 구독 취소 URL을 설정하려면 원클릭 옵트아웃 링크를 이메일 콘텐츠에 삽입합니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=ko#one-click-opt-out" text="원클릭 옵트아웃"

채널 표면 수준에서 [목록 구독 취소 옵션](../configuration/channel-surfaces.md#list-unsubscribe)을 사용하도록 설정한 경우 [!DNL Journey Optimizer] (으)로 보낸 해당 이메일의 헤더에 구독 취소 링크가 포함됩니다.

예를 들어 구독 취소 링크는 Gmail에서 다음과 같이 표시됩니다.

![](assets/unsubscribe-header.png)

>[!NOTE]
>
>이메일 헤더에 구독 취소 링크를 표시하려면 수신자의 이메일 클라이언트가 이 기능을 지원해야 합니다.

구독 취소 주소는 해당 채널 표면에 표시되는 기본 **[!UICONTROL Mailto(구독 취소)]** 주소입니다. [자세히 알아보기](../configuration/channel-surfaces.md#list-unsubscribe).

개인화된 구독 취소 URL을 설정하려면 이메일 메시지 콘텐츠에 원클릭 옵트아웃 링크를 삽입하고 원하는 URL을 입력합니다. [자세히 알아보기](#one-click-opt-out)

이메일 클라이언트에 따라 헤더에서 구독 취소 링크를 클릭하면 다음 결과가 발생할 수 있습니다.

* 기본 구독 취소 주소로 구독 취소 요청을 보냅니다.

* 메시지에 옵트아웃 링크를 추가할 때 지정한 랜딩 페이지 URL로 수신자가 이동합니다.

   >[!NOTE]
   >
   >메시지 콘텐츠에 원클릭 옵트아웃 링크를 추가하지 않으면 랜딩 페이지가 표시되지 않습니다.

* 해당 프로필이 즉시 옵트아웃되고 이 선택 사항이 Experience Platform에서 업데이트됩니다. 자세한 내용은 [Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=ko#getting-started){target="_blank"}.
