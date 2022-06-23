---
title: SMS 메시지 만들기
description: Journey Optimizer에서 SMS 메시지를 만드는 방법을 알아봅니다
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 67fcddc77ad5493905a0f1894a0cf497b0bfa2f9
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 12%

---

# SMS 메시지 만들기 {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="SMS 만들기"
>abstract="텍스트 메시지를 추가하고 표현식 편집기를 사용하여 개인화를 시작합니다."

>[!AVAILABILITY]
>
>SMS 채널은 현재 조직 집합(제한된 가용성)에만 사용할 수 있습니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.

일단 [메시지를 만들었습니다.](get-started-content.md)를 사용하려면 **[!UICONTROL SMS]** 탭을 클릭하여 SMS 채널의 설정 및 콘텐츠를 정의합니다.

![](assets/sms_1.png)

SMS 메시지 개인화를 시작하려면 다음 단계를 수행합니다.

1. 을(를) 클릭합니다. **[!UICONTROL Add text message]** 필드 를 클릭하여 표현식 편집기를 엽니다.

   ![](assets/sms_3.png)

1. 표현식 편집기를 사용하여 컨텐츠 및 개인화 데이터를 정의합니다. 의 표현식 편집기에서 개인화에 대해 자세히 알아보십시오 [이 섹션](../personalization/personalize.md)

   >[!NOTE]
   >
   > SMS 메시지는 160자로 제한됩니다.

   ![](assets/sms_2.png)

1. 클릭 **[!UICONTROL Save]** 개인화된 메시지가 준비되면.

1. 클릭 **[!UICONTROL Preview]** 모바일 장치에서 SMS 메시지가 표시되는 방식을 시각화하십시오. 이 작업에 대한 자세한 정보는 [이 섹션](../design/preview.md)을 참조하십시오.

1. 메시지가 준비되면 게시하여 을 사용하여 실행할 수 있도록 할 수 있습니다. **[!UICONTROL Publish]** 버튼을 클릭합니다. 이 작업을 수행하면 여정에서 다음 실행에 사용될 메시지의 새 버전이 게시됩니다.

이제 여정에서 SMS 메시지를 사용할 수 있습니다. [여정 만들기 방법 알아보기](../building-journeys/journey-gs.md).

## 옵트인 및 옵트아웃{#sms-opt-in-out}

SMS 수신자는 옵트인 및 옵트아웃 키워드로 회신할 수 있습니다. Adobe Journey Optimizer은 업계 표준 및 규정에 따라 수신 메시지에서 다음 키워드를 자동으로 처리합니다. 시작, 중지, 중지. 이러한 키워드는 SMS 공급자로부터 자동 표준 응답을 트리거합니다.

**관련 항목**

* [SMS 채널 구성](../configuration/sms-configuration.md)
* [SMS 보고서](../reports/journey-global-report.md#sms-global)
* [새 메시지 만들기](get-started-content.md)
* [여정에 메시지 추가](../building-journeys/journeys-message.md)
