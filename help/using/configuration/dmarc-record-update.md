---
solution: Journey Optimizer
product: journey optimizer
title: 새로운 DMARC 요구 사항 준수
description: Journey Optimizer에서 DMARC 레코드를 설정해야 하는 이유와 시기에 대해 알아봅니다
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 하위 도메인, 도메인, 메일, 도메인, 레코드
source-git-commit: a153960d083cbeab8beca30733832a9df8af9cbc
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 7%

---

# 새로운 DMARC 요구 사항 준수 {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="필수 DMARC 업데이트에 대해 자세히 알아보기"
>abstract="시행 중인 업계 모범 사례의 일부로서 Google과 Yahoo는 모두 다음을 보유해야 합니다. **레코드** (으)로 이메일을 보내는 데 사용하는 모든 도메인의 경우 시작 **2024년 2월 1일**.<br>따라서 Journey Optimizer에서 Adobe에 위임한 모든 하위 도메인에 대해 DMARC 레코드가 설정되어 있는지 확인해야 합니다."

시행 중인 업계 모범 사례의 일부로서 Google과 Yahoo는 모두 다음을 보유해야 합니다. **레코드** (으)로 이메일을 전송하는 데 사용하는 모든 도메인의 경우 이 새 요구 사항은에 시작됩니다. **2024년 2월 1일**.

에서 Google 및 Yahoo 요구 사항에 대해 자세히 알아보십시오. [이 섹션](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>Gmail 및 Yahoo의 이 새로운 요구 사항을 준수하지 않으면 이메일이 스팸 폴더로 도착하거나 차단될 것으로 예상됩니다.

따라서 Adobe은에서 Adobe으로 위임한 모든 하위 도메인에 대해 DMARC 레코드를 설정했는지 확인할 것을 강력히 권장합니다 [!DNL Journey Optimizer]. 사용 사례에 적용되는 아래 단계를 따르십시오.

* 다음을 보유한 경우: [완전히 위임됨](delegate-subdomain.md#full-subdomain-delegation) 하위 도메인을 Adobe으로 보내려면 아래 두 옵션 중 하나를 따르십시오.

   * 위임된 하위 도메인의 상위 도메인에 DMARC 설정 **호스팅 솔루션에서**.

   * 위임된 하위 도메인에서 DMARC 설정 **다음에서 [!DNL Journey Optimizer] 관리 UI** - 호스팅 솔루션에 대한 추가 작업 없음. [방법 알아보기](dmarc-record.md#implement-dmarc)

* 을 사용하여 전송 하위 도메인을 설정한 경우 [CNAME](delegate-subdomain.md#cname-subdomain-delegation)를 클릭하고 아래 두 옵션 중 하나를 수행합니다.
   * 하위 도메인 또는 하위 도메인의 상위 도메인에서 DMARC 설정 **호스팅 솔루션에서**.
   * 위임된 하위 도메인에서 DMARC 설정 **다음에서 [!DNL Journey Optimizer] 관리 UI**. [방법 알아보기](dmarc-record.md#implement-dmarc)

     그러나 CNAME 위임을 사용하면 호스팅 솔루션에 항목을 입력해야 합니다. 따라서 IT 부서가 최대한 빨리 업데이트를 수행할 수 있도록 조율하십시오. [!DNL Journey Optimizer] 기능을 사용할 수 있습니다(1월 30일). [자세히 알아보기](dmarc-record.md#implement-dmarc)

**에 대한 자세한 내용 [!DNL Journey Optimizer] DMARC의 향후 기능은 [이 섹션](dmarc-record.md).**

>[!NOTE]
>
>질문이 있거나 지원이 필요한 경우 Adobe 전달성 컨설턴트 또는 Adobe 담당자에게 문의하십시오.

Google과 Yahoo가 공유하는 가장 최근 타임라인은 다음과 같습니다.

* Google:

   * **2024년 2월** - 규정 미준수를 경고하기 위해 고안된 임시 바운스가 시작됩니다. 아직 규정을 준수하지 않는 경우 짧은 지연 후에도 이메일은 정상적으로 배달됩니다. 완전히 준수하는 경우 일시적인 바운스가 발생하지 않으며 영향을 받지 않습니다.

   * **2024년 4월** - DMARC 요구 사항을 준수하지 않는 발신자에 대한 차단이 시작됩니다. 호환되지 않는 이메일은 일부만 차단되며 차단되는 비율은 시간이 지남에 따라 증가합니다.

   * **2024년 6월 1일** - 규정을 준수하지 않는 모든 발신자는 차단됩니다.

* 야후는 정확한 시행일을 밝히지 않았지만 &quot;시행일이 2024년 2월부터 시작될 것&quot;이라고 말했다. 시행은 점진적으로 이루어질 것이다.&quot;

>[!NOTE]
>
>에서 DMARC 구현에 대해 자세히 알아보기 [전달성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} 이메일 전달성에 미치는 영향을 더 잘 이해할 수 있습니다.
