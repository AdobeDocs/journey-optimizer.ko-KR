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
source-git-commit: f59f6a60aabb793aec0cb813ddd9cee10c0fc097
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 87%

---

# 새로운 DMARC 요구 사항 준수 {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="필수 DMARC 업데이트에 대해 자세히 알아보기"
>abstract="업계 모범 사례 시행의 일환으로, Google과 Yahoo 모두 **2024년 2월 1일**&#x200B;부터 자사에 이메일을 보내는 데 사용하는 모든 도메인에 대해 **DMARC 레코드**&#x200B;를 보유할 것을 의무화할 예정입니다.<br>따라서 Journey Optimizer에서 Adobe에 위임한 모든 하위 도메인에 대해 DMARC 레코드가 설정되어 있는지 확인해야 합니다."

도메인 기반 메시지 인증, 보고 및 적합성(DMARC)은 도메인 소유자가 도메인을 무단 사용으로부터 보호할 수 있는 이메일 인증 방법입니다. 이메일 공급자/ISP에 명확한 정책을 제공함으로써 악의적인 행위자가 도메인에서 온 것으로 주장하는 이메일을 보내지 못하게 하는 데 도움이 됩니다. DMARC를 구현하면 합법적인 이메일이 스팸으로 표시되거나 거부될 위험이 줄어들고 이메일 전달성이 향상됩니다.

시행 중인 업계 모범 사례의 일부인 Google 및 Yahoo! 둘 다 **레코드** (으)로 이메일을 전송하는 데 사용하는 모든 도메인의 경우 이 새 요구 사항은 **2024년 2월 1일**&#x200B;부터 적용됩니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=ko#dmarc){target="_blank"}

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

  >[!IMPORTANT]
  >
  >그러나 CNAME 설정을 사용하려면 호스팅 솔루션에 몇 가지 추가 항목이 필요합니다. 따라서 IT 부서에서 [이 섹션](dmarc-record.md#implement-dmarc)에 설명된 업데이트를 수행할 수 있게 해야 합니다. .

Google과 Yahoo!에서 공유한 가장 최근 타임라인 은 다음과 같습니다.

* Google:

   * **2024년 2월** - 규정 미준수를 경고하기 위해 고안된 임시 바운스가 시작됩니다. 아직 규정을 준수하지 않는 경우 짧은 지연 후에도 이메일은 정상적으로 배달됩니다. 완전히 준수하는 경우 일시적인 바운스가 발생하지 않으며 영향을 받지 않습니다.

   * **2024년 4월** - DMARC 요구 사항을 준수하지 않는 발신자에 대한 차단이 시작됩니다. 호환되지 않는 이메일은 일부만 차단되며 차단되는 비율은 시간이 지남에 따라 증가합니다.

   * **2024년 6월 1일** - 규정을 준수하지 않는 모든 발신자는 차단됩니다.

* 야후! 는 정확한 날짜는 밝히지 않았지만 &quot;2024년 2월부터 강제집행이 시작될 것&quot;이라고 말했다. 시행은 점진적으로 이루어질 것입니다”라고 했습니다.

>[!NOTE]
>
>질문이 있거나 지원이 필요한 경우 Adobe 전달성 컨설턴트 또는 Adobe 담당자에게 문의하십시오.

**유용한 링크**

* [전달성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=ko#about){target="_blank"}에서 DMARC에 대해 자세히 알아보기
* [전달성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=ko){target="_blank"}에서 이러한 변경 사항에 대한 추가 지침을 확인하십시오.
* 다음을 읽어 보십시오. [Google Gmail 공지](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}
* 다음을 읽어 보십시오. [야후! 공지](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"} 참조
