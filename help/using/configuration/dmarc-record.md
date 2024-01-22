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
source-git-commit: 7d5a2a9b80110505688b5bfda2e286c7a6432441
workflow-type: tm+mt
source-wordcount: '905'
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

따라서 Adobe은에서 Adobe으로 위임한 모든 하위 도메인에 대해 DMARC 레코드를 설정했는지 확인할 것을 강력히 권장합니다 [!DNL Journey Optimizer]. 사용 사례에 적용되는 아래 단계를 따르십시오.

* 다음을 보유한 경우: [완전히 위임됨](delegate-subdomain.md#full-subdomain-delegation) 하위 도메인을 Adobe으로 보내려면 아래 두 옵션 중 하나를 따르십시오.

   * 위임된 하위 도메인의 상위 도메인에 DMARC 설정 **호스팅 솔루션에서**.

   * 위임된 하위 도메인에서 DMARC 설정 **에서 예정된 기능 사용 [!DNL Journey Optimizer] 관리 UI** - 호스팅 솔루션에 대한 추가 작업 없음.

* 을 설정한 경우 [CNAME 위임](delegate-subdomain.md#cname-subdomain-delegation) 보내는 하위 도메인의 경우 아래 두 옵션 중 하나를 따르십시오.

   * 하위 도메인 또는 하위 도메인의 상위 도메인에서 DMARC 설정 **호스팅 솔루션에서**.

   * 위임된 하위 도메인에서 DMARC 설정 **에서 예정된 기능 사용 [!DNL Journey Optimizer] 관리 UI**. 그러나 호스팅 솔루션에도 입력해야 합니다. 따라서 IT 부서가 최대한 빨리 업데이트를 수행할 수 있도록 조율하십시오. [!DNL Journey Optimizer] 기능을 사용할 수 있습니다(1월 30일). <!--and be ready on February 1st, 2024-->

**에 대한 자세한 내용 [!DNL Journey Optimizer] 곧 DMARC 예정된 기능이 제공될 예정입니다.**

>[!NOTE]
>
>에서 DMARC 구현에 대해 자세히 알아보기 [전달성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} 이메일 전달성에 미치는 영향을 더 잘 이해할 수 있습니다.

## DMARC란?

DMARC는 **도메인 기반 메시지 인증, 보고 및 적합성**&#x200B;는 도메인 소유자가 도메인을 무단 사용으로부터 보호할 수 있는 이메일 인증 방법/프로토콜입니다.

발신자의 도메인을 인증하는 방법을 제공하면 악의적인 행위자가 도메인에서 온 것처럼 보이는 이메일을 보내지 못하게 하는 데 도움이 됩니다.

또한 DMARC는 이메일 인증 상태에 대한 피드백을 제공하며 발신자가 인증에 실패한 이메일에 발생하는 일을 제어할 수 있습니다. 여기에는 구현된 DMARC 정책에 따라 메일을 모니터링, 격리 또는 거부하는 옵션이 포함됩니다.

<!--Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.-->

DMARC에는 세 가지 정책 옵션이 있습니다.

* Monitor (p=none): 사서함 공급자/ISP가 메시지에 대해 일반적으로 수행하는 작업을 수행하도록 지시합니다.
* 격리(p=격리): 사서함 공급자/ISP에 DMARC를 전달하지 않는 메일을 받는 사람의 스팸 또는 정크 폴더로 배달하도록 지시합니다.
* 거부(p=reject): 사서함 공급자/ISP가 DMARC를 전달하지 않아 바운스가 발생하는 메일을 차단하도록 지시합니다.

## DMARC는 어떻게 작동합니까?

SPF와 DKIM은 둘 다 이메일을 도메인과 연결하고 이메일을 인증하기 위해 함께 작업하는 데 사용됩니다. DMARC는 이 단계를 한 단계 더 발전시켰으며 DKIM과 SPF로 확인된 도메인을 일치시켜 스푸핑을 방지하는 데 도움이 됩니다. DMARC를 전달하려면 메시지가 SPF 또는 DKIM을 전달해야 합니다. 이 두 가지 인증이 모두 실패하면 DMARC가 실패하고 선택한 DMARC 정책에 따라 이메일이 전달됩니다.

* SPF(Sender Policy Framework): DMARC는 SPF를 사용하여 보내는 메일 서버의 ID를 인증합니다. SPF는 도메인에 대해 승인된 IP 주소 목록에 대해 전송 서버의 IP 주소를 확인하여 승인된 소스에서 이메일 메시지가 왔는지 확인하는 데 도움이 됩니다.
* DKIM(DomainKeys Identified Mail): DMARC는 또한 DKIM을 사용하여 이메일 메시지에 디지털 서명을 추가하여 수신자가 메시지의 무결성과 신뢰성을 확인할 수 있도록 합니다.

>[!NOTE]
>
>DMARC를 사용하려면 &#39;보낸 사람&#39; 주소와 &#39;반환 경로&#39; 주소 간에 정렬해야 합니다.


<!--

* DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

* DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

DMARC helps protect against email spoofing, phishing, and other fraudulent activities.

It allows you to decide how a mailbox provider should handle emails that fail SPF and DKIM checks, providing a way to authenticate the sender's domain and prevent unauthorized use of the domain for malicious purposes.

-->


## DMARC 구현 {#implement-dmarc}

DMARC를 구현하려면 사용 사례에 적용되는 아래 단계를 따르십시오.

* DMARC를 추가하지 않으면 격리됩니다(최소).

### 완전히 위임된 하위 도메인

DMARC가 실패할 경우 수신자 서버가 수행할 작업을 설정합니다.

DMARC에는 세 가지 정책 옵션이 있습니다.

* Monitor (p=none): 사서함 공급자/ISP가 메시지에 대해 일반적으로 수행하는 작업을 수행하도록 지시합니다. 이 값은 기본값입니다.
* 격리(p=격리): 사서함 공급자/ISP에 DMARC를 전달하지 않는 메일을 받는 사람의 스팸 또는 정크 폴더로 배달하도록 지시합니다.
* 거부(p=reject): 사서함 공급자/ISP가 DMARC를 전달하지 않아 바운스가 발생하는 메일을 차단하도록 지시합니다.

집계 DMARC 보고서 및 포렌식 DMARC 오류 보고서를 수신하기 위한 이메일: 최대 5개의 주소를 추가할 수 있습니다.

* 제어에서 수신할 수 있는 정품 받은 편지함이 있는지 확인합니다. 이 받은 편지함을 관리하면 됩니다(Adobe 받은 편지함이 아니어야 함).

DMARC를 적용할 이메일의 해당 비율:

보고 간격: 일반적으로 ISP에는 이것이 있으므로 권장 사항은 24입니다.
부족할 경우 용량을 평가하거나 > 채팅 GPT를 확인하십시오.

DMARC 레코드가 감지되면 나열된 값과 동일한 값을 복사하여 붙여넣거나 필요한 경우 변경할 수 있습니다.

아무 것도 입력하지 않으면 기본값이 사용됩니다.

### CNAME을 사용하여 위임된 하위 도메인

에디션 플로우의 CNAME의 경우 CSV 파일을 다시 다운로드해야 합니다(완전히 위임되지 않은 경우)





