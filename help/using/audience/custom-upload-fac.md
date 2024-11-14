---
solution: Journey Optimizer
product: journey optimizer
title: 사용자 지정 업로드(CSV) 및 페더레이션 대상 구성
description: CSV(사용자 지정 업로드) 및 Federated Audience Composition 대상으로 작업하는 동안 주요 정보와 모범 사례를 알아봅니다.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
exl-id: d2365e3f-fbef-43c2-bf2a-0a868cb93015
source-git-commit: a98312d9ac5a457bfd6789bf79ad80a24d894a0b
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 1%

---

# 사용자 지정 업로드(CSV) 및 페더레이션 대상 구성 {#csv-fac}

## 사용자 지정 업로드 및 페더레이션 대상 구성 정보 {#about}

세그먼트 정의 및 대상 구성 외에 [!DNL Journey Optimizer]을(를) 사용하면 CSV 파일에서 가져오거나 데이터 웨어하우스의 데이터를 활용하여 대상을 생성하고 타깃팅할 수 있습니다.

* **사용자 지정 업로드**: CSV 파일을 사용하여 대상을 가져옵니다. Adobe Experience Platform [세그먼테이션 서비스 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"}에서 대상을 가져오는 방법을 알아보세요.

* **페더레이션 대상 구성**: 기존 데이터 웨어하우스에서 직접 데이터 세트를 페더레이션하여 하나의 시스템에 Adobe Experience Platform 대상 및 특성을 모두 빌드하고 보강합니다. [Federated Audience Composition](https://experienceleague.adobe.com/ko/docs/federated-audience-composition/using/home)에 대한 안내서를 읽어 보십시오.

Journey Optimizer에서 이러한 대상을 타기팅하거나 Adobe Experience Platform에서 지원하는 모든 대상으로 활성화할 수 있습니다

➡️0}비디오에서 이러한 기능 살펴보기](#video)[

## 반드시 알아야 할 사항 {#must-read}

이 섹션에서는 사용자 지정 업로드(CSV 파일) 및 Federated Audience Composition 대상으로 작업하는 동안 유의해야 할 주요 정보를 제공합니다.

* **미리 보기 및 증명 지원:** 현재 미리 보기 및 증명은 CSV 업로드 또는 Federated Audience Composition을 사용하여 만든 대상에 대해 지원되지 않습니다. 캠페인을 계획할 때는 이 점을 염두에 두십시오.

* **활성화 지연:** 대상자가 수집이 완료된 직후 Journey Optimizer에서 사용할 준비가 되었습니다. 일반적으로 1시간 이내이지만 약간의 변동성이 있습니다.

* **활성화된 레코드 및 ID 결합:** 대상자의 모든 레코드는 모든 중복을 포함하여 활성화됩니다. 다음 UPS 프로필 내보내기 동안 이러한 레코드는 ID 결합을 거칩니다. 그 결과 활성화된 레코드 수는 ID 결합 후 프로필 수와 다를 수 있습니다.

* **새 프로필 타깃팅:** 레코드와 UPS 프로필 간에 일치하는 항목을 찾을 수 없으면 새 빈 프로필이 만들어집니다. 이 프로필은 데이터 레이크에 저장된 데이터 보강 속성에 연결됩니다. 이 새 프로필은 비어 있으므로 Journey Optimizer에서 일반적으로 사용되는 타겟팅 필드(예: personalEmail.address, mobilePhone.number)는 비어 있으므로 타겟팅에 사용할 수 없습니다.

  이를 해결하려면 채널 구성에서 &quot;실행 필드&quot;(또는 채널에 따른 &quot;실행 주소&quot;)를 &quot;identityMap&quot;으로 지정할 수 있습니다. 이렇게 하면 대상을 만들 때 ID로 선택한 속성이 Journey Optimizer에서 타깃팅에 사용되는 속성이 됩니다.

## 방법 비디오 {#video}

CSV 형식으로 대상을 Adobe Experience Platform에 업로드하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3421714?quality=12)

Federated Audience 구성에 대해 자세히 알아보십시오 .

>[!VIDEO](https://video.tv.adobe.com/v/3432261?quality=12)
