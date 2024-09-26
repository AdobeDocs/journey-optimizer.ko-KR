---
solution: Journey Optimizer
product: journey optimizer
title: 다른 샌드박스로 여정 복사
description: 여정을 다른 샌드박스로 복사하는 방법 알아보기
feature: Journeys, Sandboxes
topic: Content Management
role: User, Developer, Data Engineer
level: Experienced
keywords: 샌드박스, 여정, 복사, 환경
exl-id: 8c63f2f2-5cec-4cb2-b3bf-2387eefb5002
source-git-commit: 62b5cfd480414c898ab6f123de8c6b9f99667b7d
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 21%

---

# 다른 샌드박스로 여정 복사 {#copy-to-sandbox}

<!--
>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="Copy a journey to another sandbox"
>abstract="Journey Optimizer allows you to copy an entire journey from one sandbox to another. For example, you can copy a journey from the Stage sandbox environment to your Production sandbox. In addition to the Journey itself, Journey Optimizer also copies most of the objects the journey depends on."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="Sandbox details"
>abstract="Select the destination sandbox you want to copy the journey to. Only sandboxes within your organization are available."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="Object details"
>abstract="This is the journey you are going to copy."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="Dependent objects"
>abstract="This is the list of associated objects used in the journey. This list displays the name, the object type, as well as the internal Journey Optimizer ID."
-->

Journey Optimizer를 사용하여 한 샌드박스에서 다른 샌드박스로 전체 여정을 복사할 수 있습니다. 예를 들어 Stage 샌드박스 환경에서 프로덕션 샌드박스로 여정을 복사할 수 있습니다.

Journey Optimizer은 여정 자체 외에도 여정이 의존하는 대부분의 개체(대상, 스키마, 이벤트 및 작업)도 복사합니다.

복사 프로세스는 원본 샌드박스와 대상 샌드박스 간에 **패키지 내보내기 및 가져오기**&#x200B;를 통해 수행됩니다. 개체를 내보내고 대상 샌드박스로 가져오는 방법에 대한 자세한 내용은 [다른 샌드박스로 개체 복사](../configuration/copy-objects-to-sandbox.md) 섹션을 참조하십시오.
