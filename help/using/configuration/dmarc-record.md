---
solution: Journey Optimizer
product: journey optimizer
title: 레코드
description: Journey Optimizer에서 DMARC 레코드를 설정하는 방법 알아보기
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 하위 도메인, 도메인, 메일, 도메인, 레코드
source-git-commit: f9d3234a64ad659660c2d2c4ad24ab5c240cb857
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# 레코드 {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="DMARC 레코드 설정"
>abstract="ISP의 전달성 문제를 방지하려면 DMARC 레코드를 설정하십시오. 시행 업계 모범 사례의 일부로서, Google과 Yahoo는 모두 이메일을 보내는 데 사용하는 도메인에 대한 DMARC 레코드가 있어야 합니다."

>[!CAUTION]
>
>대량 발신자에 대한 최근 Gmail 및 Yahoo 공지에 이어 이제 Journey Optimizer에서 DMARC 인증 기술을 지원합니다.

<!--TO ADD TO AJO HOME PAGE (first tab)

>[!TAB Mandatory DMARC update]

As part of their enforcing industry best practices, Google and Yahoo will both be requiring that you have a DMARC record for any domain you use to send email to them, starting on **February 1st, 2024**. Make sure that you have DMARC record set up for all the subdomains that you have delegated to Adobe in Journey Optimizer.

[![image](using/assets/do-not-localize/learn-more-button.svg)](using/configuration/dmarc-record-update.md)
-->

시행 중인 업계 모범 사례의 일부로서 Google과 Yahoo는 모두 다음을 보유해야 합니다. **레코드** (으)로 이메일을 전송하는 데 사용하는 모든 도메인의 경우 이 새 요구 사항은에 시작됩니다. **2024년 2월 1일**.

에서 Google 및 Yahoo 요구 사항에 대해 자세히 알아보십시오. [이 섹션](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>Gmail 및 Yahoo의 이 새로운 요구 사항을 준수하지 않으면 이메일이 스팸 폴더로 도착하거나 차단될 것으로 예상됩니다.

따라서 Adobe은에서 Adobe으로 위임한 모든 하위 도메인에 대해 DMARC 레코드를 설정했는지 확인할 것을 강력히 권장합니다 [!DNL Journey Optimizer]. 아래 두 옵션 중 하나를 따르십시오.

* 하위 도메인 또는 하위 도메인의 상위 도메인에서 DMARC를 설정합니다. **호스팅 솔루션에서**.

* 위임된 하위 도메인에서 DMARC 설정 **의 새 기능 사용 [!DNL Journey Optimizer] 관리 UI** - 호스팅 솔루션에 대한 추가 작업 없음. [자세히 알아보기](#implement-dmarc)

  >[!CAUTION]
  >
  >을 설정한 경우 [CNAME 위임](delegate-subdomain.md#cname-subdomain-delegation) 보내는 하위 도메인의 경우 호스팅 솔루션에도 일부 항목이 필요합니다. 최대한 빨리 업데이트를 수행할 수 있도록 IT 부서와 협력해야 합니다. [!DNL Journey Optimizer] 기능을 사용할 수 있습니다(2024년 1월 30일). <!--and be ready on February 1st, 2024-->

>[!NOTE]
>
>에서 DMARC 구현에 대해 자세히 알아보기 [전달성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} 이메일 전달성에 미치는 영향을 더 잘 이해할 수 있습니다.

## DMARC란?

DMARC는 **도메인 기반 메시지 인증, 보고 및 적합성**&#x200B;는 이메일 스푸핑, 피싱 및 기타 사기 행위로부터 보호하는 이메일 인증 프로토콜입니다.

* 전자 메일 인증:

   * SPF(Sender Policy Framework): DMARC는 SPF를 사용하여 보내는 메일 서버의 ID를 인증합니다. SPF는 도메인에 대해 승인된 IP 주소 목록에 대해 전송 서버의 IP 주소를 확인하여 승인된 소스에서 이메일 메시지가 왔는지 확인하는 데 도움이 됩니다.
   * DKIM(DomainKeys Identified Mail): DMARC는 또한 DKIM을 사용하여 이메일 메시지에 디지털 서명을 추가하여 수신자가 메시지의 무결성과 신뢰성을 확인할 수 있도록 합니다.

* DMARC는 악의적인 행위자가 도메인에서 온 것처럼 보이는 이메일을 보내지 못하게 합니다. DMARC를 설정하면 이메일 공급자가 인증 검사에 실패한 메시지를 처리하는 방법을 지정할 수 있으므로 피싱 이메일이 수신자에게 도달할 가능성을 줄일 수 있습니다.

* DMARC는 도메인에서 온 것으로 주장하는 메시지가 발생할 때 이메일 공급자가 따라야 하는 명확한 정책을 제공하여 이메일 전달성을 향상시킵니다. 이렇게 하면 합법적인 이메일이 스팸으로 표시되거나 거부될 가능성을 줄일 수 있습니다.

* DMARC를 구현하면 승인되지 않은 당사자가 피싱 또는 기타 악의적인 활동에 대해 도메인을 남용할 수 없도록 하여 브랜드 평판을 보호할 수 있습니다. 이는 고객 및 파트너와의 이메일 커뮤니케이션에 의존하는 기업 및 조직에 특히 중요합니다.

DMARC 레코드 설정에는 도메인의 DNS 설정에 DNS TXT 레코드를 추가하는 작업이 포함됩니다. 이 레코드는 인증에 실패한 메시지를 격리할지 또는 거부할지 여부와 같이 DMARC 정책을 지정합니다. DMARC 구현은 이메일 보안을 강화하고 이메일 기반 위협으로부터 조직과 수신자 모두를 보호하기 위한 사전 예방적 단계입니다.

## DMARC 구현 {#implement-dmarc}

* DMARC를 추가하지 않으면 격리됩니다(최소).

* 제어에서 수신할 수 있는 정품 받은 편지함이 있는지 확인합니다. 이 받은 편지함을 관리하면 됩니다(Adobe 받은 편지함이 아니어야 함).

일반적으로 ISP에는 이것이 있으므로 권장 사항은 24입니다.
부족할 경우 용량을 평가하거나 > 채팅 GPT를 확인하십시오.

DMARC 레코드가 감지되면 나열된 값과 동일한 값을 복사하여 붙여넣거나 필요한 경우 변경할 수 있습니다.

아무 것도 입력하지 않으면 기본값이 사용됩니다.

### 완전히 위임된 하위 도메인

### CNAME을 사용하여 위임된 하위 도메인

에디션 플로우의 CNAME의 경우 CSV 파일을 다시 다운로드해야 합니다(완전히 위임되지 않은 경우)





