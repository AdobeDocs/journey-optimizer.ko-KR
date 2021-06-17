---
title: 테스트 프로필 만들기
description: 테스트 프로필을 만드는 방법을 알아봅니다
feature: 여정
topic: 콘텐츠 관리
role: User
level: Intermediate
source-git-commit: 8f77802fcaa23790f9de4e8f15e593643b13fb1e
workflow-type: tm+mt
source-wordcount: '1318'
ht-degree: 1%

---

# 테스트 프로필 만들기 {#create-test-profiles}

테스트 모드를 사용할 때 테스트 프로필이 필요합니다. 여정에서 [테스트 모드](../building-journeys/testing-the-journey.md)를 사용하는 방법을 배우고, 메시지](../preview.md)를 미리 보고 테스트하는 방법을 배우려면 테스트 프로필이 필요합니다.[

테스트 프로필을 만드는 데 사용할 수 있는 방법은 아래에 자세히 설명되어 있습니다.

* [기존 프로필](#turning-profile-into-test)을 테스트 프로필로 변환할 수 있습니다

* [csv 파일](#create-test-profiles-csv)을 업로드하거나 [API 호출](#create-test-profiles-api)을 사용하여 테스트 프로필을 만들 수 있습니다. Adobe Journey Optimizer에는 이 두 메서드 외에 특정 [제품 내 사용 사례](#use-case-1)가 포함되어 있어 테스트 프로필 생성을 용이하게 합니다.

* 데이터 세트에 JSON 파일을 업로드할 수도 있습니다. 자세한 내용은 [데이터 수집 설명서](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html#add-data-to-dataset)를 참조하십시오.

테스트 프로필을 만드는 것은 Adobe Experience Platform에서 일반 프로필을 만드는 것과 비슷합니다. 자세한 내용은 [실시간 고객 프로필 설명서](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html)를 참조하십시오.

## 사전 요구 사항 {#test-profile-prerequisites}

프로필을 만들려면 먼저 Adobe [!DNL Journey Optimizer]에서 스키마와 데이터 세트를 만들어야 합니다.

먼저 **스키마를 만들어야 합니다**. 다음 단계를 수행합니다.

1. 데이터 관리 메뉴 섹션에서 **[!UICONTROL Schemas]** 을 클릭합니다.
   ![](../assets/test-profiles-0.png)
1. 오른쪽 상단에 있는 **[!UICONTROL Create schema]** 을 클릭한 다음, 스키마 유형을 선택합니다(예: **XDM 개별 프로필**).
   ![](../assets/test-profiles-1.png)
1. 적절한 필드 그룹을 선택합니다. **프로필 테스트 세부 사항** 필드 그룹을 추가해야 합니다.
   ![](../assets/test-profiles-1-ter.png)
완료되면  **[!UICONTROL Add field groups]**:필드 그룹 목록이 스키마 개요 화면에 표시됩니다.
   ![](../assets/test-profiles-2.png)

   >[!NOTE]
   >
   >* 스키마 이름을 클릭하여 변경하고 해당 속성을 업데이트합니다.
      >
      >
   * 필드 그룹 섹션에서 **[!UICONTROL Add]** 단추를 클릭하여 스키마에 추가할 다른 필드 그룹을 선택합니다


1. 필드 목록에서 기본 ID로 정의할 필드를 클릭합니다.
   ![](../assets/test-profiles-3.png)
1. **[!UICONTROL Field properties]** 오른쪽 창에서 **[!UICONTROL Identity]** 및 **[!UICONTROL Primary Identity]** 옵션을 선택하고 네임스페이스를 선택합니다. 기본 ID를 이메일 주소로 지정하려면 **[!UICONTROL Email]** 네임스페이스를 선택합니다. **[!UICONTROL Apply]**을(를) 클릭합니다.
   ![](../assets/test-profiles-4bis.png)
1. 스키마를 선택하고 **[!UICONTROL Schema properties]** 창에서 **[!UICONTROL Profile]** 옵션을 활성화합니다.
   ![](../assets/test-profiles-5.png)
1. **저장**&#x200B;을 클릭합니다.

>[!NOTE]
>
>스키마 만들기에 대한 자세한 내용은 [XDM 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#prerequisites) 를 참조하십시오.

그런 다음 프로필을 가져올 데이터 세트&#x200B;**를 만들어야 합니다.** 다음 단계를 수행합니다.

1. **[!UICONTROL Datasets]** 로 이동한 다음 **[!UICONTROL Create dataset]** 를 클릭합니다.
   ![](../assets/test-profiles-6.png)
1. **[!UICONTROL Create dataset from schema]**을 선택합니다.
   ![](../assets/test-profiles-7.png)
1. 앞에서 만든 스키마를 선택하고 **[!UICONTROL Next]** 을 클릭합니다.
   ![](../assets/test-profiles-8.png)
1. 이름을 선택한 다음 **[!UICONTROL Finish]** 를 클릭합니다.
   ![](../assets/test-profiles-9.png)
1. **[!UICONTROL Profile]** 옵션을 활성화합니다.
   ![](../assets/test-profiles-10.png)

>[!NOTE]
>
> 데이터 집합 만들기에 대한 자세한 내용은 [카탈로그 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html#getting-started)를 참조하십시오.

## 제품 내 사용 사례{#use-case-1}

Adobe Journey Optimizer 홈페이지에서 테스트 프로필 제품 내 사용 사례를 활용할 수 있습니다. 이 사용 사례를 사용하면 게시하기 전에 여정을 테스트하는 데 사용되는 테스트 프로필을 쉽게 만들 수 있습니다.

![](../assets/use-cases-home.png)

**[!UICONTROL Begin]** 단추를 클릭하여 사용 사례를 시작합니다.

다음 정보가 필요합니다.

1. **ID 네임스페이스**:테스트  [프로필을 ](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html) 고유하게 식별하는 데 사용되는 ID입니다. 예를 들어 이메일을 사용하여 테스트 프로필을 식별하는 경우 ID 네임스페이스 **이메일**&#x200B;을(를) 선택해야 합니다. 고유 식별자가 전화 번호인 경우 ID 네임스페이스 **Phone**&#x200B;을(를) 선택해야 합니다.

2. **CSV 파일**:만들 테스트 프로필 목록이 포함된 쉼표로 구분된 파일입니다. 사용 사례에는 만들 테스트 프로필 목록이 포함된 CSV 파일에 대해 사전 정의된 형식이 필요합니다. 파일의 각 행에는 다음과 같이 올바른 순서로 다음 필드가 포함되어야 합니다.

   1. **개인 Id**:테스트 프로필의 고유 식별자입니다. 이 필드의 값은 선택한 ID 네임스페이스를 반영해야 합니다. 예를 들어 ID 네임스페이스에 대해 **Phone**&#x200B;을(를) 선택한 경우 이 필드의 값은 전화 번호여야 합니다. 마찬가지로 **이메일**&#x200B;을 선택한 경우 이 필드의 값은 이메일 값이어야 합니다.
   1. **이메일**:테스트 프로필 이메일 주소입니다. (**개인 Id** 필드 및 **이메일** 필드는 **이메일**&#x200B;을 ID 네임스페이스로 선택한 경우 동일한 값을 포함할 수 있습니다.)
   1. **이름**:테스트 프로필 이름.
   1. **성**:테스트 프로필 성.
   1. **구/군/시**:테스트 프로필 구/군/시
   1. **국가**:테스트 프로필 국가 거주
   1. **성별**:테스트 프로필 성별 사용 가능한 값은 **male**, **female** 및 **non_specified**&#x200B;입니다.

ID 네임스페이스를 선택하고 위의 형식을 기반으로 CSV 파일을 제공한 후 오른쪽 상단의 **[!UICONTROL Run]** 단추를 클릭합니다. 사용 사례를 완료하는 데 몇 분이 걸릴 수 있습니다. 사용 사례 처리가 완료되고 테스트 프로필 만들기가 완료되면 사용자에게 알림을 보냅니다.

>[!NOTE]
>
>테스트 프로필은 기존 프로필을 재정의할 수 있습니다. 사용 사례를 실행하기 전에 CSV에 테스트 프로필만 포함되어 있으며 이 프로필이 올바른 샌드박스에 대해 실행되었는지 확인하십시오.

## 프로필을 테스트 프로필{#turning-profile-into-test}으로 변환

기존 프로필을 테스트 프로필로 전환할 수 있습니다.프로필을 만들 때와 동일한 방법으로 프로필 속성을 업데이트할 수 있습니다.

이렇게 하는 간단한 방법은 여정에서 **[!UICONTROL Update Profile]** 작업 활동을 사용하고 testProfile 부울 필드를 false에서 true로 변경하는 것입니다.

여정은 **[!UICONTROL Read Segment]** 및 **[!UICONTROL Update Profile]** 활동으로 구성됩니다. 먼저 테스트 프로필로 전환할 프로필을 타겟팅하는 세그먼트를 만들어야 합니다.

>[!NOTE]
>
> **testProfile** 필드를 업데이트할 예정이므로 선택한 프로필에 이 필드가 포함되어야 합니다. 관련 스키마에는 **프로필 테스트 세부 사항** 필드 그룹이 있어야 합니다. [이 섹션](../building-journeys/creating-test-profiles.md#test-profiles-prerequisites)을 참조하십시오.

1. 오른쪽 상단에 있는 **세그먼트**, **세그먼트 만들기**로 이동합니다.
   ![](../assets/test-profiles-22.png)
1. 세그먼트의 이름을 정의하고 세그먼트를 만듭니다.원하는 프로필을 타겟팅할 필드와 값을 선택합니다.
   ![](../assets/test-profiles-23.png)
1. **저장**을 클릭하고 프로필이 세그먼트의 타겟팅이 되는지 확인합니다.
   ![](../assets/test-profiles-24.png)

   >[!NOTE]
   >
   > 세그먼트 계산에 시간이 걸릴 수 있습니다. [이 섹션](../segment/about-segments.md)의 세그먼트에 대해 자세히 알아보십시오.

1. 이제 새 여정을 만들고 **[!UICONTROL Read Segment]** 오케스트레이션 활동으로 시작합니다.
1. 앞에서 만든 세그먼트와 프로필에서 사용하는 네임스페이스를 선택합니다.
   ![](../assets/test-profiles-25.png)
1. **[!UICONTROL Update Profile]** 작업 활동을 추가합니다.
1. 스키마, **testProfiles** 필드, 데이터 세트를 선택하고 값을 **True**&#x200B;로 설정합니다. 이렇게 하려면 **[!UICONTROL VALUE]** 필드에서 오른쪽에 있는 **펜** 아이콘을 클릭하고 **[!UICONTROL Advanced mode]** 을 선택하고 **true**를 입력합니다.
   ![](../assets/test-profiles-26.png)
1. **종료** 활동을 추가하고 **[!UICONTROL Publish]**&#x200B;를 클릭합니다.
1. **[!UICONTROL Segments]** 섹션에서 프로필이 올바르게 업데이트되었는지 확인합니다.
   ![](../assets/test-profiles-28.png)

   >[!NOTE]
   >
   > **[!UICONTROL Update Profile]** 활동에 대한 자세한 정보는 [이 섹션](../building-journeys/update-profiles.md)을 참조하십시오.

## csv 파일{#create-test-profiles-csv}을 사용하여 테스트 프로필 만들기

Adobe Experience Platform에서 다른 프로필 필드가 포함된 csv 파일을 데이터 세트에 업로드하여 프로필을 만들 수 있습니다. 이것이 가장 쉬운 방법입니다.

1. 스프레드시트 소프트웨어를 사용하여 간단한 csv 파일을 만듭니다.
1. 필요한 필드마다 열을 하나씩 추가합니다. 기본 ID 필드(&quot;personID&quot; 위의 예에서 )와 &quot;testProfile&quot; 필드를 &quot;true&quot;로 설정해야 합니다.
   ![](../assets/test-profiles-11.png)
1. 프로필당 한 줄을 추가하고 각 필드의 값을 입력합니다.
   ![](../assets/test-profiles-12.png)
1. 스프레드시트를 csv 파일로 저장합니다. 쉼표가 구분 기호로 사용되는지 확인하십시오.
1. Adobe Experience Platform **워크플로우**로 이동합니다.
   ![](../assets/test-profiles-14.png)
1. **CSV를 XDM 스키마에 매핑**&#x200B;을 선택한 다음 **Launch**를 클릭합니다.
   ![](../assets/test-profiles-16.png)
1. 프로필을 가져올 데이터 세트를 선택합니다. **다음**을 클릭합니다.
   ![](../assets/test-profiles-17.png)
1. **파일 선택**&#x200B;을 클릭하고 csv 파일을 선택합니다. 파일이 업로드되면 **다음**을 클릭합니다.
   ![](../assets/test-profiles-18.png)
1. 소스 csv 필드를 스키마 필드에 매핑한 다음 **완료**를 클릭합니다.
   ![](../assets/test-profiles-19.png)
1. 데이터 가져오기가 시작됩니다. 상태는 **처리**&#x200B;에서 **성공**&#x200B;으로 이동합니다. 오른쪽 상단에 있는 **미리 보기 데이터 세트**를 클릭합니다.
   ![](../assets/test-profiles-20.png)
1. 테스트 프로필이 올바르게 추가되었는지 확인합니다.
   ![](../assets/test-profiles-21.png)

테스트 프로필이 추가되었으며 이제 여정을 테스트할 때 사용할 수 있습니다. [이 섹션](../building-journeys/testing-the-journey.md)을 참조하십시오.
>[!NOTE]
>
> csv 가져오기에 대한 자세한 내용은 [데이터 수집 설명서](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html#tutorials) 를 참조하십시오.

## API 호출을 사용하여 테스트 프로필 만들기{#create-test-profiles-api}

API 호출을 통해 테스트 프로필을 만들 수도 있습니다. 자세한 내용은 이 [페이지](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html)를 참조하십시오.

프로필 테스트 세부 사항 필드 그룹을 포함하는 프로필 스키마를 사용해야 합니다. testProfile 플래그는 이 필드 그룹의 일부입니다.
프로필을 만들 때 값을 전달해야 합니다.testProfile = true.

기존 프로필을 업데이트하여 testProfile 플래그를 &quot;true&quot;로 변경할 수도 있습니다.

다음은 테스트 프로필을 만들기 위한 API 호출의 예입니다.

```
curl -X POST \
'https://dcs.adobedc.net/collection/xxxxxxxxxxxxxx' \
-H 'Cache-Control: no-cache' \
-H 'Content-Type: application/json' \
-H 'Postman-Token: xxxxx' \
-H 'cache-control: no-cache' \
-H 'x-api-key: xxxxx' \
-H 'x-gw-ims-org-id: xxxxx' \
-d '{
"header": {
"msgType": "xdmEntityCreate",
"msgId": "xxxxx",
"msgVersion": "xxxxx",
"xactionid":"xxxxx",
"datasetId": "xxxxx",
"imsOrgId": "xxxxx",
"source": {
"name": "Postman"
},
"schemaRef": {
"id": "https://example.adobe.com/mobile/schemas/xxxxx",
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"body": {
"xdmMeta": {
"schemaRef": {
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"xdmEntity": {
"_id": "xxxxx",
"_mobile":{
"ECID": "xxxxx"
},
"testProfile":true
}
}
}'
```
