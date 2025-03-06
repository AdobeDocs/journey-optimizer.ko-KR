---
title: 도우미 함수 시작
description: Journey Optimizer Helper 함수 라이브러리
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 9b0b0d8e-a819-4d2e-a241-f3c4d104eab9
source-git-commit: ff6619925a36d2687922d1b631d1cabbcb98167e
workflow-type: tm+mt
source-wordcount: '2388'
ht-degree: 27%

---

# 도우미 함수 시작{#functions}

[!DNL Journey Optimizer] 템플릿 언어를 사용하여 계산, 데이터 형식 지정 또는 전환, 조건 등 데이터에 대한 작업을 수행하고, 개인화의 컨텍스트에서 이를 조작합니다. [이 페이지](../personalization-syntax.md)에서 개인화 구문 지침을 알아보세요.

➡️[이 비디오에서 도우미 함수를 사용하는 방법을 알아보세요](#video)

템플릿 언어는 아래와 같이 개인화 편집기의 개인화 드롭다운 목록에서 사용할 수 있는 도우미 함수에서 활용됩니다.

![](../assets/access-helper-functions.png)

>[!NOTE]
>
>개인화 편집기에서 사용할 수 있는 기능 및 기능은 [여정 고급 표현식 편집기](../../building-journeys/expression/expressionadvanced.md)에서 사용할 수 있는 기능 및 기능과 다릅니다.

[!DNL Journey Optimizer] 개인화 편집기에서 도우미 함수는 [함수](#functions-helper), [도우미](#helper-helper) 및 [연산자](#operators-helper)의 세 가지 범주로 그룹화됩니다.

카테고리를 선택하여 하위 카테고리 및 기능에 액세스합니다.

`>` 아이콘을 클릭하여 하위 범주에 액세스합니다. `+` 아이콘을 클릭하여 함수를 선택하십시오. 함수는 자동으로 개인화 화면에 추가됩니다.

`...` 아이콘을 클릭하여 함수에 대한 설명을 보고 즐겨찾기에 추가합니다. [자세히 알아보기](../personalize.md#fav)

## 함수{#functions-helper}

### 집계 및 스토리지 기능

<table>
    <tr>
        <td><a href="aggregation.md#average">평균</a></td><td>이 함수는 배열에서 선택한 모든 값의 산술 평균을 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">계수</a></td><td>이 함수는 특정 배열에서 요소의 수를 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-only-null">null만 계산</a></td><td>이 함수는 목록의 null 값 숫자를 계산합니다.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-with-null">null이 포함된 개수</a></td><td>이 함수는 null 값을 포함하여 목록의 모든 요소를 계산합니다.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">고유</a></td><td>이 함수는 중복 값이 제거된 배열 또는 목록에서 값을 가져옵니다.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct-count-with-null">null이 포함된 고유 개수</a></td><td>이 함수는 null 값을 포함한 다른 값의 수를 계산합니다.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">첫 번째 항목</a></td><td>이 함수는 배열 또는 목록의 첫 번째 항목을 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">배열의 첫 번째 n</a></td><td>이 함수는 특정 수식에 따라 내림차순으로 정렬되면 배열에서 첫 번째 'N' 항목을 반환합니다</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">안에 있음</a></td><td>이 함수는 항목이 배열의 멤버인지 또는 목록의 멤버인지 확인하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">다음을 포함</a></td><td>이 함수는 배열 또는 목록에 지정된 항목이 포함되어 있는지 확인합니다.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">교차</a></td><td>이 함수는 두 배열 또는 목록에 최소 하나 이상의 공통 멤버가 있는지 확인합니다.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">배열의 마지막 n</a></td><td>이 함수는 특정 수식에 따라 내림차순으로 정렬되면 배열에서 마지막 'N' 항목을 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">최대</a></td><td>이 함수는 배열에서 선택한 모든 값 중 가장 큰 값을 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">최소</a></td><td>이 함수는 배열에서 선택한 모든 값 중 가장 작은 값을 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">안에 없음</a></td><td>이 함수는 항목이 배열의 멤버인지 또는 목록의 멤버가 아닌지 확인합니다.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">하위 집합</a></td><td>이 함수는 특정 배열(배열 A)이 다른 배열(배열 B)의 하위 집합인지 여부, 즉 배열 A의 모든 요소가 배열 B의 요소인지 여부를 결정합니다</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">합계</a></td><td>이 함수는 배열에서 선택한 모든 값의 합계를 반환합니다.</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">상위 집합</a></td><td>이 함수는 특정 배열(배열 A)이 다른 배열(배열 B)의 상위 집합인지, 즉 배열 A에 배열 B의 모든 요소가 포함되어 있는지 확인합니다</td>
    </tr>
</table>

### 날짜 시간 함수{#date-functions}

<table>
    <tr>
        <td><a href="dates.md#add-days">일 추가</a></td><td>이 함수는 양수 값을 사용하여 증가 값을 하고 음수 값을 사용하여 지정된 일 수만큼 지정된 날짜를 조정합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-hours">시간 추가</a></td><td>이 함수는 양수 값을 사용하여 증분 및 음수 값을 사용하여 지정된 시간 수만큼 지정된 날짜를 조정합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-minutes">분 추가</a></td><td>이 함수는 양수 값을 사용하여 증분 및 음수 값을 사용하여 지정된 분 단위로 지정된 날짜를 조정합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-months">월 추가</a></td><td>이 함수는 양수 값을 사용하여 증가 값을 하고 음수 값을 사용하여 지정된 개월 수만큼 지정된 날짜를 조정합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-seconds">초 추가</a></td><td>이 함수는 양수 값을 사용하여 증분 및 음수 값을 사용하여 지정된 시간(초)만큼 지정된 날짜를 조정합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-years">년 추가</a></td><td>이 함수는 양수 값을 사용하여 증가 값을 하고 음수 값을 사용하여 지정된 연도 수만큼 지정된 날짜를 조정합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#age">처리 시간</a></td><td>이 함수는 특정 날짜의 연령을 검색합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#age-days">나이 (일 기준)</a></td><td>이 함수는 특정 일자의 기간(예: 특정 일자와 현재 일자 사이에 경과된 일 수)을 계산합니다. 이 수치는 미래 일자의 경우 음수이고, 과거 일자의 경우 양수입니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#age-months">나이 (월 기준)</a></td><td>이 함수는 특정 날짜의 기간(예: 특정 날짜와 현재 날짜 사이에 경과된 개월 수)을 월 단위로 계산합니다. 이 수는 미래 날짜의 경우 음수이고, 과거 날짜의 경우 양수입니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#compare-dates">날짜 비교</a></td><td>이 함수는 첫 번째 입력 날짜를 다른 날짜와 비교합니다. date1이 date2와 같으면 0을 반환하고, date1이 date2보다 앞에 오면 -1을 반환하고, date1이 date2보다 뒤에 오면 1을 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#convert-zoned-date-time">ZonedDateTime 변환</a></td><td>이 함수는 날짜-시간을 지정된 시간대로 변환합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#current">현재 시간(밀리초)</a></td><td>이 함수는 현재 시간을 에포크 밀리초 단위로 검색합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#date-diff">날짜 차이</a></td><td>이 함수는 일 수로 두 날짜 간의 차이를 검색합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-month">월일</a></td><td>이 함수는 해당 월의 일자를 나타내는 숫자를 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-week">요일</a></td><td>이 함수는 요일을 검색합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-year">연간 일자</a></td><td>이 함수는 연간 일자를 검색합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-seconds">초 단위 차이</a></td><td>이 함수는 초 단위로 두 날짜의 차이를 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-hours">시간 추출</a></td><td>이 함수는 주어진 타임스탬프에서 시간 구성 요소를 추출합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-minutes">분 추출</a></td><td>이 함수는 주어진 타임스탬프에서 분 구성 요소를 추출합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-months">월 추출</a></td><td>이 함수는 주어진 타임스탬프에서 월 구성 요소를 추출합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-seconds">초 추출</a></td><td>이 함수는 주어진 타임스탬프에서 초 구성 요소를 추출합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date">날짜 포맷</a></td><td>이 함수는 날짜 시간 값의 형식을 지정합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date-locale">로케일 지원을 사용하여 날짜 형식 지정</a></td><td>이 함수는 날짜 시간 값의 형식을 해당 언어 구분 표시, 즉 원하는 로케일로 지정합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#get-current-zoned-date-time">CurrentZonedDateTime 가져오기</a></td><td>이 함수는 표준 시간대 정보와 함께 현재 날짜와 시간을 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#hours-difference">시간 차이</a></td><td>이 함수는 시간 측면에서 두 날짜 간의 차이를 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-minutes">분 차이</a></td><td>이 함수는 분 단위로 두 날짜 간의 차이를 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#months-difference">월 차이</a></td><td>이 함수는 월 단위로 두 날짜 간의 차이를 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-days">요일 설정</a></td><td>이 함수는 특정 날짜-시간에 대한 월 중 특정 일을 설정합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-hours">시간 설정</a></td><td>이 함수는 날짜-시간의 시간을 설정합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-date-time">날짜로 변환</a></td><td>이 함수는 문자열을 날짜로 변환합니다. 잘못된 입력에 대한 출력으로 에포크 날짜를 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-utc">UTC로 변환</a></td><td>이 함수는 날짜/시간을 UTC로 변환합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-day">일의 시작으로 잘라내기</a></td><td>이 함수는 주어진 날짜-시간을 하루의 시작 시간으로 설정하고 시간을 00:00으로 설정합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-quarter">truncateToStartOfQuarter</a></td><td>이 함수는 00:00에 분기 첫째 날(예: 1월 1일, 4월 1일, 7월 1일, 10월 1일)까지 날짜-시간을 자릅니다.
</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-week">truncateToStartOfWeek</a></td><td>이 함수는 주어진 날짜-시간을 주 시작(월요일 00:00)으로 설정하여 수정합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-year">truncateToStartOfYear</a></td><td>이 함수는 주어진 날짜-시간을 해당 연도의 첫날(1월 1일) 00:00으로 잘라 수정합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#week-of-year">연간 주</a></td><td>이 함수는 연간 주를 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-years">연도 차이</a></td><td>이 함수는 연도 단위로 두 날짜 간의 차이를 반환합니다.</td>
    </tr>
</table>
</table>

### 맵 함수 {#map-functions}

<table>
    <tr>
        <td><a href="maps.md#get">다운로드</a></td><td>이 함수는 특정 키에 대한 맵의 값을 검색하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">키</a></td><td>이 함수는 특정 맵에 대한 모든 키를 검색하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">값</a></td><td>이 함수는 특정 맵의 모든 값을 검색합니다.</td>
    </tr>
</table>

### 수학 함수 {#math-functions}

<table>
    <tr>
        <td><a href="math.md#absolute">절대</a></td><td>이 함수는 모든 숫자를 해당 언어 구분 표현으로 서식을 지정합니다.</td>
    </tr>
    <tr>
        <td><a href="math.md#format-number">포맷 번호</a></td><td>이 함수는 모든 숫자를 해당 언어 구분 표현으로 서식을 지정합니다.</td>
    </tr>
    <tr>
        <td><a href="math.md#random">무작위</a></td><td>이 함수는 0과 1 사이의 임의 값을 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="math.md#round-down">내림</a></td><td>이 함수는 숫자를 내림합니다.</td>
    </tr>
    <tr>
        <td><a href="math.md#round-up">올림</a></td><td>이 함수는 숫자를 올림합니다.</td>
    </tr>
    <tr>
    <td><a href="math.md#to-hex-string">16진수 문자열로 변환</a></td><td>는 임의의 숫자를 16진수 문자열로 변환합니다.</td>
    </tr>
    <tr>
    <td><a href="math.md#to-int">대상 정수</a></td><td>이러한 유형(숫자, 더블, int, long, float, short, 바이트, 부울, 문자열) 중 하나를 정수로 변환합니다.</td>
    </tr>
    <tr>
        <td><a href="math.md#to-percentage">백분율로 변환</a></td><td>이 함수는 숫자를 백분율로 변환합니다.</td>
    </tr>
    <tr>
        <td><a href="math.md#to-precision">전체 자릿수로 변환</a></td><td>이 함수는 숫자를 필요한 전체 자릿수로 변환합니다.</td>
    </tr>
    <tr>
        <td><a href="math.md#to-string">대상 문자열</a></td><td>이 함수는 모든 숫자를 문자열 표현으로 변환합니다. </td>
    </tr>
</table>

### 오브젝트 함수 {#object-functions}

<table>
    <tr>
        <td><a href="objects.md#isNotNull">null이 아님</a></td><td>이 함수는 오브젝트 참조가 존재하는지 확인하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">null임</a></td><td>이 함수는 오브젝트 참조가 존재하지 않은지 확인하는 데 사용합니다.</td>
    </tr>
</table>

### 문자열 함수 {#string-functions}

<table>
    <tr>
        <td><a href="string.md#camelCase">카멜 대/소문자</a></td><td>이 함수는 문자열의 각 단어의 첫 번째 문자를 대문자로 사용하는 데 사용합니다</td>
    </tr>
    <tr>
        <td><a href="string.md#char-code-at">의 문자 코드</a></td><td>이 함수는 JavaScript의 charCodeAt 함수와 같은 문자의 ASCII 값을 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#concat">Concat</a></td><td>이 함수는 2개의 문자열을 하나로 결합하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">다음 포함</a></td><td>이 함수는 문자열에 지정된 하위 문자열이 포함되어 있는지 확인하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">포함하지 않음</a></td><td>이 함수는 문자열에 지정된 하위 문자열이 포함되어 있지 않은지 확인하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotEndWith">다음으로 끝나지 않음</a></td><td>이 함수는 문자열이 지정된 하위 문자열로 끝나지 않은지 확인하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotStartWith">다음으로 시작하지 않음</a></td><td>이 함수는 문자열이 지정된 하위 문자열로 시작되지 않는지 확인하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#encode64">인코딩 64</a></td><td>이 함수는 문자열을 인코딩하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">다음으로 끝남</a></td><td>이 함수는 문자열이 지정된 하위 문자열로 끝나는지 확인하는 데 사용합니다.</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">같음</a></td><td>이 함수는 대/소문자 구분을 통해 문자열이 지정된 하위 문자열로 시작되지 않는지 확인하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">대/소문자 무시와 같음</a></td><td>이 함수는 대/소문자를 구분하지 않고 문자열이 지정된 하위 문자열로 시작되지 않는지 확인하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#extractEmailDomain">이메일 도메인 추출</a></td><td>이 함수는 이메일 주소의 도메인을 추출하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#format-currency">통화 포맷</a></td><td>이 함수는 두 번째 인수에서 문자열로 전달된 로케일에 따라 모든 숫자를 해당 언어 구분 통화 표시로 변환합니다</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-host">URL 호스트 다운로드</a></td><td>이 함수는 URL 호스트를 다운로드하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-path">URL 경로 다운로드</a></td><td>이 함수는 URL 경로를 가져오는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-protocol">URL 프로토콜 다운로드</a></td><td>이 함수는 URL 프로토콜을 가져오는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#index-of">색인</a></td><td>이 함수는 (첫 번째 인수에서) 두 번째 매개 변수의 첫 번째 발생 횟수 위치를 반환합니다. 일치하는 항목이 없으면 -1을 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#isEmpty">IsEmpty</a></td><td>이 함수는 문자열이나 표현식이 비어 있는지 확인하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#is-not-empty">비어 있지 않음</a></td><td>이 함수는 매개 변수의 문자열이 비어 있지 않으면 true를 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#last-index-of">마지막 색인</a></td><td>이 함수는 (첫 번째 인수에서) 두 번째 매개 변수의 마지막 발생 횟수 위치를 반환합니다. 일치하는 위치가 없는 경우 -1을 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">Left trim</a></td><td>이 함수는 문자열의 시작에서 공백을 제거합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#length">길이</a></td><td>이 함수는 문자열 또는 표현식의 문자 수를 가져오는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#like">좋아요</a></td><td>이 함수는 문자열이 지정된 패턴과 일치하는지 확인하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">소문자</a></td><td>이 함수는 문자열을 소문자로 변환합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#mask">마스크</a></td><td>이 함수는 문자열의 일부를 "X" 문자로 바꾸는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">일치</a></td><td>이 함수는 문자열이 특정 정규 표현식과 일치하는지 확인하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#md5">MD5</a></td><td>이 함수는 입력 문자열의 MD5 해시를 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">다음과 같지 않음</a></td><td>이 함수는 문자열이 지정된 문자열과 같지 않은지 확인하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#not-equal-with-ignore-case">대/소문자 무시와 같지 않음</a></td><td>이 함수는 대/소문자를 무시하는 2개의 문자열을 비교합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">정규 표현식 그룹</a></td><td>이 함수는 제공된 정규 표현식에 따라 특정 정보를 추출하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">바꾸기</a></td><td>이 함수는 문자열에서 지정된 하위 문자열을 다른 하위 문자열로 대체합니다</td>
    </tr>
    <tr>
        <td><a href="string.md#replaceAll">모두 바꾸기</a></td><td>이 함수는 "target"과 일치하는 텍스트의 모든 하위 문자열을 지정된 리터럴 "replacement" 문자열로 바꿉니다</td>
    </tr>
    <tr>
        <td><a href="string.md#rightTrim">오른쪽 트림</a></td><td>이 함수는 문자열의 끝에서 공백을 제거합니다. </td>
    </tr>
    <tr>
        <td><a href="string.md#split">분할</a></td><td>이 함수는 특정 문자로 문자열을 분할하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">다음으로 시작</a></td><td>이 함수는 문자열이 지정된 하위 문자열로 시작하는지 확인하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-date">문자열을 날짜로 변환</a></td><td>이 함수는 문자열 값을 날짜-시간 값으로 변환합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-integer">문자열을 정수로 변환</a></td><td>이 함수는 문자열 값을 정수 값으로 변환합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-number">문자열을 숫자로 변환</a></td><td>이 함수는 문자열을 숫자로 변환하는 데 사용합니다. 잘못된 입력에 대한 출력으로 동일한 문자열을 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#sub-string">하위 문자열</a></td><td>이 함수는 시작 색인과 종료 색인 사이에서 문자열 표현식의 하위 문자열을 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">제목 대/소문자</a></td><td>이 함수는 문자열의 각 단어의 첫 문자를 대문자로 사용하는 데 사용합니다</td>
    </tr>
    <tr>
        <td><a href="string.md#to-bool">부울로 변환</a></td><td>이 함수는 인수 유형에 따라 인수 값을 부울 값으로 변환합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time">날짜로 변환</a></td><td>이 함수는 문자열을 날짜로 변환하는 데 사용합니다. 잘못된 입력에 대한 출력으로 에포크 날짜를 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time-only">종료 날짜/시간만</a></td><td>이 함수는 인수 값을 날짜/시간 전용 값으로 변환합니다. 잘못된 입력에 대한 출력으로 에포크 날짜를 반환합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">트리밍</a></td><td>이 함수는 문자열의 시작과 끝에서 공백을 제거합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">대문자</a></td><td>이 함수는 문자열을 대문자로 변환합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#url-decode">URL 디코드</a></td><td>이 함수는 URL로 인코딩된 문자열을 디코딩하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="string.md#url-encode">URL 인코드</a></td><td>이 함수는 문자열을 URL 인코딩하는 데 사용합니다.</td>
    </tr>
</table>


## 도우미{#helper-helper}

도우미는 [이 페이지](helpers.md)에 자세히 설명되어 있습니다.


<table>
    <tr>
        <td><a href="helpers.md#default">기본 대체 값</a></td><td>이 함수는 기본값으로 변수를 렌더링하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="helpers.md#each">Each</a></td><td>이 함수는 배열을 반복하는 데 사용합니다.</td>
    </tr>
    <tr>
        <td><a href="helpers.md#if-function">조건</a></td><td>이 함수는 조건부 블록을 정의하는 데 사용합니다. 식 계산이 true를 반환하면 블록이 렌더링됩니다.</td>
    </tr>
    <tr>
        <td><a href="helpers.md#let">Let</a></td><td>이 함수를 사용하면 표현식을 나중에 쿼리에서 사용할 변수로 저장할 수 있습니다</td>
    </tr>
   <tr>
        <td><a href="helpers.md#unless">Unless</a></td><td>이 함수는 조건부 블록을 정의하는 데 사용합니다. 표현식 평가에서 false를 반환하면 블록이 렌더링됩니다.</td>
    </tr>
    <tr>
        <td><a href="helpers.md#with">With</a></td><td>이 함수는 템플릿 일부의 평가 토큰을 변경하는 데 사용합니다.</td>
    </tr>
</table>

## 연산자{#operators-helper}

### 산술 함수 {#arithmetic-helper}

산술 함수는 값에 대한 기본 계산을 수행하는 데 사용됩니다.

<table>
    <tr>
        <td><a href="arithmetic-functions.md#add">더하기</a></td><td>이 연산자는 두 인수 표현식의 합을 찾는 데 사용됩니다.</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#divide">나누기</a></td><td>이 연산자는 두 인수 표현식의 몫을 찾는 데 사용됩니다</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#multiply">곱하기</a></td><td>이 연산자는 두 인수 표현식의 곱을 찾는 데 사용됩니다</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#remainder">나머지</a> </td><td>이 연산자는 두 인수 표현식을 나눈 후 나머지를 찾는 데 사용됩니다</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#substract">빼기</a> </td><td>이 연산자는 두 표현식 간의 차이점을 찾습니다</td>
    </tr>
</table>


### 부울 함수 {#boolean-functions}

부울 함수는 다른 요소에 부울 로직을 수행하는 데 사용됩니다.

<table>
    <tr>
        <td><a href="operators.md#and">And</a></td><td>이 연산자는 논리 결합을 생성합니다.</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">또는</a></td><td>이 연산자는 논리합을 생성합니다.</td>
    </tr>
</table>


### 비교 함수 {#comparison-functions}

비교 함수는 다른 표현식과 값을 비교하는 데 사용되며, 그에 따라 true 또는 false를 반환합니다.

<table>
    <tr>
        <td><a href="operators.md#equals">같음</a></td><td>이 작업은 값이 같은지 확인합니다.</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">보다 큼</a></td><td>이 연산자는 첫 번째 값이 두 번째 값보다 큰지 확인합니다</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">크거나 같음</a></td><td>이 연산자는 첫 번째 값이 두 번째 값보다 크거나 같은지 확인합니다</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">작거나 같음</a> </td><td>이 연산자는 첫 번째 값이 두 번째 값보다 작거나 같은지 확인합니다</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">다음과 같지 않음</a></td><td>이 연산자는 특정 표현식이 특정 값과 같지 않은지 확인합니다.</td>
    </tr>
</table>

## 사용 방법 비디오{#video}

개인화 도우미 기능을 사용하여 개인화 값을 변형하는 방법을 알아보고 도우미 기능의 다양한 사용 사례를 이해합니다.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
