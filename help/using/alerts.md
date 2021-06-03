---
title: 메시지의 경고
description: 메시지 콘텐츠 유효성 검사 및 문제 해결 방법을 알아봅니다
source-git-commit: 627ffade10a420c6dea7377f6e39360abad44f32
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# 메시지에 대한 경고 {#publish-manage-messages}

![](assets/do-not-localize/badge.png)

## 게시 전 확인 {#message-alerting}

메시지를 만드는 동안 메시지를 게시하기 전에 중요한 작업을 수행해야 할 때 경고 메시지가 표시됩니다.

경고는 아래와 같이 화면 오른쪽 상단에 표시됩니다.

![](assets/message-alerts.png)

>[!NOTE]
>
>이 단추가 표시되지 않으면 경고가 감지되지 않습니다.

다음 두 가지 유형의 경고가 발생할 수 있습니다.

* **** 경고: 권장 사항 및 우수 사례를 참조하십시오. 예를 들어 옵트아웃 링크가 누락된 경우 메시지가 표시됩니다.

* **** 메시지가 해결되지 않는 한 메시지를 게시할 수 없습니다. 예를 들어 제목 줄이 누락되었다는 메시지가 표시됩니다.

가능한 모든 경고 및 오류는 [아래에 자세히 표시됩니다](#alerts-and-warnings).

>[!CAUTION]
>
> 게시하기 전에 모든 **오류** 경고를 해결해야 합니다.

## 경고 및 오류 목록 {#alerts-and-warnings}

시스템에서 선택한 설정 및 요소는 아래에 나와 있습니다. 또한 구성을 조정하여 해당 문제를 해결하는 방법에 대한 정보도 확인할 수 있습니다.

**경고**:

* **[!UICONTROL Opt out link not present in the email body]**:이메일 본문에 구독 취소 링크를 추가하는 것이 가장 좋습니다. [이 섹션](consent.md)에서 구성하는 방법을 알아봅니다.

* **[!UICONTROL Text version of html is empty]**:HTML 콘텐츠를 표시할 수 없을 때 사용되므로 이메일 본문의 텍스트 버전을 정의하는 것을 잊지 마십시오. [이 섹션](create-email-content.md#generate-text-version)에서 텍스트 버전을 만드는 방법을 알아봅니다.

* **[!UICONTROL Empty link is present in email body]**:이메일의 모든 링크가 올바른지 확인합니다. [이 섹션](create-email-content.md)에서 컨텐츠 및 링크를 관리하는 방법을 알아봅니다.

* **[!UICONTROL Email size has exceeded the limit of 100KB]**:최적의 전달을 위해 이메일 크기가 100KB를 초과하지 않도록 하십시오. [이 섹션](create-email-content.md)에서 전자 메일 콘텐츠를 편집하는 방법을 알아봅니다.

**오류**:

* **[!UICONTROL Subject Line Not Present]**:이메일 제목란은 필수입니다. [이 섹션](create-email.md)에서 정의하고 개인화하는 방법을 알아봅니다.

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL Push Variant is empty]**:이 오류는 푸시 알림 본문 또는 제목이 누락된 경우 표시됩니다. [이 섹션](create-push.md)에서 푸시 알림 콘텐츠를 정의하는 방법을 알아봅니다.

* **[!UICONTROL Email Variant is empty]**:이 오류는 이메일 컨텐츠가 구성되지 않은 경우 표시됩니다. [이 섹션](design-emails.md)에서 전자 메일 콘텐츠를 디자인하는 방법을 배웁니다.

* **[!UICONTROL Preset doesn’t exist]**:선택한 사전 설정이 메시지를 만든 후 삭제되면 메시지를 게시할 수 없습니다. 이 오류가 발생하면 메시지 **[!UICONTROL Properties]**&#x200B;에서 다른 사전 설정을 선택합니다. [이 섹션](configuration/about-subdomain-delegation.md)의 브랜딩에 대해 자세히 알아보십시오.

* **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB]**:푸시 알림 크기는 4KB를 초과할 수 없습니다. 이 제한을 준수하려면 이미지나 이모지의 사용을 줄이십시오. [이 섹션](create-push.md)에서 푸시 알림 콘텐츠를 관리하는 방법을 알아봅니다.

>[!CAUTION]
>
> 메시지를 게시하려면 모든 **error** 경고를 해결해야 합니다.

<!--Other issues can stop publication such as:
* The push notification title is empty-->
