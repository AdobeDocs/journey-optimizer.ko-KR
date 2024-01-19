---
solution: Journey Optimizer
product: journey optimizer
title: 필수 DMARC 업데이트
description: Journey Optimizer에서 DMARC 레코드를 설정해야 하는 이유와 시기에 대해 알아봅니다
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 하위 도메인, 도메인, 메일, 도메인, 레코드
source-git-commit: 7cbd6a9e80a8d6b87b3c3011db80549a3b5f6e73
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# 필수 DMARC 업데이트 {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="필수 DMARC 업데이트에 대한 자세한 내용"
>abstract="시행 중인 업계 모범 사례의 일부로서 Google과 Yahoo는 모두 다음을 보유해야 합니다. **레코드** (으)로 이메일을 전송하는 데 사용하는 모든 도메인의 경우 이 새 요구 사항은에 시작됩니다. **2024년 2월 1일**. <br>따라서 Adobe에서는 Journey Optimizer의 Adobe으로 위임한 모든 하위 도메인에 대해 DMARC 레코드를 설정했는지 확인할 것을 강력히 권장합니다."

시행 중인 업계 모범 사례의 일부로서 Google과 Yahoo는 모두 다음을 보유해야 합니다. **레코드** (으)로 이메일을 전송하는 데 사용하는 모든 도메인의 경우 이 새 요구 사항은에 시작됩니다. **2024년 2월 1일**.

에서 Google 및 Yahoo 요구 사항에 대해 자세히 알아보십시오. [이 섹션](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>Gmail 및 Yahoo의 이 새로운 요구 사항을 준수하지 않으면 이메일이 스팸 폴더로 도착하거나 차단될 것으로 예상됩니다.

따라서 Adobe은에서 Adobe으로 위임한 모든 하위 도메인에 대해 DMARC 레코드를 설정했는지 확인할 것을 강력히 권장합니다 [!DNL Journey Optimizer]. 아래 두 옵션 중 하나를 따르십시오.

* 하위 도메인 또는 하위 도메인의 상위 도메인에서 DMARC를 설정합니다. **호스팅 솔루션에서**.

* 위임된 하위 도메인에서 DMARC 설정 **에서 예정된 기능 사용 [!DNL Journey Optimizer] 관리 UI** - 호스팅 솔루션에 대한 추가 작업 없음.

  >[!CAUTION]
  >
  >을 설정한 경우 [CNAME 위임](delegate-subdomain.md#cname-subdomain-delegation) 보내는 하위 도메인의 경우 호스팅 솔루션에도 일부 항목이 필요합니다. 최대한 빨리 업데이트를 수행할 수 있도록 IT 부서와 협력해야 합니다. [!DNL Journey Optimizer] 기능을 사용할 수 있습니다(2024년 1월 30일). <!--and be ready on February 1st, 2024-->

  에 대한 자세한 내용 [!DNL Journey Optimizer] 곧 DMARC 예정된 기능이 제공될 예정입니다.

<!--
* If you have [fully delegated](delegate-subdomain.md#full-subdomain-delegation) your sending subdomains to Adobe, follow either one of the two options below:

    * Set up DMARC on your subdomains or on the parent domain of your subdomains **in your hosting solution**.

    * Set up DMARC on your delegated subdomains **using the upcoming feature in the [!DNL Journey Optimizer] administration UI** - with no extra work on your hosting solution.

* If you have set up [CNAME delegation](delegate-subdomain.md#cname-subdomain-delegation) for your sending subdomains, follow either one of the two options below:
    * Set up DMARC on your subdomains or on the parent domain of your subdomains **in your hosting solution**.
    * Set up DMARC on your delegated subdomains **using the upcoming feature in the [!DNL Journey Optimizer] administration UI**. However, it will also require entry in your hosting solution. Consequently, make sure you coordinate with your IT department so that they can perform the update as soon as the [!DNL Journey Optimizer] feature is available (on January, 30) - and be ready on February 1st, 2024.
    
-->

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
