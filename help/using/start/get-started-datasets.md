---
title: 데이터 세트 시작
description: Adobe Journey Optimizer에서 Adobe Experience Platform 데이터 세트를 사용하는 방법을 알아봅니다
role: User
level: Beginner
exl-id: dcdd3c81-0f00-4259-a8a5-9062a4c40b6f
source-git-commit: 9ebcfd6c41c17fe3be0423822209443fc55244a7
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 11%

---

# 데이터 세트 시작 {#datasets-gs}

Adobe Experience Platform에 수집된 모든 데이터는 데이터 세트로 데이터 레이크 내에서 유지됩니다. 데이터 세트는 스키마(열) 및 필드(행)를 포함하는 데이터 수집을 위한 저장소 및 관리 구조입니다. 

## 데이터 세트 액세스{#access-datasets}

다음 **데이터 세트** 작업 공간 [!DNL Adobe Journey Optimizer] 사용자 인터페이스를 통해 데이터를 탐색하고 데이터 세트를 만들 수 있습니다.

선택 **데이터 세트** 왼쪽 탐색에서 데이터 세트 대시보드를 엽니다.

![](assets/datasets-home.png)

Adobe Experience Platform에 데이터를 추가하는 것은 프로필 작성의 기반입니다. 그러면 에서 프로필을 활용할 수 있습니다 [!DNL Adobe Journey Optimizer]. 먼저 스키마를 정의하고 ETL 도구를 사용하여 데이터를 준비하고 표준화한 다음 스키마를 기반으로 데이터 세트를 만듭니다.

을(를) 선택합니다 **찾아보기** 탭을 클릭하여 조직에서 사용 가능한 모든 데이터 세트 목록을 표시합니다. 세부 사항은 해당 이름, 데이터 세트가 준수하는 스키마 및 가장 최근 수집 실행 상태를 포함하여 나열된 각 데이터 세트에 대해 표시됩니다.

기본적으로 수집된 데이터 세트만 표시됩니다. 시스템에서 생성한 데이터 세트를 보려면 **시스템 데이터 세트 표시** 필터에서 전환합니다.

![](assets/ajo-system-datasets.png)

데이터 세트 이름을 선택하여 해당 데이터 세트 활동 화면에 액세스하고 선택한 데이터 세트에 대한 세부 사항을 확인합니다. 활동 탭에는 사용 중인 메시지 수와 성공 및 실패한 일괄 처리 목록을 시각화하는 그래프가 포함되어 있습니다.

## 데이터 세트 만들기{#create-datasets}

새 데이터 세트를 만들려면 먼저 **데이터 집합 만들기** 데이터 세트 대시보드에서 을 참조하십시오.

다음을 수행할 수 있습니다.

* 스키마에서 데이터 집합을 만듭니다. [자세한 내용은 이 문서에서 알아보십시오](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#schema){target=&quot;_blank&quot;}
* CSV 파일에서 데이터 세트를 만듭니다. [자세한 내용은 이 문서에서 알아보십시오](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html?lang=ko-KR){target=&quot;_blank&quot;}


이 비디오에서 데이터 세트를 만들고 스키마에 매핑하고 데이터를 추가하고 데이터가 수집되었는지 확인하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334293?quality=12)


에서 Adobe Journey Optimizer에서 스키마, 데이터 세트 및 데이터를 수집하여 테스트 프로필을 추가하는 방법을 알아봅니다 [이 종단 간 샘플](../segment/creating-test-profiles.md)

에서 데이터 집합 만들기에 대해 자세히 알아보십시오 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target=&quot;_blank&quot;}.

에서 데이터 세트 UI를 사용하는 방법을 알아봅니다 [데이터 수집 개요 설명서](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=ko){target=&quot;_blank&quot;}.


**참조 -**

* [스키마, 데이터 세트 및 데이터를 수집하여 Journey Optimizer에서 테스트 프로필을 추가합니다](../segment/creating-test-profiles.md)
* [스트리밍 수집 개요](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=ko){target=&quot;_blank&quot;}
* [Adobe Experience Platform에 데이터 수집](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html){target=&quot;_blank&quot;}
