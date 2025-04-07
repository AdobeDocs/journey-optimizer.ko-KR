---
title: 승인 정책 만들기 및 관리
description: 승인 정책을 만들고 관리하는 방법을 알아봅니다.
role: User
level: Beginner
feature: Approval
exl-id: e518cb3c-f361-43a4-b9a5-ec070c612e75
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 13%

---

# 승인 정책 만들기 및 관리 {#approval-policies}


>[!CONTEXTUALHELP]
>id="ajo_approval_policy_request_approval"
>title="승인 요청"
>abstract="승인 요청"

>[!CONTEXTUALHELP]
>id="ajo_approval_policy_request_change"
>title="변경 요청"
>abstract="변경 요청"


>[!NOTE]
>
>승인 정책을 만들려면 Adobe Experience Platform에서 시스템 또는 제품 관리자 권한이 있어야 합니다. [자세히 알아보기](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home)

승인 정책을 사용하면 관리자가 여정 및 캠페인에 대한 유효성 검사 프로세스를 설정할 수 있습니다. 이 시스템은 여정 또는 캠페인에 승인이 필요한지 여부를 결정하는 특정 조건을 간략하게 설명합니다. 이러한 정책은 단순히 모든 캠페인을 특정 사용자 또는 팀이 검토하도록 하는 것에서부터 캠페인을 만든 사람을 기준으로 기준을 설정하는 것까지 복잡성에 따라 달라질 수 있습니다.

## 승인 정책 만들기 {#create-policies}

>[!CONTEXTUALHELP]
>id="ajo_permissions_approval_policy"
>title="새 승인 정책"
>abstract="이 화면에서 승인 정책의 이름을 입력하고 컨텍스트를 선택한 다음, 승인 요청을 실행할 수 있는 사람과 이를 검증할 수 있는 사람을 결정하는 조건을 설정합니다."

승인 정책을 만들려면 다음 단계를 수행합니다.

1. Journey Optimizer의 **[!UICONTROL 관리]** 메뉴에서 **[!UICONTROL 권한]** 및 **[!UICONTROL 정책]**&#x200B;에 액세스합니다.

   ![](assets/policy_create_1.png)

1. **[!UICONTROL 승인 정책]** 탭에서 **[!UICONTROL 만들기]**&#x200B;를 클릭하고 **[!UICONTROL 승인 정책]**&#x200B;을 선택한 다음 **[!UICONTROL 확인]**&#x200B;을 클릭합니다.

1. 정책에 대한 **[!UICONTROL 이름]** 및 **[!UICONTROL 설명]**&#x200B;을 입력하십시오.

1. 정책이 **[!UICONTROL 여정]** 또는 **[!UICONTROL 캠페인]**&#x200B;에 적용되는지 여부를 선택하십시오.

   ![](assets/policy_create_2.png)

이제 조건을 세분화하여 승인 요청을 시작할 수 있는 사용자와 승인 요청을 검증할 수 있는 사용자를 지정할 수 있습니다.

## 승인 정책 조건 설정 {#conditions}

승인 정책과 연관된 조건을 정의하려면 다음 단계를 수행합니다.

1. **[!UICONTROL 승인 정책]**&#x200B;에 액세스합니다.

1. **[!UICONTROL If]** 메뉴에서 **[!UICONTROL 조건 추가]**&#x200B;를 클릭하여 승인 요청을 트리거할 개체 또는 사용자를 정의합니다.

1. 적절한 **[!UICONTROL 범주]**, **[!UICONTROL 일치 규칙]** 및 **[!UICONTROL 옵션]**&#x200B;을 선택하세요.

   예를 들어 &quot;작업이 Dm과 일치하는 경우&quot; 또는 &quot;요청자 사용자 이름이 John Doe와 일치하는 경우&quot;가 있습니다.

   ![](assets/policy_condition_1.png)

+++ 사용 가능한 범주 및 옵션에 대해 자세히 알아보기
   <table>
    <tr>
      <th>카테고리</th>
      <th>옵션</th>
    </tr>
    <tr>
      <td rowspan="3">캠페인 유형</td>
      <td>예약됨(마케팅)</td>
    </tr>
    <tr>
    <td>API 트리거됨(마케팅)</td>
    </tr>
    <tr>
    <td>API 트리거됨(트랜잭션)</td>
    </tr>
    <tr>
    <td rowspan="8">작업</td>
    <td>인앱</td>
    </tr>
    <tr>
    <td>푸시 알림</td>
   </tr>
    <tr>
    <td>SMS</td>
    </tr>
    <tr>
    <td>이메일</td>
    </tr>
    <tr>
    <td>다이렉트 메일</td>
    </tr>
    <tr>
    <td>웹</td>
    </tr>
    <tr>
    <td>코드 기반</td>
    </tr>
    <tr>
    <td>콘텐츠 카드</td>
    </tr>
    <tr>
    <td>태그</td>
    <td>대상을 구성하는 데 사용되는 태그의 이름입니다. </td>
    </tr>
    <tr>
    <td>개체 이름</td>
    <td>개체의 이름입니다.</td>
    </tr>
    <tr>
    <td>요청자 사용자 이름</td>
    <td>설계된 요청자의 이름 및 이메일 주소</td>
    </tr>
    <tr>
    <td>요청자 사용자 그룹</td>
    <td>디자인된 요청자의 사용자 그룹 이름</td>
    </tr>
    </table>


1. 조건을 더 추가하려면 **[!UICONTROL 조건 추가]**&#x200B;를 클릭하여 추가 규칙을 정의하고 **[!UICONTROL And]** 또는 **[!UICONTROL Or]**&#x200B;을(를) 선택하여 조건 연결 방식을 지정하십시오.

1. **[!UICONTROL 그런 다음]** 메뉴에 승인 요청을 보내세요. **[!UICONTROL 조건 추가]**&#x200B;를 클릭하여 승인 요청을 수락할 수 있는 사용자를 정의합니다.

1. **[!UICONTROL 범주]** 드롭다운에서 사용자 그룹을 선택할지 개별 사용자를 선택할지를 선택합니다.

1. 그런 다음 **[!UICONTROL 옵션]** 드롭다운에서 특정 사용자 그룹 또는 사용자를 선택합니다.

   선택한 사용자 또는 사용자 그룹이 승인 요청의 유효성을 검사합니다.

   ![](assets/policy_condition_2.png)

1. 조건을 더 추가하려면 **[!UICONTROL 조건 추가]**&#x200B;를 클릭하여 추가 규칙을 정의하고 **[!UICONTROL And]** 또는 **[!UICONTROL Or]**&#x200B;을(를) 선택하여 조건 연결 방식을 지정하십시오.

1. 정책이 완전히 구성되면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

이제 승인 정책을 활성화하여 적용할 수 있습니다.

## 승인 정책 활성화 및 관리 {#activate-policies}

승인 정책을 적용하려면 승인 정책을 활성화해야 합니다. 이렇게 하려면 다음 단계를 수행합니다.

1. **[!UICONTROL 승인 정책]**&#x200B;에 액세스합니다.

1. **[!UICONTROL 활성화]**&#x200B;를 클릭하여 구성된 조건을 환경에 적용합니다.

   >[!NOTE]
   >
   >활성화되면 정책을 편집할 수 없습니다. 조건을 수정하려면 먼저 정책을 비활성화합니다.

   ![](assets/policy_activate_1.png)

1. **[!UICONTROL 정책]** 메뉴에서 필요에 따라 정책을 **[!UICONTROL 편집]**, **[!UICONTROL 비활성화]** 또는 **[!UICONTROL 복제]**&#x200B;하는 고급 옵션을 엽니다.

   ![](assets/policy_activate_2.png)
