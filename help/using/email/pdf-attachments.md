---
solution: Journey Optimizer
product: journey optimizer
title: 이메일에 PDF 파일 첨부
description: 이메일에 정적 또는 개인화된 PDF 파일을 첨부하는 방법을 알아봅니다
feature: Email Design
topic: Content Management
role: User
level: Beginner
keywords: 이메일, 메시지, 첨부 파일, pdf, 편집기, 개인화된, API 트리거된
exl-id: 71e218d0-5b3b-4db5-8b7b-d08df8f088c4
TQID: https://experienceleague.adobe.com/9IgYERskcUrIAhTb3xlNgWTRyY-04O58ZB8I0lYFh4g
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: ee5bb250-0884-4d71-86eb-d8489e8bcaddid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: c1270581f5184ca1f5375a2838dfb2906805a259
workflow-type: tm+mt
source-wordcount: 916
ht-degree: 11%

---

# 이메일에 PDF 파일 첨부 {#pdf-attachments}

>[!BEGINSHADEBOX]

**이 페이지에서:** 지원되는 캠페인 유형, 적용 가능한 개수, 크기 및 볼륨 제한을 포함하여 정적 또는 개인화된 PDF 파일을 전자 메일에 첨부하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_pdf_attachments"
>title="PDF 첨부 파일 추가"
>abstract="이메일에 첨부할 PDF 파일을 찾아 선택합니다.</br>매년 프로필별로 PDF 첨부 파일이 포함된 최대 6개의 메시지를 보낼 수 있습니다. 각 첨부 파일의 최대 크기는 5MB입니다.</br>크기나 볼륨이 더 필요하다면 PDF 첨부 파일 추가 기능을 구매할 수 있습니다. 자세한 내용은 Adobe 담당자에게 문의하십시오."

[!DNL Journey Optimizer]&#x200B;(으)로 보내는 전자 메일 메시지에 정적 PDF 파일을 첨부할 수 있습니다. [API 트리거 캠페인](../campaigns/api-triggered-campaigns.md)을 사용하는 경우 각 수신자에 대해 [개인화된 PDF 파일을 첨부](#personalized-attachments)할 수도 있습니다.

개인화된 PDF 첨부 파일은 추가 검색 및 처리가 필요합니다. 특히 여러 개 이상의 PDF 파일을 사용하는 경우 이를 사용하는 캠페인은 첨부 파일이 없는 캠페인보다 처리 지연 시간이 길고 처리량이 적을 수 있습니다.

>[!IMPORTANT]
>
>* 프로필당 연간 최대 6개의 PDF 첨부 파일이 있는 메시지를 보낼 수 있습니다(첨부 파일이 정적인지 또는 개인화되었는지 여부).
>
>* 각 첨부 파일의 최대 크기는 5MB입니다. [개인 맞춤화된 첨부 파일](#personalized-attachments)이 있는 전자 메일의 경우 전자 메일의 모든 정적 및 개인 맞춤화된 PDF 첨부 파일은 기본적으로 총 5MB 제한을 공유합니다.
>
> 추가 크기나 볼륨의 경우 PDF 첨부 파일 추가 기능을 구매할 수 있으며, 이렇게 하면 개인화된 첨부 파일의 결합된 제한이 10MB로 늘어납니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.

이메일 메시지에 PDF 파일을 첨부하려면 아래 단계를 따르십시오.

1. 여정 또는 캠페인에서 이메일을 만듭니다. [자세히 알아보기](create-email.md)

1. 여정 또는 캠페인 **[!UICONTROL 콘텐츠]** 탭의 **[!UICONTROL 첨부 파일]** 섹션에서 **[!UICONTROL 에셋 추가]**&#x200B;를 선택합니다.

   ![](assets/email-select-pdf.png)

1. Assets Essentials 저장소가 표시됩니다.

   >[!NOTE]
   >
   >메시지를 디자인할 때는 Journey Optimizer 인터페이스 내에서 Assets Essentials 저장소에 직접 액세스합니다. 포함된 [!DNL Assets Essentials] 사용자 인터페이스에 대한 자세한 내용은 [Experience Manager Assets Essentials 설명서](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}를 참조하세요.

1. **[!UICONTROL MIME 형식]** 섹션의 **[!UICONTROL PDF]** 필터를 사용하여 올바른 파일 형식으로 선택을 제한하십시오.

   ![](assets/email-assets-pdf.png)

   >[!NOTE]
   >
   >PDF 형식만 첨부 파일에 허용됩니다.

1. 선택한 파일을 선택합니다.

   * 한 번에 하나의 파일만 선택할 수 있습니다.
   * 각 첨부 파일의 최대 크기는 5MB입니다.

1. 완료되면 선택한 파일의 이름과 크기가 **[!UICONTROL 첨부 파일]** 섹션에 표시됩니다.

   파일 이름 옆에 있는 추가 작업 아이콘을 사용하여 선택한 파일을 제거할 수 있습니다.

   ![](assets/email-remove-attachment.png)

>[!NOTE]
>
>메시지를 [콘텐츠 템플릿](../content-management/create-content-templates.md)(으)로 저장하면 PDF 첨부 파일이 템플릿과 함께 유지되지 않습니다. 저장된 콘텐츠 템플릿에서 새 이메일을 만드는 경우 파일을 다시 첨부해야 합니다.

## API 트리거 캠페인을 위한 개인화된 PDF 파일 첨부 {#personalized-attachments}

[API 트리거 캠페인](../campaigns/api-triggered-campaigns.md)을 통해 보낸 단일 전자 메일에 수신자별 PDF 파일을 첨부할 수도 있습니다. 정적 첨부 파일과는 달리 각 수신자는 송장, 탑승권, 계약서 또는 배송 레이블과 같은 다른 파일을 받을 수 있습니다.

이메일에 있는 모든 정적 및 개인화된 PDF 첨부 파일의 결합된 크기는 기본적으로 5MB로 제한됩니다. 적용 가능한 PDF 첨부 파일 추가 기능이 있는 조직은 최대 10MB의 통합 제한을 사용할 수 있습니다.

>[!IMPORTANT]
>
>* 개인화된 PDF 첨부 파일은 트랜잭션 API가 트리거된 이메일 캠페인에 대해서만 지원됩니다.
>
>* 이메일에 PDF 첨부 파일을 최대 5개까지 포함할 수 있습니다. 이 제한에는 정적 및 개인화된 첨부 파일이 모두 포함됩니다. 예를 들어 하나의 정적 PDF이 포함된 이메일에는 최대 4개의 개인화된 PDF를 포함할 수 있습니다. 더 전송해야 하는 경우 여러 통신으로 분할합니다.
>
>* 개인화된 정적 PDF 첨부 파일은 동일한 할당량에 포함됩니다. [자세히 알아보기](#pdf-attachments)

개인화된 PDF 첨부 파일을 첨부 파일별 [데이터 랜딩 영역](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/cloud-storage/data-landing-zone){target="_blank"} 컨테이너로 업로드한 다음 API 페이로드에서 참조해야 합니다. 데이터 랜딩 영역 은 현재 개인화된 PDF 첨부 파일에 대해 유일하게 지원되는 저장소 위치입니다.

1. [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/cloud-storage/data-landing-zone){target="_blank"}에 설명된 대로 실행 요청과 동일한 IMS 조직 및 샌드박스에 대해 `type=ajoemailattachments`을(를) 사용하여 샌드박스의 데이터 랜딩 영역 자격 증명을 검색합니다. 클라우드 공급자에 따라 Azure 컨테이너 또는 API에서 반환한 AWS 버킷 및 폴더를 사용합니다.

1. 선택한 도구로 PDF 파일을 생성하고 데이터 랜딩 영역 컨테이너에 업로드합니다.

   데이터 랜딩 영역 은 7일 후에 파일을 자동으로 삭제합니다. 메시지 배달과 다시 시도가 완료될 때까지 PDF 파일을 컨테이너에 계속 사용할 수 있는지 확인합니다.

1. API 페이로드에서 각 수신자에 대해 전송할 PDF의 파일 이름, 콘텐츠 형식 및 데이터 랜딩 영역 경로가 포함된 `attachments` 배열을 추가합니다. [API로 트리거된 캠페인 콘텐츠를 개인화하는 방법을 알아보세요](../campaigns/api-triggered-campaign-content.md#contextual)

   ```json
   "attachments": [
     {
       "name": "invoice-12345.pdf",
       "contentType": "application/pdf",
       "source": {
         "type": "dlzPath",
         "path": "attachments/invoice-12345.pdf"
       }
     }
   ]
   ```

   `source.path`은(는) `type=ajoemailattachments`(으)로 검색된 첨부 파일별 데이터 랜딩 영역 컨테이너에 상대적인 개체 경로입니다. Azure 컨테이너 이름, AWS 버킷 또는 폴더, 자격 증명 또는 전체 저장소 URL을 포함하지 마십시오.

전송 시 [!DNL Journey Optimizer]은(는) 지정된 위치에서 파일을 가져와서 해당 수신자의 메시지에 연결합니다. 개인화된 PDF 첨부 파일은 기본 지역의 [높은 처리량](../campaigns/api-triggered-high-throughput.md) 캠페인에 대해 지원됩니다. 이 기능은 지역 장애 조치(failover) 중에는 지원되지 않습니다.

전체 API 페이로드 참조에 대해서는 [대화형 메시지 실행 API 설명서](https://developer.adobe.com/journey-optimizer-apis/references/messaging#tag/execution){target="_blank"}를 참조하십시오.
