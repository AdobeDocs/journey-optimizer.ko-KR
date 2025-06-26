---
solution: Journey Optimizer
product: journey optimizer
title: 여정 게시
description: 여정 게시 방법 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 게시, 여정, 라이브, 유효성, 확인
exl-id: e0ca8aef-4f1d-4631-8c34-1692d96e8b51
source-git-commit: fa46397b87ae3a81cd016d95afd3e09bb002cfaa
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 42%

---

# 여정 게시 {#publishing-the-journey}

여정을 활성화하려면 여정을 게시하고 새 프로필에서 프로필을 입력할 수 있도록 해야 합니다. 여정을 게시하기 전에 유효하고 오류가 없는지 확인하십시오. 오류가 있는 여정은 게시할 수 없습니다.

➡️ [비디오에서 이 기능 살펴보기](#video)

## 게시 프로세스 {#journey-publication}

여정 게시 단계는 아래에 자세히 설명되어 있습니다.

1. 여정을 게시하기 전에 유효하고 오류가 없는지 확인하십시오. 오류가 있는 여정은 게시할 수 없습니다.

   * [이 페이지](testing-the-journey.md)에서 여정을 테스트하는 방법을 알아보세요.
   * [이 섹션](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)에서 여정 오류를 해결하는 방법을 알아봅니다.

1. 여정을 게시하려면 오른쪽 상단 드롭다운 메뉴에 있는 **[!UICONTROL 게시]** 옵션을 클릭합니다.

   >[!NOTE]
   >
   > 여정이 승인 정책의 적용을 받는 경우 여정을 게시하려면 승인을 요청해야 합니다. [자세히 알아보기](../test-approve/gs-approval.md)

   ![](assets/journeyuc1_18.png)

여정이 게시되면 **읽기 전용** 모드에 있습니다. 읽기 전용 모드에서는 활동 레이블 및 설명, 여정 이름 및 여정 설명만 수정할 수 있습니다. 게시된 여정을 추가로 수정해야 하는 경우 여정의 [새 버전](journey-ui.md#journey-versions)을 만드십시오.

여정을 중지하면 영구적으로 중지됩니다. 여정을 통해 흘러가는 모든 개인은 영구적으로 정지되며, 여정은 새로운 항목을 허용하는 것을 중단한다. 여정을 다시 실행해야 하는 경우 복제하고 새 여정을 게시합니다.

>[!IMPORTANT]
>
>여정의 메시지에 사용된 여정 결정이 변경되는 경우 오퍼 게시를 취소하고 다시 게시해야 합니다. 이렇게 하면 변경 사항이 여정 메시지에 통합되고 메시지가 최신 업데이트와 일관되게 표시됩니다.

## 여정 버전 {#journey-versions}

여정 목록에는 모든 여정 버전이 버전 번호와 함께 표시됩니다. 여정을 검색하면 애플리케이션이 처음 열릴 때 최신 버전이 목록 맨 위에 나타납니다. 그런 다음 원하는 정렬을 정의하면 애플리케이션이 이를 사용자 기본 설정으로 유지합니다. 여정 버전은 여정 편집 인터페이스의 맨 위에 캔버스 위에 표시됩니다.

![](assets/journeyversions1.png)

>[!NOTE]
>
>일반적으로 프로필은 모든 활성 버전의 여정에 대해 동일한 여정에 동시에 여러 번 있을 수 없습니다. 재진입이 활성화된 경우 프로필은 여정에 다시 진입할 수 있지만 여정의 이전 인스턴스를 완전히 종료할 때까지는 다시 진입할 수 없습니다. [자세히 보기](entry-management.md).

### 여정의 새 버전 만들기 {#journey-create-new-version}

라이브 여정으로 수정해야 하는 경우 여정의 새 버전을 만듭니다. 기존 여정의 새 버전을 생성하려면 아래 단계를 수행하십시오.

1. 최신 버전의 라이브 여정을 열고 **[!UICONTROL 새 버전 만들기]**&#x200B;를 클릭한 후 확인합니다.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >최신 버전의 여정에서만 새 버전을 만들 수 있습니다.

1. 수정하고 **[!UICONTROL 게시]**&#x200B;를 클릭한 후 확인합니다.

여정이 게시되는 순간부터 개인 사용자는 최신 버전의 여정으로 유입되기 시작합니다. 이미 이전 버전으로 진입한 사람은 여정이 완료될 때까지 해당 버전을 유지합니다. 나중에 동일한 여정으로 다시 진입하면 최신 버전으로 이동합니다.

여정 버전은 개별적으로 중지할 수 있습니다. 여정의 모든 버전은 이름이 같습니다.

새 여정 버전을 게시하면 이전 버전이 자동으로 종료되고 **닫힌** 상태로 전환됩니다. 여정 출입이 있을 수 없습니다. 최신 버전을 중지해도 이전 버전은 닫힌 상태로 유지됩니다.


>[!NOTE]
>
>특정 보호 기능 및 제한 사항은 여정 버전 관리에 적용됩니다. [이 페이지](../start/guardrails.md#journey-versions-journey-versions-g)에서 자세히 알아보십시오.


## 사용 방법 비디오 {#video}

이 비디오에서 여정을 게시하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3427937?quality=12&captions=kor)