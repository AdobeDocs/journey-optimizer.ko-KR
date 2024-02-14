---
solution: Journey Optimizer
product: journey optimizer
title: 고객 관리 키
description: Adobe Journey Optimizer의 고객 키를 설정하고 관리하는 방법에 대해 알아봅니다.
feature: Privacy, Monitoring
role: Developer, User, Admin, Leader
level: Intermediate
exl-id: f0985d1f-0bcf-452f-bd46-dfeca0424f01
source-git-commit: a939d06d26d64a72eaec0ddc7f22b074ad463150
workflow-type: ht
source-wordcount: '228'
ht-degree: 100%

---

# Adobe Journey Optimizer의 고객 관리형 키 설정 및 관리 {#cmk}

>[!AVAILABILITY]
>
>[!DNL Customer Managed Keys] 기능은 현재 [Healthcare Shield 또는 Privacy &amp; Security Shield](https://experienceleague.adobe.com/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield.html?lang=ko) 추가 기능 서비스를 구입한 조직에서만 사용할 수 있습니다.

[Healthcare Shield](https://www.adobe.com/kr/trust/compliance/hipaa-ready.html) 및 Privacy &amp; Security Shield 고객은 Adobe Journey Optimizer를 통해 Azure CMK(고객 관리형 키)를 활용하고 데이터에 적용할 수 있습니다.

Journey Optimizer의 설정 프로세스는 크게 두 부분으로 나뉩니다. Adobe Experience Platform과 CJA(Customer Journey Analytics)의 기술을 모두 활용하기 때문입니다.

* [Adobe Experience Platform의 고객 관리형 키](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys.html?lang=ko-KR) 설명서의 단계를 따라 진행하십시오.
* [Customer Journey Analytics의 고객 관리형 키](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-privacy/cmk.html?lang=ko) 설명서의 단계를 따라 진행하십시오.

  CJA(Customer Journey Analytics)를 구매하지 않은 경우에도 CJA의 특정 구성 요소를 배경에서 사용하기 때문에 이 설정 프로세스를 완료해야 합니다.

설정 프로세스를 진행할 때는 [Adobe Experience Platform의 고객 관리형 키](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/encryption.html?lang=ko) 설명서에 자세히 나와 있는 단계별 지침을 참조할 수 있습니다.

Adobe Experience Platform과 고객 관리형 키 모두 데이터를 전송할 때나 사용하지 않을 때 암호화함으로써 데이터의 보안을 보장합니다. 고객 관리형 키를 사용하는지 여부에 관계없이 데이터는 계속 보호됩니다.

Adobe Experience Platform의 데이터 암호화에 대한 자세한 내용은 데이터 암호화에 대한 [설명서](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/encryption.html?lang=ko)에서 확인하실 수 있습니다.
