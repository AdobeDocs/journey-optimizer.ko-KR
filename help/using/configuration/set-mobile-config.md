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
hide: true
hidefromtoc: true
source-git-commit: 4a089308cfc2fa90cc4c0a6baa15a89598e8edd6
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 25%

---

# 가이드 채널 설정 시작 {#set-mobile-config}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_name"
>title="모바일 및 웹 구성 이름"
>abstract="모바일 또는 웹 구성의 이름을 입력합니다. 이 이름은 가이드 채널 설정으로 자동으로 만들어지는 모든 리소스에 사용됩니다."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_validate_assurance"
>title="Assurance를 사용한 유효성 검사"
>abstract="Adobe Experience Platform Assurance는 이 워크플로에 포함되어 있어 SDK 구현을 검사하고 애플리케이션 이벤트를 시뮬레이션하고 확인하는 데 도움이 됩니다."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/assurance/home" text="Adobe Experience Platform Assurance 개요"


이 설정을 사용하면 마케팅 채널을 신속하게 구성할 수 있으므로 필요한 모든 리소스를 Experience Platform, Journey Optimizer 및 데이터 수집 내에서 쉽게 사용할 수 있습니다. 이렇게 하면 마케팅 팀이 캠페인 및 여정 생성을 즉시 시작할 수 있습니다.

이를 효과적으로 구현하려면 웹 사이트 또는 모바일 코드를 수정할 수 있는 권한과 기술 능력을 갖춘 조직 구성원이 설정을 감독해야 합니다.

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

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="set-mobile-android.md">
<img alt="리드" src="assets/do-not-localize/config-android.jpeg">
</a>
<div><a href="set-mobile-android.md"><strong>Android 모바일 구성 설정</strong>
</div>
<p>
</td>
<td>
<a href="set-mobile-ios.md">
<img alt="드물게" src="assets/do-not-localize/config-ios.jpeg">
</a>
<div>
<a href="set-mobile-ios.md"><strong>iOS 모바일 구성 설정</strong></a>
</div>
<p></td>
<td>
<a href="set-mobile-web.md">
<img alt="유효성 검사" src="assets/do-not-localize/config-web.jpeg">
</a>
<div>
<a href="set-mobile-web.md"><strong>웹 구성 설정</strong></a>
</div>
<p>
</td>
</tr></table>
