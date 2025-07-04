---
solution: Journey Optimizer
product: journey optimizer
title: Infobip 공급자 구성
description: Infobip을 사용하여 Journey Optimizer으로 문자 메시지 및 MMS를 전송하도록 환경을 구성하는 방법에 대해 알아봅니다
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '748'
ht-degree: 3%

---

# Infobip 공급자 구성 {#sms-configuration-infobip}

>[!BEGINSHADEBOX]

옵트인 또는 옵트아웃 키워드가 제공되지 않으면 표준 동의 메시지가 사용자 개인 정보를 보장하는 데 사용됩니다. 사용자 지정 키워드를 추가하면 기본값이 자동으로 재정의됩니다.

**기본 키워드:**

* **옵트인**: 구독, 예, 중지 취소, 시작, 계속, 다시 시작, 시작
* **옵트아웃**: 중지, 종료, 취소, 종료, 구독 취소, 아니요
* **도움말**: 도움말

>[!ENDSHADEBOX]

## SMS에 대한 API 자격 증명 구성

Journey Optimizer을 사용하여 Infobip을 구성하려면 다음 단계를 수행합니다.

1. 왼쪽 레일에서 **[!UICONTROL 관리]** `>` **[!UICONTROL 채널]**(으)로 이동한 다음 **[!UICONTROL API 자격 증명]** 메뉴를 선택하십시오. **[!UICONTROL 새 API 자격 증명 만들기]** 단추를 클릭합니다.

1. 아래에 자세히 설명된 대로 SMS API 자격 증명을 구성합니다.

+++ 구성을 위한 SMS 자격 증명 목록

   | 구성 필드 | 설명 |
   |---|---|    
   | SMS 공급업체 | 정보 피드 |
   | 이름 | API 자격 증명의 이름을 선택합니다. |
   | API 기본 URL 및 API 키 | 웹 인터페이스 홈 페이지 또는 API 키 관리 페이지에 액세스하여 자격 증명을 찾을 수 있습니다. [Infobip 설명서](https://www.infobip.com/docs/api){target="_blank"}에서 자세히 알아보기 |
   | 옵트인 키워드 | 옵트인 메시지를 자동으로 트리거할 기본 또는 사용자 지정 키워드를 입력합니다. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오. |
   | 옵트인 메시지 | 옵트인 메시지로 자동 전송되는 사용자 지정 응답을 입력합니다. |
   | 옵트아웃 키워드 | 옵트아웃 메시지를 자동으로 트리거할 기본 또는 사용자 지정 키워드를 입력합니다. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오. |
   | 옵트아웃 메시지 | 옵트아웃 메시지로 자동 전송되는 사용자 지정 응답을 입력합니다. |
   | 도움말 키워드 | **도움말 메시지**&#x200B;를 자동으로 트리거할 기본 또는 사용자 지정 키워드를 입력하십시오. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오. |
   | 도움말 메시지 | **도움말 메시지**(으)로 자동으로 전송되는 사용자 지정 응답을 입력하십시오. |
   | 이중 옵트인 키워드 | 이중 옵트인 프로세스를 트리거하는 키워드를 입력합니다. 사용자 프로필이 존재하지 않으면 확인 후 생성됩니다. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오. [SMS 이중 옵트인에 대해 자세히 알아보기](https://video.tv.adobe.com/v/3440286/?learn=on&captions=kor). |
   | 이중 옵트인 메시지 | 이중 옵트인 확인에 대한 응답으로 자동으로 전송되는 사용자 지정 응답을 입력합니다. |
   | 주체 엔티티 ID | 할당된 DLT 주체 엔티티 ID를 입력합니다. |
   | 컨텐츠 템플릿 ID | 등록된 DLT 콘텐츠 템플릿 ID를 입력합니다. |
   | 유효 기간 | 메시지 유효 기간(시간)을 입력합니다. 이 기간 내에 메시지를 게재할 수 없는 경우 시스템에서 다시 전송을 시도합니다. 기본 유효 기간은 48시간으로 설정됩니다. |
   | 콜백 데이터 | 알림 URL에서 전송할 추가 클라이언트 데이터를 입력합니다. |
   | 인바운드 번호 | 고유 인바운드 번호를 추가합니다. 이를 통해 서로 다른 샌드박스에서 동일한 API 자격 증명을 사용할 수 있으며, 각 샌드박스는 고유한 인바운드 번호를 가지고 있습니다. |
   | 사용자 지정 인바운드 키워드 | 특정 작업(예: 할인, 오퍼, 등록)에 대한 고유 키워드를 정의합니다. 이러한 키워드는 프로필의 속성으로 캡처 및 저장되므로 여정 내에서 스트리밍 세그먼트 자격을 트리거하고 사용자 지정된 응답 또는 작업을 제공할 수 있습니다. |
   | 기본 인바운드 회신 메시지 | 최종 사용자가 정의된 키워드와 일치하지 않는 인바운드 SMS를 전송할 때 전송되는 기본 응답을 입력합니다. |

+++

1. API 자격 증명 구성을 마치면 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

1. **[!UICONTROL API 자격 증명]** 메뉴에서 bin 아이콘을 클릭하여 API 자격 증명을 삭제합니다.

1. 기존 자격 증명을 수정하려면 원하는 API 자격 증명을 찾은 다음 **[!UICONTROL 편집]** 옵션을 클릭하여 필요한 변경을 수행합니다.

API 자격 증명을 만들고 구성한 후에는 SMS 및 MMS 메시지에 대한 채널 구성을 만들어야 합니다. [자세히 알아보기](sms-configuration-surface.md)

## RCS에 대한 API 자격 증명 구성

RCS 메시지는 [사용자 지정 SMS 공급자](sms-configuration-custom.md) 기능을 사용하여 Adobe Journey Optimizer에서 Infobip를 통해 지원됩니다. 이를 통해 캐러셀, 버튼 및 멀티미디어 컨텐츠와 같은 요소를 통합하여 검증된 비즈니스 프로필을 통해 풍부한 대화형 메시지를 전달할 수 있습니다.

Infobip을 사용하여 RCS 메시지를 활성화하려면 사용자 지정 SMS 공급자를 통해 새 API 자격 증명을 구성해야 합니다. RCS에는 고유한 페이로드 형식이 필요하므로 기존 Infobip SMS 자격 증명이 호환되지 않습니다.

1. **Infobip를 통해 RCS에 대한 비즈니스 등록**

   Infobip 플랫폼 내에서 RCS 온보딩 및 등록 프로세스를 완료합니다. 여기에는 RCS 발신자 프로필 설정 및 계정이 RCS를 사용할 수 있는지 확인하는 작업이 포함됩니다. [Infobip 설명서](https://www.infobip.com/docs/rcs/get-started)에서 자세히 알아보기

1. **SMS 웹후크 만들기**

   Journey Optimizer에서 [사용자 지정 SMS Webhook 구성](sms-configuration-custom.md#webhook). 이 웹후크는 Infobip의 플랫폼에서 게재 수신, 인바운드 RCS 메시지 및 상태 업데이트를 처리합니다.

1. **SMS 공급업체로 사용자 지정을 사용하여 API 자격 증명 만들기**

   Journey Optimizer 내에서 [새 API 자격 증명을 만듭니다](sms-configuration-custom.md#api-credential). SMS 공급자로 &quot;사용자 지정&quot;을 선택합니다. 적절한 RCS 끝점 인증 방법, 기본 URL 및 헤더를 사용합니다.

API 자격 증명을 만들고 구성한 후에는 RCS 메시지에 대한 채널 구성을 만들어야 합니다. [자세히 알아보기](sms-configuration-surface.md)
