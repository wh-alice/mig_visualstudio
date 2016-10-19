---
title: "Step 5: Add Label References"
ms.custom: ""
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d418350c-0396-494e-8149-71fa61b395c5
caps.latest.revision: 20
ms.author: "kempb"
manager: "ghogen"
translation.priority.ht: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# Step 5: Add Label References
The program needs to track which label controls the player chooses. Right now, the program shows all labels chosen by the player. But we're going to change that. After the first label is chosen, the program should show the label's icon. After the second label is chosen, the program should display both icons for a brief time, and then hide both icons again. Your program will now keep track of which label control is chosen first and which is chosen second by using *reference variables*.  
  
### To add label references  
  
1.  Add label references to your form by using the following code.  
  
     [!code[VbExpressTutorial4Step5#5](../ide/codesnippet/VisualBasic/step-5--add-label-references_1.vb)]
[!code[VbExpressTutorial4Step5#5](../ide/codesnippet/CSharp/step-5--add-label-references_1.cs)]  
  
     These reference variables look similar to the statements you used earlier to add objects (like `Timer` objects, `List` objects, and `Random` objects) to your form. However, these statements don't cause two extra label controls to appear on the form because there's no `new` keyword used in either of the two statements. Without the `new` keyword, no object is created. That's why `firstClicked` and `secondClicked` are called reference variables: They just keep track (or, refer to) `Label` objects.  
  
     When a variable isn't keeping track of an object, it's set to a special reserved value: `null` in Visual C# and `Nothing` in Visual Basic. So, when the program starts, both `firstClicked` and `secondClicked` are set to `null` or `Nothing`, which means that the variables aren't keeping track of anything.  
  
2.  Modify your Click event handler to use the new `firstClicked` reference variable. Remove the last statement in the `label_Click()` event handler method (`clickedLabel.ForeColor = Color.Black;`) and replace it with the `if` statement that follows. (Be sure you include the comment, and the whole `if` statement.)  
  
     [!code[VbExpressTutorial4Step5#6](../ide/codesnippet/VisualBasic/step-5--add-label-references_2.vb)]
[!code[VbExpressTutorial4Step5#6](../ide/codesnippet/CSharp/step-5--add-label-references_2.cs)]  
  
3.  Save and run your program. Choose one of the label controls, and its icon appears.  
  
4.  Choose the next label control, and notice that nothing happens. The program is already keeping track of the first label that the player chose, so `firstClicked` isn't equal to `null` in Visual C# or `Nothing` in Visual Basic. When your `if` statement checks `firstClicked` to determine if it's equal to `null` or `Nothing`, it finds that it isn't, and it doesn't execute the statements in the `if` statement. So, only the first icon that's chosen turns black, and the other icons are invisible, as shown in the following picture.  
  
     ![Matching game showing one icon](../ide/media/express_tut4step5.png "Express_Tut4Step5")  
Matching game showing one icon  
  
     You'll fix this situation in the next step of the tutorial by adding a **Timer** control.  
  
### To continue or review  
  
-   To go to the next tutorial step, see [Step 6: Add a Timer](../ide/step-6--add-a-timer.md).  
  
-   To return to the previous tutorial step, see [Step 4: Add a Click Event Handler to Each Label](../ide/step-4--add-a-click-event-handler-to-each-label.md).