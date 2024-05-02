---
solution: Journey Optimizer
product: journey optimizer
title: Infobip 공급자 구성
description: Infobip을 사용하여 Journey Optimizer으로 문자 메시지 및 MMS를 전송하도록 환경을 구성하는 방법에 대해 알아봅니다
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 4%

---

# Infobip 공급자 구성 {#sms-configuration-infobip}

Journey Optimizer을 사용하여 Infobip을 구성하려면 다음 단계를 수행합니다.

1. 왼쪽 레일에서 다음을 찾습니다. **[!UICONTROL 관리]** `>` **[!UICONTROL 채널]** 및 선택 **[!UICONTROL API 자격 증명]** 메뉴 아래의 제품에서 사용할 수 있습니다. 다음을 클릭합니다. **[!UICONTROL 새 API 자격 증명 만들기]** 단추를 클릭합니다.

   ![](assets/sms_6.png)

1. 아래 설명된 대로 API 자격 증명을 구성합니다.

   * **[!UICONTROL 이름]**: API 자격 증명의 이름을 선택합니다.

   * **[!UICONTROL API 기본 URL]** 및 **[!UICONTROL API 키]**: 웹 인터페이스 홈 페이지 또는 API 키 관리 페이지에 액세스하여 자격 증명을 찾을 수 있습니다. 다음에서 자세히 알아보기 [Infobip 설명서](https://www.infobip.com/docs/api){target="_blank"}.

   * **[!UICONTROL 옵트인 키워드]**: 를 자동으로 트리거할 기본 또는 사용자 지정 키워드를 입력합니다. **[!UICONTROL 옵트인 메시지]**. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오.

   * **[!UICONTROL 옵트인 메시지]**: (으)로 자동으로 전송되는 사용자 지정 응답을 입력합니다. **[!UICONTROL 옵트인 메시지]**.

   * **[!UICONTROL 옵트아웃 키워드]**: 를 자동으로 트리거할 기본 또는 키워드를 입력합니다. **[!UICONTROL 옵트아웃 메시지]**. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오.

   * **[!UICONTROL 옵트아웃 메시지]**: (으)로 자동으로 전송되는 사용자 지정 응답을 입력합니다. **[!UICONTROL 옵트아웃 메시지]**.

   * **[!UICONTROL 도움말 키워드]**: 를 자동으로 트리거할 기본 또는 사용자 지정 키워드를 입력합니다. **도움말 메시지**. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오.

   * **[!UICONTROL 도움말 메시지]**: (으)로 자동으로 전송되는 사용자 지정 응답을 입력합니다. **도움말 메시지**.

   * **[!UICONTROL 이중 옵트인 키워드]**: 이중 옵트인 프로세스를 트리거하는 키워드를 입력합니다. 사용자 프로필이 존재하지 않으면 확인 후 생성됩니다. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오.

   * **[!UICONTROL 이중 옵트인 메시지]**: 이중 옵트인 확인에 응답하여 자동으로 전송되는 사용자 지정 응답을 입력합니다.

   * **[!UICONTROL 주체 엔티티 ID]**: 할당된 DLT 주체 엔티티 ID를 입력합니다.

   * **[!UICONTROL 컨텐츠 템플릿 ID]**: 등록된 DLT 콘텐츠 템플릿 ID를 입력합니다.

   * **[!UICONTROL 유효 기간]**: 메시지 유효 기간을 시간 단위로 입력합니다. 이 기간 내에 메시지를 게재할 수 없는 경우 시스템에서 다시 전송을 시도합니다. 기본 유효 기간은 48시간으로 설정됩니다.

   * **[!UICONTROL 콜백 데이터]**: 알림 URL에 전송할 추가 클라이언트 데이터를 입력합니다.

1. 클릭 **[!UICONTROL 제출]** api 자격 증명 구성을 완료한 경우입니다.

API 자격 증명을 만들고 구성한 후에는 SMS 및 MMS 메시지에 대한 채널 표면을 만들어야 합니다. [자세히 알아보기](sms-configuration-surface.md)
