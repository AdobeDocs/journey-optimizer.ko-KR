---
solution: Journey Optimizer
product: journey optimizer
title: 새로운 DMARC 요구 사항 준수
description: Journey Optimizer에서 DMARC 레코드를 설정해야 하는 이유와 시기에 대해 알아봅니다
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: 하위 도메인, 도메인, 메일, DMARC, 레코드
exl-id: 15b10a61-6ecd-4ffa-b1c2-21e862263f6d
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 98%

---

# 새로운 DMARC 요구 사항 준수 {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="필수 DMARC 업데이트에 대해 자세히 알아보기"
>abstract="업계 모범 사례 시행의 일환으로 Google과 Yahoo 모두 **2024년 2월 1일**&#x200B;부터 자사에 이메일을 보내는 데 사용하는 모든 도메인에 대해 **DMARC 레코드**&#x200B;를 보유할 것을 의무화할 예정입니다.<br>따라서 Journey Optimizer에서 Adobe에 위임한 모든 하위 도메인에 대해 DMARC 레코드가 설정되어 있는지 확인해야 합니다."

도메인 기반 메시지 인증, 보고 및 적합성(DMARC)은 도메인 소유자가 도메인을 무단 사용으로부터 보호할 수 있는 이메일 인증 방법입니다. 이메일 공급자/ISP에 명확한 정책을 제공함으로써 악의적인 행위자가 도메인에서 온 것으로 주장하는 이메일을 보내지 못하게 하는 데 도움이 됩니다. DMARC를 구현하면 합법적인 이메일이 스팸으로 표시되거나 거부될 위험이 줄어들고 이메일 전달성이 향상됩니다.

시행 중인 업계 모범 사례의 일부인 Google 및 Yahoo! 의 경우 이메일을 전송하는 데 사용하는 모든 도메인에 **DMARC 레코드**&#x200B;가 필요합니다. 이 새 요구 사항은 **2024년 2월 1일**&#x200B;부터 적용됩니다.

>[!CAUTION]
>
>Gmail 및 Yahoo!의 새로운 요구 사항을 준수하지 못하면 이메일이 스팸 폴더에 포함되거나 차단될 수 있습니다.

따라서 Adobe는 [!DNL Journey Optimizer]에서 Adobe에 위임한 모든 하위 도메인에 대해 DMARC 레코드가 설정되어 있는지 확인하는 것을 강력히 권장합니다. 사용 사례에 적용되는 아래 단계를 따르십시오.

* 하위 도메인 보내기를 Adobe로 [완전히 위임하였다면](delegate-subdomain.md#full-subdomain-delegation) 아래 옵션 중 하나를 따르십시오.

   * **호스팅 솔루션에서** 위임된 하위 도메인의 상위 도메인에 DMARC를 설정합니다.
또는
   * 호스팅 솔루션에 대한 추가 작업 없이 구성 사용자 인터페이스&#x200B;**의[!DNL Journey Optimizer]** 위임된 하위 도메인에서 DMARC를 설정합니다. [방법 알아보기](dmarc-record.md#implement-dmarc)

* [CNAME](delegate-subdomain.md#cname-subdomain-delegation)를 사용하여 하위 도메인 전송을 설정한 경우 아래 옵션 중 하나를 수행합니다.

   * **호스팅 솔루션에서** 하위 도메인에서 또는 하위 도메인의 상위 도메인에서 DMARC를 설정합니다.
또는
   * 구성 사용자 인터페이스&#x200B;**에서[!DNL Journey Optimizer]** 위임된 하위 도메인에 DMARC를 설정합니다. [방법 알아보기](dmarc-record.md#implement-dmarc)

  그러나 CNAME 설정을 사용하려면 호스팅 솔루션에 몇 가지 추가 항목이 필요합니다. 따라서 IT 부서에서 [이 섹션](dmarc-record.md#implement-dmarc)에 설명된 업데이트를 수행할 수 있게 해야 합니다.

<!--The most recent timelines shared by Google and Yahoo! are as follows:

* Google:

    * **February 2024** – Temporary bounces designed to provide warning of non-compliance will begin. Emails will still be delivered as normal after a short delay if you are not yet in compliance. If you are fully in compliance there will be no temporary bounces and you will not be affected.

    * **April 2024** – Blocks will begin for senders who are not in compliance with DMARC requirement. Only a portion of non-compliant email will be blocked at first, with the percentage blocked increasing over time.

    * **June 1st, 2024** – Any sender not in full compliance will experience blocking.

* Yahoo! has not provided exact dates, but has said "the rollout of enforcement will begin in February 2024. Enforcement will be gradually rolled out".
-->

>[!NOTE]
>
>질문이 있거나 지원이 필요한 경우 Adobe 전달성 컨설턴트 또는 Adobe 담당자에게 문의하십시오.

**유용한 링크**

* [전달성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=ko#about){target="_blank"}에서 DMARC에 대해 자세히 알아보기
* [Google Gmail 공지](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"} 읽기
* [Yahoo! 공지](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"} 읽기

<!--Find more guidance about these changes in the [Deliverability Best Practice Guide]-->
