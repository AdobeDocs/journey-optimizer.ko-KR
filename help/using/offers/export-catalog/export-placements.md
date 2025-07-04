---
title: 배치 데이터 세트
description: 이 섹션에는 배치용으로 내보낸 데이터 세트에 사용된 모든 필드가 나열됩니다
badge: label="레거시" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer
level: Intermediate
exl-id: 3e45f3cf-e17e-43a6-8424-98afef07aaa3
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 1%

---

# 배치 데이터 세트 {#placements-dataset}

오퍼가 수정될 때마다 배치에 대해 자동 생성된 데이터 세트가 업데이트됩니다.

![](../assets/dataset-placements.png)

데이터 세트에서 가장 최근에 성공한 일괄 처리가 오른쪽에 표시됩니다. 데이터 세트에 대한 스키마의 계층 구조 보기가 왼쪽 창에 표시됩니다.

>[!NOTE]
>
>[이 섹션](../export-catalog/access-dataset.md)에서 오퍼 라이브러리의 각 개체에 대해 내보낸 데이터 세트에 액세스하는 방법에 대해 알아봅니다.

다음은 **[!UICONTROL 의사 결정 개체 저장소 - 배치]** 데이터 집합에서 사용할 수 있는 모든 필드 목록입니다.

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

+++ 식별자

**필드:** _id
**제목:** 식별자
**설명:** 레코드의 고유 식별자입니다.
**유형:** 문자열

+++

+++ 경험(_E)

**필드:** 경험(_E)
**유형:** 개체

+++

+++ 경험 > 의사 결정(_e)

**필드:** 의사 결정
**유형:** 개체

+++

+++ 경험 > 의사 결정 > 배치의 채널 식별자(_E)

**필드:** channelID
**제목:** 배치의 채널 식별자
**설명:** 제안이 만들어진 채널입니다. 값이 올바른 채널 URI입니다. https://ns.adobe.com/xdm/channels/channel 을 참조하십시오.
**유형:** 문자열

+++

+++ _experience > 의사 결정 > 콘텐츠 구성 요소 유형

**필드:** componentType
**제목:** 콘텐츠 구성 요소 유형
**설명:** 각 값이 콘텐츠 구성 요소에 지정된 형식에 매핑되는 열거형 URI 집합입니다. 콘텐츠 표현의 일부 소비자는 @type 값이 콘텐츠 구성 요소의 추가 속성을 설명하는 스키마에 대한 참조가 될 것으로 예상합니다.
**유형:** 문자열

+++

+++ _experience > 의사 결정 > contentTypes

**필드:** contentTypes
**유형:** 배열

+++

+++_경험 > 의사 결정 > contentTypes > MIME 미디어 유형

**제목:** MIME 미디어 유형
**설명:** 해당 배치에 필요한 구성 요소의 미디어 유형에 대한 제한 사항입니다. 하나의 구성 요소(예: 다른 이미지 형식)에 대해 가능한 미디어 유형은 두 개 이상일 수 있습니다.
**유형:** 문자열

+++

+++ _experience > 의사 결정 > 배치 설명

**필드:** 설명
**제목:** 배치 설명
**설명:** 동적 콘텐츠가 전체 메시지 게재에서 사용되는 방식에 대해 사람이 읽을 수 있는 의도를 전달하는 데 사용됩니다. 웹 페이지의 특정 공간이 \&quot;Banner\&quot;라는 사실은 대개 설명을 통해 전달되며, 공식적인 방법으로는 전달되지 않습니다.
**유형:** 문자열

+++

+++ _experience > 의사 결정 > 배치 이름

**필드:** 이름
**제목:** 배치 이름
**설명:** 상호 작용에서 참조할 수 있도록 배치에 할당된 이름입니다.
**유형:** 문자열

+++

+++ _repo

**필드:** _repo
**유형:** 개체

+++

+++ _repo > 배치 ETag

**필드:** etag
**제목:** 배치 ETag
**설명:** 스냅숏을 만들 때 결정 옵션 개체가 수정되었습니다.
**유형:** 문자열

+++
