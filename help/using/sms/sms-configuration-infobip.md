---
solution: Journey Optimizer
product: journey optimizer
title: Infobip 공급자 구성
description: Infobip을 사용하여 Journey Optimizer으로 문자 메시지 및 MMS를 전송하도록 환경을 구성하는 방법에 대해 알아봅니다
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: c9a35c2950c061318f673cdd53d0a5fd08063c27
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 4%

---

# Infobip 공급자 구성 {#sms-configuration-infobip}

Journey Optimizer을 사용하여 Infobip을 구성하려면 다음 단계를 수행합니다.

1. 왼쪽 레일에서 **[!UICONTROL 관리]** `>` **[!UICONTROL 채널]**(으)로 이동한 다음 **[!UICONTROL API 자격 증명]** 메뉴를 선택하십시오. **[!UICONTROL 새 API 자격 증명 만들기]** 단추를 클릭합니다.

1. 아래 설명된 대로 API 자격 증명을 구성합니다.

   * **[!UICONTROL SMS 공급업체]**: Infobip.

   * **[!UICONTROL 이름]**: API 자격 증명의 이름을 선택하십시오.

   * **[!UICONTROL API 기본 URL]** 및 **[!UICONTROL API 키]**: 웹 인터페이스 홈 페이지 또는 API 키 관리 페이지에 액세스하여 자격 증명을 찾습니다. 자세한 내용은 [Infobip 설명서](https://www.infobip.com/docs/api){target="_blank"}를 참조하세요.

   * **[!UICONTROL 옵트인 키워드]**: **[!UICONTROL 옵트인 메시지]**&#x200B;를 자동으로 트리거할 기본 또는 사용자 지정 키워드를 입력하십시오. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오.

   * **[!UICONTROL 옵트인 메시지]**: **[!UICONTROL 옵트인 메시지]**(으)로 자동으로 전송되는 사용자 지정 응답을 입력하십시오.

   * **[!UICONTROL 옵트아웃 키워드]**: **[!UICONTROL 옵트아웃 메시지]**&#x200B;를 자동으로 트리거할 기본 또는 키워드를 입력하십시오. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오.

   * **[!UICONTROL 옵트아웃 메시지]**: **[!UICONTROL 옵트아웃 메시지]**(으)로 자동으로 전송되는 사용자 지정 응답을 입력하십시오.

   * **[!UICONTROL 도움말 키워드]**: **도움말 메시지**&#x200B;를 자동으로 트리거할 기본 키워드 또는 사용자 지정 키워드를 입력하십시오. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오.

   * **[!UICONTROL 도움말 메시지]**: **도움말 메시지**(으)로 자동으로 전송되는 사용자 지정 응답을 입력하십시오.

   * **[!UICONTROL 이중 옵트인 키워드]**: 이중 옵트인 프로세스를 트리거하는 키워드를 입력하십시오. 사용자 프로필이 존재하지 않으면 확인 후 생성됩니다. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오.

   * **[!UICONTROL 이중 옵트인 메시지]**: 이중 옵트인 확인에 대한 응답으로 자동으로 전송되는 사용자 지정 응답을 입력하십시오.

   * **[!UICONTROL 주체 엔터티 ID]**: 할당된 DLT 주체 엔터티 ID를 입력하십시오.

   * **[!UICONTROL 콘텐츠 템플릿 ID]**: 등록된 DLT 콘텐츠 템플릿 ID를 입력하십시오.

   * **[!UICONTROL 유효 기간]**: 메시지 유효 기간을 시간 단위로 입력하십시오. 이 기간 내에 메시지를 게재할 수 없는 경우 시스템에서 다시 전송을 시도합니다. 기본 유효 기간은 48시간으로 설정됩니다.

   * **[!UICONTROL 콜백 데이터]**: Notify URL에서 전송할 추가 클라이언트 데이터를 입력하십시오.

   * **[!UICONTROL 인바운드 번호]**: 고유한 인바운드 번호를 추가합니다. 이를 통해 서로 다른 샌드박스에서 동일한 API 자격 증명을 사용할 수 있으며, 각 샌드박스는 고유한 인바운드 번호를 가지고 있습니다.

   * **[!UICONTROL 사용자 지정 인바운드 키워드]**: 특정 작업(예: DISCOUNT, OFFERS, ENROLL)에 대해 고유한 키워드를 정의합니다. 이러한 키워드는 프로필의 속성으로 캡처 및 저장되므로 여정 내에서 스트리밍 세그먼트 자격을 트리거하고 사용자 지정된 응답 또는 작업을 제공할 수 있습니다.

   * **[!UICONTROL 기본 인바운드 회신 메시지]**: 최종 사용자가 정의된 키워드와 일치하지 않는 인바운드 SMS를 보낼 때 보내는 기본 답변을 입력하십시오.

1. API 자격 증명 구성을 마치면 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

1. **[!UICONTROL API 자격 증명]** 메뉴에서 bin 아이콘을 클릭하여 API 자격 증명을 삭제합니다.

1. 기존 자격 증명을 수정하려면 원하는 API 자격 증명을 찾은 다음 **[!UICONTROL 편집]** 옵션을 클릭하여 필요한 변경을 수행합니다.

API 자격 증명을 만들고 구성한 후에는 SMS 및 MMS 메시지에 대한 채널 구성을 만들어야 합니다. [자세히 알아보기](sms-configuration-surface.md)
