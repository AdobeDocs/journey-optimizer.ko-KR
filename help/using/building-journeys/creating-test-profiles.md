---
solution: Journey Optimizer
product: journey optimizer
title: 테스트 프로필 만들기
description: 테스트 프로필을 만드는 방법을 알아봅니다
feature: Test Profiles, Profiles
topic: Content Management
role: User, Data Engineer
level: Intermediate
keywords: 테스트 프로필, 테스트, 테스트, 여정
exl-id: bd5e053a-69eb-463b-add3-8b9168c8e280
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '1328'
ht-degree: 2%

---

# 테스트 프로필 만들기 {#create-test-profiles}

여정에서 [테스트 모드](../building-journeys/testing-the-journey.md)를 사용할 때, [콘텐츠를 미리 보고 테스트하려면](../content-management/preview-test.md) 테스트 프로필이 필요합니다.

테스트 프로필을 만드는 방법에는 몇 가지가 있습니다. 이 페이지에서 자세한 내용을 찾아 다음과 같은 작업을 수행할 수 있습니다.

* [기존 프로필](#turning-profile-into-test)을 테스트 프로필로 전환

* [csv 파일](#create-test-profiles-csv)을 업로드하거나 [API 호출](#create-test-profiles-api)을(를) 사용하여 테스트 프로필을 만듭니다.

  이 두 가지 방법 외에도 Adobe Journey Optimizer에는 테스트 프로필을 쉽게 만들 수 있는 특정 [제품 내 사용 사례](#use-case-1)가 포함되어 있습니다.

기존 데이터 세트에 json 파일을 업로드할 수도 있습니다. 자세한 내용은 [데이터 수집 설명서](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html#add-data-to-dataset){target="_blank"}를 참조하세요.

테스트 프로필을 만드는 것은 Adobe Experience Platform에서 일반 프로필을 만드는 것과 비슷합니다. 자세한 내용은 [실시간 고객 프로필 설명서](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=ko){target="_blank"}를 참조하세요.

➡️0}이 비디오에서 테스트 프로필을 만드는 방법을 알아봅니다](#video)[

## 전제 조건 {#test-profile-prerequisites}

프로필을 만들려면 먼저 Adobe [!DNL Journey Optimizer]에서 스키마와 데이터 세트를 만들어야 합니다.

**스키마를 만들려면** 다음 단계를 수행하십시오.

1. 데이터 관리 메뉴 섹션에서 **[!UICONTROL 스키마]**를 클릭합니다.
   ![](assets/test-profiles-0.png)
1. 오른쪽 상단에서 **[!UICONTROL 스키마 만들기]**&#x200B;를 클릭하고 스키마 유형(예: **개인 프로필**)을 선택한 후 **다음**을 클릭합니다.
   ![](assets/test-profiles-1.png)
1. 스키마 이름을 입력하고 **마침**을 클릭합니다.
   ![](assets/test-profiles-1-bis.png)
1. **필드 그룹** 섹션에서 왼쪽의 **추가$$을(를) 클릭하고 적절한 필드 그룹을 선택합니다. **프로필 테스트 세부 정보** 필드 그룹을 추가해야 합니다.
   ![](assets/test-profiles-1-ter.png)
완료되면 **[!UICONTROL 필드 그룹 추가]**를 클릭합니다. 필드 그룹 목록이 스키마 개요 화면에 표시됩니다.
   ![](assets/test-profiles-2.png)

   >[!NOTE]
   >
   >스키마 속성을 업데이트하려면 스키마 이름을 클릭합니다.

1. 필드 목록에서 기본 ID로 정의할 필드를 클릭합니다.
   ![](assets/test-profiles-3.png)
1. **[!UICONTROL 필드 속성]** 오른쪽 창에서 **[!UICONTROL ID]** 및 **[!UICONTROL 기본 ID]** 옵션을 확인하고 네임스페이스를 선택하십시오. 기본 ID를 전자 메일 주소로 설정하려면 **[!UICONTROL 전자 메일]** 네임스페이스를 선택하세요. **[!UICONTROL 적용]**을 클릭합니다.
   ![](assets/test-profiles-4bis.png)
1. 스키마를 선택하고 **[!UICONTROL 스키마 속성]** 창에서 **[!UICONTROL 프로필]** 옵션을 활성화하십시오.
   ![](assets/test-profiles-5.png)
1. **저장**&#x200B;을 클릭합니다.

>[!NOTE]
>
>스키마 만들기에 대한 자세한 내용은 [XDM 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#prerequisites){target="_blank"}를 참조하세요.

프로필을 가져올 데이터 집합을 **만들어야** 합니다. 다음 단계를 수행하십시오.

1. **[!UICONTROL 데이터 세트]**(으)로 이동한 다음 **[!UICONTROL 데이터 세트 만들기]**를 클릭합니다.
   ![](assets/test-profiles-6.png)
1. **[!UICONTROL 스키마에서 데이터 집합 만들기]**를 선택합니다.
   ![](assets/test-profiles-7.png)
1. 이전에 만든 스키마를 선택한 다음 **[!UICONTROL 다음]**을 클릭합니다.
   ![](assets/test-profiles-8.png)
1. 이름을 선택한 다음 **[!UICONTROL 마침]**을 클릭하세요.
   ![](assets/test-profiles-9.png)
1. **[!UICONTROL 프로필]** 옵션을 사용하도록 설정합니다.
   ![](assets/test-profiles-10.png)

>[!NOTE]
>
> 데이터 집합 만들기에 대한 자세한 내용은 [카탈로그 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html#getting-started){target="_blank"}를 참조하세요.

## 제품 내 사용 사례{#use-case-1}

Adobe Journey Optimizer 홈페이지에서 테스트 프로필의 제품 내 사용 사례를 활용할 수 있습니다. 이 사용 사례는 게시하기 전에 여정 테스트에 사용되는 테스트 프로필을 쉽게 만듭니다.

![](assets/use-cases-home.png)

**[!UICONTROL 시작]** 버튼을 클릭하여 사용 사례를 시작합니다.

다음 정보가 필요합니다.

1. **ID 네임스페이스**: 테스트 프로필을 고유하게 식별하는 데 사용되는 [ID 네임스페이스](../audience/get-started-identity.md)입니다. 예를 들어 테스트 프로필을 식별하는 데 이메일을 사용하는 경우 ID 네임스페이스 **이메일**&#x200B;을(를) 선택해야 합니다. 고유 식별자가 전화번호인 경우 ID 네임스페이스 **Phone**&#x200B;을(를) 선택해야 합니다.

2. **CSV 파일**: 만들 테스트 프로필 목록이 포함된 쉼표로 구분된 파일입니다. 사용 사례에서는 생성할 테스트 프로필 목록이 포함된 CSV 파일에 대해 사전 정의된 형식이 필요합니다. 파일의 각 행에는 다음과 같이 올바른 순서로 다음 필드가 포함되어야 합니다.

   1. **개인 ID**: 테스트 프로필의 고유 식별자입니다. 이 필드의 값은 선택한 ID 네임스페이스를 반영해야 합니다. (예를 들어 ID 네임스페이스에 대해 **전화**&#x200B;를 선택한 경우 이 필드의 값은 전화번호여야 합니다. 마찬가지로 **전자 메일**&#x200B;을 선택한 경우 이 필드의 값은 전자 메일이 됩니다.
   1. **전자 메일 주소**: 프로필 전자 메일 주소를 테스트합니다. (ID 네임스페이스로 **전자 메일**&#x200B;을(를) 선택한 경우 **개인 ID** 필드와 **전자 메일 주소** 필드에 동일한 값이 포함될 수 있습니다.)
   1. **이름**: 테스트 프로필 이름.
   1. **성**: 테스트 프로필의 성.
   1. **구/군/시**: 테스트 프로필 구/군/시
   1. **국가**: 테스트 프로필 거주 국가
   1. **성별**: 프로필 성별을 테스트합니다. 사용 가능한 값은 **male**, **female** 및 **non_specified**&#x200B;입니다.

ID 네임스페이스를 선택하고 위의 형식을 기반으로 CSV 파일을 제공한 후 오른쪽 상단의 **[!UICONTROL 실행]** 단추를 클릭하십시오. 사용 사례를 완료하는 데 몇 분 정도 걸릴 수 있습니다. 사용 사례에서 테스트 프로필 처리 및 생성을 완료하면 사용자에게 알리는 알림이 전송됩니다.

>[!NOTE]
>
>테스트 프로필이 기존 프로필을 재정의할 수 있습니다. 사용 사례를 실행하기 전에 CSV에 테스트 프로필만 포함되어 있는지 그리고 올바른 샌드박스에 대해 CSV가 실행되는지 확인하십시오.

## 프로필을 테스트 프로필로 만들기{#turning-profile-into-test}

기존 프로필을 테스트 프로필로 만들 수 있습니다. 프로필을 만들 때와 동일한 방법으로 프로필 속성을 업데이트할 수 있습니다.

이를 위해 여정에서 **[!UICONTROL 프로필 업데이트]** 작업 활동을 사용하고 **testProfile** 부울 필드를 false에서 true로 변경하는 간단한 방법이 있습니다.

여정은 **[!UICONTROL 대상자 읽기]** 및 **[!UICONTROL 프로필 업데이트]** 활동으로 구성됩니다. 먼저 테스트 프로필로 전환할 프로필을 타겟팅하는 대상을 만들어야 합니다.

>[!NOTE]
>
> **testProfile** 필드를 업데이트하게 되므로 선택한 프로필에 이 필드가 포함되어야 합니다. 관련 스키마에 **프로필 테스트 정보** 필드 그룹이 있어야 합니다. [이 섹션](../audience/creating-test-profiles.md#test-profiles-prerequisites)을 참조하십시오.

1. 오른쪽 상단에서 **대상**&#x200B;을 찾은 다음 **대상 만들기**를 찾습니다.
   ![](assets/test-profiles-22.png)
1. 대상자의 이름을 정의하고 대상자를 구성합니다. 원하는 프로필을 타겟팅할 필드 및 값을 선택합니다.
   ![](assets/test-profiles-23.png)
1. **저장**을 클릭하고 대상자에 의해 프로필이 올바르게 타겟팅되었는지 확인하십시오.
   ![](assets/test-profiles-24.png)

   >[!NOTE]
   >
   > 대상 계산에는 시간이 걸릴 수 있습니다. [이 섹션](../audience/about-audiences.md)의 대상자에 대해 자세히 알아보세요.

1. 이제 새 여정을 만들고 **[!UICONTROL 대상자 읽기]** 오케스트레이션 활동으로 시작합니다.
1. 이전에 만든 대상자와 프로필에서 사용하는 네임스페이스를 선택합니다.
   ![](assets/test-profiles-25.png)
1. **[!UICONTROL 프로필 업데이트]** 작업 활동을 추가합니다.
1. 스키마, **testProfiles** 필드, 데이터 세트를 선택하고 값을 **True**(으)로 설정하십시오. 이렇게 하려면 **[!UICONTROL VALUE]** 필드에서 오른쪽의 **Pen** 아이콘을 클릭하고 **[!UICONTROL 고급 모드]**&#x200B;를 선택한 다음 **true**을(를) 입력합니다.
   ![](assets/test-profiles-26.png)
1. **[!UICONTROL Publish]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL 대상]** 섹션에서 프로필이 올바르게 업데이트되었는지 확인합니다.
   ![](assets/test-profiles-28.png)

   >[!NOTE]
   >
   > **[!UICONTROL 프로필 업데이트]** 활동에 대한 자세한 내용은 [이 섹션](../building-journeys/update-profiles.md)을 참조하세요.

## csv 파일을 사용하여 테스트 프로필 만들기{#create-test-profiles-csv}

Adobe Experience Platform에서는 다른 프로필 필드가 포함된 csv 파일을 데이터 세트에 업로드하여 프로필을 만들 수 있습니다. 이것이 가장 쉬운 방법입니다.

1. 스프레드시트 소프트웨어를 사용하여 간단한 csv 파일을 만듭니다.
1. 필요한 각 필드에 하나의 열을 추가합니다. 기본 ID 필드(&quot;위의 예에서 &quot;personID&quot;)와 &quot;testProfile&quot; 필드를 &quot;true&quot;로 설정해야 합니다.
   ![](assets/test-profiles-11.png)
1. 프로필당 한 줄을 추가하고 각 필드의 값을 입력합니다.
   ![](assets/test-profiles-12.png)
1. 스프레드시트를 csv 파일로 저장합니다. 쉼표를 구분 기호로 사용해야 합니다.
1. Adobe Experience Platform **워크플로**(으)로 이동합니다.
   ![](assets/test-profiles-14.png)
1. **XDM 스키마에 CSV 매핑**&#x200B;을 선택한 다음 **시작**을 클릭합니다.
   ![](assets/test-profiles-16.png)
1. 프로필을 가져올 데이터 세트를 선택합니다. **다음**을 클릭합니다.
   ![](assets/test-profiles-17.png)
1. **파일 선택**&#x200B;을 클릭하고 csv 파일을 선택하십시오. 파일이 업로드되면 **다음**을(를) 클릭합니다.
   ![](assets/test-profiles-18.png)
1. 소스 csv 필드를 스키마 필드에 매핑한 다음 **마침**을 클릭합니다.
   ![](assets/test-profiles-19.png)
1. 데이터 가져오기가 시작됩니다. 상태가 **처리 중**&#x200B;에서 **성공**(으)로 이동합니다. 오른쪽 상단에서 **데이터 집합 미리 보기**를 클릭합니다.
   ![](assets/test-profiles-20.png)
1. 테스트 프로필이 올바르게 추가되었는지 확인합니다.
   ![](assets/test-profiles-21.png)

테스트 프로필이 추가되었으며 이제 여정 테스트 시 사용할 수 있습니다. [이 섹션](../building-journeys/testing-the-journey.md)을 참조하십시오.
>[!NOTE]
>
> csv 가져오기에 대한 자세한 내용은 [데이터 수집 설명서](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html#tutorials){target="_blank"}를 참조하세요.

## API 호출을 사용하여 테스트 프로필 만들기{#create-test-profiles-api}

API 호출을 통해 테스트 프로필을 만들 수도 있습니다. 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=ko){target="_blank"}를 참조하세요.

&quot;프로필 테스트 세부 정보&quot; 필드 그룹을 포함하는 프로필 스키마를 사용해야 합니다. testProfile 플래그는 이 필드 그룹의 일부입니다.
프로필을 만들 때 다음 값을 전달하십시오. testProfile = true.

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

## 방법 비디오 {#video}

테스트 프로필을 만드는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334236?quality=12)
