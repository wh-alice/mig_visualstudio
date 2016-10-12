---
title: "Step 8: Write Code for the Show a Picture Button Event Handler"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: na
ms.topic: "article"
ms.assetid: 07f4ec00-cda4-42f4-98bb-37edc7167de7
caps.latest.revision: 24
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
# Step 8: Write Code for the Show a Picture Button Event Handler
In this step, you make the **Show a picture** button work like this:  
  
-   When a user chooses that button, the program opens an **Open File** dialog box.  
  
-   If a user opens a picture file, the program shows that picture in the PictureBox.  
  
 The IDE has a powerful tool called IntelliSense that helps you write code. As you enter code, the IDE opens a box with suggested completions for partial words that you enter. It tries to determine what you want to do next, and automatically jumps to the last item you choose from the list. You can use the up or down arrows to move in the list, or you can keep typing letters to narrow the choices. When you see the choice you want, choose the TAB key to select it. Or, you can ignore the suggestions, if not needed.  
  
 ![link to video](../VS_IDE/media/playvideo.gif "PlayVideo")For a video version of this topic, see [Tutorial 1: Create a Picture Viewer in Visual Basic - Video 4](http://go.microsoft.com/fwlink/?LinkId=205215) or [Tutorial 1: Create a Picture Viewer in C# - Video 4](http://go.microsoft.com/fwlink/?LinkId=205203). These videos use an earlier version of Visual Studio, so there are slight differences in some menu commands and other user interface elements. However, the concepts and procedures work similarly in the current version of Visual Studio.  
  
### To write code for the Show a picture button event handler  
  
1.  Go to Windows Forms Designer and double-click the **Show a picture** button. The IDE immediately goes to the code designer and moves your cursor so it's inside the `showButton_Click()` method that you added previously.  
  
2.  Type an `i` on the empty line between the two braces { }. (In Visual Basic, type on the empty line between Private Sub… and End Sub.) An **IntelliSense** window opens, as shown in the following picture.  
  
     ![IntelliSense with Visual C&#35; code](../VS_IDE/media/express_ifintellisense.png "Express_IfIntellisense")  
IntelliSense with Visual C# code  
  
3.  The **IntelliSense** window should be highlighting the word **if**. (If not, enter a lowercase `f`, and it will.) Notice how a little *tooltip* box next to the **IntelliSense** window appears with the description, **Code snippet for if statement**. (In Visual Basic, the tooltip also states that this is a snippet, but with slightly different wording.) You want to use that snippet, so choose the TAB key to insert **if** into your code. Then choose the TAB key again to use the **if** snippet. (If you chose somewhere else and your **IntelliSense** window disappeared, backspace over the **i** and retype it, and the **IntelliSense** window opens again.)  
  
     ![Visual C&#35; code](../VS_IDE/media/express_highlighttrue.png "Express_HighlightTrue")  
Visual C# code  
  
4.  Next, you use IntelliSense to enter more code to open an **Open File** dialog box. If the user chose the **OK** button, the PictureBox loads the file that the user selected. The following steps show how to enter the code, and although it's numerous steps, it's just a few keystrokes:  
  
    1.  Start with the selected text **true** in the snippet. Type `op` to overwrite it. (In Visual Basic, you start with an initial cap, so type `Op`.)  
  
    2.  The **IntelliSense** window opens and displays **openFileDialog1**. Choose the TAB key to select it. (In Visual Basic, it starts with an initial cap, so you see **OpenFileDialog1**. Ensure that **OpenFileDialog1** is selected.)  
  
         To learn more about `OpenFileDialog`, see [OpenFileDialog](http://msdn.microsoft.com/library/system.windows.forms.openfiledialog.aspx).  
  
    3.  Type a period (`.`) (Many programmers call this a dot.) Because you typed a dot right after **openFileDialog1**, an **IntelliSense** window opens, filled in with all of the **OpenFileDialog** component's properties and methods. These are the same properties that appear in the **Properties** window when you choose it in Windows Forms Designer. You can also choose methods that tell the component to do things (like open a dialog box).  
  
        > [!NOTE]
        >  The **IntelliSense** window can show you both properties and methods. To determine what is being shown, look at the icon on the left side of each item in the **IntelliSense** window. You see a picture of a block next to each method, and a picture of a wrench (or spanner) next to each property. There's also a lightning bolt icon next to each event. These pictures display as follows.  
  
         ![Method icon](../VS_IDE/media/express_iconmethod.png "Express_IconMethod")  
Method icon  
  
         ![Property icon](../VS_IDE/media/express_iconproperty.png "Express_IconProperty")  
Property icon  
  
         ![Event icon](../VS_IDE/media/express_iconevent.png "Express_IconEvent")  
Event icon  
  
    4.  Start to type `ShowDialog` (capitalization is unimportant to IntelliSense). The `ShowDialog()` method will show the **Open File** dialog box. After the window has highlighted **ShowDialog**, choose the TAB key. You can also highlight “ShowDialog” and choose the F1 key to get help for it.  
  
         To learn more about the `ShowDialog()` method, see [ShowDialog Method](http://msdn.microsoft.com/library/c7ykbedk.aspx).  
  
    5.  When you use a method on a control or a component (referred to as *calling a method*), you need to add parentheses. So enter opening and closing parentheses immediately after the "g" in `ShowDialog`: `()` It should now look like "openFileDialog1.ShowDialog()".  
  
        > [!NOTE]
        >  Methods are an important part of any program, and this tutorial has shown several ways to use methods. You can call a component's method to tell it to do something, like how you called the **OpenFileDialog** component's `ShowDialog()` method. You can create your own methods to make your program do things, like the one you're building now, called the `showButton_Click()` method, which opens a dialog box and a picture when a user chooses a button.  
  
    6.  For Visual C#, add a space, and then add two equal signs (`==`). For Visual Basic, add a space, and then use a single equal sign (`=`). (Visual C# and Visual Basic use different equality operators.)  
  
    7.  Add another space. As soon as you do, another **IntelliSense** window opens. Start to type `DialogResult` and choose the TAB key to add it.  
  
        > [!NOTE]
        >  When you write code to call a method, sometimes it returns a value. In this case, the **OpenFileDialog** component's `ShowDialog()` method returns a DialogResult value. DialogResult is a special value that tells you what happened in a dialog box. An **OpenFileDialog** component can result in the user choosing **OK** or **Cancel**, so its `ShowDialog()` method returns either DialogResult.OK or DialogResult.Cancel.  
  
    8.  Type a dot to open the DialogResult value **IntelliSense** window. Enter the letter `O` and choose the TAB key to insert **OK**.  
  
         To learn more about `DialogResult`, see [DialogResult](http://msdn.microsoft.com/library/system.windows.forms.dialogresult.aspx).  
  
        > [!NOTE]
        >  The first line of code should be complete. For Visual C#, it should be the following.  
        >   
        >  `if (openFileDialog1.ShowDialog() == DialogResult.OK)`  
        >   
        >  For Visual Basic, it should be the following.  
        >   
        >  `If OpenFileDialog1.ShowDialog() = DialogResult.OK Then`  
  
    9. Now add one more line of code. You can type it (or copy and paste it), but consider using IntelliSense to add it. The more familiar you are with IntelliSense, the more quickly you can write your own code. Your final `showButton_Click()` method looks like the following. (Choose the **VB** tab to view the Visual Basic version of the code.)  
  
         [!code[VbExpressTutorial1Step8#1](../VS_IDE/codesnippet/CSharp/step-8--write-code-for-the-show-a-picture-button-event-handler_1.cs)]
[!code[VbExpressTutorial1Step8#1](../VS_IDE/codesnippet/VisualBasic/step-8--write-code-for-the-show-a-picture-button-event-handler_1.vb)]  
  
### To continue or review  
  
-   To go to the next tutorial step, see [Step 9: Review, Comment, and Test Your Code](../VS_IDE/step-9--review--comment--and-test-your-code.md).  
  
-   To return to the previous tutorial step, see [Step 7: Add Dialog Components to Your Form](../VS_IDE/step-7--add-dialog-components-to-your-form.md).