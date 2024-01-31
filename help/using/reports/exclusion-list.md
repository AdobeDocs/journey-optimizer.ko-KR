---
solution: Journey Optimizer
product: journey optimizer
title: 제외 목록
description: 보내는 동안 발생하는 제외에 대해 자세히 알아보기
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: a34ba1a8-87d5-4f9c-a181-2f49e74e8f09
source-git-commit: d26dbebaf36241d0e91c36c95f83ce6cf712ecee
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 9%

---

# 제외 이유 {#exclusion-list}

| 제외 이유 | 오류 코드 | 채널 | 설명 |
|-|-|-|-|
| RuntimeDispatchError | 050301 | 모든 채널 | 런타임 디스패치 오류에 대한 일반 제외 이벤트. |
| 런타임 렌더링 오류 | 050302 | 모든 채널 | 런타임 렌더링 오류에 대한 일반 제외 이벤트. |
| 네임스페이스 오류: 실험 | 050017 | 모든 채널 | 실험의 네임스페이스가 프로필의 네임스페이스와 다른 경우 제외 이벤트가 생성됩니다. |
| 실험홀드아웃제외 | 050018 | 모든 채널 | 이 제외 이벤트는 실험에 대한 적격 처리가 &quot;보류&quot;인 경우 생성됩니다. |
| ExcludedForControlRules | 050002 | 모든 채널 | 이 제외 이벤트는 현재 메시지 게재가 제어 규칙(예: 한 달에 허용된 이메일 수)을 위반하는 경우 생성됩니다. |
| DirectMailNoVariantDefined | 050062 | 다이렉트 메일 | DM 변형에서 가 정의되지 않은 경우 제외 이벤트가 생성됩니다. |
| DmNoMessageFoundForTreatment | 050061 | 다이렉트 메일 | 메시지에 대해 실험이 활성화되고 적격 처리에 대한 메시지가 없는 경우 제외 이벤트가 생성됩니다. |
| EmailNoConsent | 050101 | 이메일 | 제외 이벤트는 사용자가 마케팅 이메일 수신을 옵트아웃한 경우 생성됩니다. |
| 억제됨 | 050107 | 이메일 | 비표시 이유 중 하나로 인한 제외. |
| 이메일 억제 | 050102 | 이메일 | 대상 이메일이 억제되면 제외 이벤트가 생성됩니다. |
| 도메인 억제 | 050105 | 이메일 | 타겟팅된 이메일의 도메인이 억제되면 제외 이벤트가 생성됩니다. |
| 허용되지 않음 | 050108 | 이메일 | 허용 목록이 활성화되고 타겟팅된 이메일이 허용 목록에서 제외될 때 제외 이벤트가 생성됩니다. |
| EmailNotAllow | 050103 | 이메일 | 허용 목록이 활성화되고 타겟팅된 이메일이 허용 목록에서 제외될 때 제외 이벤트가 생성됩니다. |
| 도메인이 허용되지 않음 | 050106 | 이메일 | 허용 목록이 활성화되고 타겟팅된 이메일의 도메인이 허용 목록에서 제외될 때 제외 이벤트가 생성됩니다. |
| EmailNoSubscriberIdFoundInProfile | 050025 | 이메일 | 구독 이메일의 프로필에서 subscriberId를 찾을 수 없는 경우 제외 이벤트가 생성됩니다. |
| EmailNoAddressFoundInProfile | 050020 | 이메일 | 실행 주소에서 이메일 주소를 찾을 수 없을 때 제외 이벤트가 생성됩니다. |
| EmailNoAddressDefinedInPreset | 050021 | 이메일 | 제외 이벤트는 실행 주소가 표면에 정의되어 있지 않은 경우 생성됩니다. |
| EmailNoVariantDefined | 050026 | 이메일 | 이메일 메시지에 변형이 정의되지 않으면 제외 이벤트가 생성됩니다. |
| EmailNoMessageFoundForProcessing | 050027 | 이메일 | 메시지에 대해 실험이 활성화되고 적격 처리에 대한 메시지가 없는 경우 제외 이벤트가 생성됩니다. |
| 이메일 형식이 잘못된 주소 | 050024 | 이메일 | 이메일에 잘못된 주소가 포함된 경우 제외 이벤트가 생성됩니다. |
| InAppNoVariantDefinition | 050041 | 인앱 | InApp 메시지에 대한 변형이 정의되지 않은 경우 제외 이벤트가 생성됩니다. |
| InAppNoMessageFoundForProcessing | 050042 | 인앱 | 메시지에 대해 실험이 활성화되고 적격 처리에 대한 메시지가 없는 경우 제외 이벤트가 생성됩니다. |
| PushNoTokenFoundInProfile | 050030 | 푸시 | 프로필에 푸시 토큰이 없을 경우 제외 이벤트가 생성됩니다. |
| 푸시NoValidTokenFoundForApps | 050031 | 푸시 | 표면에 타겟팅된 앱에 대한 유효한 토큰이 없으면 제외 이벤트가 생성됩니다. |
| PushMalformedProfile | 050034 | 푸시 | 프로필의 pushNotificationDetails가 잘못된 경우 제외 이벤트가 생성됩니다. |
| PushNoConsent | 050111 | 푸시 | 사용자가 마케팅 푸시 알림을 옵트아웃하면 제외 이벤트가 생성됩니다. |
| PushNoApplicationDefinedInPreset | 050033 | 푸시 | 서피스에 타겟에 대한 애플리케이션이 없으면 제외 이벤트가 생성됩니다. |
| 정의된 푸시 번호 | 050035 | 푸시 | 변형이 정의되지 않으면 제외 이벤트가 생성됩니다. |
| PushNoMessageFoundForProcessing | 050036 | 푸시 | 메시지에 대해 실험이 활성화되고 적격 처리에 대한 메시지가 없는 경우 제외 이벤트가 생성됩니다. |
| SMSNoConsent | 050104 | SMS | 사용자가 마케팅 SMS를 옵트아웃하면 제외 이벤트가 생성됩니다. |
| SMSFromNumberNotDefinedInPreset | 050152 | SMS | 제외 이벤트는 &quot;FromNumber&quot;가 표면에 정의되어 있지 않을 때 생성됩니다. |
| SMSNoToNumberDefinedInProfile | 050153 | SMS | 제외 이벤트는 &quot;ToNumber&quot;가 표면에 정의되어 있지 않을 때 생성됩니다. |
| SMSNoVariantDefined | 050154 | SMS | 변형이 정의되지 않으면 제외 이벤트가 생성됩니다. |
| SMSNoMessageFoundForTreatment | 050155 | SMS | 메시지에 대해 실험이 활성화되고 적격 처리에 대한 메시지가 없는 경우 제외 이벤트가 생성됩니다. |
| WebNovariantDefined | 050041 | 웹 | 웹 메시지에 대한 변형이 정의되지 않은 경우 제외 이벤트가 생성됩니다. |
| WebNoMessageFoundForProcessing | 050042 | 웹 | 메시지에 대해 실험이 활성화되고 적격 처리에 대한 메시지가 없는 경우 제외 이벤트가 생성됩니다. |
