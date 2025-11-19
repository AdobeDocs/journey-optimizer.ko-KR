---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 검토 및 활성화
description: Journey Optimizer에서 캠페인을 검토하고 활성화하는 방법에 대해 알아봅니다
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: 캠페인, 검토, 유효성 검사, 활성화, 활성화, 최적화
exl-id: 86f35987-f0b7-406e-9ae6-0e4a2e651610
source-git-commit: 8cb37cf0fb9dc8048d7da8ddda0c67280477d57f
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 1%

---


# API에서 트리거된 캠페인 실행 {#execute}

캠페인이 활성화되면 생성된 샘플 cURL 요청을 검색하고 API에 사용하여 페이로드를 빌드하고 캠페인을 트리거해야 합니다.

## 반드시 알아야 할 사항 {#must-read}

* **캠페인 시작/종료 날짜** - 캠페인을 만들 때 특정 시작 및/또는 종료 날짜를 구성한 경우 이 날짜 이후에 실행되지 않으며 API 호출이 실패합니다.

* **호출 시간 제한** - 대화형 메시지 실행 REST API에 대한 호출의 시간 제한이 60초입니다. 그러나 게재를 보장하기 위해 예기치 않은 시간 초과가 발생하는 경우 내부 재시도가 수행됩니다.

## 캠페인 트리거 {#trigger}

1. 캠페인을 연 다음 **[!UICONTROL cURL 요청]** 섹션에서 페이로드 요청을 복사하여 붙여 넣으십시오. 이 페이로드에는 메시지에 사용된 모든 개인화(프로필 및 컨텍스트) 변수가 포함됩니다. 캠페인이 라이브되면 사용할 수 있습니다.

   ![](assets/api-triggered-curl.png)

   >[!IMPORTANT]
   >
   >cURL 섹션의 끝점은 표준 및 [높은 처리량 캠페인](../campaigns/api-triggered-high-throughput.md)마다 다릅니다.

1. 이 cURL 요청을 API에 사용하여 페이로드를 빌드하고 캠페인을 트리거합니다. 자세한 내용은 [대화형 메시지 실행 API 설명서](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution)를 참조하세요. 여기서 표준 및 높은 처리량 캠페인의 모든 끝점이 나열됩니다.

   API 호출 예는 [이 페이지](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/)에서도 사용할 수 있습니다.

## 문제 해결 {#troubleshooting}

### Azure Cosmos DB 인증 오류(500 내부 서버 오류) {#cosmosdb-auth-errors}

API 트리거 캠페인을 트리거할 때 **500개의 내부 서버 오류가 발생하고 시스템 로그에 다음과 같은 메시지와 함께 Azure Cosmos DB의** 403 금지됨&#x200B;**오류가 표시됩니다.**

_&quot;Azure Cosmos DB 서비스가 계정의 기본 ID에 대한 AAD 인증 토큰을 가져올 수 없기 때문에 계정에 대한 액세스가 현재 취소되었습니다.&quot;_

이 오류는 일반적으로 Cosmos DB 인증에 필요한 Azure 서비스 사용자가 비활성화, 삭제 또는 잘못 구성된 경우 발생합니다.

+++이 문제를 해결하는 방법

1. **Azure 서비스 사용자 확인** - Azure 서비스 사용자 또는 관리되는 ID가 사용하도록 설정되어 있고 Azure Active Directory에서 사용하지 않도록 설정되거나 삭제되지 않았는지 확인하세요.

1. **권한 확인** - 서비스 주체가 Azure Key Vault 및 Cosmos DB 리소스에 액세스하는 데 필요한 권한이 있는지 확인합니다. 서비스 주체가 Azure Cosmos DB를 인증하려면 적절한 역할 할당이 있어야 합니다.

1. **Azure Cosmos DB CMK 구성 검토** - CMK(Customer-Managed Key)를 사용하는 경우 [Azure Cosmos DB CMK 문제 해결 안내서](https://learn.microsoft.com/en-us/azure/cosmos-db/cmk-troubleshooting-guide#azure-active-directory-token-acquisition-error){target="_blank"}에서 AAD 토큰 획득을 복원하는 자세한 단계를 참조하세요.

1. **다시 사용 및 테스트** - 구성을 수정한 후 서비스 주체가 사용하지 않도록 설정된 경우 다시 사용하도록 설정하고 트랜잭션 캠페인 API 호출을 다시 테스트하여 인증이 성공하고 메시지가 전달되는지 확인합니다.

>[!NOTE]
>
>이 문제는 일반적으로 Cosmos DB 인증에 필요한 Azure 서비스 사용자를 잘못 구성하거나 실수로 비활성화하여 발생합니다. 서비스 주체를 활성화하고 올바르게 구성하면 나중에 이 오류가 발생하지 않습니다.

+++
