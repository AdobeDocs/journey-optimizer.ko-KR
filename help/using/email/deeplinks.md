---
solution: Journey Optimizer
product: journey optimizer
title: 이메일 및 SMS 메시지에서 딥링크 사용 및 구성
description: 이메일 및 SMS 콘텐츠에 딥링크를 추가하는 방법과 iOS 및 Android 앱에서 딥링크 처리를 구현하는 방법을 알아봅니다.
feature: Email, SMS
topic: Content Management
role: User, Developer
level: Intermediate
keywords: 딥링크, 딥링크, 범용 링크, 앱 링크, 이메일, sms
source-git-commit: 3d3218e24074ffb8ec36f1ec14ff8a6c45950d90
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 1%

---


# 이메일 및 SMS에서 딥 링크 사용 및 구성 {#deeplinks}

딥 링크를 사용하면 이메일 또는 SMS 메시지에서 수신자를 모바일 앱의 특정 화면이나 콘텐츠로 안내할 수 있습니다. 웹 브라우저나 앱스토어를 통해 라우팅하지 않고도 의도한 인앱 여정으로 바로 이동할 수 있으므로 사용자가 브랜드에 맞게 적절한 작업을 수행할 수 있습니다.

수신자가 딥링크를 클릭하면 의도한 인앱 콘텐츠로 바로 이동합니다. **완료한 경우**:

* Journey Optimizer의 [구성 단계](#configuration);

* 모바일 앱에서 iOS 및 Android에 대한 [모바일 앱 구현](#mobile-implementation) 단계입니다.

>[!NOTE]
>
>[!DNL Adobe Journey Optimizer]에서는 호환성과 클릭 추적을 보장하기 위해 추적된 URL(`/ee/v1/mclick/*`)을 사용하여 iOS과 Android 모두에 대한 딥링크를 지원합니다.

## 딥링크 작성 {#authoring}

### 이메일 {#authoring-email}

이메일 메시지의 경우 딥 링크를 삽입하는 두 가지 옵션이 있습니다.

* **전자 메일 Designer**: [링크 추적이 활성화되어 있는지 확인](message-tracking.md#enable-tracking). 연결할 요소(텍스트, 단추 또는 이미지)를 선택하고 상황별 도구 모음에서 **[!UICONTROL 링크 삽입]**&#x200B;을 클릭한 다음 **[!UICONTROL 딥링크]**&#x200B;를 선택하여 딥링크 URL을 입력합니다. [링크 삽입에 대한 자세한 정보](message-tracking.md#insert-links)

* **Personalization 편집기(코드)**: 다음 코드 조각을 사용하여 HTML에 바로 딥링크를 삽입합니다.

  ```html
  <a class="arc-link" data-nl-type="DEEPLINK" href="<<deeplink_url>>" id="acr-link-7821368" style="text-decoration:underline;" target="_blank" data-tracking-type="DEEPLINK">Click Here</a>
  ```

  `<<deeplink_url>>`을(를) 실제 딥링크 URL로 바꾸고 각 블록에 대해 고유한 `id`을(를) 사용하여 충돌을 방지하십시오.

### SMS {#authoring-sms}

SMS의 경우, 딥링크는 개인화 편집기에서 **Url** 도우미 함수를 사용하여 작성됩니다. [이 섹션](../sms/create-sms.md#sms-content)에서 SMS 콘텐츠에 링크를 추가하는 방법에 대해 자세히 알아보세요.

SMS 콘텐츠에 딥링크를 삽입하려면 다음 구문을 사용합니다.

```
{{url originalUrl='<<url>>' type='DEEPLINK' action='CLICK'}}
```

`<<url>>`을(를) 실제 딥링크 URL로 바꾸십시오.

## Journey Optimizer의 구성 {#configuration}

모바일 앱용 이메일 및 SMS에서 딥 링크를 사용하려면 아래 구성 단계를 완료하십시오.

>[!NOTE]
>
>이 섹션은 **범용 링크(iOS)** 및 **앱 링크(Android)**(HTTPS 기반 딥링크)를 사용하는 경우에 적용됩니다.

1. Journey Optimizer에서 딥링크가 활성화된 하위 도메인을 위임합니다. [자세히 알아보기](../configuration/delegate-subdomain.md)

1. 하위 도메인에서 iOS용 AASA 파일 및 Android용 assetLinks.json 파일을 호스팅합니다. 자세한 내용은 [Adobe 고객 지원 센터](https://helpx.adobe.com/kr/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} 또는 Adobe 담당자에게 문의하십시오.

   * AASA(iOS)의 **1}:**
      * 위임된 하위 도메인
      * 앱 번들 ID
   * **Android(assetLinks.json)의 경우**:
      * 위임된 하위 도메인
      * 앱 번들 ID
      * SHA-256 인증서 지문

>[!IMPORTANT]
>
>Adobe 인프라를 통한 딥링크는 SMS 캠페인에 대한 [전자 메일 추적 설정](message-tracking.md#enable-tracking) 또는 **[!UICONTROL 작업 추적]** 섹션에서 메시지에 대해 링크 추적이 활성화되면 적용됩니다. 추적된 딥링크 클릭은 Adobe에서 호스팅 및 확인하는 `/ee/v1/mclick/*`의 URL을 사용합니다.
>
>**추적되지 않는** 링크의 경우 Adobe 시스템을 통해 URL이 다시 작성되지 않습니다. 범용 링크 또는 앱 링크를 자체 도메인 및 호스팅에 구성하여 해당 링크가 의도한 대로 앱을 열도록 해야 합니다.

## 모바일 앱 구현 {#mobile-implementation}

이 섹션에서는 일반적인 **HTTPS** 설정(범용 링크 및 앱 링크)에서 단일 URL이 다음을 수행할 수 있도록 [!DNL Adobe Journey Optimizer]을(를) 사용하여 모바일 딥링크를 구현하는 방법을 설명합니다.

* 앱이 설치되면 모바일 앱 내의 특정 화면을 엽니다. 또는
* 앱이 설치되지 않은 경우 웹 사이트를 대체 항목으로 엽니다.

메시지에 대해 링크 추적이 활성화되면 [!DNL Journey Optimizer]은(는) 이러한 클릭을 계속 추적하여 보고에 포함시키며, 메시지에서 실행하는 경우 [콘텐츠 실험](../content-management/content-experiment.md)에서 사용할 수 있습니다.

이 섹션에서는 딥링크에 대한 일반적인 구현 패턴을 제공합니다. 정확한 설정은 앱 아키텍처 및 라우팅 프레임워크에 따라 다릅니다.

### iOS(범용 링크) {#ios-implementation}

1. Xcode에서 **[!UICONTROL 서명 및 기능]** > **[!UICONTROL + 기능]** > **[!UICONTROL 관련 도메인]**&#x200B;을 통해 대상을 선택합니다.
1. 위임된 하위 도메인에 대한 항목을 추가합니다. 예:

   ```text
   applinks:www.mybusiness.com
   applinks:data.email.mybusiness.com
   ```

1. 앱에서 범용 링크를 처리하고 응답 헤더에서 원래 링크를 가져옵니다.

   +++ 예: iOS 13+(장면 포함)

   ```swift
   class SceneDelegate: UIResponder, UIWindowSceneDelegate {
   
       func scene(_ scene: UIScene,
                 continue userActivity: NSUserActivity) {
           guard userActivity.activityType == NSUserActivityTypeBrowsingWeb,
                 let incomingURL = userActivity.webpageURL else {
               return
           }
   
           handleUniversalLink(url: incomingURL)
       }
   
       private func handleUniversalLink(url: URL) {
           // Only handle AJO tracked mobile clicks
           guard url.host == "data.email.mybusiness.com",
                 url.path.hasPrefix("/ee/v1/mclick") else {
               // Could also handle direct www.mybusiness.com links here
               return
           }
   
           resolveTrackedUrlAndRoute(url)
       }
   
       private func resolveTrackedUrlAndRoute(_ trackedUrl: URL) {
           var request = URLRequest(url: trackedUrl)
           request.httpMethod = "GET"
   
           URLSession.shared.dataTask(with: request) { _, response, error in
               guard error == nil,
                     let httpResponse = response as? HTTPURLResponse,
                     let locationValue = httpResponse.allHeaderFields["Location"] as? String,
                     let finalUrl = URL(string: locationValue) else {
                   return
               }
   
               DispatchQueue.main.async {
                   self.routeToDestination(finalUrl)
               }
           }.resume()
       }
   
       private func routeToDestination(_ url: URL) {
           // Example: map URL paths to screens
           // https://www.mybusiness.com/dashboard/offers/coupons
           // → OffersViewController for Coupons
       }
   }
   ```

   +++

>[!IMPORTANT]
>
>앱은 `mclick` URL에서 **GET**&#x200B;을(를) 수행하고 **`Location`** 헤더를 읽은 다음 **final** URL을 기반으로 라우팅해야 합니다.
>
>Safari에서 `mclick` URL을 열지 마십시오. 딥링크의 목적을 무시합니다.

### Android(앱 링크) {#android-implementation}

1. Android 앱에 앱 링크 의도 필터를 추가합니다.

   ```xml
   <activity
       android:name=".DeepLinkActivity"
       android:exported="true">
   
       <intent-filter android:autoVerify="true">
           <action android:name="android.intent.action.VIEW" />
           <category android:name="android.intent.category.DEFAULT" />
           <category android:name="android.intent.category.BROWSABLE" />
   
           <data
               android:scheme="https"
               android:host="data.email.mybusiness.com"
               android:pathPrefix="/ee/v1/mclick" />
       </intent-filter>
   
   </activity>
   ```

1. 딥링크 핸들러를 구현합니다.

   +++ 코틀린에서:

   ```kotlin
   class DeepLinkActivity : AppCompatActivity() {
   
       override fun onCreate(savedInstanceState: Bundle?) {
           super.onCreate(savedInstanceState)
   
           val trackedUri = intent?.data
           if (trackedUri == null ||
               trackedUri.host != "data.email.mybusiness.com" ||
               !trackedUri.path.orEmpty().startsWith("/ee/v1/mclick")) {
               finish()
               return
           }
   
           resolveTrackedUrlAndRoute(trackedUri)
       }
   
       private fun resolveTrackedUrlAndRoute(trackedUri: Uri) {
           lifecycleScope.launch(Dispatchers.IO) {
               try {
                   val finalUrl = followRedirect(trackedUri.toString())
                   withContext(Dispatchers.Main) {
                       routeToDestination(finalUrl)
                       finish()
                   }
               } catch (e: Exception) {
                   // Optionally log error, fallback to browser
                   finish()
               }
           }
       }
   
       private fun followRedirect(trackedUrl: String): Uri {
           val client = OkHttpClient.Builder()
               .followRedirects(false) // We want to read Location ourselves
               .build()
   
           val request = Request.Builder()
               .url(trackedUrl)
               .get()
               .build()
   
           client.newCall(request).execute().use { response ->
               val location = response.header("Location")
                   ?: throw IllegalStateException("Missing Location header")
               return Uri.parse(location)
           }
       }
   
       private fun routeToDestination(finalUri: Uri) {
           // Example: interpret https://www.mybusiness.com/dashboard/offers/coupons
           // and open the correct Activity / Fragment
       }
   }
   ```

   +++

>[!IMPORTANT]
>
>iOS과 마찬가지로 앱은 `mclick` URL을 호출하고 **`Location`** 헤더를 사용하여 최종 대상을 결정해야 합니다.
>
>리디렉션 처리를 제어하고 필요한 경우 분석을 정확하게 기록할 수 있도록 `followRedirects(false)`을(를) 사용합니다.
>
>라우팅 논리는 앱별로 다르므로 URL에서 화면으로의 명확한 매핑을 정의합니다.

## 권장 사례 {#deeplink-best-practices}

* **안정적인 경로 사용**: 앱 UI 변경에 탄력적인 경로를 선호합니다(예: `/tab/3/view/2` 대신 `/account/orders`).
* **추적된 경로에 대한 계정**: 링크 추적이 활성화되면 클릭한 링크는 추적된 경로 패턴(예: `/ee/v1/mclick/`)을 사용할 수 있습니다. 추적된 링크를 확인한 후 라우터가 최종 URL을 구문 분석할 수 있는지 확인합니다.
* **매개 변수를 예측 가능한 상태로 유지**: 일관된 매개 변수 체계를 정의합니다(예: `?orderId=12345`).
* **URL에 중요한 데이터를 사용하지 마십시오**: 딥링크 URL에 직접 비밀 또는 개인 데이터를 넣지 마십시오.
* **딥 링크를 테스트합니다**: 증명을 보내고 앱이 설치된 장치에서 딥 링크를 클릭합니다.
* **실제 장치에서 유효성 검사**: 범용 링크 및 추적된 링크 확인 동작은 시뮬레이터보다 실제 장치에서 유효성을 검사하는 데 더 안정적입니다.
* **앱 측 라우팅 유효성 검사**: 딥링크가 필요한 화면을 열지 않으면 앱 측 라우팅 및 URL 형식(호스트/경로/쿼리 및 URL 인코딩)을 검사하십시오.
* **앱 초기화를 염두에 두십시오**: 앱 링크/범용 링크 동작은 앱을 한 번 이상 설치하고 연 후에 가장 안정적입니다.

## 문제 해결 및 FAQ {#troubleshooting-faq}

+++ 딥 링크를 탭해도 앱이 열리지 않습니다.

* 링크 추적이 활성화된 경우 추적된 클릭 경로를 포함하여 URL이 앱이 처리하도록 등록된 호스트 및 경로 패턴과 일치하는지 확인합니다(예: `/ee/v1/mclick/` 아래의 경로).
* iOS 범용 링크 및 Android 앱 링크의 경우 도메인 연결(AASA / `assetlinks.json`)이 올바르게 구성되어 연결할 수 있는지 확인하십시오.
* 실제 장치에서 테스트합니다(시뮬레이터/에뮬레이터는 링크 연결에 대해 다르게 작동할 수 있음).

+++

+++ 앱이 열리지만 예상 화면으로 이동하지 않습니다.

* 앱 측 라우터가 URL 경로/쿼리를 올바르게 구문 분석하는지 확인합니다.
* URL 인코딩 확인: 예약된 문자는 URL로 인코딩해야 합니다.
* 매개 변수 이름 및 값이 라우터의 예상 값과 일치하는지 확인합니다.

+++

+++ 앱이 설치되지 않으면 어떻게 됩니까?

* 웹 사이트에서 동일한 HTTPS URL을 제공할 수 있는 경우 링크는 앱이 설치되지 않은 경우 대체 항목으로 웹 페이지를 열 수 있습니다(그에 따라 웹 대상 및 라우팅을 구성).

+++

+++ 매개 변수에 특수 문자를 안전하게 포함하려면 어떻게 해야 합니까?

URL 인코딩 쿼리 매개 변수 값입니다. 이렇게 하면 게재 및 렌더링 문제가 줄어들고 앱의 구문 분석 오류가 방지됩니다.

+++

+++ 엔드투엔드 테스트를 어떻게 수행합니까?

* 딥 링크를 사용하여 증명을 만든 후 iOS 및 Android 장치(설치 및 설치되지 않은 시나리오)에서 클릭합니다.
* 유효성 검사:
   * 최종 이메일 또는 SMS 링크 값(호스트/경로/쿼리)
   * OS 수준 연결(범용 링크/앱 링크를 사용하는 경우)
   * 인앱 라우팅 결과

+++

+++ 나는 하나의 앱이 있지만 조직에 대한 하위 도메인은 다릅니다. 각 하위 도메인에 대해 AASA 및 assetLinks.json을 생성하도록 요청해야 합니까?

예. 위임된 모든 하위 도메인을 정의하려면 기능을 지원해야 하는 각 하위 도메인에 대해 AASA 및 `assetlinks.json` 구성을 요청하십시오.

+++

+++ 구성된 URL에서 딥링크 형식을 사용해야 합니까(예: `appname://path`)?

사용자 지정 URL 체계(예: `appname://path`)를 사용할 수 있지만 권장되는 접근 방식은 범용 링크 또는 앱 링크(`https://`)로서, 이 페이지의 구성 및 구현 섹션에 있는 HTTPS 기반 설정과 일치합니다.

+++

+++ Analytics용 모바일 앱에서 URL의 UTM 매개 변수를 사용할 수 있습니까?

예. [!DNL Journey Optimizer]에서 구성하는 UTM 매개 변수는 앱이 `mclick` URL에서 GET을 수행할 때 `Location` 헤더에 반환되는 최종 URL에 포함되므로 인앱 분석에 사용할 수 있습니다.

+++

+++ `/ee/v1/click/` URL의 사용자 경험은 무엇입니까?

링크는 이 페이지에 설명된 `mclick` 흐름을 통해 앱 딥링크로 처리되지 않고, 장치의 기본 웹 브라우저(표준 클릭 추적 동작)에서 열립니다.

+++
