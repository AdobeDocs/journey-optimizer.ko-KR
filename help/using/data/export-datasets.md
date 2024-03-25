---
solution: Journey Optimizer
product: journey optimizer
title: 데이터 세트를 클라우드 스토리지 위치로 내보내기
description: Adobe Experience Platform 클라우드 스토리지 대상을 사용하여 데이터 세트를 내보내는 방법을 알아봅니다.
feature: Datasets
role: User
level: Beginner
keywords: Platform, Data Lake, 만들기, 레이크, 데이터 세트, 프로필
exl-id: 66b5c691-ddc4-4e9b-9386-2ce6c307451c
source-git-commit: e45ec5f0e1bbcc73892f9cde5923627886f44ef6
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 9%

---

# 데이터 세트를 클라우드 스토리지 위치로 내보내기 {#export-datasets}

Journey Optimizer을 사용하면 데이터 세트의 콘텐츠를 내보내기 위해 클라우드 스토리지 위치와 라이브 연결을 설정할 수 있습니다.

정기적으로 데이터를 내보내면 고객 상호 작용에 대한 완전한 최신 기록을 확보할 수 있으므로 보고, 보관 또는 데이터 분석 목적으로 쉽게 사용할 수 있습니다.

## 사용 가능한 클라우드 스토리지 대상 {#destinations}

에서 액세스할 수 있는 6개의 클라우드 스토리지 대상으로 데이터 세트를 내보낼 수 있습니다. **[!UICONTROL 대상]** 메뉴, **[!UICONTROL 카탈로그]** 탭.

![](assets/dataset-export-setup.png)


각 대상에 대한 자세한 내용은 Adobe Experience Platform 설명서에서 확인할 수 있습니다.

* [Amazon S3](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3.html)
* [Azure Blob](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob.html)
* [Azure Data Lake Gen 2](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2.html)
* [데이터 랜딩 영역](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html)
* [Google 클라우드 스토리지](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage.html)
* [SFTP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/sftp.html)

## 내보내기에 사용 가능한 데이터 세트 {#datasets}

아래 표에서 내보낼 수 있는 Journey Optimizer 데이터 세트를 이해합니다.

| 데이터 세트 | 설명 |
| ------- | ------- | 
| AJO BCC 피드백 이벤트 데이터 세트 | AJO BCC 피드백 이벤트 데이터 세트 |
| AJO 분류 데이터 세트 | Journey Optimizer에서 이메일 및 푸시 애플리케이션 피드백 이벤트를 수집하기 위한 데이터 세트입니다. SDK를 통해 만들어집니다. |
| AJO 동의 서비스 데이터 세트 | 프로필의 동의 정보를 저장합니다. |
| AJO 이메일 추적 경험 이벤트 데이터 세트 | 보고 및 대상자 만들기 목적으로 사용되는 이메일 채널에 대한 상호 작용 로그.  |
| AJO 엔티티 데이터 세트 | 최종 사용자에게 전송된 메시지의 엔티티 메타데이터를 저장하는 데이터 세트입니다.  |
| AJO 인바운드 활동 이벤트 데이터 세트 | 게재 및 상호 작용 이벤트를 위한 Journey Optimizer 웹 및 inApp 채널에 대한 데이터 세트입니다. |
| AJO 대화형 메시징 프로필 데이터 세트 | API 트리거 캠페인을 지원하기 위해 만든 프로필을 저장합니다. |
| AJO 메시지 피드백 이벤트 데이터 세트 | 메시지 게재 로그. Journey Optimizer의 모든 메시지 게재에 대한 정보입니다. 보고하고 대상자를 만드는 데 사용합니다. 바운스에 대한 이메일 ISP의 피드백도 이 데이터 세트에 기록됩니다. |
| AJO 프로필 카운터 확장 | counter_value 및 expiryDate를 포함하고 counter_id로 키로 처리된 오브젝트 맵을 보관합니다. |
| AJO 푸시 프로필 데이터 세트 | 프로필의 푸시 토큰을 저장합니다. |
| AJO 푸시 추적 경험 이벤트 데이터 세트 | 보고 및 대상자 만들기 목적으로 사용되는 푸시 채널에 대한 상호 작용 로그  |
| AJO 표면 데이터 세트 | Journey Optimizer 인바운드 표면 스키마와 관련된 빈 데이터 세트 |
| AOOutputForUPSDataset | UPS에 다시 기록할 모든 AO 대상자 멤버십을 포함합니다. |
| Audience Orchestration 프로필 데이터 세트 | 대상 구성 대상을 위한 대상 구성으로 생성되었습니다. 모든 대상 구성 대상, 해당 속성 및 데이터 보강 포함 |
| 의사 결정 객체 저장소 - 활동 | 사용자 인터페이스에서 의사 결정이라고도 합니다. 하지만 이러한 요소들은 의사 결정 논리를 포함하여 모든 기본 요소를 함께 배치하는 사용자가 만드는 개체입니다. 예를 들어, 특정 배치(위치)의 경우, 오퍼를 고려할 위치(오퍼 컬렉션)와 해당 오퍼에 사용할 순위 지정 방법을 선택할 수 있습니다. |
| 의사 결정 개체 저장소 - 대체 오퍼 | 사용자가 만드는 다른 유형의 오퍼에 대한 저장소입니다. 특히 개인화된 오퍼를 볼 자격이 없고 항목을 봐야 하는 경우 적어도 대체 오퍼가 표시됩니다. 이 데이터 세트에는 이 유형의 오퍼에 대한 특성이 포함되어 있습니다. |
| 의사 결정 개체 저장소 - 개인화된 오퍼 | 사용자가 만드는 오퍼 유형에 대한 저장소입니다. 따라서 이 데이터 세트에는 이 유형의 오퍼에 대한 속성이 포함되어 있습니다. | Ultimate |
| 의사 결정 객체 저장소 - 배치 | 오퍼가 표시되어야 하는 위치를 정의하는 오브젝트 저장소입니다. |
| 여정 단계 이벤트 | Journey Optimizer에서 생성된 모든 여정 단계 경험 이벤트를 캡처하여 보고와 같은 서비스에서 사용할 수 있습니다. |
| 여정 | 여정 내 각 단계의 메타데이터 데이터 세트 하우징 정보 |
| ODE DecisionEvents - prod decisioning | 우리가 요청에 따라 결정을 내릴 때마다, 우리는 그것을 결정 이벤트로 간주한다 |

## 전제 조건 {#prerequisites}

데이터 세트를 내보내려면 [액세스 제어 권한](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html#permissions){target="_blank"} listed below. Read the [access control overview](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/overview.html){target="_blank"} 필요한 권한을 얻으려면 제품 관리자에게 문의하십시오.

| 카테고리 | 사용 권한 |
|--|--|
| 대상 | 데이터 세트 대상 관리 및 활성화 |
| 데이터 관리 | 데이터 세트 보기 |
| 대상 | 대상 보기 |

## 데이터 세트를 내보내는 주요 단계 {#main-steps}

데이터 세트를 클라우드 스토리지 위치로 내보내는 주요 단계는 다음과 같습니다.

![](assets/dataset-export-process.png)

각 단계에 대한 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html){target="_blank"}.

1. **클라우드 스토리지 대상 설정**. 아직 연결하지 않은 경우 대상 카탈로그에서 클라우드 스토리지 대상에 연결합니다. 에서 새 대상 연결을 만드는 방법을 알아봅니다 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html#setup){target="_blank"}.

   <!--![](assets/dataset-export-setup.png)-->

1. **클라우드 스토리지 대상 선택** 데이터 세트를 내보낼 위치입니다. 대상 카탈로그에서 **[!UICONTROL 데이터 세트 내보내기]** 원하는 카드를 누르고 사용할 연결을 선택합니다.

   <!--![](assets/dataset-export-destination.png)-->

   >[!NOTE]
   >
   >실시간 고객 프로필과 함께 Adobe Journey Optimizer을 사용하는 경우 대상 카드에 **활성화** 단추를 사용하여 데이터 세트를 내보내고 활성화한 권한에 따라 이 대상에 대한 대상을 활성화할 수 있습니다.

1. **데이터 세트 선택** 을(를) 선택한 대상으로 내보냅니다. [내보내기에 사용할 수 있는 Journey Optimizer 데이터 세트에 대한 자세한 정보](#datasets)

   <!--![](assets/dataset-export-dataset-selection.png)-->

1. **내보내기 예약** 데이터 세트. 내보내기를 시작해야 하는 시기와 실행 빈도를 지정합니다.

   <!--![](assets/dataset-export-schedule.png)-->

1. **내보내기 검토 및 확인** 구성 끝에 표시되는 요약을 확인합니다.

   <!--![](assets/dataset-export-review.png)-->

내보내기가 완료되면 데이터 세트의 콘텐츠가 사용자가 구성한 일정에 따라 클라우드 저장소 위치에 저장됩니다. [성공적인 데이터 세트 내보내기를 확인하는 방법 알아보기](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html#verify){target="_blank"}.
