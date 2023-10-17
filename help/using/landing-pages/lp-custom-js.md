---
solution: Journey Optimizer
product: journey optimizer
title: 랜딩 페이지에서 사용자 지정 JavaScript 사용
description: Journey Optimizer에서 랜딩 페이지의 콘텐츠를 디자인하는 방법을 알아봅니다
feature: Landing Pages
topic: Content Management
role: Developer
level: Experienced
keywords: 랜딩, 랜딩 페이지, javascript, 코드
exl-id: 2a7ebead-5f09-4ea5-8f00-8b5625963290
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 2%

---

# 랜딩 페이지에서 사용자 지정 JavaScript 사용 {#lp-custom-js}

사용자 지정 JavaScript를 사용하여 랜딩 페이지 콘텐츠를 정의할 수 있습니다. 예를 들어 고급 스타일을 수행해야 하거나 랜딩 페이지에 사용자 지정 동작을 추가하려는 경우, 고유한 컨트롤을 빌드하고에서 실행할 수 있습니다. [!DNL Journey Optimizer].

## 랜딩 페이지에 JavaScript 코드 삽입

사용자 지정 JavaScript를 랜딩 페이지 콘텐츠에 삽입하려면 다음 중 하나를 수행할 수 있습니다.

* 콘텐츠 만들기를 시작할 때 기존 HTML 콘텐츠를 가져온 다음 사용자 지정 JavaScript 코드가 포함된 파일을 선택합니다. 콘텐츠를 가져오는 방법 알아보기 [이 섹션에서](../email/existing-content.md).

* 랜딩 페이지를 처음부터 디자인하거나 저장된 템플릿에서 디자인할 수 있습니다. 을(를) 끌어다 놓습니다. **[!UICONTROL HTML]** 콘텐츠 구성 요소를 캔버스에 표시하고 소스 코드를 표시하여 구성 요소에 JavaSCript를 추가합니다. 에서 HTML 구성 요소를 사용하는 방법 알아보기 [이 섹션](../email/content-components.md#HTML). <!--You can also simply switch the whole landing page content to code view and enter or paste your JavaScript code.-->

  ![](assets/lp_designer-html-component.png)

* 콘텐츠 디자이너에 JavaScript 코드를 직접 입력하거나 붙여 넣습니다. 콘텐츠를 코딩하는 방법에 대해 알아봅니다. [이 섹션에서](../email/code-content.md).

>[!NOTE]
>
>현재 다음과 같은 경우에는 JavaScript를 실제로 표시할 수 없습니다. [랜딩 페이지 미리 보기](create-lp.md#test-landing-page).

랜딩 페이지를 올바르게 표시하려면 아래 섹션에 설명된 대로 다음 구문을 사용합니다.

## 코드 초기화

JavaScript 코드를 초기화하려면 `lpRuntimeReady` 이벤트. 이 이벤트는 라이브러리의 초기화 성공 후 트리거됩니다. 콜백은 `lpRuntime` 라이브러리 메서드 및 후크를 노출하는 개체입니다.

`LpRuntime` 는 &quot;랜딩 페이지 런타임&quot;을 나타냅니다. 이 개체는 기본 라이브러리 식별자입니다. 사용자 지정 JavaScript에서 사용할 수 있는 후크, 양식 제출 방법 및 기타 유틸리티 방법이 표시됩니다.

**예:**

```
if(window.lpRuntime){
    init(window.lpRuntime);
}else{
    window.addEventListener('lpRuntimeReady',function(e){
        init(e.detail);
    });
}
 
function init(lpRuntime){
    // Enter custom JavaScript here using methods from lpRuntime.
}
```

## 후크

후크를 사용하여 양식 제출의 라이프사이클 동안 메서드를 첨부할 수 있습니다. 예를 들어, 양식이 실제로 제출되기 전에 후크를 사용하여 일부 양식 유효성 검사를 수행할 수 있습니다.

다음은 사용할 수 있는 후크입니다.

| 이름 | 설명 |
|--- |--- |
| addBeforeSubmitHook | 양식 제출 전에 호출될 사용자 지정 후크입니다. 제출을 계속하려면 true를 반환하고, 제출하지 않으려면 false를 반환합니다. |
| addOnFailHook | 양식 제출 실패 시 호출될 사용자 지정 후크입니다. |
| addOnSuccessHook | 양식 제출 시 호출될 사용자 지정 후크입니다. |

**예:**

```
//LpRuntime hooks
lpRuntime.hooks.addBeforeSubmitHook(function(){
    // Add your validation logic here.
});
```

## 사용자 정의 양식 제출

아래 나열된 방법은 사용자 정의 양식 제출을 수행하는 데 사용됩니다.

>[!NOTE]
>
>양식 제출은 사용자 지정 JavaScript에 의해 처리되므로 글로벌 변수를 설정하여 기본 제출을 명시적으로 비활성화해야 합니다 `disableDefaultFormSubmission` 끝 `true`.

| 이름 | 설명 |
|--- |--- |
| submitForm | 이 메서드는 양식을 제출하고 사후 제출 플로우를 처리합니다. |
| 양식 전송 | 이 메서드는 양식도 제출하지만 이후 제출 흐름은 건너뜁니다. 예를 들어 제출 성공 페이지로의 리디렉션을 구성한 경우 부분 양식 제출의 경우 해당 리디렉션이 발생하지 않습니다. |

**예:**

```
//LpRuntime methods
window.disableDefaultFormSubmission = true        // Flag to disable the default submission flow.
 
lpRuntime.submitForm(formSubmissionData);         // This will trigger the default form submission handling like redirecting to error or success page.
  
lpRuntime.submitFormPartial(formSubmissionData,{   // This will not trigger the default submission handling.
    beforeSubmit : callback,
    onFailure : failureCallback,                   // Custom onFailureCallback - will be used in partial submission of form.
    onSuccess : successCallback                    // Custom onSuccessCallback - will be used in partial submission of form.
})
```

## 효용 함수

| 이름 | 설명 |
|--- |--- |
| getFormData | 이 메서드는 를 가져오는 데 사용할 수 있습니다. `formData` JSON 개체의 형식입니다. 이 개체는에 전달할 수 있습니다. `submitForm` 양식 제출용. |

**예:**

```
let formData = lpRuntime.getFormData();                           // Method to generate formdata
 
lpRuntime.submitForm(formData);
```

## 사용 사례

### 사용 사례 1: 양식 제출 전에 유효성 검사 추가

```
<html>
<body>
// Enter HTML body here.
  
<script>
        if(window.lpRuntime){
          console.log('got runtime',lpRuntime);
          init(window.lpRuntime);
        }else{
          window.addEventListener('lpRuntimeReady',function(e){
            init(window.lpRuntime);
          });
        }
        
  
      // Here validate the function is checking if the checkbox is selected. This method should return true if you want form submission.
      function validateForm(){
        return document.querySelector('.spectrum-Checkbox-input').checked;
      }    
  
      function init(lpRuntime){
          lpRuntime.hooks.addBeforeSubmitHook(function(){
              return validateForm(); // This method should return true if you want to proceed with submission.
          })
      }
  
</script>  
  
</body>
</html>
```

### 사용 사례 2: 부분 양식 제출

예를 들어 페이지에 여러 개의 확인란이 있는 양식이 있습니다. 확인란을 선택하면 사용자가 제출 버튼을 클릭할 때까지 기다리지 않고 이 데이터를 백엔드에 저장할 수 있습니다.

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <input type='checkbox' value="2" name="name2"/>
        <input type='checkbox' value="3" name="name3"/>
        <input type='checkbox' value="4" name="name4"/>
    </form>
  
<script>
      window.disableDefaultFormSubmission=true;
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
     function init(lpRuntime){
        window.getElementByTagName('input').addEventListener('change',function(e){
            let formData = lpRuntime.getFormData();
            lpRuntime.submitFormPartial(formData);
        })
      }
    </script>
  
</body>
</html>
```

### 사용 사례 3: 사용자 지정 분석 태그

JavaScript를 사용하여 입력 필드의 리스너를 추가하고 사용자 지정 분석 호출 트리거를 첨부할 수 있습니다.

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <input type='checkbox' value="2" name="name2"/>
        <input type='checkbox' value="3" name="name3"/>
        <input type='checkbox' value="4" name="name4"/>
    </form>
  
<script>
      window.disableDefaultFormSubmission=false;  
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
     function init(lpRuntime){
         window.getElementByTagName('input').addEventListener('change',function(e){
            //trigger analytics events
        })
      }
        
    </script>
  
</body>
</html>
```

### 사용 사례 4: 동적 양식

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <div class="hiddenInput hidden">
            <input type='text' name="name2"/>
        </div>
    </form>
  
<script>
      window.disableDefaultFormSubmission=false;     
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
      function init(lpRuntime){
        window.getElementByTagName('input').addEventListener('change',function(e){
            document.querySelector('.hiddenInput').toggleClass('hidden');
        })
      }
        
    </script>
  
</body>
</html>
```
