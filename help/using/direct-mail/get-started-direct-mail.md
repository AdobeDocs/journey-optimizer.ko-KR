---
solution: Journey Optimizer
product: journey optimizer
title: 다이렉트 메일 시작
description: Journey Optimizer에서 다이렉트 메일 메시지를 만드는 방법 알아보기
feature: Direct Mail
topic: Content Management
role: User
level: Beginner
keywords: 다이렉트 메일, 메시지, 캠페인
exl-id: bb52f400-6289-4a7f-a34f-98eb5d27c76a
TQID: https://experienceleague.adobe.com/Gmtr-7HW70-cg7va8iHfR5xKdYts-ZdDCm6CeQHJ0tg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: cb1f1586-9fb4-4de2-8332-02cebb88d42d
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 436
ht-degree: 83%

---

# 다이렉트 메일 시작 {#create-direct}

다이렉트 메일은 서드파티 다이렉트 메일 공급자가 고객에게 메일을 보내는 데 필요한 추출 파일을 개인화하고 생성할 수 있는 오프라인 채널입니다.

다이렉트 메일 캠페인 또는 여정을 생성할 때 Journey Optimizer는 우편 주소 및 프로필 속성과 같은 모든 대상 프로필과 선택한 데이터가 포함된 파일을 자동으로 생성합니다. 이 파일은 선택한 서드파티 다이렉트 메일 공급자가 액세스할 수 있도록 선택한 서버로 전송되며, 이 공급자가 실제 메일링 프로세스를 처리합니다.

사용자는 선택한 서드파티 다이렉트 메일 공급자와 협력하여 고객이 사용자의 메일을 받는 데 필요한 동의(해당하는 경우)를 고객으로부터 받아야 합니다.

메일링 서비스 사용에는 해당하는 서드파티 다이렉트 메일 공급자의 추가 약관이 적용됩니다.  Adobe는 사용자의 서드파티 제품 사용을 통제하지 않으며 이에 대한 책임을 지지 않습니다. 다이렉트 메일 캠페인의 메일링과 관련된 문제 또는 지원 요청은 선택한 서드파티 다이렉트 메일 공급자에게 문의하십시오.

## 시작하기 전에 {#before-you-start}

DM 메시지를 만들기 전에 [파일 라우팅 및 DM 채널 구성을 구성](direct-mail-configuration.md)하세요. 또한 Adobe Experience Platform에는 대상자 및 프로필 데이터(예: 우편 주소)가 필요합니다.

다이렉트 메일 메시지를 보내는 주요 단계는 다음과 같습니다.

![구성에서 배달까지의 DM 만들기 워크플로](assets/dm-creation-process.png)

>[!AVAILABILITY]
>
>다이렉트 메일 메시지는 여정 및 캠페인 컨텍스트에서 생성할 수 있습니다. API 트리거 캠페인에서는 사용할 수 없습니다.

![Journey Optimizer DM 채널의 애니메이션 개요](../rn/assets/do-not-localize/gif-dm.gif)

## 추가 리소스 {#additional-resources}

* **[다이렉트 메일 만들기](create-direct-mail.md)** - 다이렉트 메일 게재를 만들고 오프라인 채널용 추출 파일을 구성하는 방법을 알아봅니다.
* **[다이렉트 메일 채널 구성](direct-mail-configuration.md)** - 다이렉트 메일 표면 및 파일 라우팅 구성을 설정합니다.
* **[다이렉트 메일 테스트 및 보내기](test-send-direct-mail.md)** - 다이렉트 메일 게재의 테스트, 유효성 검사, 게시 방법을 알아봅니다.
* **[다이렉트 메일 튜토리얼](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/channels/direct-mail-channel/direct-mail){target="_blank"}** - 다이렉트 메일 기능 및 모범 사례에 대한 단계별 비디오 튜토리얼을 살펴봅니다.

## 사용 방법 비디오 {#how-to-video}

Adobe Journey Optimizer의 다이렉트 메일 채널을 활용하여 여정 내에서 다이렉트 메일 전달을 자동화하고 예약하는 방법을 알아보세요.

+++ 비디오 보기

>[!VIDEO](https://video.tv.adobe.com/v/3479169?captions=kor&quality=12)

+++

동일한 단계에 대한 서면 설명은 [DM 채널 자습서](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/channels/direct-mail-channel/direct-mail){target="_blank"}를 참조하십시오.

DM에 대한 일반적인 질문은 위의 [추가 리소스](#additional-resources) 섹션을 참조하십시오.
