---
title: 인앱 알림 확인하고 보내기
description: Journey Optimizer에서 인앱 메시지를 확인하고 보내는 방법 알아보기
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: 인앱, 메시지, 만들기, 시작
exl-id: 9e9c235a-b78c-4669-af82-822b6f1e6fca
source-git-commit: 8fecd0d4812ba875dba1d47bc32ab08178a13f2c
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 13%

---

# 인앱 알림 확인하고 보내기 {#create-in-app}

## 디바이스에서 미리보기 {#preview-device}

모든 사용자가 라이브로 전환되기 전에 인앱 알림을 살짝 확인하려는 경우 특정 디바이스에서 미리 볼 수 있습니다. 이 기능을 사용하면 알림이 선택한 디바이스에서 의도한 대로 표시되고 작동하여 대상자에게 더 나은 사용자 경험을 제공할 수 있습니다.

이렇게 하려면 아래 단계를 수행합니다.

1. **[!UICONTROL 장치에서 미리 보기]**&#x200B;를 클릭합니다.

   ![](assets/in_app_create_6.png)

1. **[!UICONTROL 장치에 연결]** 창에서 **[!UICONTROL 시작]**&#x200B;을 클릭합니다.

1. 응용 프로그램의 **[!UICONTROL 기본 URL]**&#x200B;을(를) 입력하고 **[!UICONTROL 다음]**&#x200B;을(를) 클릭합니다.

   ![](assets/in_app_create_7.png)

1. 장치로 QR 코드를 스캔하고 표시된 PIN 코드를 입력합니다.

이제 인앱 메시지를 장치에서 직접 트리거하여 실제 장치에서 메시지를 미리 보고 검토할 수 있습니다.

## 테스트 프로필로 미리 보기 {#simulate}

인앱 메시지가 정의되면 테스트 프로필을 사용하여 미리 볼 수 있습니다. 개인화된 콘텐츠를 삽입한 경우 테스트 프로필 데이터를 활용하여 이 콘텐츠가 메시지에 어떻게 표시되는지 확인할 수 있습니다.

이렇게 하려면 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 클릭한 다음 테스트 프로필을 추가하여 테스트 프로필 데이터를 사용하여 메시지를 확인하세요.

테스트 프로필을 선택하고 콘텐츠를 미리 보는 방법에 대한 자세한 내용은 [콘텐츠 관리](../content-management/preview-test.md) 섹션에서 확인할 수 있습니다.

## 인앱 알림 검토 및 활성화{#in-app-review}

>[!IMPORTANT]
>
> 캠페인이 승인 정책의 대상인 경우 인앱 알림을 보내려면 승인을 요청해야 합니다. [자세히 알아보기](../test-approve/gs-approval.md)

인앱 메시지가 만들어지고 콘텐츠가 정의되고 개인화되면 이를 검토하고 활성화할 수 있습니다.

이렇게 하려면 아래 단계를 수행합니다.

1. **[!UICONTROL 활성화]** 단추를 사용하여 메시지 요약을 표시합니다.

   요약을 사용하면 필요한 경우 캠페인을 수정하고 매개 변수가 틀리거나 누락되었는지 확인할 수 있습니다.

   ![](assets/in_app_create_5.png)

1. 캠페인이 올바르게 구성되었는지 확인한 다음 **[!UICONTROL 활성화]**&#x200B;를 클릭합니다.

이제 캠페인이 활성화되었습니다. 캠페인에 구성된 인앱 알림은 즉시 전송되거나 지정된 날짜에 전송됩니다.

전송되면 Campaign 또는 여정 보고서 내에서 인앱 메시지의 영향을 측정할 수 있습니다. 보고와 관련한 자세한 정보는 [이 섹션](../reports/campaign-global-report-cja-inapp.md)을 참조하십시오.

**관련 항목:**

* [인앱 메시지 만들기 ](create-in-app.md)
* [인앱 메시지 디자인](design-in-app.md)
* [인앱 보고서 ](../reports/campaign-global-report-cja-inapp.md)
* [인앱 구성](inapp-configuration.md)
