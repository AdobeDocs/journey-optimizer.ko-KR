---
solution: Journey Optimizer
product: journey optimizer
title: 고객 관리 키
description: Adobe Journey Optimizer의 고객 키를 설정하고 관리하는 방법에 대해 알아봅니다.
feature: Privacy, Monitoring
role: Developer, User, Admin, Leader
level: Intermediate
exl-id: f0985d1f-0bcf-452f-bd46-dfeca0424f01
TQID: https://experienceleague.adobe.com/yCl5CISD1-Xx6gfcK2sWdFWAeE0LicO-3r3YndB2cVQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2:
  - id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56
  - id: f365ec33-2b99-4b7f-b4ee-c743dd7f615f
  - id: c8d5f2ce-ba44-43e9-a2bf-94a3d7d85ec3
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 279
ht-degree: 100%

---

# 고객 관리형 키 설정 및 관리 {#cmk}

>[!AVAILABILITY]
>
>[!DNL Customer Managed Keys] 기능은 현재 [Healthcare Shield 또는 Privacy &amp; Security Shield](https://experienceleague.adobe.com/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield.html?lang=ko){target="_blank"} 추가 기능 서비스를 구입한 조직에서만 사용할 수 있습니다.

[Healthcare Shield](https://www.adobe.com/trust/compliance/hipaa-ready.html){target="_blank"} 및 Privacy &amp; Security Shield 고객은 Adobe Journey Optimizer를 통해 Azure CMK(고객 관리형 키)를 활용하고 데이터에 적용할 수 있습니다.

Journey Optimizer의 설정 프로세스는 크게 두 부분으로 나뉩니다. Adobe Experience Platform과 CJA(Customer Journey Analytics)의 기술을 모두 활용하기 때문입니다.

* [Adobe Experience Platform의 고객 관리형 키](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys.html?lang=ko){target="_blank"} 설명서의 단계를 따라 진행하십시오.
* [Customer Journey Analytics의 고객 관리형 키](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-privacy/cmk.html?lang=ko){target="_blank"} 설명서의 단계를 따라 진행하십시오.

  CJA(Customer Journey Analytics)를 구매하지 않은 경우에도 CJA의 특정 구성 요소를 배경에서 사용하기 때문에 이 설정 프로세스를 완료해야 합니다.

설정 프로세스를 진행할 때는 [Adobe Experience Platform의 고객 관리형 키](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/encryption.html?lang=ko){target="_blank"} 설명서에 자세히 나와 있는 단계별 지침을 참조할 수 있습니다.

Adobe Experience Platform과 고객 관리형 키 모두 데이터를 전송할 때나 사용하지 않을 때 암호화함으로써 데이터의 보안을 보장합니다. 고객 관리형 키를 사용하는지 여부에 관계없이 데이터는 계속 보호됩니다.

Adobe Experience Platform의 데이터 암호화에 대한 자세한 내용은 데이터 암호화에 대한 [설명서](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/encryption.html?lang=ko){target="_blank"}에서 확인하실 수 있습니다.
