---
solution: Journey Optimizer
product: journey optimizer
title: 온보딩 프로젝트 안내서 | ADOBE JOURNEY OPTIMIZER
description: 관리자, 데이터, 개발자 및 마케터 역할에서 Adobe Journey Optimizer 온보딩 프로젝트를 계획 및 관리합니다.
feature: Get Started
topic: Content Management
role: Admin
level: Intermediate
keywords: 여정 최적화 도구, 온보딩, 온보딩 프로젝트, 롤아웃, 구현 계획, 관리자, csm, 구현 파트너, 단계별 체크리스트
source-git-commit: 6a653e1dbb00f68ff689ea3e0dc0b15abda1e21e
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 4%

---

# 온보딩 프로젝트 안내서 {#onboarding-hub}

>[!BEGINSHADEBOX]

**이 페이지에서:** 관리자, 데이터 엔지니어, 개발자 및 마케터 역할에 적용되는 단계별 체크리스트를 사용하여 전체 Adobe Journey Optimizer 롤아웃을 계획하고 조정합니다.

>[!ENDSHADEBOX]

이 페이지는 전체 Journey Optimizer 롤아웃을 조정하는 **시스템 관리자 및 구현 파트너**&#x200B;를 위한 페이지입니다. 모든 역할을 다루는 단계별 체크리스트와 자세한 역할별 안내서에 대한 링크를 제공합니다.

>[!NOTE]
>
>특정 역할을 시작하는 개별 사용자의 경우 대신 [Journey Optimizer 시작](../../rp_landing_pages/get-started-landing-page.md)(으)로 이동합니다.

## 1단계 — 환경 설정(관리자) {#phase-1}

다른 역할이 작업을 시작할 수 있도록 먼저 다음 기본 작업을 완료하십시오.

* [ ] 프로비전 샌드박스(개발, 스테이징, 프로덕션)
* [ ] Adobe Admin Console에서 사용자 역할 및 권한 구성
* [ ] 제품 프로필 및 개체 수준 액세스 제어 설정
* [ ] 하위 도메인 위임 및 IP 풀 구성
* [ ] 채널 구성(전자 메일, SMS, 푸시, 웹, 인앱, DM)
* [ ] 비표시 목록 및 동의 정책 설정

➡️ 자세한 내용 보기: [관리자를 위한 시작](path/administrator.md)

## 2단계 — 데이터 기반(데이터 엔지니어) {#phase-2}

프로필, 대상 및 여정 트리거를 구동하는 데이터 레이어를 만듭니다.

* [ ] ID 네임스페이스 정의
* [ ] XDM 스키마(프로필, 경험 이벤트, 관계형) 만들기
* [ ] 실시간 고객 프로필에 대한 데이터 세트 설정 및 활성화
* [ ] 데이터 수집 구성(일괄 처리 및 스트리밍)
* [ ] 계산된 특성 만들기
* [ ] 여정 이벤트 및 데이터 원본 구성

➡️ 자세한 내용 보기: [데이터 엔지니어 시작](path/data-engineer.md)

## 3단계 — 기술 통합(개발자) {#phase-3}

실시간 데이터에서 여정을 실행할 수 있도록 애플리케이션을 연결합니다.

* [ ] 푸시 설정과 모바일 SDK(iOS/Android) 통합
* [ ] 웹 경험 및 웹 푸시를 위한 웹 SDK 구현
* [ ] 응용 프로그램에서 이벤트 전송 구현
* [ 외부 시스템 통합을 위한 사용자 지정 작업 끝점 ] 빌드
* [ Adobe Experience Platform Assurance을 사용하여 ] 유효성 검사

➡️ 자세한 내용 보기: [개발자용 시작하기](path/developer.md)

## 4단계 - 첫 번째 경험(마케터) {#phase-4}

첫 번째 여정 및 캠페인을 시작하여 토대를 구축하십시오.

* [ ] 첫 번째 대상 작성(세그먼트 정의 또는 CSV 업로드)
* [ ] 전자 메일 작업으로 테스트 여정 만들기
* [ ] 콘텐츠 템플릿 및 조각 설정
* [ ] 캠페인 게시 및 모니터링
* [ ] 실시간 보고서 검토

➡️ 자세한 내용 보기: [마케터용 시작](path/marketer.md)

## 온보딩 체크리스트(인쇄 가능) {#checklist}

| 단계 | 소유자 | 상태 |
|-------|-------|--------|
| 환경 설정 | 관리자 | |
| 데이터 기반 | 데이터 엔지니어 | |
| 기술 통합 | Developer | |
| 첫 번째 경험 | 마케터 | |

## 관련 리소스 {#related-resources}

* [역할 및 책임](quick-start.md) - 네 가지 역할이 함께 작동하는 방식 및 권장 구현 순서.
* [Journey Optimizer 자습서](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} - 모든 역할에 대한 단계별 비디오 및 안내식 워크스루.
* [데이터 관리 시작](../data/gs-data.md) - 데이터를 수집, 통합 및 활성화하는 방법.
