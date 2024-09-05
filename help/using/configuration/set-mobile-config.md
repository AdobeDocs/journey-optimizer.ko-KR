---
solution: Journey Optimizer
product: journey optimizer
title: 모바일 및 웹 설정
description: 모바일 및 웹 채널을 구성하고 모니터링하는 방법에 대해 알아봅니다
feature: Surface, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 채널, 표면, 기술, 매개변수, 최적기
exl-id: 846e0d11-798b-4f3b-80db-848a17d32830
source-git-commit: 77e2892dc188ebdd79031792434b4f55913ee811
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 20%

---

# 안내형 채널 설정 시작 {#set-mobile-config}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_name"
>title="모바일 및 웹 구성 이름"
>abstract="모바일이나 웹 구성의 이름을 입력합니다. 이 이름은 안내 채널 설정을 통해 자동으로 생성되는 모든 리소스에 사용됩니다."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_validate_assurance"
>title="Assurance를 사용한 유효성 검사"
>abstract="Adobe Experience Platform Assurance가 이 워크플로에 임베드되어 있어 SDK 구현을 검사하고 애플리케이션 이벤트를 시뮬레이션 및 검증하는 데 도움이 됩니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-platform/assurance/home" text="Adobe Experience Platform Assurance 개요"

이 설정을 사용하면 마케팅 채널을 신속하게 구성할 수 있으므로 필요한 모든 리소스를 Experience Platform, Journey Optimizer 및 데이터 수집 내에서 쉽게 사용할 수 있습니다. 이렇게 하면 마케팅 팀이 캠페인 및 여정 생성으로 시작할 수 있습니다.

안내식 채널 설정은 다음 플랫폼 및 채널을 지원합니다.

* 플랫폼 및 SDK:

   * Swift by Apple, iOS

   * 코틀린, Android

   * Javascript, 웹

* 채널:

   * 모바일 인앱

   * 모바일 푸시 메시지

   * 웹 기본


설정하려는 각 플랫폼에 대해 별도의 구성을 만들어야 합니다. 각 앱에는 고유한 채널 구성이 필요하며, 이를 통해 각 플랫폼에 대해 원하는 채널을 유연하게 결정할 수 있기 때문입니다.

## 전제 조건 {#prereq}

* 이를 효과적으로 구현하려면 웹 사이트 또는 모바일 코드를 수정할 수 있는 권한과 기술 능력을 갖춘 조직 구성원이 설정을 감독해야 합니다.

  다음은 안내가 있는 채널 설정을 실행하는 데 필요한 권한입니다.

+++ 필요한 권한

  <table>
    <thead>
      <tr>
        <th><strong>솔루션</strong></th>
        <th><strong>권한</strong></th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>
          <p>데이터 수집</p>
        </td>
        <td>
          <ul>
            <li>회사 권한 &gt; 속성</li>
            <li>속성 권한: 확장 및 환경 개발, 게시, 관리</li>
            <li>앱 표면: 앱 구성 관리</li>
         </ul>
        </td>
      </tr>
      <tr>
        <td>
          <p>Adobe Experience Platform</p>
        </td>
        <td>
        <ul>
            <li>데이터 수집: 데이터스트림 관리</li>
           <li>샌드박스: 샌드박스에 대한 액세스 권한 부여</li>
            <li>세그먼트 관리: 세그먼트 정의 읽기, 만들기, 편집 및 삭제</li>
            <li>프로필 관리: 프로필 읽기, 만들기, 편집 및 삭제</li>
            <li>데이터 세트 읽기: 데이터 세트에 대한 읽기 전용 액세스</li>
            <li>스키마 읽기: 스키마에 대한 읽기 전용 액세스</li>
            <li>ID 네임스페이스 읽기: ID 네임스페이스에 대한 읽기 전용 액세스</li>
          </ul>
        </td>
      </tr>
      <tr>
        <td>
         <p>Adobe Journey Optimizer</p>
        </td>
        <td>
          <p>캠페인: 캠페인 관리 및 게시</p>
        </td>
      </tr>
    </tbody>
  </table>

+++

* 기존 구성 옵션을 사용 중인 경우 다음 Adobe Experience Platform Mobile SDK 확장 버전을 사용 중인지 확인하십시오. 필요한 종속성 및 초기화 코드를 포함하여 SDK 설정에 대한 자세한 내용은 [다음 설명서](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/install-sdks?lang=en)를 참조하십시오.

  Android용

   * Mobile Core v3.1.0 이상
   * Adobe Journey Optimizer v3.1.0 이상

  iOS용

   * Mobile Core v5.2.0 이상
   * Adobe Journey Optimizer v5.1.1 이상

## 자동 생성된 리소스 {#auto-create-resources}

가이드 채널 설정 은 마케팅 채널의 빠른 구성을 단순화하여 Experience Platform, Journey Optimizer 및 데이터 수집 앱에서 모든 필수 리소스를 쉽게 사용할 수 있도록 합니다. 이렇게 하면 마케팅 팀이 캠페인 및 여정 만들기를 빠르게 시작할 수 있습니다. 다음은 안내식 채널 설정의 일부로 자동 생성되고 구성된 리소스 목록입니다.

아래 탭을 탐색하여 자동으로 생성되는 모든 리소스의 포괄적인 목록에 액세스합니다.

>[!BEGINTABS]

>[!TAB iOS]

**초기 구성**&#x200B;의 경우 **리소스 자동 만들기**&#x200B;를 클릭하면 **구성 세부 정보** 화면에서 만든 모든 리소스의 전체 목록이 아래에 표시됩니다.

<table>
  <thead>
  <tr>
  <th><strong>솔루션</strong></th>
  <th><strong>자동 생성된 리소스</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>태그</p>
  </td>
  <td>
  <ul>
  <li>모바일 태그 속성</li>
  <li>규칙</li>
  <li>데이터 요소</li>
  <li>라이브러리</li>
  <li>환경(스테이징, 프로덕션, 개발)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>태그 확장</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP 보증</li>
  <li>동의(기본 동의 정책이 활성화됨)</li>
  <li>ID(기본 ECID 사용, 기본 결합 규칙 사용)</li>
  <li>모바일 코어</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>보증</p>
  </td>
  <td>
  <p>보증 세션</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>데이터스트림</p>
  </td>
  <td>
  <p>서비스가 포함된 데이터 스트림</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>데이터 세트</li>
  <li>스키마</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

**채널 설정**&#x200B;의 경우 **채널 추가** 화면에서 만든 모든 리소스의 전체 목록은 다음과 같습니다.

<table>
  <thead>
  <tr>
  <th><strong>솔루션</strong></th>
  <th><strong>자동 생성된 리소스</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Journey Optimizer</p>
  </td>
  <td>
  <ul>
  <li>채널 구성</li>
  <li>푸시 자격 증명 업로드(모바일 푸시 메시지만 해당)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB Android]

**초기 구성**&#x200B;의 경우 **리소스 자동 만들기**&#x200B;를 클릭하면 **구성 세부 정보** 화면에서 만든 모든 리소스의 전체 목록이 아래에 표시됩니다.

<table>
  <thead>
  <tr>
  <th><strong>솔루션</strong></th>
  <th><strong>자동 생성된 리소스</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>태그</p>
  </td>
  <td>
  <ul>
  <li>모바일 태그 속성</li>
  <li>규칙</li>
  <li>데이터 요소</li>
  <li>라이브러리</li>
  <li>환경(스테이징, 프로덕션, 개발)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>태그 확장</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP 보증</li>
  <li>동의(기본 동의 정책이 활성화됨)</li>
  <li>ID(기본 ECID 사용, 기본 결합 규칙 사용)</li>
  <li>모바일 코어</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>보증</p>
  </td>
  <td>
  <p>보증 세션</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>데이터스트림</p>
  </td>
  <td>
  <p>서비스가 포함된 데이터 스트림</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>데이터 세트</li>
  <li>스키마</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

**채널 설정**&#x200B;의 경우 **채널 추가** 화면에서 만든 모든 리소스의 전체 목록은 다음과 같습니다.

<table>
  <thead>
  <tr>
  <th><strong>솔루션</strong></th>
  <th><strong>자동 생성된 리소스</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Journey Optimizer</p>
  </td>
  <td>
  <ul>
  <li>채널 구성</li>
  <li>푸시 자격 증명 업로드(모바일 푸시 메시지만 해당)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB 웹]

**초기 구성**&#x200B;의 경우 **리소스 자동 만들기**&#x200B;를 클릭하면 **구성 세부 정보** 화면에서 만든 모든 리소스의 전체 목록이 아래에 표시됩니다.

<table>
  <thead>
  <tr>
  <th><strong>솔루션</strong></th>
  <th><strong>자동 생성된 리소스</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>태그</p>
  </td>
  <td>
  <ul>
  <li>모바일 태그 속성</li>
  <li>규칙</li>
  <li>데이터 요소</li>
  <li>라이브러리</li>
  <li>환경(스테이징, 프로덕션, 개발)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>태그 확장</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP 보증</li>
  <li>동의(기본 동의 정책이 활성화됨)</li>
  <li>ID(기본 ECID 사용, 기본 결합 규칙 사용)</li>
  <li>모바일 코어</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>보증</p>
  </td>
  <td>
  <p>보증 세션</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>데이터스트림</p>
  </td>
  <td>
  <p>서비스가 포함된 데이터 스트림</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>데이터 세트</li>
  <li>스키마</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!ENDTABS]

