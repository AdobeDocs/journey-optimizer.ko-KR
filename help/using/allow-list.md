---
title: 허용 목록
description: 허용 목록 사용 방법을 알아봅니다.
feature: 전달성
topic: 콘텐츠 관리
role: User
level: Intermediate
source-git-commit: e2743c8fa624a7a95b12c3adb5dc17a1b632c25d
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 1%

---

# 허용 목록 {#allow-list}

이제 [sandbox](administration/sandboxes.md) 수준에서 특정 전송 안전 목록을 정의하여 테스트 목적으로 안전한 환경을 가질 수 있습니다. 허용 목록이 실수가 발생할 수 있는 비프로덕션 인스턴스에서 고객에게 원치 않는 메시지를 보낼 위험이 없습니다.

허용 목록을 사용하면 특정 샌드박스에서 보내는 이메일을 받을 수 있는 권한이 있는 유일한 수신자 또는 도메인이 되는 개별 이메일 주소 또는 도메인을 지정할 수 있습니다. 따라서 테스트 환경에 있을 때 실수로 실제 고객 주소로 이메일을 보내지 않을 수 있습니다.

>[!CAUTION]
>
>이 기능은 프로덕션 샌드박스에서 사용할 수 있는 **이 아닙니다.** 이메일 채널에만 적용됩니다.

## 허용 목록 활성화 {#enable-allow-list}

비프로덕션 샌드박스에서 이 기능을 활성화하려면 더 이상 비어 있지 않도록 허용 목록을 업데이트하십시오. 비활성화하려면 다시 비어 있도록 허용 목록을 지워야 합니다.

[이 섹션](#logic)의 허용 목록 논리에 대해 자세히 알아보십시오.

<!--
To enable the allowed list on a non-production sandbox, you need to make an Adobe API call.

* Using this API, you can also disable the feature at any time.

* You can update the allowed list before or after enabling the feature.

* The allowed list logic applies when the feature is enabled and if the allowed list is not empty. Learn more in this section (logic).
-->

>[!NOTE]
>
>활성화되면 여정을 실행할 때 허용 목록 기능이 적용되지만 [증명](preview.md#send-proofs)으로 메시지를 테스트하고 [테스트 모드](building-journeys/testing-the-journey.md)를 사용하여 여정을 테스트할 때에도 이 기능이 적용됩니다.

## 허용 목록에 엔티티 추가 {#add-entities}

특정 샌드박스의 허용 목록에 새 이메일 주소 또는 도메인을 추가하려면 `listType` 속성에 대해 `ALLOWED` 값이 있는 제외 API를 호출해야 합니다. 예:

![](assets/allow-list-api.png)

**추가**, **삭제** 및 **Get** 작업을 수행할 수 있습니다.

>[!NOTE]
>
>허용 목록은 최대 1,000개의 항목을 포함할 수 있습니다.

<!--Learn more on making Adobe API calls in the [Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).-->

## 허용 목록 논리 {#logic}

<!-- When the allowed list is enabled (enable-allow-list) at the sandbox level using the API call above, the following applies.-->

허용 목록이 **비어 있으면 허용 목록 논리가 적용되지 않습니다.** 즉, [제외 목록](suppression-list.md)에 없는 경우 모든 프로필에 이메일을 보낼 수 있습니다.

허용 목록이 **비어 있지 않으면 허용 목록 논리가 적용됩니다.**

* 엔티티가 허용 목록&#x200B;**에 없고 제외 목록에 없는**&#x200B;인 경우 해당 수신자는 이메일을 받지 못합니다. 이유는 **[!UICONTROL Not allowed]**.

* 엔티티가 허용 목록&#x200B;**에서**&#x200B;이고 제외 목록에 없으면 이메일을 해당 수신자에게 보낼 수 있습니다. 그러나 엔티티가 [제외 목록](suppression-list.md)에도 있는 경우 해당 수신자가 이메일을 받지 못합니다. 이유는 **[!UICONTROL Suppressed]**.




