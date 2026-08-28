---
solution: Journey Optimizer
product: journey optimizer
title: 이메일 및 랜딩 페이지 Designer의 C2PA 메타데이터
description: Adobe Journey Optimizer의 이메일 및 랜딩 페이지 디자이너를 통해 이동할 때 이미지에 이미 첨부된 C2PA 메타데이터가 어떻게 되는지 알아봅니다.
feature: Content Management
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
source-git-commit: 47e95cbc3716e650492e9cda4a4fddbe61f56ffd
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---


# 이메일 및 랜딩 페이지 Designer의 C2PA 메타데이터 {#c2pa-email-landing-page-designer}

>[!BEGINSHADEBOX]

**이 페이지에서:** Adobe Journey Optimizer의 전자 메일 및 랜딩 페이지 디자이너를 통해 이동할 때 이미지에 이미 첨부된 C2PA 메타데이터가 어떻게 되는지 알아봅니다.

>[!ENDSHADEBOX]

>[!INFO]
>
>생성 AI 투명성을 중심으로 새로운 법이 등장하고 있으며, Adobe은 관할권 전반에서 적용 가능한 요구 사항을 충족하기 위해 노력하고 있습니다. C2PA 메타데이터는 Adobe이 이러한 법률의 요구 사항을 충족하기 위해 사용하는 증명 도구입니다.

이메일 및 랜딩 페이지 디자이너는 이미지 자체를 생성하거나 편집하지 않습니다. 콘텐츠 생성, Adobe Express 또는 Firefly과 같은 다른 Adobe 도구 또는 파트너 모델에서 생성 AI로 이미 생성 또는 편집된 이미지를 참조합니다. 이러한 이미지에 이미 첨부된 C2PA 메타데이터는 빌드, 게시 및 전송 시 유지되며 변경되지 않습니다.

## C2PA 메타데이터는 작성 및 전송 시 보존됩니다 {#c2pa-preserved}

다음 표에서는 이메일 및 랜딩 페이지 디자이너를 사용하여 콘텐츠를 빌드하고 전송하는 각 단계에서 C2PA 메타데이터가 어떻게 되는지 요약합니다.

| 작업 | 다음 단계 | C2PA 메타데이터가 유지됩니까? | 예 |
| --- | --- | --- | --- |
| **템플릿에 이미지 삽입** | 디자이너는 콘텐츠 생성, Adobe Express, Firefly 또는 파트너 모델과 같은 다른 곳에서 생성 AI로 이미 생성되거나 편집된 이미지에 참조를 추가합니다. 이미지 파일 자체는 변경되지 않습니다. | 예, 변경되지 않음 | Firefly 생성 배너가 이메일 템플릿에 삽입됩니다. |
| **대체 텍스트 크기 조정, 위치 변경 또는 추가** | 템플릿의 HTML 변경 사항에만 속성을 표시합니다. 이미지 파일이 다시 인코딩되지 않았습니다. | 예, 변경되지 않음 | 모바일 레이아웃과 제공된 대체 텍스트에 맞게 이미지 크기가 조정됩니다. |
| **게시** | 이메일 또는 랜딩 페이지가 게시되고, 이미지가 게재를 위해 저장됩니다. | 예, 변경되지 않음 | 캠페인이 게시되고 해당 이미지가 보내기 위해 저장됩니다. |
| **전자 메일 보내기 또는 랜딩 페이지 보기** | 이미지가 수신자의 받은 편지함으로 전달되거나 라이브 페이지에 표시됩니다. | 예, 변경되지 않음 | 수신자가 이메일을 열고 이미지를 다운로드합니다. 자격 증명은 여전히 원본과 일치합니다. |

## 컨텐츠 유형 및 해당 범위 {#c2pa-content-types}

* **이미지**: 적용됨. 이미지에 이미 첨부된 C2PA 메타데이터는 위와 같이 삽입, 조정, 게시 및 전달될 때 보존됩니다.
* **비디오, 오디오, 텍스트**: 적용할 수 없습니다. 이메일 및 랜딩 페이지 디자이너는 생성 AI를 사용하여 이러한 콘텐츠 유형을 생성하거나 편집하지 않습니다.

## 콘텐츠가 이동할 때 수행되는 작업 {#c2pa-content-moves}

C2PA 메타데이터는 Adobe Journey Optimizer의 이메일 및 랜딩 페이지 디자이너를 통해 편집기에서 저장소를 거쳐 수신자의 받은 편지함 또는 라이브 페이지에 이르기까지 이미지와 함께 이동합니다. 이러한 단계 중 어느 단계에서도 자격 증명이 생성, 변경 또는 제거되지 않습니다.

생성 AI로 생성 또는 편집되지 않은 이미지이므로 생성 AI C2PA 메타데이터가 없는 경우 여기에 자격 증명이 표시되지 않습니다. 오류가 아니라 예상되었습니다.

## 자격 증명 확인 {#c2pa-checking-credential}

아직 이메일 또는 랜딩 페이지 디자이너 내에서 Content Credential을 직접 검사할 수 있는 방법은 없습니다.

## 추가 리소스

* [콘텐츠 생성의 C2PA 메타데이터](generative-c2pa-metadata.md)
* [생성 AI 콘텐츠 투명도](https://experienceleague.adobe.com/ko/docs/cx-enterprise-ai/experience-cloud-ai/overview/content-transparency)
