---
title: 이메일 교정쇄 보내기
description: 이메일 증명을 보내는 방법을 알아봅니다.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: e742c04e-2987-4466-84af-bdaf4d714552
source-git-commit: aa28d13b2ad874e4dc61510bfdc250415e8e8be1
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 16%

---

# 테스트 프로필 데이터를 사용하여 증명 보내기 {#send-proofs}

증명은 메시지를 주 대상자에게 보내기 전에 테스트하기 위해 사용할 수 있는 전용 메시지입니다. 증명의 수신자는 메시지의 렌더링, 내용, 개인화 설정, 구성 등 요소를 승인해야 합니다.

>[!NOTE]
>
>[!DNL Journey optimizer]을(를) 사용하면 CSV/JSON 파일에서 업로드하거나 수동으로 추가한 샘플 입력 데이터를 사용하여 콘텐츠를 미리 보고 증명을 전송하여 다양한 변형을 테스트할 수도 있습니다. [콘텐츠 변형을 시뮬레이션하는 방법을 알아봅니다](../test-approve/simulate-sample-input.md)

테스트 프로필 데이터를 사용하여 전자 메일 증명을 보내려면 먼저 [테스트 프로필](test-profiles.md)을 선택해야 합니다. 그런 다음 다음 다음 단계를 수행합니다.

1. **[!UICONTROL 시뮬레이션]** 화면에서 **[!UICONTROL 증명 보내기]** 단추를 클릭합니다.

   ![](../email/assets/send-proof-button.png)

1. **[!UICONTROL 증명 보내기]** 창에서 받는 사람의 전자 메일을 입력하고 **[!UICONTROL 추가]**&#x200B;를 클릭하여 본인 또는 조직의 구성원에게 증명을 보냅니다.

   증명 게재에 최대 10명의 수신자를 추가할 수 있습니다.

   ![](../email/assets/send-proof-add.png)

1. 메시지 콘텐츠를 개인화하는 데 사용할 **테스트 프로필**&#x200B;을(를) 선택하십시오.

   증명의 각 수신자는 선택한 테스트 프로필 수만큼 메시지를 수신합니다. 예를 들어 5개의 수신자 이메일을 추가하고 10개의 테스트 프로필을 선택한 경우 50개의 증명 메시지를 보내고 각 수신자는 그 중 10개를 받습니다.

1. 필요한 경우 증명의 제목 줄에 접두사를 추가할 수 있습니다. 영숫자와 특수 문자(예: )만 - _ ( ) [ ]은(는) 제목 줄에 접두사로 사용할 수 있습니다.

1. **[!UICONTROL 증명 보내기]**&#x200B;를 클릭합니다.

   ![](../email/assets/send-proof-select.png)

1. **[!UICONTROL 시뮬레이션]** 화면으로 돌아가서 **[!UICONTROL 증명 보기]** 단추를 클릭하여 상태를 확인하세요.

   ![](../email/assets/send-proof-view.png)

메시지 콘텐츠를 수정할 때마다 증명을 보내는 것이 좋습니다.

>[!NOTE]
>
>보낸 증명에서 미러 페이지 링크가 활성화되지 않았습니다. 최종 메시지에서만 활성화됩니다.
