---
solution: Journey Optimizer
product: journey optimizer
title: 다시 시도
description: 금지 목록에 주소를 보내기 전에 다시 시도를 수행하는 방법 알아보기
feature: Deliverability, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 재시도, 바운스, 소프트, 최적화 프로그램, 오류
exl-id: 05564a99-da50-4837-8dfb-bb1d3e0f1097
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 9%

---

# 다시 시도 {#retries}

일시적인 문제로 인해 이메일 메시지가 실패하는 경우 **소프트 바운스** 특정 주소에 대한 오류 발생. 여러 번 다시 시도합니다. 각 오류는 오류 카운터를 증가시킵니다. 이 카운터가 제한 임계값에 도달하면 전자 메일 주소가 제외 목록에 추가됩니다.

>[!NOTE]
>
>의 오류 유형에 대해 자세히 알아보십시오. [게재 실패 유형](../reports/suppression-list.md#delivery-failures) 섹션.

기본 구성에서 임계값은 5개의 오류로 설정됩니다.

* 동일한 게재의 경우 다섯 번째에 [재시도 기간](#retry-duration): 주소가 표시되지 않습니다.

* 게재가 다르고 24시간 이상 차이가 나는 오류가 두 번 발생하면 각 오류마다 오류 카운터가 증가하고 5번째 시도에서도 주소가 표시되지 않습니다. 오류는 각 주소에 대해 누적됩니다.

다시 시도한 후 게재가 성공하면 주소의 오류 카운터가 다시 초기화됩니다.

예:

* 다시 시도 기간을 24시간으로 설정하여 월요일에 이메일을 보내게 됩니다. emma.jones@mail.com 주소를 배달할 수 없습니다. 이메일은 최대 3회까지 재시도되며 24시간 재시도 기간에 도달하면 재시도를 중지합니다.

* 수요일에 다른 이메일을 보내세요. 이미 3개의 오류 카운트가 있는 emma.jones@mail.com도 타깃팅되며 다시 배달되지 않습니다(두 번). 두 개의 오류가 추가로 확인됩니다.

두 이메일 간에 다른 게재를 시도하지 않고 성공한 경우, 3 + 2 오류의 누적 영향을 고려할 때 emma.jones@mail.com 주소가 제외 목록에 추가됩니다.

## 재시도 임계값 버전 {#edit-retry-threshold}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_bounces"
>title="재시도 임계값 업데이트"
>abstract="기본값이 사용자 요구에 맞지 않으면 허용되는 연속 소프트 바운스 수를 수정할 수 있습니다. 재시도 카운터가 특정 이메일 주소에 대한 오류 임계값에 도달하면 이 주소를 금지 목록에 추가합니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/reporting/deliverability/suppression-list.html" text="금지 목록 이해하기"

기본값 5가 사용자의 요구 사항에 맞지 않는 경우 아래 단계에 따라 오류 임계값을 수정할 수 있습니다.

1. 다음으로 이동 **[!UICONTROL 채널]** > **[!UICONTROL 이메일 구성]** > **[!UICONTROL 비표시 목록]**.

1. 다음 항목 선택 **[!UICONTROL 비표시 규칙 편집]** 단추를 클릭합니다.

   ![](assets/suppression-list-edit-retries.png)

1. 필요에 따라 허용된 연속 소프트 바운스 수를 편집합니다.

   ![](assets/suppression-list-edit-soft-bounces.png)

   1에서 20 사이의 정수 값을 입력해야 합니다. 즉, 최소 다시 시도 횟수는 1이고 최대 다시 시도 횟수는 20입니다.

   >[!CAUTION]
   >
   >값이 10보다 높을 경우 전달률에 문제가 발생하고 IP가 조절되거나 ISP에 의한 차단 목록에 추가가 발생할 수 있습니다. [전달성에 대해 자세히 알아보기](../reports/deliverability.md)

## 재시도 기간 {#retry-duration}

다음 **재시도 기간** 일시적인 오류나 소프트 바운스가 발생한 게재의 이메일 메시지가 다시 시도하는 시간대입니다.

기본적으로 다음에 대해 재시도가 수행됩니다. **3.5일** (또는 **84시간**) 메시지가 이메일 큐에 추가된 시간.

그러나 더 이상 필요하지 않은 경우 다시 시도 시도가 더 이상 수행되지 않도록 를 만들거나 편집할 때 필요에 따라 이 설정을 변경할 수 있습니다 [채널 표면](channel-surfaces.md) (즉, 메시지 사전 설정)가 이메일 채널에 적용됩니다.

예를 들어 암호 재설정과 관련되고 하루 동안만 유효한 링크가 포함된 트랜잭션 이메일에 대해 다시 시도 기간을 24시간으로 설정할 수 있습니다. 마찬가지로 자정 세일의 경우 6시간의 재시도 기간을 정의할 수 있습니다.

>[!NOTE]
>
>재시도 기간은 84시간을 초과할 수 없습니다. 최소 재시도 기간은 마케팅 이메일의 경우 6시간, 트랜잭션 이메일의 경우 10분입니다.

에서 채널 표면을 만들 때 이메일 재시도 매개 변수를 조정하는 방법을 알아봅니다 [이 섹션](../email/email-settings.md#email-retry).

