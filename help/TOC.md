---
product: Journey Optimizer
audience: end-user
user-guide-title: Journey Optimizer 안내서
user-guide-description: Journey Optimizer를 사용하여 고객에게 연관성 있고 상황에 맞으며 개인화된 경험 구축 및 제공
type: Documentation
solution: Journey Optimizer
source-git-commit: 4df89a36705fb53984ba04ba1ae2f45554e47f77
workflow-type: tm+mt
source-wordcount: '1311'
ht-degree: 99%

---

# Adobe Journey Optimizer 도움말 {#using}

+ [Journey Optimizer 설명서](ajo-home.md)
+ 새로운 기능 {#whats-new}
   + [최신 릴리스 정보](using/rn/release-notes.md)
   + 이전 릴리스 정보 {#previous-rn-new}
      + [2022년 릴리스 정보](using/rn/release-notes-2022.md)
      + [2021년 릴리스 정보](using/rn/release-notes-2021.md)
   + [설명서 업데이트](using/rn/documentation-updates.md)
+ 시작{#get-started}
   + [Journey Optimizer 소개](using/start/get-started.md)
   + 빠른 시작{#quick-start}
      + [개요](using/start/quick-start.md)
      + [마케터로 시작하기](using/start/path/marketer.md)
      + [데이터 엔지니어로 시작하기](using/start/path/data-engineer.md)
      + [관리자로 시작하기](using/start/path/administrator.md)
      + [개발자로 시작하기](using/start/path/developer.md)
   + [사용자 인터페이스](using/start/user-interface.md)
   + [접근성](using/start/accessibility.md)
   + [통합](using/start/ajo-integrations.md)
   + [가드레일](using/start/guardrails.md)
+ 여정 {#orchestrate-journeys}
   + [여정 시작](using/building-journeys/journey.md)
   + 여정 만들기{#create-journey}
      + [첫 여정 만들기](using/building-journeys/journey-gs.md)
      + [여정 디자인](using/building-journeys/using-the-journey-designer.md)
      + [여정 테스트](using/building-journeys/testing-the-journey.md)
      + [여정 게시](using/building-journeys/publishing-the-journey.md)
   + 여정 관리{#mannage-journey}
      + [여정 끝내기](using/building-journeys/end-journey.md)
      + [시간대 관리](using/building-journeys/timezone-management.md)
      + [프로필 시작 관리](using/building-journeys/entry-management.md)
      + [다른 샌드박스로 여정 복사](using/building-journeys/copy-to-sandbox.md)
      + [여정 문제 해결](using/building-journeys/troubleshooting.md)
      + [인텔리전트 서비스와 통합](using/building-journeys/ai-services-overview.md)
   + 활동 {#about-journey-building}
      + [여정 활동 시작](using/building-journeys/about-journey-activities.md)
      + [일반 이벤트](using/building-journeys/general-events.md)
      + [반응](using/building-journeys/reaction-events.md)
      + [세그먼트 자격 조건](using/building-journeys/segment-qualification-events.md)
      + [조건](using/building-journeys/condition-activity.md)
      + [대기](using/building-journeys/wait-activity.md)
      + [세그먼트 읽기](using/building-journeys/read-segment.md)
      + [이메일, SMS, 푸시](using/building-journeys/journeys-message.md)
      + [사용자 정의 작업](using/building-journeys/using-custom-actions.md)
      + [Adobe Campaign Standard 작업](using/building-journeys/using-adobe-campaign-standard.md)
      + [Adobe Campaign v7/v8 작업](using/building-journeys/using-adobe-campaign-classic.md)
      + [점프](using/building-journeys/jump.md)
      + [프로필 업데이트](using/building-journeys/update-profiles.md)
   + 표현식 작성 {#building-advanced-conditions-journeys}
      + [개요](using/building-journeys/expression/expressionadvanced.md)
      + 구문 {#syntax}
         + [일반성](using/building-journeys/expression/generalities.md)
         + [조건부 지침](using/building-journeys/expression/conditional-instruction.md)
         + [데이터 유형](using/building-journeys/expression/data-types.md)
         + [필드 참조](using/building-journeys/expression/field-references.md)
         + [컬렉션 관리 기능](using/building-journeys/expression/collection-management-functions.md)
         + [연산자](using/building-journeys/expression/operators.md)
         + [여정 속성](using/building-journeys/expression/journey-properties.md)
         + [예시](using/building-journeys/expression/advanced-editor-use-cases.md)
      + 함수 {#main-functions-journey}
         + [기본 함수](using/building-journeys/expression/functions.md)
         + Adobe Experience Platform {#adobe-experience-platform}
            + [inSegment](using/building-journeys/functions/functioninsegment.md)
         + 집계 {#aggregation}
            + [avg](using/building-journeys/functions/functionavg.md)
            + [count](using/building-journeys/functions/functioncount.md)
            + [countOnlyNull](using/building-journeys/functions/functioncountonlynull.md)
            + [countWithNull](using/building-journeys/functions/functioncountwithnull.md)
            + [distinctCount](using/building-journeys/functions/functiondistinctcount.md)
            + [distinctCountWithNull](using/building-journeys/functions/functiondistinctcountwithnull.md)
            + [max](using/building-journeys/functions/functionmax.md)
            + [min](using/building-journeys/functions/functionmin.md)
            + [sum](using/building-journeys/functions/functionsum.md)
         + 전환 {#conversion}
            + [toBool](using/building-journeys/functions/functiontobool.md)
            + [toDateOnly](using/building-journeys/functions/functiontodateonly.md)
            + [toDateTime](using/building-journeys/functions/functiontodatetime.md)
            + [toDateTimeOnly](using/building-journeys/functions/functiontodatetimeonly.md)
            + [toDecimal](using/building-journeys/functions/functiontodecimal.md)
            + [toDuration](using/building-journeys/functions/functiontoduration.md)
            + [toInteger](using/building-journeys/functions/functiontointeger.md)
            + [toString](using/building-journeys/functions/functiontostring.md)
         + 날짜 {#date}
            + [currentTimeInMillis](using/building-journeys/functions/functioncurrenttimeinmillis.md)
            + [inLastDays](using/building-journeys/functions/functioninlastdays.md)
            + [inLastHours](using/building-journeys/functions/functioninlasthours.md)
            + [inLastMonths](using/building-journeys/functions/functioninlastmonths.md)
            + [inLastYears](using/building-journeys/functions/functioninlastyears.md)
            + [inNextDays](using/building-journeys/functions/functioninnextdays.md)
            + [inNextHours](using/building-journeys/functions/functioninnexthours.md)
            + [inNextMonths](using/building-journeys/functions/functioninnextmonths.md)
            + [inNextYears](using/building-journeys/functions/functioninnextyears.md)
            + [now](using/building-journeys/functions/functionnow.md)
            + [nowWithDelta](using/building-journeys/functions/functionnowwithdelta.md)
            + [setHours](using/building-journeys/functions/functionsethours.md)
            + [setDays](using/building-journeys/functions/functionsetdays.md)
            + [updateTimeZone](using/building-journeys/functions/functionupdatetimezone.md)
         + 목록 {#list}
            + [distinct](using/building-journeys/functions/functiondistinct.md)
            + [distinctWithNull](using/building-journeys/functions/functiondistinctwithnull.md)
            + [filter](using/building-journeys/functions/functionfilter.md)
            + [getListItem](using/building-journeys/functions/functiongetlistitem.md)
            + [in](using/building-journeys/functions/functionin.md)
            + [intersect](using/building-journeys/functions/functionintersect.md)
            + [limit](using/building-journeys/functions/functionlimit.md)
            + [listSize](using/building-journeys/functions/functionlistsize.md)
            + [serializeList](using/building-journeys/functions/functionserializelist.md)
            + [sort](using/building-journeys/functions/functionsort.md)
         + 수학 {#math}
            + [random](using/building-journeys/functions/functionrandom.md)
            + [round](using/building-journeys/functions/functionround.md)
         + 문자열 {#string}
            + [concat](using/building-journeys/functions/functionconcat.md)
            + [contain](using/building-journeys/functions/functioncontain.md)
            + [containIgnoreCase](using/building-journeys/functions/functioncontainwithignorecase.md)
            + [endWith](using/building-journeys/functions/functionendwith.md)
            + [endWithIgnorecase](using/building-journeys/functions/functionendwithignorecase.md)
            + [equalIgnoreCase](using/building-journeys/functions/functionequalignorecase.md)
            + [indexOf](using/building-journeys/functions/functionindexof.md)
            + [isEmpty](using/building-journeys/functions/functionisempty.md)
            + [isNotEmpty](using/building-journeys/functions/functionisnotempty.md)
            + [lastIndexOf](using/building-journeys/functions/functionlastindexof.md)
            + [length](using/building-journeys/functions/functionlength.md)
            + [lower](using/building-journeys/functions/functionlower.md)
            + [matchRegExp](using/building-journeys/functions/functionmatchregexp.md)
            + [notequalIgnoreCase](using/building-journeys/functions/functionnotequalignorecase.md)
            + [replace](using/building-journeys/functions/functionreplace.md)
            + [replaceAll](using/building-journeys/functions/functionreplaceall.md)
            + [split](using/building-journeys/functions/functionsplit.md)
            + [startWith](using/building-journeys/functions/functionstartwith.md)
            + [startWithIgnoreCase](using/building-journeys/functions/functionstartwithignorecase.md)
            + [substr](using/building-journeys/functions/functionsubstr.md)
            + [trim](using/building-journeys/functions/functiontrim.md)
            + [upper](using/building-journeys/functions/functionupper.md)
            + [uuid](using/building-journeys/functions/functionuuid.md)
   + 사용 사례 {#journey-use-cases}
      + 비즈니스 사용 사례 {#business-use-cases} 
         + [다중 채널 메시지 보내기](using/building-journeys/journeys-uc.md)
         + [Campaign v7/v8을 사용하여 메시지 보내기](using/building-journeys/ajo-ac.md)
         + [구독자에게 메시지 보내기](using/building-journeys/message-to-subscribers-uc.md)
      + 기술 사용 사례 {#technical-use-cases} 
         + [사용자 지정 작업으로 컬렉션을 동적으로 보내기](using/building-journeys/collections.md)
         + [게재 램프 업](using/building-journeys/ramp-up-deliveries-uc.md)
         + [외부 데이터 원본 및 사용자 지정 작업으로 처리량 제한](using/building-journeys/limit-throughput.md)
+ 캠페인{#campaigns}
   + [캠페인 시작](using/campaigns/get-started-with-campaigns.md)
   + [캠페인 만들기](using/campaigns/create-campaign.md)
   + [캠페인 검토 및 활성화](using/campaigns/review-activate-campaign.md)
   + [캠페인 관리](using/campaigns/modify-stop-campaign.md)
   + 콘텐츠 실험 {#content-experiment}
      + [콘텐츠 실험 시작](using/campaigns/get-started-experiment.md)
      + [콘텐츠 실험 만들기](using/campaigns/content-experiment.md)
      + [통계 계산 이해](using/campaigns/experiment-calculations.md)
      + [실험 보고서 구성](using/campaigns/reporting-configuration.md)
      + [실험 보고서의 통계 계산](using/campaigns/experiment-report-calculations.md)
   + [API를 사용하여 캠페인 트리거](using/campaigns/api-triggered-campaigns.md)
+ 이메일 채널 {#email}
   + [이메일 시작](using/email/get-started-email.md)
   + [이메일 만들기](using/email/create-email.md)
   + 이메일 콘텐츠 디자인 {#design-email}
      + [이메일 디자인 시작](using/email/get-started-email-design.md)
      + 콘텐츠 만들기 시작 {#start-creating-content}
         + [처음부터 시작](using/email/content-from-scratch.md)
         + [이메일 콘텐츠 가져오기](using/email/existing-content.md)
         + [나만의 콘텐츠 코딩](using/email/code-content.md)
         + [템플릿 작업](using/email/email-templates.md)
      + 콘텐츠 디자인 {#add-content}
         + [콘텐츠 구성 요소 사용](using/email/content-components.md)
         + [링크 추가 및 메시지 추적](using/email/message-tracking.md)
         + 자산 관리 {#manage-asset}
            + [Assets Essentials 작업](using/email/assets-essentials.md)
            + [Adobe Stock 작업](using/email/stock.md)
         + [개인화된 오퍼 삽입](using/email/add-offers-email.md)
         + [텍스트 버전 생성](using/email/text-version-email.md)
         + [사전 헤더 추가](using/email/preheader.md)
      + 스타일 편집 {#edit-style}
         + [이메일 스타일 시작](using/email/get-started-email-style.md)
         + [배경 설정 편집](using/email/backgrounds.md)
         + [세로 정렬 및 패딩 조정](using/email/alignment-and-padding.md)
         + [링크의 스타일 정의](using/email/styling-links.md)
         + [인라인 스타일 속성 추가](using/email/inline-styling.md)
   + [이메일 미리 보기 및 테스트](using/email/preview.md)
   + [콘텐츠 템플릿 만들기](using/email/content-templates.md)
   + [이메일 옵트아웃 관리](using/email/email-opt-out.md)
   + 이메일 채널 구성 {#configure-email}
      + [이메일 구성 시작](using/email/get-started-email-config.md)
      + [이메일 표면 설정 구성](using/email/email-settings.md)
+ 인앱 채널{#in-app}
   + [인앱 채널 시작하기](using/in-app/get-started-in-app.md)
   + [인앱 채널 구성](using/in-app/inapp-configuration.md)
   + [인앱 메시지 만들기 ](using/in-app/create-in-app.md)
   + [인앱 콘텐츠 디자인 ](using/in-app/design-in-app.md)
   + [인앱 보고서 ](using/in-app/inapp-report.md)
+ 푸시 알림 채널{#push}
   + [푸시 알림 시작](using/push/get-started-push.md)
   + [푸시 알림 만들기](using/push/create-push.md)
   + [푸시 알림 디자인](using/push/design-push.md)
   + [푸시 알림 보내기](using/push/send-push.md)
   + 푸시 알림 구성{#push-config}
      + [푸시 알림과 Adobe Journey Optimizer](using/push/push-gs.md)
      + [푸시 알림 채널 구성](using/push/push-configuration.md)
+ SMS 채널{#sms}
   + [SMS 시작](using/sms/get-started-sms.md)
   + [SMS 메시지 만들기](using/sms/create-sms.md)
   + [SMS 메시지 보내기](using/sms/send-sms.md)
   + [SMS 옵트아웃 관리](using/sms/sms-opt-out.md)
   + [SMS 채널 구성](using/sms/sms-configuration.md)
+ 다이렉트 메일 {#direct-mail}
   + [다이렉트 메일 만들기](using/direct-mail/create-direct-mail.md)
   + [다이렉트 메일 구성](using/direct-mail/direct-mail-configuration.md)
+ 웹 채널{#web}
   + [웹 채널 시작하기](using/web/get-started-web.md)
   + [웹 경험 만들기 ](using/web/create-web.md)
   + [웹 페이지 작성 ](using/web/author-web.md)
   + [Visual Editing Helper 확장 기능](using/web/visual-editing-helper.md)
   + [웹 보고 ](using/web/web-report.md)
+ 랜딩 페이지 {#landing-pages}
   + [랜딩 페이지 시작](using/landing-pages/get-started-lp.md)
   + [랜딩 페이지 만들기](using/landing-pages/create-lp.md)
   + 콘텐츠 디자인 {#landing-pages-design}
      + [랜딩 페이지 디자인 정보](using/landing-pages/design-lp.md)
      + [랜딩 페이지 컨텐츠 만들기](using/landing-pages/lp-content.md)
      + [템플릿 만들기](using/landing-pages/lp-templates.md)
      + [사용자 지정 JavaScript 추가](using/landing-pages/lp-custom-js.md)
   + [구독 목록 만들기](using/landing-pages/subscription-list.md)
   + [사용 사례를 통해 알아보기](using/landing-pages/lp-use-cases.md)
   + 랜딩 페이지 구성 {#lp-configuration}
      + [랜딩 페이지 하위 도메인 구성](using/landing-pages/lp-subdomains.md)
      + [랜딩 페이지 사전 설정 정의](using/landing-pages/lp-presets.md)
+ 개인화 및 다이내믹 콘텐츠 {#personalized-dynamic-content}
   + 개인화 {#personalization}
      + [개인화 시작](using/personalization/personalize.md)
      + [개인화 컨텍스트](using/personalization/personalization-contexts.md)
      + 표현식 작성 {#build-expressions}
         + [개인화 구문](using/personalization/personalization-syntax.md)
         + 표현식 편집기 작업 {#expression-editor}
            + [표현식 편집기 정보](using/personalization/personalization-build-expressions.md)
            + [즐겨찾기에 속성 추가](using/personalization/personalization-favorites.md)
            + [저장된 표현식으로 작업하기](using/personalization/personalization-library.md)
            + [개인화 유효성 검사](using/personalization/personalization-validation.md)
         + 도우미 함수{#functions}
            + [도우미 함수 시작](using/personalization/functions/functions.md)
            + [집계 함수](using/personalization/functions/aggregation.md)
            + [산술 함수](using/personalization/functions/arithmetic-functions.md)
            + [배열 및 목록 함수](using/personalization/functions/arrays-list.md)
            + [날짜 함수](using/personalization/functions/dates.md)
            + [부울 및 비교 함수](using/personalization/functions/operators.md)
            + [도우미](using/personalization/functions/helpers.md)
            + [맵 함수](using/personalization/functions/maps.md)
            + [수학 함수](using/personalization/functions/math.md)
            + [개체 함수](using/personalization/functions/objects.md)
            + [문자열 함수](using/personalization/functions/string.md)
      + 사용 사례{#personalization-use-cases}
         + [주문 상태 알림](using/personalization/personalization-use-case.md)
         + [장바구니 포기 이메일](using/personalization/personalization-use-case-helper-functions.md)
   + 다이내믹 콘텐츠 {#dynamic}
      + [다이내믹 콘텐츠 시작](using/personalization/get-started-dynamic-content.md)
      + [조건부 규칙 만들기](using/personalization/create-conditions.md)
      + [다이내믹 콘텐츠 만들기](using/personalization/dynamic-content.md)
+ 세그먼트, 프로필, 신원{#segment}
   + 세그먼트 {#segments}
      + [세그먼트 시작](using/segment/about-segments.md)
      + [세그먼트 작성](using/segment/creating-a-segment.md)
   + 프로필{#profiles}
      + [프로필 시작](using/segment/get-started-profiles.md)
      + [테스트 프로필 만들기](using/segment/creating-test-profiles.md)
   + [ID](using/segment/get-started-identity.md)
   + 대상자 구성 {#audience-orchestration}
      + [대상자 구성 시작](using/segment/get-started-audience-orchestration.md)
      + [컴포지션 워크플로우 만들기](using/segment/create-compositions.md)
      + [컴포지션 캔버스 작업](using/segment/composition-canvas.md)
      + [대상자 액세스 및 관리](using/segment/access-audiences.md)
   + [라이선스 사용](using/segment/license-usage.md)
+ 추적 및 모니터링 {#reporting}
   + 라이브 보고서 {#live-report}
      + [라이브 보고서 시작](using/reports/live-report.md)
      + [여정 라이브 보고서](using/reports/journey-live-report.md)
      + [캠페인 실시간 보고서](using/reports/campaign-live-report.md)
      + [랜딩 페이지 실시간 보고서](using/reports/lp-report-live.md)
      + [구독 목록 실시간 보고서](using/reports/subscription-report-live.md)
   + 글로벌 보고서 {#global-report}
      + [글로벌 보고서 시작](using/reports/global-report.md)
      + [여정 글로벌 보고서](using/reports/journey-global-report.md)
      + [캠페인 글로벌 보고서](using/reports/campaign-global-report.md)
      + [랜딩 페이지 글로벌 보고서](using/reports/lp-report-global.md)
      + [구독 목록 글로벌 보고서](using/reports/subscription-report-global.md)
   + 여정 보고서 {#reports}
      + [여정 보고서 만들기](using/reports/sharing-overview.md)
      + [단계 이벤트 필드 목록](using/reports/sharing-field-list.md)
      + 레거시 단계 이벤트 필드 {#legacy-step-event-fields}
         + [레거시 필드 정보](using/reports/sharing-legacy-fields.md)
         + [여정 필드](using/reports/sharing-journey-fields.md)
         + [공통 필드](using/reports/sharing-common-fields.md)
         + [작업 실행 필드](using/reports/sharing-execution-fields.md)
         + [데이터 가져오기 필드](using/reports/sharing-fetch-fields.md)
         + [ID 필드](using/reports/sharing-identity-fields.md)
      + [쿼리 예제](using/reports/query-examples.md)
   + 전달성 {#deliverability}
      + [전달성 시작](using/reports/deliverability.md)
      + [제외 목록 이해하기](using/reports/suppression-list.md)
   + [경고](using/reports/alerts.md)
   + [Customer Journey Analytics 작업](using/reports/cja-ajo.md)
+ 의사 결정 관리 {#offer-decisioning}
   + 의사 결정 관리 시작 {#get-started-decision}
      + [의사 결정 관리 정보](using/offers/get-started/starting-offer-decisioning.md)
      + [사용자 인터페이스](using/offers/get-started/user-interface.md)
      + [오퍼를 만들고 관리하는 주요 단계](using/offers/offer-library/key-steps.md)
      + [사용 사례: 이메일에 오퍼 삽입](using/offers/offers-e2e.md)
   + 구성 요소 만들기 {#create-components}
      + [배치 만들기](using/offers/offer-library/creating-placements.md)
      + [의사 결정 규칙 만들기](using/offers/offer-library/creating-decision-rules.md)
      + [태그 만들기](using/offers/offer-library/creating-tags.md)
   + {#rankings} 등급 만들기
      + [등급 시작](using/offers/ranking/get-started-rankings.md)
      + [등급 공식](using/offers/ranking/create-ranking-formulas.md)
      + AI 모델 {#ai-models}
         + [AI 모델 정보](using/offers/ranking/ai-models.md)
         + AI 모델 유형 {#ai-model-types}
            + [자동 최적화 모델](using/offers/ranking/auto-optimization-model.md)
            + [개인화된 최적화 모델](using/offers/ranking/personalized-optimization-model.md)
         + AI 모델 만들기 {#configure-ai-model}
            + [이벤트를 수집할 데이터 세트 만들기](using/offers/ranking/create-dataset.md)
            + [AI 모델 만들기](using/offers/ranking/create-ranking-strategies.md)
            + [이벤트 캡처 구성](using/offers/ranking/schema-requirement.md)
   + 오퍼 만들기 및 관리 {#managing-offers-in-the-offer-library}
      + 오퍼 구성 {#configure-offers}
         + [개인화된 오퍼 만들기](using/offers/offer-library/creating-personalized-offers.md)
         + [표시 추가](using/offers/offer-library/add-representations.md)
         + [제한 추가](using/offers/offer-library/add-constraints.md)
      + [대체 오퍼 만들기](using/offers/offer-library/creating-fallback-offers.md)
      + [컬렉션 만들기](using/offers/offer-library/creating-collections.md)
   + 의사 결정을 만들고 관리하기 {#create-manage-activities}
      + [의사 결정 만들기](using/offers/offer-activities/create-offer-activities.md)
      + [의사 결정에서 오퍼 선택 구성](using/offers/offer-activities/configure-offer-selection.md)
      + [시뮬레이션 만들기](using/offers/offer-activities/simulation.md)
   + [일괄 의사 결정](using/offers/batch-delivery.md)
   + 의사 결정 관리 보고서 만들기 {#create-reports}
      + [의사 결정 관리 이벤트 시작](using/offers/reports/get-started-events.md)
      + [의사 결정 관리 이벤트 주요 정보](using/offers/reports/key-information.md)
      + [이벤트 XDM 필드 액세스](using/offers/reports/xdm-fields.md)
   + 오퍼 카탈로그 내보내기 {#export-catalog}
      + [오퍼 카탈로그 내보내기 시작 ](using/offers/export-catalog/get-started-export.md)
      + [내보낸 오퍼 카탈로그에 액세스하기](using/offers/export-catalog/access-dataset.md)
      + [개인화된 오퍼 데이터 세트](using/offers/export-catalog/export-offers.md)
      + [의사 결정 데이터 세트](using/offers/export-catalog/export-decisions.md)
      + [배치 데이터 세트](using/offers/export-catalog/export-placements.md)
      + [대체 데이터 세트](using/offers/export-catalog/export-fallback.md)
   + API 참조 {#api-reference}
      + [시작](using/offers/api-reference/getting-started.md)
      + API를 사용하여 오퍼 만들기 및 관리 {#offers-api}
         + 배치 {#placements}
            + [배치 나열](using/offers/api-reference/offers-api/placements/placements-list.md)
            + [배치 조회](using/offers/api-reference/offers-api/placements/lookup.md)
            + [배치 만들기](using/offers/api-reference/offers-api/placements/create.md)
            + [배치 업데이트](using/offers/api-reference/offers-api/placements/update.md)
            + [배치 삭제](using/offers/api-reference/offers-api/placements/delete.md)
         + 의사 결정 규칙 {#decision-rules}
            + [의사 결정 규칙 나열](using/offers/api-reference/offers-api/decision-rules/rules-list.md)
            + [의사 결정 규칙 조회](using/offers/api-reference/offers-api/decision-rules/lookup.md)
            + [의사 결정 규칙 만들기](using/offers/api-reference/offers-api/decision-rules/create.md)
            + [의사 결정 규칙 업데이트](using/offers/api-reference/offers-api/decision-rules/update.md)
            + [의사 결정 규칙 삭제](using/offers/api-reference/offers-api/decision-rules/delete.md)
         + 태그 {#tags}
            + [태그 나열](using/offers/api-reference/offers-api/tags/tags-list.md)
            + [태그 조회](using/offers/api-reference/offers-api/tags/lookup.md)
            + [태그 만들기](using/offers/api-reference/offers-api/tags/create.md)
            + [태그 업데이트](using/offers/api-reference/offers-api/tags/update.md)
            + [태그 삭제](using/offers/api-reference/offers-api/tags/delete.md)
         + 개인화된 오퍼 {#personalized-offers}
            + [개인화된 오퍼 나열](using/offers/api-reference/offers-api/personalized-offers/offers-list.md)
            + [개인화된 오퍼 조회](using/offers/api-reference/offers-api/personalized-offers/lookup.md)
            + [개인화된 오퍼 만들기](using/offers/api-reference/offers-api/personalized-offers/create.md)
            + [개인화된 오퍼 업데이트](using/offers/api-reference/offers-api/personalized-offers/update.md)
            + [개인화된 오퍼 삭제](using/offers/api-reference/offers-api/personalized-offers/delete.md)
         + 컬렉션 {#collections}
            + [컬렉션 나열](using/offers/api-reference/offers-api/collections/collections-list.md)
            + [컬렉션 조회](using/offers/api-reference/offers-api/collections/lookup.md)
            + [컬렉션 만들기](using/offers/api-reference/offers-api/collections/create.md)
            + [컬렉션 업데이트](using/offers/api-reference/offers-api/collections/update.md)
            + [컬렉션 삭제](using/offers/api-reference/offers-api/collections/delete.md)
         + 대체 오퍼 {#fallback-offers}
            + [대체 오퍼 나열](using/offers/api-reference/offers-api/fallback-offers/fallback-list.md)
            + [대체 오퍼 조회](using/offers/api-reference/offers-api/fallback-offers/lookup.md)
            + [대체 오퍼 만들기](using/offers/api-reference/offers-api/fallback-offers/create.md)
            + [대체 오퍼 업데이트](using/offers/api-reference/offers-api/fallback-offers/update.md)
            + [대체 오퍼 삭제](using/offers/api-reference/offers-api/fallback-offers/delete.md)
      + API를 사용하여 오퍼를 만들고 관리하기 {#activities-api}
         + [의사 결정 나열](using/offers/api-reference/activities-api/activities/activities-list.md)
         + [의사 결정 조회](using/offers/api-reference/activities-api/activities/lookup.md)
         + [의사 결정 만들기](using/offers/api-reference/activities-api/activities/create.md)
         + [의사 결정 업데이트](using/offers/api-reference/activities-api/activities/update.md)
         + [의사 결정 삭제](using/offers/api-reference/activities-api/activities/delete.md)
      + API를 사용하여 오퍼 게재 {#offer-delivery-api}
         + [오퍼 게재 API 시작](using/offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
         + [Decisioning API](using/offers/api-reference/offer-delivery-api/decisioning-api.md)
         + [Edge Decisioning API](using/offers/api-reference/offer-delivery-api/edge-decisioning-api.md)
         + [Batch Decisioning API](using/offers/api-reference/offer-delivery-api/batch-decisioning-api.md)
+ 데이터 관리 {#data-management}
   + [데이터 관리 시작](using/data/gs-data.md)
   + [스키마 작업](using/data/get-started-schemas.md)
   + Journey Optimizer 데이터셋 {#datasets}
      + [데이트 세트 시작](using/data/get-started-datasets.md)
      + [쿼리 예](using/data/datasets-query-examples.md)
   + [쿼리](using/data/get-started-queries.md)
+ 구성{#configuration}
   + [Journey Optimizer 구성 시작](using/configuration/get-started-configuration.md)
   + 이메일 하위 도메인 위임 {#delegate-subdomains}
      + [하위 도메인 위임 시작](using/configuration/about-subdomain-delegation.md)
      + [하위 도메인 위임](using/configuration/delegate-subdomain.md)
      + [Google TXT 레코드 추가](using/configuration/google-txt.md)
      + [PTR 레코드 액세스 및 편집](using/configuration/ptr-records.md)
      + [IP 풀 만들기](using/configuration/ip-pools.md)
   + [채널 표면 설정](using/configuration/channel-surfaces.md)
   + 이메일 주소 모니터링 {#monitor-reputation}
      + [제외 목록](using/configuration/manage-suppression-list.md)
      + [다시 시도](using/configuration/retries.md)
      + [허용 목록](using/configuration/allow-list.md)
   + [아카이브 지원](using/configuration/archiving-support.md)
   + [빈도 규칙 구성](using/configuration/frequency-rules.md)
   + [실행 주소 관리](using/configuration/primary-email-addresses.md)
   + 여정 구성 {#configure-journeys}
      + [데이터 소스, 이벤트 및 작업 정보](using/configuration/about-data-sources-events-actions.md)
      + [외부 시스템과 통합](using/configuration/external-systems.md)
      + 이벤트 구성 {#events-journeys}
         + [일반 원칙](using/event/about-events.md)
         + 단일 이벤트 구성 {#unitary-events}
            + [단일 이벤트 시작](using/event/about-creating.md)
            + [ExperienceEvent 스키마 정보](using/event/experience-event-schema.md)
            + [Adobe Analytics 활용](using/event/about-analytics.md)
         + [비즈니스 이벤트 구성](using/event/about-creating-business.md)
         + [추가적인 이벤트 전송 단계](using/event/additional-steps-to-send-events-to-journey.md)
      + 데이터 소스 구성{#data-source-journeys}
         + [데이터 소스 정보](using/datasource/about-data-sources.md)
         + [데이터 소스 구성](using/datasource/configure-data-sources.md)
         + [Adobe Experience Platform 데이터 소스](using/datasource/adobe-experience-platform-data-source.md)
         + [외부 데이터 소스](using/datasource/external-data-sources.md)
      + 작업 구성 {#action-journeys}
         + [작업 정보](using/action/action.md)
         + [작업 구성](using/action/about-custom-action-configuration.md)
         + [Adobe Campaign Standard 통합](using/action/acs-action.md)
         + [Adobe Campaign v7/v8과 통합](using/action/acc-action.md)
   + [소스](using/start/get-started-sources.md)
+ 액세스 제어 {#access-control}
   + [액세스 제어 개요](using/administration/permissions-overview.md)
   + [내장 제품 프로필](using/administration/ootb-product-profiles.md)
   + [사용자 및 제품 프로필 관리](using/administration/permissions.md)
   + [권한 수준](using/administration/high-low-permissions.md)
   + [샌드박스 관리](using/administration/sandboxes.md)
   + [속성 기반 액세스 제어](using/administration/attribute-based-access.md)
   + [객체 수준 액세스 제어](using/administration/object-based-access.md)
+ 개인정보 보호 {#privacy}
   + [개인 정보 시작](using/privacy/get-started-privacy.md)
   + [개인 정보 보호 요청](using/privacy/requests.md)
   + [리소스에 대한 작업 감사](using/privacy/audit-logs.md)
   + [데이터 위생 작업 수행](using/privacy/data-hygiene.md)
   + 동의 관리 {#consent}
      + [옵트아웃 관리](using/privacy/opt-out.md)
      + [동의 정책 사용](using/action/consent.md)
   + [데이터 거버넌스](using/action/action-privacy.md)
