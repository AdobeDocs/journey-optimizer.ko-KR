---
title: 이메일 스팸 보고서 사용
description: 이메일 스팸 보고서를 사용하는 방법을 알아봅니다.
feature: Preview
role: User
level: Beginner
badge: label="Beta"
exl-id: 9ab43b14-41cf-49f1-bdcf-6fee58db5000
source-git-commit: 5f69b252f5812f43b3d0a6fed0aac074ece0d10f
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 2%

---

# 이메일 스팸 보고서 {#spam-report}

>[!CONTEXTUALHELP]
>id="ajo_simulate_spam_report"
>title="이메일 스팸 보고서"
>abstract="스팸 보고서를 사용하면 이메일 콘텐츠 스팸 점수를 확인할 수 있습니다. 이 점수는 ISP 또는 사서함 공급자가 메시지를 스팸으로 간주할지 여부를 나타냅니다. 점수가 낮을수록 더 좋습니다. 이메일 콘텐츠 점수가 2점 이상인 경우 테스트 실패를 초래하는 문제를 해결하는 것을 고려해야 합니다."

전용 스팸 보고서에서 이메일 콘텐츠 스팸 점수를 확인할 수 있습니다. 사용 [SpamAssassin](https://spamassassin.apache.org/){target="_blank"}, Adobe Journey Optimizer은 이메일 콘텐츠를 테스트하고 ISP 또는 사서함 공급자가 스팸으로 간주할지 여부를 나타내는 점수를 제공할 수 있습니다.

>[!AVAILABILITY]
>
>이 기능은 현재 Beta 버전으로 Beta 고객에게만 제공됩니다. Beta 프로그램에 참여하려면 Adobe 고객 지원 센터에 문의해 주십시오.

이메일 콘텐츠를 편집하거나 미리 볼 때 **[!UICONTROL 스팸 보고서]** 버튼은 나열된 각 개별 항목에 대한 점수를 개선하기 위한 점수 및 조언을 제공합니다.

이 기능을 사용하면 수신 시 사용된 스팸 방지 도구에서 메시지를 스팸으로 간주할 수 있는지 여부를 확인하고 이러한 경우 조치를 취할 수 있습니다. 많은 이메일 받은 편지함 공급자가 스팸 필터링 프로세스의 일부로 도구를 사용합니다. 점수가 잘못된 이메일을 보내면 게재 기능에 심각한 영향을 줄 수 있습니다.

에 액세스하려면 **[!UICONTROL 스팸 보고서]**&#x200B;을(를) 통해 아래 단계를 수행합니다.

1. 다음에서 **[!UICONTROL 시뮬레이트]** 화면에서 **[!UICONTROL 스팸 보고서]** 단추를 클릭합니다.

   ![](assets/spam-report-button.png)

<!--
    You can also open the [Email Designer](../email/content-from-scratch.md), click the **[!UICONTROL More]** button and select **[!UICONTROL Check spam score]** from the menu.

    ![](assets/spam-report-check-score.png)
-->

1. 스팸 방지 검사가 자동으로 수행되며 **[!UICONTROL 스팸 보고서]** 창에 결과가 표시됩니다. 본문 레이아웃, 구조, 이미지 크기, 스팸 트리거 단어(있는 경우) 등의 측면에서 콘텐츠가 수행되는 방식을 보여 줍니다.

   ![](assets/spam-report-high-score.png)

1. 각 항목에 대한 점수와 설명을 확인합니다.

   점수가 낮을수록 더 좋습니다. 점수가 5보다 높으면 일부 메시지가 차단되거나 수신 시 스팸으로 표시될 수 있다는 경고가 표시됩니다. 가장 좋은 방법은 점수가 2보다 낮은 것입니다.

1. 해당 점수를 기반으로, 일부 요소를 개선할 수 있다고 판단되면 [이메일 디자이너](../email/content-from-scratch.md) 필요한 업데이트를 수행합니다.

1. 변경이 완료되면 다음으로 돌아가기 **[!UICONTROL 스팸 보고서]** 점수가 향상되었는지 확인하는 화면입니다.

   ![](assets/spam-report-low-score.png)

<!--You can also check the message's alerts for warnings on potential risk of spam detection. Follow the steps below.

1. Click the **[!UICONTROL Alerts]** button on top right of the screen. [Learn more on email alerts](../email/create-email.md#check-email-alerts)

1. If **[!UICONTROL Spam checker alert]** is displayed, you should check your content for a potential risk of spam using the **[!UICONTROL Spam report]** feature as detailed above.

    ![](assets/spam-report-alert.png)
-->
