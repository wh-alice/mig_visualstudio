---
title: "Shared Colors for Visual Studio | Microsoft Docs"
ms.custom: ""
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 8d11b9a0-6175-4f2e-8e7f-79daee1bfd41
caps.latest.revision: 5
ms.author: "gregvanl"
manager: "ghogen"
translation.priority.mt: 
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
# Shared Colors for Visual Studio
When you are designing UI that uses common Visual Studio shell elements, or you would like your interface element to be consistent with similar features, use existing token names in package definition files to choose and assign colors. This ensures that your UI stays consistent with the overall Visual Studio environment and that it updates automatically when themes are added or updated.  
  
 This article describes common UI elements and the token names that they use, which you can reference when building similar UI. For specific information about how to access these color tokens, see [The VSColor Service](../extensibility/colors-and-styling-for-visual-studio.md#BKMK_TheVSColorService).  
  
 Make sure to use token names correctly:  
  
-   **Use token names based on function, not on the color itself.** The common shared colors are associated with specific interface elements and are only intended to be used for the same or similar features. For example, don't reuse the color of a pressed combo box for a spinning progress animation just because you like the color. The functions of the combo box and the animation are different, and if the color associated with the combo box changes, it may no longer be an appropriate color for your animation element. Consistent use of color helps orient your users and prevent confusion.  
  
-   **Use background and text colors in the correct combination.** Background colors that are intended to be used with text will have an associated text color. Don't use text colors other than what is specified for that background. If there is not an associated text color, don't use that background color for any surface on which you expect to display text. Other combinations of text and background colors may result in an unreadable interface.  
  
-   **Use control colors that are appropriate for their location.** In certain states, some Visual Studio controls do not have separate border and background colors. Instead, they pick up those colors from the surfaces behind them. Make sure that you always use the token names that are appropriate for the location where you are placing the control.  
  
> [!IMPORTANT]
>  Do not use tokens found in the categories "Start Page" or "Cider."  
  
## Command structures  
  
###  <a name="BKMK_CommandMenus"></a> Menus  
 Menus can occur at several places within Visual Studio: the main menu bar, embedded in document or tool windows, or on right-click in various locations throughout the IDE. Implementations of menus associated with other UI elements are discussed in the section for the respective element. You should always use the standard menu implementation provided by the Visual Studio environment. However, in some rare instances you might not have access to the standard Visual Studio menus. In these situations, use the following token names to ensure that your UI is consistent with other menus in Visual Studio.  
  
 ![Menus redline](../extensibility/media/0303-000_menuredline.png "0303-000_MenuRedline")  
  
 Use …  
 -   whenever you need to create a custom menu.  
  
-   when you have a new UI component that you want to match the Visual Studio menus.  
  
 Do not use …  
 the background color alone. Always use the background/foreground combination as specified.  
  
#### Menu title  
 Menu titles consist of a background, a border, and the title text, as well as an optional glyph, usually when the menu is found in a command bar.  
  
 ![Menu title redline](../extensibility/media/0303-001_menutitleredline.png "0303-001_MenuTitleRedline")  
  
 Use…  
 whenever you are creating a custom menu title.  
  
 Do not use…  
 -   for anything that you don't want to always match the menu title.  
  
-   in any background/foreground combination other than specified.  
  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Menu title default](../extensibility/media/0303-002_menutitledefault.png "0303-002_MenuTitleDefault")  
  
 **Menu title**  
  
 Background  
  
 None  
  
 Foreground (Text)  
  
 `Environment.CommandBarTextActive`  
  
 ![Menu title with glyph default](../extensibility/media/0303-003_menutitlewithglyphdefault.png "0303-003_MenuTitleWithGlyphDefault")  
  
 **Menu title with glyph**  
  
 Foreground (Glyph)  
  
 `Environment.CommandBarMenuGlyph`  
  
 Border  
  
 None  
  
 **Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Menu title on hover](../extensibility/media/0303-004_menutitlehover.png "0303-004_MenuTitleHover")  
  
 **Menu title**  
  
 Background  
  
 `Environment.CommandBarMouseOverBackgroundBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `Environment.CommandBarTextHover`  
  
 ![Menu title with glyph on hover](../extensibility/media/0303-005_menutitlewithglyphhover.png "0303-005_MenuTitleWithGlyphHover")  
  
 **Menu title with glyph**  
  
 Foreground (Glyph)  
  
 `Environment.CommandBarMenuMouseOverGlyph`  
  
 Border  
  
 `Environment.CommandBarBorder`  
  
 **Pressed**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Menu title pressed](../extensibility/media/0303-006_menutitlepressed.png "0303-006_MenuTitlePressed")  
  
 **Menu title**  
  
 Background  
  
 `Environment.CommandBarMenuBackgroundGradientBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `Environment.CommandBarTextActive`  
  
 ![Menu title with glyph pressed](../extensibility/media/0303-007_menutitlewithglyphpressed.png "0303-007_MenuTitleWithGlyphPressed")  
  
 **Menu title with glyph**  
  
 Foreground (Glyph)  
  
 `Environment.CommandBarMenuMouseDownGlyph`  
  
 Border  
  
 `Environment.CommandBarMenuBorder`  
  
 Only left, top, and right sides.  
  
 **Disabled**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Menu title with glyph disabled](../extensibility/media/0303-008_menutitlewithglyphdisabled.png "0303-008_MenuTitleWithGlyphDisabled")  
  
 **Menu title with glyph**  
  
 Background  
  
 None  
  
 Foreground (Text)  
  
 `Environment.CommandBarTextInactive`  
  
 Foreground (Glyph)  
  
 `Environment.CommandBarTextInactive`  
  
 Border  
  
 None  
  
#### Menu  
 An individual menu item consists of the menu text and an optional icon, check box, or submenu glyph. Its background and text color change on hover. This color token is a background/foreground pair.  
  
 ![Menu items redline](../extensibility/media/0303-009_menuitemredline.png "0303-009_MenuItemRedline")  
  
 Use…  
 for any drop-down list that is launched from a menu bar or command bar.  
  
 Do not use…  
 -   for any drop-down list that occurs in another context.  
  
-   in any background/foreground combination other than specified.  
  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Menu default](../extensibility/media/0303-010_menudefault.png "0303-010_MenuDefault")  
  
 **Menu**  
  
 Background  
  
 `Environment.CommandBarMenuBackgroundGradientBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `Environment.CommandBarTextActive`  
  
 Foreground (Submenu glyph)  
  
 `Environment.CommandBarMenuSubmenuGlyph`  
  
 Border  
  
 `Environment.CommandBarMenuBorder`  
  
 Icon channel background  
  
 `Environment.CommandBarMenuIconBackground`  
  
 Separator  
  
 `Environment.CommandBarMenuSeparator`  
  
 Shadow  
  
 `Environment.DropShadowBackground`  
  
 ![Menu checked](../extensibility/media/0303-011_menuchecked.png "0303-011_MenuChecked")  
  
 **Checked**  
  
 Check mark  
  
 `Environment.CommandBarCheckBox`  
  
 Check mark background  
  
 `Environment.CommandBarSelectedIcon`  
  
 ![Menu selected](../extensibility/media/0303-012_menuselected.png "0303-012_MenuSelected")  
  
 **Selected**  
  
 Icon background  
  
 `Environment.CommandBarSelected`  
  
 Icon border  
  
 `Environment.CommandBarSelectedBorder`  
  
 **Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Menu hover](../extensibility/media/0303-013_menuhover.png "0303-013_MenuHover")  
  
 **Menu item**  
  
 Background  
  
 `Environment.CommandBarMenuItemMouseOver`  
  
 Foreground (Text)  
  
 `Environment.CommandBarMenuItemMouseOver`  
  
 Foreground (Submenu glyph)  
  
 `Environment.CommandBarMenuMouseOverSubmenuGlyph`  
  
 ![Menu hover checked](../extensibility/media/0303-014_menuhoverchecked.png "0303-014_MenuHoverChecked")  
  
 **Checked**  
  
 Check mark  
  
 `Environment.CommandBarCheckBoxMouseOver`  
  
 Check mark background  
  
 `Environment.CommandBarHoverOverSelectedIcon`  
  
 ![Menu hover selected](../extensibility/media/0303-015_menuhoverselected.png "0303-015_MenuHoverSelected")  
  
 **Selected**  
  
 Icon background  
  
 `Environment.CommandBarHoverOverSelected`  
  
 Icon border  
  
 `Environment.CommandBarHoverOverSelectedIconBorder`  
  
 **Disabled**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Menu disabled](../extensibility/media/0303-016_menudisabled.png "0303-016_MenuDisabled")  
  
 Menu item  
  
 Foreground (Text)  
  
 `Environment.CommandBarTextInactive`  
  
 Foreground (Submenu glyph)  
  
 `Environment.CommandBarMenuSubmenuGlyph`  
  
 ![Menu disabled checked](../extensibility/media/0303-017_menudisabledchecked.png "0303-017_MenuDisabledChecked")  
  
 Checked  
  
 Check mark  
  
 `Environment.CommandBarCheckBoxDisabled`  
  
 Check mark background  
  
 `Environment.CommandBarSelectedIconDisabled`  
  
### Command bar  
 The command bar can appear in multiple places within the Visual Studio IDE, most notably the command shelf and embedded in tool or document windows.  
  
 In general, always use the standard command bar implementation provided by the Visual Studio environment. Using the standard mechanism ensures that all visual details will appear correctly and that interactive elements, will behave consistently with other Visual Studio command bar controls. However, if it is necessary for you to build your own command bar, make sure you style it correctly using the following token names.  
  
 ![Command bar redline](../extensibility/media/0303-018_commandbarredline.png "0303-018_CommandBarRedline")  
  
 ![Overflow button redline](../extensibility/media/0303-019_overflowbuttonredline.png "0303-019_OverflowButtonRedline")  
  
 Use…  
 in places where you need an embedded command bar but are unable to use the standard Visual Studio command bar implementation.  
  
 Do not use…  
 -   for UI elements that are not similar to a command bar.  
  
-   for command bar components other than the ones for which token names are specified.  
  
#### Command bar group  
 A command bar group consists of a related set of command bar controls and might contain any number of buttons, split buttons, drop-down menus, combo boxes, or menus. Colors for those controls are regulated by separate token names and are discussed individually elsewhere in this guide. A separator line is used to divide a command bar group into related subgroups.  
  
 ![Command bar group redline](../extensibility/media/0303-020_commandbargroupredline.png "0303-020_CommandBarGroupRedline")  
  
 Use…  
 in places where you need an embedded command bar but are unable to use the standard Visual Studio command bar implementation.  
  
 Do not use…  
 -   for UI elements that are not similar to a command bar.  
  
-   for command bar components other than the ones for which token names are specified.  
  
 **Default** (no other states)  
  
 Element  
  
 Token name: Category.color  
  
 Background  
  
 `Environment.CommandBarGradientBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Border  
  
 `Environment.CommandBarToolBarBorder`  
  
 Drag handle  
  
 `Environment.CommandBarDragHandle`  
  
 Separator  
  
 `Environment.CommandBarToolBarSeparator`  
  
 `Environment.CommandBarToolBarSeparatorHighlight`  
  
#### Command icons  
 ![Command icon redline](../extensibility/media/0303-021_commandiconredline1.png "0303-021_CommandIconRedline1")  
  
 ![Command icon redline](../extensibility/media/0303-022_commandiconredline2.png "0303-022_CommandIconRedline2")  
  
 Use…  
 for any buttons that will be placed on a command bar.  
  
 Do not use…  
 -   for controls that have their own token names.  
  
-   in any background/foreground combination other than specified.  
  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Command icon default](../extensibility/media/0303-023_commandicondefault.png "0303-023_CommandIconDefault")  
  
 **Default**  
  
 Background  
  
 N/A (inherits from command bar background)  
  
 Foreground (Text)  
  
 `Environment.CommandBarTextActive`  
  
 Border  
  
 N/A  
  
 ![Command icon default selected](../extensibility/media/0303-024_commandicondefaultselected.png "0303-024_CommandIconDefaultSelected")  
  
 **Selected**  
  
 Background  
  
 `Environment.CommandBarSelected`  
  
 Foreground (Text)  
  
 `Environment.CommandBarTextSelected`  
  
 Border  
  
 `Environment.CommandBarSelectedBorder`  
  
 **Hover and keyboard focused**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Command icon hover](../extensibility/media/0303-025_commandiconhover.png "0303-025_CommandIconHover")  
  
 **Standard on hover**  
  
 Background  
  
 `Environment.CommandBarMouseOverBackgroundBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `Environment.CommandBarTextHover`  
  
 Border  
  
 `Environment.CommandBarBorder`  
  
 ![Command icon hover selected](../extensibility/media/0303-026_commandiconhoverselected.png "0303-026_CommandIconHoverSelected")  
  
 **Selected on hover**  
  
 Background  
  
 `Environment.CommandBarHoverOverSelected`  
  
 Foreground (Text)  
  
 `Environment.CommandBarTextHoverOverSelected`  
  
 Border  
  
 `Environment.CommandBarHoverOverSelectedIconBorder`  
  
 **Pressed**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Command icon pressed](../extensibility/media/0303-027_commandiconpressed.png "0303-027_CommandIconPressed")  
  
 **Pressed command icon**  
  
 Background  
  
 `Environment.CommandBarMouseDownBackgroundBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `Environment.CommandBarTextMouseDown`  
  
 Border  
  
 `Environment.CommandBarBorder`  
  
 **Disabled**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Command icon disabled](../extensibility/media/0303-028_commandicondisabled.png "0303-028_CommandIconDisabled")  
  
 **Disabled command icon**  
  
 Background  
  
 N/A (inherits from command bar background)  
  
 Foreground (Text)  
  
 `Environment.CommandBarTextInactive`  
  
 Border  
  
 N/A  
  
####  <a name="BKMK_CommandComboBox"></a> Combo box  
  
> [!IMPORTANT]
>  Combo boxes are similar to drop-downs, but include an editable text region. If your drop-down does not include an editable text region, use the color tokens found under [Drop-down](../extensibility/shared-colors-for-visual-studio.md#BKMK_CommandDropDown).  
  
 ![Combo box redline](../extensibility/media/0303-029_comboboxredline.png "0303-029_ComboBoxRedline")  
  
 Use …  
 -   when building custom combo boxes.  
  
-   when creating a command bar control that is similar to a combo box.  
  
 Do not use …  
 -   for anything you don’t want always to match the command bar UI.  
  
-   when you have access to a styled combo box.  
  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Combo box input field](../extensibility/media/0303-030_comboboxinputfield.png "0303-030_ComboBoxInputField")  
  
 **Input field**  
  
 Background  
  
 `Environment.ComboBoxBackground`  
  
 Foreground (Text)  
  
 `Environment.ComboBoxText`  
  
 Border  
  
 `Environment.ComboBoxBorder`  
  
 Separator  
  
 No separator  
  
 ![Combo box drop&#45;down button](../extensibility/media/0303-031_comboboxdropdownbutton.png "0303-031_ComboBoxDropdownButton")  
  
 **Drop-down button**  
  
 Background  
  
 N/A (inherits)  
  
 Foreground (Glyph)  
  
 `Environment.ComboBoxGlyph`  
  
 ![Combo box&#47;drop&#45;down list](../extensibility/media/0303-032_comboboxdropdownlist.png "0303-032_ComboBoxDropdownList")  
  
 **Drop-down list**  
  
 Background  
  
 `Environment.ComboBoxPopupBackgroundBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `Environment.ComboBoxItemText`  
  
 Border  
  
 `Environment.ComboBoxPopupBorder`  
  
 **Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Combo box input field on hover](../extensibility/media/0303-033_comboboxinputfieldhover.png "0303-033_ComboBoxInputFieldHover")  
  
 **Input field**  
  
 Background  
  
 `Environment.ComboBoxMouseOverBackgroundBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `Environment.ComboBoxMouseOverText`  
  
 Border  
  
 `Environment.ComboBoxMouseOverBorder`  
  
 Separator  
  
 `Environment.ComboBoxMouseOverSeparator`  
  
 ![Combo box&#47;drop&#45;down button on hover](../extensibility/media/0303-034_comboboxdropdownbuttonhover.png "0303-034_ComboBoxDropdownButtonHover")  
  
 **Drop-down button**  
  
 Background  
  
 `Environment.ComboBoxButtonMouseOverBackground`  
  
 Foreground (Glyph)  
  
 `Environment.ComboBoxMouseOverGlyph`  
  
 ![Combo box&#47;drop&#45;down list on hover](../extensibility/media/0303-035_comboboxdropdownlisthover.png "0303-035_ComboBoxDropdownListHover")  
  
 **Drop-down list**  
  
 Background (Menu item)  
  
 `Environment.ComboBoxItemMouseOverBackground`  
  
 Foreground (Text)  
  
 `Environment.ComboBoxItemMouseOverText`  
  
 Border (Menu item)  
  
 `Environment.ComboBoxItemMouseOverBorder`  
  
 **Focused**  
  
 Component  
  
 Element  
  
 Token name: Color.category  
  
 ![Combo box input field focused](../extensibility/media/0303-036_comboboxinputfieldfocused.png "0303-036_ComboBoxInputFieldFocused")  
  
 **Input field**  
  
 Background  
  
 `Environment.ComboBoxFocusedBackground`  
  
 Foreground (Text)  
  
 `Environment.ComboBoxFocusedText`  
  
 Border  
  
 `Environment.ComboBoxFocusedBorder`  
  
 Separator  
  
 `Environment.ComboBoxFocusedButtonSeparator`  
  
 ![Combo box&#47;drop&#45;down button focused](../extensibility/media/0303-037_comboboxdropdownbuttonfocused.png "0303-037_ComboBoxDropdownButtonFocused")  
  
 **Drop-down button**  
  
 Background  
  
 `Environment.ComboBoxFocusedButtonBackground`  
  
 Foreground (Glyph)  
  
 `Environment.ComboBoxFocusedGlyph`  
  
 **Pressed**  
  
 Component  
  
 Element  
  
 Token name: Color.category  
  
 ![Combo box input field pressed](../extensibility/media/0303-038_comboboxinputfieldpressed.png "0303-038_ComboBoxInputFieldPressed")  
  
 **Input field**  
  
 Background  
  
 `Environment.ComboBoxMouseDownBackground`  
  
 Foreground (Text)  
  
 `Environment.ComboBoxMouseDownText`  
  
 Border  
  
 `Environment.ComboBoxMouseDownBorder`  
  
 Separator  
  
 `Environment.ComboBoxMouseDownSeparator`  
  
 ![Combo box&#47;drop&#45;down button pressed](../extensibility/media/0303-039_comboboxdropdownbuttonpressed.png "0303-039_ComboBoxDropdownButtonPressed")  
  
 **Drop-down button**  
  
 Background  
  
 `Environment.ComboBoxButtonMouseDownBackground`  
  
 Foreground (Glyph)  
  
 `Environment.ComboBoxMouseDownGlyph`  
  
 **Disabled**  
  
 ![Combo box input field disabled](../extensibility/media/0303-041_comboboxinputfielddisabled.png "0303-041_ComboBoxInputFieldDisabled")  
  
 **Input field**  
  
 Background  
  
 `Environment.ComboBoxDisabledBackground`  
  
 Foreground (Text)  
  
 `Environment.ComboBoxDisabledText`  
  
 Border  
  
 `Environment.ComboBoxDisabledBorder`  
  
 Separator  
  
 No separator  
  
 ![Combo box&#47;drop&#45;down button disabled](../extensibility/media/0303-040_comboboxdropdownbuttondisabled.png "0303-040_ComboBoxDropdownButtonDisabled")  
  
 **Drop-down button**  
  
 Background  
  
 None  
  
 Foreground (Glyph)  
  
 `Environment.ComboBoxDisabledGlyph`  
  
####  <a name="BKMK_CommandDropDown"></a> Drop-down  
  
> [!IMPORTANT]
>  Drop-downs are similar to combo boxes, but lack editable text regions. If your drop-down includes an editable text region, use the color tokens found under [Combo box](../extensibility/shared-colors-for-visual-studio.md#BKMK_CommandComboBox).  
  
 ![Drop&#45;down redline](../extensibility/media/0303-042_dropdownredline.png "0303-042_DropdownRedline")  
  
 Use …  
 when you are creating custom drop-down list controls.  
  
 Do not use …  
 -   for anything that is not similar to a drop-down list.  
  
-   for combo boxes or split buttons.  
  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Drop&#45;down selection field](../extensibility/media/0303-043_dropdownselectionfield.png "0303-043_DropdownSelectionField")  
  
 **Selection field**  
  
 Background  
  
 `Environment.DropDownBackground`  
  
 Foreground (Text)  
  
 `DropDownText`  
  
 Border  
  
 `DropDownBorder`  
  
 Separator  
  
 No separator  
  
 ![Drop&#45;down button](../extensibility/media/0303-044_dropdownbutton.png "0303-044_DropdownButton")  
  
 **Drop-down button**  
  
 Background  
  
 None  
  
 Foreground (Glyph)  
  
 `Environment.DropDownGlyph`  
  
 ![Drop&#45;down list](../extensibility/media/0303-045_dropdownlist.png "0303-045_DropdownList")  
  
 **Drop-down list**  
  
 Background  
  
 `Environment.DropDownPopupBackgroundBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `Environment.ComboBoxItemText`  
  
 Border  
  
 `Environment.DropDownPopupBorder`  
  
 Shadow  
  
 `Environment.DropShadowBackground`  
  
 **Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Drop&#45;down selection field on hover](../extensibility/media/0303-046_dropdownselectionfieldhover.png "0303-046_DropdownSelectionFieldHover")  
  
 **Selection field**  
  
 Background  
  
 `Environment.DropDownMouseOverBackgroundBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `Environment.DropDownMouseOverText`  
  
 Border  
  
 `Environment.DropDownMouseOverBorder`  
  
 Separator  
  
 `Environment.DropDownButtonMouseOverSeparator`  
  
 ![Drop&#45;down button on hover](../extensibility/media/0303-047_dropdownbuttonhover.png "0303-047_DropdownButtonHover")  
  
 **Drop-down button**  
  
 Background  
  
 `Environment.DropDownButtonMouseOverBackground`  
  
 Foreground (Glyph)  
  
 `Environment.DropDownMouseOverGlyph`  
  
 ![Drop&#45;down list on hover](../extensibility/media/0303-048_dropdownlisthover.png "0303-048_DropdownListHover")  
  
 **Drop-down list**  
  
 Background (Menu item)  
  
 `Environment.ComboBoxItemMouseOverBackground`  
  
 Foreground (Text)  
  
 `Environment.ComboBoxItemMouseOverText`  
  
 Border (Menu item)  
  
 `Environment.ComboBoxItemMouseOverBorder`  
  
 **Pressed**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Drop&#45;down selection field pressed](../extensibility/media/0303-049_dropdownselectionfieldpressed.png "0303-049_DropdownSelectionFieldPressed")  
  
 **Selection field**  
  
 Background  
  
 `Environment.DropDownMouseDownBackground`  
  
 Foreground (Text)  
  
 `Environment.DropDownMouseDownText`  
  
 Border  
  
 `Environment.DropDownMouseDownBorder`  
  
 Separator  
  
 `Environment.DropDownButtonMouseDownSeparator`  
  
 ![Drop&#45;down button pressed](../extensibility/media/0303-050_dropdownbuttonpressed.png "0303-050_DropdownButtonPressed")  
  
 **Drop-down button**  
  
 Background  
  
 `Environment.DropDownButtonMouseDownBackground`  
  
 Foreground (Glyph)  
  
 `Environment.DropDownMouseDownGlyph`  
  
 **Disabled**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Drop&#45;down selection field disabled](../extensibility/media/0303-051_dropdownselectionfielddisabled.png "0303-051_DropdownSelectionFieldDisabled")  
  
 Background  
  
 `Environment.DropDownDisabledBackground`  
  
 Foreground (Text)  
  
 `Environment.DropDownDisabledText`  
  
 Border  
  
 `Environment.DropDownDisabledBorder`  
  
 Separator  
  
 No separator  
  
 ![Drop&#45;down button disabled](../extensibility/media/0303-052_dropdownbuttondisabled.png "0303-052_DropdownButtonDisabled")  
  
 Background  
  
 N/A  
  
 Foreground (Glyph)  
  
 `Environment.DropDownDisabledGlyph`  
  
#### Split button  
 Split buttons share many token names with other command bar controls, such as buttons, menus, and command bar text. All necessary action and drop-down button token names are repeated here for convenience. Split button drop-down lists are implementations of command bar [Menus](../extensibility/shared-colors-for-visual-studio.md#BKMK_CommandMenus).  
  
 ![Split button redline](../extensibility/media/0303-053_splitbuttonredline.png "0303-053_SplitButtonRedline")  
  
 Use …  
 when you are building a custom split button.  
  
 Do not use …  
 -   for other kinds of buttons.  
  
-   in any background/foreground combination other than specified.  
  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Split button](../extensibility/media/0303-054_splitbutton.png "0303-054_SplitButton")  
  
 **Split button (default)**  
  
 Background  
  
 None  
  
 Foreground (Text)  
  
 `Environment.CommandBarTextActive`  
  
 Foreground (Glyph)  
  
 `Environment.CommandBarSplitButtonGlyph`  
  
 Border  
  
 N/A  
  
 Separator  
  
 N/A  
  
 **Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Split button on hover](../extensibility/media/0303-055_splitbuttonhover.png "0303-055_SplitButtonHover")  
  
 **Split button (on hover)**  
  
 Background  
  
 `Environment.CommandBarMouseOverBackgroundBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `Environment.CommandBarTextHover`  
  
 Foreground (Glyph)  
  
 `Environment.CommandBarSplitButtonMouseOverGlyph`  
  
 Border  
  
 `Environment.CommandBarBorder`  
  
 Separator  
  
 `Environment.CommandBarSplitButtonSeparator`  
  
 **Pressed**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Split button pressed](../extensibility/media/0303-056_splitbuttonpressed.png "0303-056_SplitButtonPressed")  
  
 **Split button (pressed)**  
  
 Background  
  
 `Environment.CommandBarMouseDownBackgroundBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `Environment.CommandBarTextMouseDown`  
  
 Foreground (Glyph)  
  
 `Environment.CommandBarSplitButtonMouseDownGlyph`  
  
 Border  
  
 `Environment.CommandBarBorder`  
  
 Separator  
  
 N/A  
  
 **Disabled**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Split button disabled](../extensibility/media/0303-057_splitbuttondisabled.png "0303-057_SplitButtonDisabled")  
  
 **Split button (disabled)**  
  
 Background  
  
 N/A  
  
 Foreground (Text)  
  
 `Environment.ComboBoxItemTextInactive`  
  
 Foreground (Glyph)  
  
 `Environment.CommandBarTextInactive`  
  
 Border  
  
 N/A  
  
 Separator  
  
 N/A  
  
#### ‘More options’ and ‘Overflow’ buttons  
 The "More options" button is used when a command bar group is customizable by either adding or removing related command bar buttons. The "Overflow" button appears when a command bar is truncated due to lack of horizontal space, and on click shows a menu containing the command bar buttons that cannot be displayed. Colors for these two buttons are controlled by the same set of token names.  
  
 ![More options redline](../extensibility/media/0303-058_moreoptionsredline.png "0303-058_MoreOptionsRedline")  
  
 Use …  
 for custom 'More options' or 'Overflow' buttons.  
  
 Do not use …  
 for buttons that don't have similar functionality to a 'More options' or 'Overflow' button.  
  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![More options](../extensibility/media/0303-059_moreoptions.png "0303-059_MoreOptions")  
  
 **More options**  
  
 ![Overflow button](../extensibility/media/0303-060_overflow.png "0303-060_Overflow")  
  
 **Overflow**  
  
 Background  
  
 `Environment.CommandBarOptionsBackground`  
  
 Foreground (Glyph)  
  
 `Environment.CommandBarOptionsGlyph`  
  
 **Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![More options on hover](../extensibility/media/0303-061_moreoptionshover.png "0303-061_MoreOptionsHover")  
  
 **More options**  
  
 ![Overflow on hover](../extensibility/media/0303-062_overflowoptions.png "0303-062_OverflowOptions")  
  
 **Overflow**  
  
 Background  
  
 `Environment.CommandBarOptionsMouseOverBackgroundBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Glyph)  
  
 `Environment.CommandBarOptionsMouseDownGlyph`  
  
 **Pressed**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![More options pressed](../extensibility/media/0303-063_moreoptionspressed.png "0303-063_MoreOptionsPressed")  
  
 **More options**  
  
 ![Overflow pressed](../extensibility/media/0303-064_overflowpressed.png "0303-064_OverflowPressed")  
  
 **Overflow**  
  
 Background  
  
 `Environment.CommandBarOptionsMouseDownBackgroundBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Glyph)  
  
 `Environment.CommandBarOptionsMouseDownGlyph`  
  
## Document windows  
 There is no need to replicate document windows, because they are provided by the Visual Studio environment. However, you might decide that you want to leverage the colors used in document windows so that your UI always appears consistent with this part of the Visual Studio environment.  
  
 When using document window color tokens, you must be careful to use them only for similar elements, and always in pairs. If you do not do so, you will have unexpected results in your UI.  
  
### Document window frame  
 Document windows can be either docked in the IDE or floating as a separate window. When a document window is floating outside the IDE, it still sits in a document well, and has background, border, text, and tab colors that are the same as when it is part of the IDE. However, the document sits inside a frame that has its own background, border, and text colors. When tool windows are docked in the document well, they inherit the behavior and color for their tabs from document window token names.  
  
 ![Docked document window redline](../extensibility/media/0303-065_dockeddocumentwindowredline.png "0303-065_DockedDocumentWindowRedline")  
  
 **Docked document window**  
  
 ![Floating document window redline](../extensibility/media/0303-066_floatingdocumentwindowredline.png "0303-066_FloatingDocumentWindowRedline")  
  
 **Floating document window**  
  
 Use …  
 anywhere you are creating UI that you want to match the document window.  
  
 Do not use …  
 for any UI that you don't want automatically to change if the shell has a theme update.  
  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 Document: docked or floating  
  
 Background  
  
 Depends on document type  
  
 Foreground (Text)  
  
 Depends on document type  
  
 Border  
  
 `Environment.ToolWindowBorder`  
  
 ![Frame focused](../extensibility/media/0303-067_framefocused.png "0303-067_FrameFocused")  
  
 **Frame: floating, focused**  
  
 Background  
  
 `Environment.ToolWindowFloatingFrame`  
  
 Foreground (Text)  
  
 `Environment.ToolWindowFloatingFrame`  
  
 Foreground (Glyph)  
  
 `Environment.RaftedWindowButtonActiveGlyph`  
  
 Border  
  
 `Environment.MainWindowActiveDefaultBorder`  
  
 Border (Glyph)  
  
 `Environment.RaftedWindowButtonActiveBorder`  
  
 Set to transparent  
  
 ![Frame unfocused](../extensibility/media/0303-068_frameunfocused.png "0303-068_FrameUnfocused")  
  
 **Frame: floating, unfocused**  
  
 Background  
  
 `Environment.ToolWindowFloatingFrameInactive`  
  
 Foreground (Text)  
  
 `Environment.ToolWindowFloatingFrameInactive`  
  
 Foreground (Glyph)  
  
 `Environment.RaftedWindowButtonInactiveGlyph`  
  
 Border  
  
 `Environment.MainWindowInactiveBorder`  
  
 Border (Glyph)  
  
 `Environment.RaftedWindowButtonInactiveBorder`  
  
 Set to transparent  
  
 **Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Frame focused on hover](../extensibility/media/0303-069_framefocusedhover.png "0303-069_FrameFocusedHover")  
  
 **Frame: floating, focused**  
  
 Background (Glyph)  
  
 `Environment.RaftedWindowButtonHoverActive`  
  
 Foreground (Glyph)  
  
 `Environment.RaftedWindowButtonHoverActiveGlyph`  
  
 Border (Glyph)  
  
 `Environment.RaftedWindowButtonHoverActiveBorder`  
  
 ![Frame unfocused on hover](../extensibility/media/0303-070_frameunfocusedhover.png "0303-070_FrameUnfocusedHover")  
  
 **Frame: floating, unfocused**  
  
 Background (Glyph)  
  
 `EnvironmentRaftedWindowButtonHoverInactive`  
  
 Foreground (Glyph)  
  
 `Environment.RaftedWindowButtonHoverInactiveGlyph`  
  
 Border (Glyph)  
  
 `Environment.RaftedWindowButtonHoverInactiveBorder`  
  
 **Pressed**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Frame focused pressed](../extensibility/media/0303-071_framefocusedpressed.png "0303-071_FrameFocusedPressed")  
  
 **Frame: floating, focused**  
  
 Background (Glyph)  
  
 `Environment.RaftedWindowButtonDown`  
  
 Foreground (Glyph)  
  
 `Environment.RaftedWindowButtonDownGlyph`  
  
 Border (Glyph)  
  
 `Environment.RaftedWindowButtonDownBorder`  
  
### Document tabs  
 Document tabs sit in the tab channel to indicate which documents are currently open, along with which one is the current selected or active document. Tool windows can also be docked in the document tab channel if the user places them there. In this situation, they use the same tab colors as document windows. If you are creating UI that you want to always match the document window colors (including theme updates or if new themes are installed), then reference these color tokens.  
  
 ![Document tab redline](../extensibility/media/0303-072_documenttabredline.png "0303-072_DocumentTabRedline")  
  
 Use …  
 anywhere you are creating UI that you want to match document tabs and automatically pick up theme updates or new theme colors.  
  
 Do not use …  
 for any UI that you don’t want to change automatically when the shell has a theme update.  
  
#### Open document tabs  
 Each open document has a tab in the document tab channel that displays its name. Documents can be either selected or open in the background, and their tabs reflect these states:  
  
-   The selected tab represents the document that is currently displayed in the document well. A selected tab has a document border that extends across the top edge of the document well.  
  
-   Background tabs are any document tabs that are not the currently selected tab. Once clicked, they become the selected tab and acquire all background, border, and text colors from those token names.  
  
 ![Open document tab redline](../extensibility/media/0303-073_opendocumenttabredline.png "0303-073_OpenDocumentTabRedline")  
  
 Use …  
 when you are creating custom document tabs.  
  
 Do not use …  
 -   for provisional (preview) tabs.  
  
-   for any UI that you don't want to change automatically if the shell has a theme update.  
  
#### Selected tab  
 **Focused**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Selected tab focused](../extensibility/media/0303-074_selectedtabfocused.png "0303-074_SelectedTabFocused")  
  
 **Selected document tab, focused**  
  
 Background  
  
 `Environment.FileTabSelectedGradientTop`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `Environment.FileTabSelectedText`  
  
 Border  
  
 `Environment.FileTabSelectedBorder`  
  
 Set to same color as background.  
  
 Document border  
  
 `Environment.FileTabDocumentBorderBackground`  
  
 **Unfocused**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Selected tab unfocused](../extensibility/media/0303-075_selectedtabunfocused.png "0303-075_SelectedTabUnfocused")  
  
 **Selected document tab, unfocused**  
  
 Background  
  
 `Environment.FileTabInactiveGradientTop`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `Environment.FileTabInactiveText`  
  
 Border  
  
 `Environment.FileTabInactiveBorder`  
  
 Set to same color as background.  
  
 Document border  
  
 `Environment.FileTabInactiveDocumentBorderBackground`  
  
#### Background tab  
 **Default**  
  
 ![Background tab](../extensibility/media/0303-076_backgroundtab.png "0303-076_BackgroundTab")  
  
 **Background tab default**  
  
 Background  
  
 `Environment.FileTabBackground`  
  
 Foreground (Text)  
  
 `Environment.FileTabText`  
  
 Border  
  
 `Environment.FileTabBorder`  
  
 Set to same color as background.  
  
 **Hover**  
  
 ![Background tab on hover](../extensibility/media/0303-077_backgroundtabhover.png "0303-077_BackgroundTabHover")  
  
 **Background tab on hover**  
  
 Background  
  
 `Environment.FileTabHotGradientTop`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `Environment.FileTabHotText`  
  
 Border  
  
 `Environment.FileTabHotBorder`  
  
 Set to same color as background.  
  
#### Preview tab  
 The preview tab appears on the right side of the document tab channel when the user clicks an item in the Solution Explorer tool window. It acts as a preview of the document and also gives the user the option to keep the document open on the left side of the document tab channel. Only one preview tab open can be open at a time. Preview tabs have both background and selected states, like open tabs, and can be focused or unfocused in their active state.  
  
 ![Preview tab redline](../extensibility/media/0303-078_previewtabredline.png "0303-078_PreviewTabRedline")  
  
 Use …  
 anywhere you are creating provisional preview and want some element to match the current preview tab color.  
  
 Do not use …  
 -   for any kind of document or tab that is not provisional (preview).  
  
-   for any UI that you don't want to change automatically if the shell has a theme update.  
  
 **Selected preview tab: Focused**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Preview tab focused](../extensibility/media/0303-079_previewtabfocused.png "0303-079_PreviewTabFocused")  
  
 **Focused preview tab**  
  
 Background  
  
 `Environment.FileTabProvisionalSelectedActive`  
  
 Foreground (Text)  
  
 `Environment.FileTabProvisionalSelectedActiveForeground`  
  
 Border  
  
 `Environment.FileTabProvisionalSelectedActiveBorder`  
  
 Set to same color as background.  
  
 Document border  
  
 `Environment.FileTabProvisionalSelectedActiveBorder`  
  
 **Selected preview tab: Unfocused**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Preview tab unfocused](../extensibility/media/0303-080_previewtabunfocused.png "0303-080_PreviewTabUnfocused")  
  
 **Unfocused preview tab**  
  
 Background  
  
 `Environment.FileTabProvisionalSelectedInactive`  
  
 Foreground (Text)  
  
 `Environment.FileTabProvisionalSelectedInactiveForeground`  
  
 Border  
  
 `Environment.FileTabProvisionalSelectedInactiveBorder`  
  
 Document border  
  
 `Environment.FileTabProvisionalSelectedInactiveBorder`  
  
 **Background preview tab: Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Preview background tab](../extensibility/media/0303-081_previewbackgroundtab.png "0303-081_PreviewBackgroundTab")  
  
 **Preview tab background tab**  
  
 Background  
  
 `Environment.FileTabProvisionalInactive`  
  
 Foreground (Text)  
  
 `Environment.FileTabProvisionalInactiveForeground`  
  
 Border  
  
 `Environment.FileTabProvisionalInactiveBorder`  
  
 Set to same color as background.  
  
 **Background preview tab: Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Preview background tab on hover](../extensibility/media/0303-082_previewbackgroundtabhover.png "0303-082_PreviewBackgroundTabHover")  
  
 **Preview tab background tab on hover**  
  
 Background  
  
 `Environment.FileTabProvisionalHover`  
  
 Foreground (Text)  
  
 `Environment.FileTabProvisionalHoverForeground`  
  
 Border  
  
 `Environment.FileTabProvisionalHoverBorder`  
  
 Set to same color as background.  
  
#### Document overflow button  
 The document overflow button is present if there are one or more documents open, regardless of whether there is vertical space in the current configuration to fit all document tabs. The document overflow drop-down menu, which is controlled by the **CommandBarMenu** colors (see [Menus](../misc/shared-colors.md#BKMK_CommandMenus)), displays a list of all open documents, both visible and hidden, and the overflow glyph changes depending on whether all the open documents are displayed in the tab channel.  
  
 ![Overflow redline](../extensibility/media/0303-083_overflowredline.png "0303-083_OverflowRedline")  
  
 Use …  
 when you are creating a custom document overflow button.  
  
 Do not use …  
 -   for UI that is not similar to an overflow button.  
  
-   for command bar overflow buttons.  
  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Overflow](../extensibility/media/0303-084_overflow.png "0303-084_Overflow")  
  
 **Document overflow button**  
  
 Background  
  
 `Environment.DocWellOverflowButtonBackground`  
  
 Foreground (Glyph)  
  
 `Environment.DocWellOverflowButtonGlyph`  
  
 Border  
  
 N/A  
  
 **Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Overflow on hover](../extensibility/media/0303-085_overflowhover.png "0303-085_OverflowHover")  
  
 **Document overflow button on hover**  
  
 Background  
  
 `Environment.DocWellOverflowButtonMouseOverBackground`  
  
 Foreground (Glyph)  
  
 `Environment.DocWellOverflowButtonMouseOverGlyph`  
  
 Border  
  
 `Environment.DocWellOverflowButtonMouseOverBorder`  
  
 **Pressed**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Overflow pressed](../extensibility/media/0303-086_overflowpressed.png "0303-086_OverflowPressed")  
  
 **Pressed document overflow button**  
  
 Background  
  
 `Environment.DocWellOverflowButtonMouseDownBackground`  
  
 Foreground (Glyph)  
  
 `Environment.DocWellOverflowButtonMouseDownGlyph`  
  
 Border  
  
 `Environment.DocWellOverflowButtonMouseDownBorder`  
  
## Tool windows  
 There is no need to replicate tool windows, because they are provided by the Visual Studio environment. However, you might decide that you want to leverage the colors used in tool windows so that your UI always appears consistent with this part of the Visual Studio environment.  
  
 ![Tool window redline](../extensibility/media/0303-087_toolwindowredline.png "0303-087_ToolWindowRedline")  
  
 Use …  
 anywhere you are creating UI that you want to match tool windows.  
  
 Do not use …  
 for any UI that you don't want to change automatically if the shell has a theme update.  
  
### Tool window frame  
 Tool windows in Visual Studio are used for many different tasks, and can exist in one of several different states. If a tool window is open, it can be assigned to any of the four sides of the document area. Tool windows can also float outside of the IDE, which allows them to be repositioned anywhere within the user's screen. Floating windows always sit on top of the IDE. Finally, tool windows can be docked as document windows and appear as a tab in the document well. Tool windows that have been docked as document windows are colored in part using document window token names.  
  
 ![Tool window frame redline](../extensibility/media/0303-088_toolwindowframeredline.png "0303-088_ToolWindowFrameRedline")  
  
 Use …  
 anywhere you are creating UI that you want to match tool windows.  
  
 Do not use …  
 for any UI that you don't want to change automatically if the shell has a theme update.  
  
 **Docked**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Tool window docked](../extensibility/media/0303-089_toolwindowdocked.png "0303-089_ToolWindowDocked")  
  
 Background  
  
 `Environment.ToolWindowBackground`  
  
 Border  
  
 `Environment.ToolWindowBorder`  
  
 **Floating: focused**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Tool window focused](../extensibility/media/0303-090_toolwindowfocused.png "0303-090_ToolWindowFocused")  
  
 Background  
  
 `Environment.ToolWindowBackground`  
  
 Border  
  
 `Environment.MainWindowActiveDefaultBorder`  
  
 **Floating: unfocused**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Tool window unfocused](../extensibility/media/0303-091_toolwindowunfocused.png "0303-091_ToolWindowUnfocused")  
  
 Background  
  
 `Environment.ToolWindowBackground`  
  
 Border  
  
 `Environment.MainWindowInactiveBorder`  
  
### Tool window title bar  
 The title bar border is not a true border, but a thick line across the top of the title bar. It does not have a token name for its unfocused state.  
  
 ![Tool window title bar redline](../extensibility/media/0303-092_toolwindowtitlebarredline.png "0303-092_ToolWindowTitleBarRedline")  
  
 Use …  
 anywhere you are creating UI that you want to match tool windows.  
  
 Do not use …  
 for any UI that you don't want to change automatically if the shell has a theme update.  
  
 **Focused**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Title bar focused](../extensibility/media/0303-093_titlebarfocused.png "0303-093_TitleBarFocused")  
  
 **Focused title bar**  
  
 Background  
  
 `Environment.TitleBarActiveGradientBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `Environment.TitleBarActiveText`  
  
 Border  
  
 `Environment.TitleBarActiveBorder`  
  
 Set to same color as background.  
  
 Drag handle  
  
 `Environment.TitleBarDragHandleActive`  
  
 **Unfocused**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Title bar unfocused](../extensibility/media/0303-094_titlebarunfocused.png "0303-094_TitleBarUnfocused")  
  
 **Unfocused title bar**  
  
 Background  
  
 `Environment.TitleBarInactiveGradientBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `Environment.TitleBarInactiveText`  
  
 Border  
  
 N/A  
  
 Drag handle  
  
 `Environment.TitleBarDragHandle`  
  
#### Title bar buttons  
 ![Title bar button redline](../extensibility/media/0303-095_titlebarbuttonredline.png "0303-095_TitleBarButtonRedline")  
  
 Use …  
 for buttons that appear in UI that uses color tokens from the tool window title bars.  
  
 Do not use …  
 -   for buttons that appear in other locations.  
  
-   in any background/foreground combination other than specified.  
  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Title bar button focused](../extensibility/media/0303-096_titlebarbuttonfocused.png "0303-096_TitleBarButtonFocused")  
  
 **Focused**  
  
 Background  
  
 N/A  
  
 Foreground (Glyph)  
  
 `Environment.ToolWindowButtonActiveGlyph`  
  
 Border  
  
 N/A  
  
 ![Title bar button unfocused](../extensibility/media/0303-097_titlebarbuttonunfocused.png "0303-097_TitleBarButtonUnfocused")  
  
 **Unfocused**  
  
 Background  
  
 N/A  
  
 Foreground (Glyph)  
  
 `Environment.ToolWindowButtonInactiveGlyph`  
  
 Border  
  
 N/A  
  
 **Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Title bar button focused on hover](../extensibility/media/0303-098_titlebarbuttonfocusedhover.png "0303-098_TitleBarButtonFocusedHover")  
  
 **Focused**  
  
 Background  
  
 `Environment.ToolWindowButtonHoverActive`  
  
 Foreground (Glyph)  
  
 `Environment.ToolWindowButtonHoverActiveGlyph`  
  
 Border  
  
 `Environment.ToolWindowButtonHoverActiveBorder`  
  
 ![Title bar button unfocused on hover](../extensibility/media/0303-099_titlebarbuttonunfocusedhover.png "0303-099_TitleBarButtonUnfocusedHover")  
  
 **Unfocused**  
  
 Background  
  
 `Environment.ToolWindowButtonHoverInactive`  
  
 Foreground (Glyph)  
  
 `Environment.ToolWindowButtonHoverInactiveGlyph`  
  
 Border  
  
 `Environment.ToolWindowButtonHoverInactiveBorder`  
  
 **Pressed**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Title bar button focused and pressed](../extensibility/media/0303-100_titlebarbuttonfocusedpressed.png "0303-100_TitleBarButtonFocusedPressed")  
  
 **Focused**  
  
 Background  
  
 `Environment.ToolWindowButtonDown`  
  
 Foreground (Glyph)  
  
 `Environment.ToolWindowButtonDownActiveGlyph`  
  
 Border  
  
 `Environment.ToolWindowButtonDownBorder`  
  
 ![Title bar button unfocused and pressed](../extensibility/media/0303-101_titlebarbuttonunfocusedpressed.png "0303-101_TitleBarButtonUnfocusedPressed")  
  
 **Unfocused**  
  
 Background  
  
 `Environment.ToolWindowButtonDown`  
  
 Foreground (Glyph)  
  
 `Environment.ToolWindowButtonDownInactiveGlyph`  
  
 Border  
  
 `Environment.ToolWindowButtonDownBorder`  
  
### Tool window tabs  
 ![Tool window tab redline](../extensibility/media/0303-102_toolwindowtabredline.png "0303-102_ToolWindowTabRedline")  
  
 Use …  
 anywhere you are creating UI that you want to match tool windows.  
  
 Do not use …  
 for any UI that you don't want to change automatically if the shell has a theme update.  
  
 **Selected tab**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Tool window tab focused](../extensibility/media/0303-103_toolwindowtabfocused.png "0303-103_ToolWindowTabFocused")  
  
 **Selected, focused tool window tab**  
  
 Background  
  
 `Environment.ToolWindowTabSelectedTab`  
  
 Foreground (Text)  
  
 `Environment.ToolWindowTabSelectedActiveText`  
  
 Border  
  
 `Environment.ToolWindowTabSelectedBorder`  
  
 Set to same color as background.  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Tool window tab unfocused](../extensibility/media/0303-104_toolwindowtabunfocused.png "0303-104_ToolWindowTabUnfocused")  
  
 **Selected, unfocused tool window tab**  
  
 Background  
  
 `Environment.ToolWindowTabSelectedTab`  
  
 Foreground (Text)  
  
 `Environment.ToolWindowTabSelectedText`  
  
 Border  
  
 `Environment.ToolWindowTabSelectedBorder`  
  
 Set to same color as background.  
  
 **Background tab**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Tool window background tab](../extensibility/media/0303-105_toolwindowbackgroundtab.png "0303-105_ToolWindowBackgroundTab")  
  
 **Background tool window tab**  
  
 Background  
  
 `Environment.ToolWindowTabGradientBegin`  
  
 Gradient stops set to the same color value in Visual Studio 2013.  
  
 `Environment.ToolWindowTabGradientEnd`  
  
 Gradient stops set to the same color value in Visual Studio 2013.  
  
 Foreground (Text)  
  
 `Environment.ToolWindowTabText`  
  
 Border  
  
 `Environment.ToolWindowTabBorder`  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Tool window background tab on hover](../extensibility/media/0303-106_toolwindowbackgroundtabhover.png "0303-106_ToolWindowBackgroundTabHover")  
  
 **Background tool window tab on hover**  
  
 Background  
  
 `Environment.ToolWindowTabMouseOverBackgroundBegin`  
  
 Gradient stops set to the same color value in Visual Studio 2013.  
  
 `Environment.ToolWindowTabMouseOverBackgroundEnd`  
  
 Gradient stops set to the same color value in Visual Studio 2013.  
  
 Foreground (Text)  
  
 `Environment.ToolWindowTabMouseOverText`  
  
 Border  
  
 `Environment.ToolWindowTabMouseOverBorder`  
  
 Set to same color as background.  
  
### Auto-hide tabs  
 ![Auto&#45;hide redline](../extensibility/media/0303-107_autohideredline.png "0303-107_AutoHideRedline")  
  
 Use …  
 anywhere you are creating UI that you want to match auto-hidden tool window tabs.  
  
 Do not use …  
 for any UI that you don’t want to change automatically if the shell has a theme update.  
  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Auto&#45;hide tab](../extensibility/media/0303-108_autohidetab.png "0303-108_AutoHideTab")  
  
 **Default auto-hide tab**  
  
 Background  
  
 `Environment.AutoHideTabBackgroundBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `Environment.AutoHideTabText`  
  
 Border  
  
 `Environment.AutoHideTabBorder`  
  
 **Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Auto&#45;hide tab on hover](../extensibility/media/0303-109_autohidetabhover.png "0303-109_AutoHideTabHover")  
  
 **Auto-hide tab on hover**  
  
 Background  
  
 `Environment.AutoHideTabMouseOverBackgroundBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `Environment.AutoHideTabMouseOverText`  
  
 Border  
  
 `Environment.AutoHideTabMouseOverBorder`  
  
## Common shared controls  
 When you use a standard Visual Studio command bar in your feature, you will have access to styled shell controls, and you should not re-template these common controls. However, if you need to build a custom command bar, you might need to build custom controls as well. In that case, make sure to use the correct token names for each of the following controls so that your UI is consistent with the rest of Visual Studio.  
  
### Search box  
 Whenever possible, use the common search control provided by the Visual Studio environment. Search box colors are found in the "SearchControl" category in the **ShellColors.pkgdef** file, which contains token names for the input field, action button, drop-down button, and drop-down menu.  
  
 A search box can be one of several states, some of which are mutually exclusive:  
  
-   "Focused" or "unfocused" refers to whether or not the cursor is in the text box.  
  
-   "Active" or "inactive" refers to whether the user has input a search query in the text box.  
  
-   "Hover" means that the user has moused over the search box with the mouse (this state overrides all other states).  
  
-   "Disabled" means that search functionality is turned off for the current context.  
  
 ![Search box redline](../extensibility/media/0303-110_searchboxredline.png "0303-110_SearchBoxRedline")  
  
 Use …  
 when you are designing a custom search box.  
  
 Do not use …  
 -   for anything that is not a search box.  
  
-   for anything that you do not want always to match the search box UI.  
  
 **Focused**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Search input field focused](../extensibility/media/0303-111_searchinputfieldfocused.png "0303-111_SearchInputFieldFocused")  
  
 **Input field**  
  
 Background  
  
 `SearchControl.FocusedBackground`  
  
 Foreground (Text)  
  
 `SearchControl.FocusedBackground`  
  
 Border  
  
 `SearchControl.FocusedBorder`  
  
 Separator  
  
 `SearchControl.FocusedDropDownSeparator`  
  
 ![Search action button focused](../extensibility/media/0303-112_searchactionbuttonfocused.png "0303-112_SearchActionButtonFocused")  
  
 **Action button**  
  
 Background  
  
 None  
  
 Foreground (Search glyph)  
  
 `SearchControl.SearchGlyph`  
  
 Foreground (Stop glyph)  
  
 `SearchControl.StopGlyph`  
  
 Foreground (Clear glyph)  
  
 `SearchControl.ClearGlyph`  
  
 Border  
  
 N/A  
  
 ![Search drop&#45;down button focused](../extensibility/media/0303-113_searchdropdownbuttonfocused.png "0303-113_SearchDropdownButtonFocused")  
  
 **Drop-down button**  
  
 Background  
  
 `SearchControl.FocusedDropDownButton`  
  
 Foreground (Glyph)  
  
 `SearchControl.FocusedDropDownButtonGlyph`  
  
 Border  
  
 `SearchControl.FocusedDropDownButtonBorder`  
  
 **Unfocused**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Search input field unfocused](../extensibility/media/0303-114_searchinputfieldunfocused.png "0303-114_SearchInputFieldUnfocused")  
  
 **Active input field**  
  
 Background  
  
 `SearchControl.SearchActiveBackground`  
  
 Foreground (Text)  
  
 `SearchControl.SearchActiveBackground`  
  
 Border  
  
 `SearchControl.UnfocusedBorder`  
  
 Separator  
  
 `SearchControl.DropDownSeparator`  
  
 ![Search input field unfocused and inactive](../extensibility/media/0303-114-1_searchinputfieldunfocusedinactive.png "0303-114-1_SearchInputFieldUnfocusedInactive")  
  
 **Inactive input field**  
  
 Background  
  
 `SearchControl.Unfocused`  
  
 Foreground (Text)  
  
 `SearchControl.Unfocused`  
  
 Border  
  
 `SearchControl.UnfocusedBorder`  
  
 Separator  
  
 `SearchControl.DropDownSeparator`  
  
 ![Search action button unfocused](../extensibility/media/0303-115_searchactionbuttonunfocused.png "0303-115_SearchActionButtonUnfocused")  
  
 **Action button**  
  
 Background  
  
 N/A  
  
 Foreground (Search glyph)  
  
 `SearchControl.SearchGlyph`  
  
 Foreground (Stop glyph)  
  
 `SearchControl.StopGlyph`  
  
 Foreground (Clear glyph)  
  
 `SearchControl.ClearGlyph`  
  
 Border  
  
 N/A  
  
 ![Search drop&#45;down button unfocused](../extensibility/media/0303-116_searchdropdownbuttonunfocused.png "0303-116_SearchDropdownButtonUnfocused")  
  
 **Drop-down button**  
  
 Background  
  
 `SearchControl.UnfocusedDropDownButton`  
  
 Foreground (Glyph)  
  
 `SearchControl.UnfocusedDropDownButtonGlyph`  
  
 Border  
  
 `SearchControl.UnfocusedDropDownButtonBorder`  
  
 **Pressed**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Search action button pressed](../extensibility/media/0303-116-1_searchactionbuttonpressed.png "0303-116-1_SearchActionButtonPressed")  
  
 **Action button**  
  
 Background  
  
 `SearchControl.ActionButtonMouseDown`  
  
 Foreground (Glyph)  
  
 `SearchControl.ActionButtonMouseDownGlyph`  
  
 Border  
  
 `SearchControl.ActionButtonMouseDownBorder`  
  
 ![Search drop&#45;down button pressed](../extensibility/media/0303-116-2_searchdropdownbuttonpressed.png "0303-116-2_SearchDropdownButtonPressed")  
  
 **Drop-down button**  
  
 Background  
  
 `SearchControl.MouseDownDropDownButton`  
  
 Foreground (Glyph)  
  
 `SearchControl.MouseDownDropDownButtonGlyph`  
  
 Border  
  
 `SearchControl.MouseDownDropDownButtonBorder`  
  
 **Highlighted (Text only)**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Search input field highlight](../extensibility/media/0303-120_searchinputfieldhighlight.png "0303-120_SearchInputFieldHighlight")  
  
 **Input field with text highlighted**  
  
 Background  
  
 `SearchControl.Selection`  
  
 Foreground (Text)  
  
 `SearchControl.FocusedBackground`  
  
 Border  
  
 None  
  
 Separator  
  
 `SearchControl.FocusedDropDownSeparator`  
  
 **Disabled**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Search input field disabled](../extensibility/media/0303-121_searchinputfielddisabled.png "0303-121_SearchInputFieldDisabled")  
  
 **Input field**  
  
 Background  
  
 `SearchControl.Disabled`  
  
 Foreground (Text)  
  
 `SearchControl.Disabled`  
  
 Border  
  
 `SearchControl.DisabledBorder`  
  
 Separator  
  
 `SearchControl.DropDownSeparator`  
  
 ![Search action button disabled](../extensibility/media/0303-122_searchactionbuttondisabled.png "0303-122_SearchActionButtonDisabled")  
  
 **Action button**  
  
 Background  
  
 None  
  
 Foreground (Glyph)  
  
 `SearchControl.ActionButtonDisabledGlyph`  
  
 Border  
  
 None  
  
 ![Search drop&#45;down button disabled](../extensibility/media/0303-123_searchdropdownbuttondisabled.png "0303-123_SearchDropdownButtonDisabled")  
  
 **Drop-down button**  
  
 Background  
  
 None  
  
 Foreground (Glyph)  
  
 `SearchControl.DisabledDownButtonGlyph`  
  
 Border  
  
 None  
  
#### Search drop-down lists  
 The search box dropdown menu has the potential to be slightly more complex than other dropdown menus in Visual Studio. The "suggested searches" and "search options" sections can appear alone or together in the menu and each one is colored separately. A line also separates these two sections when they appear together and a border surrounds the entire dropdown menu.  
  
 ![Search drop&#45;down redline](../extensibility/media/0303-124_searchdropdownredline.png "0303-124_SearchDropdownRedline")  
  
 Use …  
 -   when you are creating a custom search dropdown list.  
  
-   the correct token names for the correct list components.  
  
 Do not use …  
 -   for dropdown lists that appear in other contexts.  
  
-   in any background/foreground combination other than specified.  
  
 **Default (no other states)**  
  
 Element  
  
 Token name: Category.color  
  
 Border  
  
 `SearchControl.PopupBorder`  
  
 Separator  
  
 `SearchControl.PopupSectionHeaderSeparator`  
  
 Shadow  
  
 `Environment.DropShadowBackground`  
  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Search suggested](../extensibility/media/0303-125_searchsuggested.png "0303-125_SearchSuggested")  
  
 **Suggested searches**  
  
 Background  
  
 `SearchControl.PopupItemsListBackgroundGradientBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `SearchControl.PopupItemText`  
  
 ![Search check box](../extensibility/media/0303-126_searchcheckbox.png "0303-126_SearchCheckbox")  
  
 **Search options (check box)**  
  
 ![Search options](../extensibility/media/0303-127_searchoptions.png "0303-127_SearchOptions")  
  
 **Search options (link)**  
  
 Background  
  
 `SearchControl.PopupSectionBackgroundGradientBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Check box text)  
  
 `SearchControl.PopupCheckboxText`  
  
 Foreground (Link text)  
  
 `SearchControl.PopupButtonText`  
  
 Header background  
  
 `SearchControl.PopupSectionHeaderGradientBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Header text)  
  
 `SearchControl.PopupSectionHeaderText`  
  
 **Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Search suggested on hover](../extensibility/media/0303-128_searchsuggestedhover.png "0303-128_SearchSuggestedHover")  
  
 **Suggested searches**  
  
 Background  
  
 `SearchControl.PopupControlMouseOverBackgroundGradientBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Text)  
  
 `SearchControl.PopupMouseOverItemText`  
  
 Border  
  
 `SearchControl.PopupControlMouseOverBorder`  
  
 ![Search check box on hover](../extensibility/media/0303-129_searchcheckboxhover.png "0303-129_SearchCheckboxHover")  
  
 **Suggested searches (check box)**  
  
 ![Search options on hover](../extensibility/media/0303-130_searchoptionshover.png "0303-130_SearchOptionsHover")  
  
 **Search options**  
  
 Background  
  
 `SearchControl.PopupControlMouseOverBackgroundGradientBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Check box text)  
  
 `SearchControl.PopupCheckboxMouseDownText`  
  
 Foreground (Link text)  
  
 `SearchControl.PopupButtonMouseDownText`  
  
 Border  
  
 `SearchControl.PopupControlMouseOverBorder`  
  
 **Pressed**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Search suggested pressed](../extensibility/media/0303-131_searchsuggestedpressed.png "0303-131_SearchSuggestedPressed")  
  
 **Suggested searches (check box)**  
  
 ![Search options pressed](../extensibility/media/0303-132_searchoptionspressed.png "0303-132_SearchOptionsPressed")  
  
 **Search options**  
  
 Check box background  
  
 `SearchControl.PopupControlMouseDownBackgroundGradientBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 `SearchControl.PopupControlMouseDownBackgroundGradientEnd`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Check box text)  
  
 `SearchControl.PopupCheckboxMouseDownText`  
  
 Link background  
  
 `SearchControl.PopupButtonMouseDownBackgroundGradientBegin`  
  
 While not used in modern themed UI, there are gradient stops and values for this background.  
  
 Foreground (Link text)  
  
 `SearchControl.PopupButtonMouseDownText`  
  
### Hyperlink  
 The hyperlink is one control that does not have a foreground/background pair. In all cases, use the foreground hyperlink color, which will appear correctly on dark, gray and white backgrounds. If you do not use the color token for the hyperlink control, you will see the default system color for "pressed,"" which will flash red. That is the signal that the control is not using the correct environment color token.  
  
 ![Hyperlink redline](../extensibility/media/0303-133_hyperlinkredline.png "0303-133_HyperlinkRedline")  
  
 Use …  
 when you need to create a custom hyperlink.  
  
 Do not use …  
 for anything that is not a hyperlink.  
  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Hyperlink default](../extensibility/media/0303-134_hyperlink.png "0303-134_Hyperlink")  
  
 Foreground (Text)  
  
 `Environment.PanelHyperlink`  
  
 **Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Hyperlink on hover](../extensibility/media/0303-135_hyperlinkhover.png "0303-135_HyperlinkHover")  
  
 Foreground (Text)  
  
 `Environment.PanelHyperlinkHover`  
  
 **Pressed**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Hyperlink pressed](../extensibility/media/0303-136_hyperlinkpressed.png "0303-136_HyperlinkPressed")  
  
 Foreground (Text)  
  
 `Environment.PanelHyperlinkPressed`  
  
 **Disabled**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Hyperlink disabled](../extensibility/media/0303-137_hyperlinkdisabled.png "0303-137_HyperlinkDisabled")  
  
 Foreground (Text)  
  
 `Environment.PanelHyperlinkDisabled`  
  
### Infobar  
 Infobars are used to provide more information about a given context and always appear at the top of a document window or tool window.  
  
 ![Infobar redline](../extensibility/media/0303-138_infobarredline.png "0303-138_InfobarRedline")  
  
 Use …  
 when creating custom infobars.  
  
 Do not use …  
 for UI elements that are not similar to an infobar.  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Infobar](../extensibility/media/0303-139_infobar.png "0303-139_Infobar")  
  
 **Infobar**  
  
 Background  
  
 `Environment.InfoBackground`  
  
 Foreground (Text)  
  
 `Environment.InfoText`  
  
 Border  
  
 `Environment.ToolWindowBorder`  
  
### Scroll bar  
 Scroll bars are styled by the Visual Studio environment, and will not need to be themed. However, you might decide that you want to leverage the colors used in scroll bars so that your UI always appears consistent with this this part of the Visual Studio environment.  
  
 ![Scroll bar redline](../extensibility/media/0303-140_scrollbarredline.png "0303-140_ScrollbarRedline")  
  
 Use …  
 when you are creating UI that you want to match Visual Studio scrollbars.  
  
 Do not use ...  
 for anything you don't want to always match scrollbar UI.  
  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Scroll bar](../extensibility/media/0303-141_scrollbar.png "0303-141_Scrollbar")  
  
 **Scrollbar**  
  
 Scrollbar  
  
 `Environment.ScrollBarBackground`  
  
 Foreground (Thumb)  
  
 `Environment.ScrollBarThumbBackground`  
  
 ![Scroll bar arrow](../extensibility/media/0303-142_scrollbararrow.png "0303-142_ScrollbarArrow")  
  
 **Scroll arrow**  
  
 Background  
  
 `Environment.ScrollBarArrowBackground`  
  
 Set to same color as scroll bar.  
  
 Foreground (Glyph)  
  
 `Environment.ScrollBarArrowGlyph`  
  
 **Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Scroll bar on hover](../extensibility/media/0303-143_scrollbarhover.png "0303-143_ScrollbarHover")  
  
 **Scrollbar**  
  
 Scrollbar  
  
 `Environment.ScrollBarBackground`  
  
 Foreground (Thumb)  
  
 `Environment.ScrollBarThumbMouseOverBackground`  
  
 ![Scroll bar arrow on hover](../extensibility/media/0303-144_scrollbararrowhover.png "0303-144_ScrollbarArrowHover")  
  
 **Scroll arrow**  
  
 Background  
  
 `Environment.ScrollBarArrowMouseOverBackground`  
  
 Set to same color as scroll bar.  
  
 Foreground (Glyph)  
  
 `Environment.ScrollBarArrowGlyphMouseOver`  
  
 **Pressed**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Scroll bar pressed](../extensibility/media/0303-145_scrollbarpressed.png "0303-145_ScrollbarPressed")  
  
 **Scrollbar**  
  
 Scrollbar  
  
 `Environment.ScrollBarBackground`  
  
 Foreground (Thumb)  
  
 `Environment.ScrollBarThumbPressedBackground`  
  
 ![Scroll bar arrow pressed](../extensibility/media/0303-146_scrollbararrowpressed.png "0303-146_ScrollbarArrowPressed")  
  
 **Scroll arrow**  
  
 Background  
  
 `Environment.ScrollBarArrowPressedBackground`  
  
 Set to same color as scrollbar.  
  
 Foreground (Glyph)  
  
 `Environment.ScrollBarArrowGlyphPressed`  
  
###  <a name="BKMK_TreeView"></a> Tree view  
 Several tool windows, including the Solution Explorer, Server Explorer, and Class View, implement a hierarchical organizational scheme whose colors are controlled by color names in the TreeView category. All items in a tree view have background and text colors. Items that have nested child elements also have glyphs that indicate whether the item is expanded or collapsed.  
  
 ![Tree view redline](../extensibility/media/0303-147_treeviewredline.png "0303-147_TreeViewRedline")  
  
 Use …  
 anywhere you need to implement a hierarchical organizational view.  
  
 Do not use …  
 -   for anything that is not similar to a tree view.  
  
-   in any background/foreground combination other than specified.  
  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Tree view](../extensibility/media/0303-148_treeview.png "0303-148_TreeView")  
  
 Background  
  
 `TreeView.Background`  
  
 Foreground (Text)  
  
 `TreeView.Background`  
  
 Foreground (Glyph)  
  
 `TreeView.Glyph`  
  
 Border  
  
 None  
  
 **Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Tree view on hover](../extensibility/media/0303-149_treeviewhover.png "0303-149_TreeViewHover")  
  
 Background  
  
 `TreeView.Background`  
  
 Foreground (Text)  
  
 `TreeView.Background`  
  
 Foreground (Glyph)  
  
 `TreeView.GlyphMouseOver`  
  
 Border  
  
 None  
  
 **Drag over**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Tree view dragover](../extensibility/media/0303-150_treeviewdragover.png "0303-150_TreeViewDragOver")  
  
 Background  
  
 `TreeView.DragOverItem`  
  
 Foreground (Text)  
  
 `TreeView.DragOverItem`  
  
 Foreground (Glyph)  
  
 `TreeView.DragOverItemGlyph`  
  
 Border  
  
 None  
  
 **Selected**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Tree view focused](../extensibility/media/0303-151_treeviewfocused.png "0303-151_TreeViewFocused")  
  
 **Focused**  
  
 Background  
  
 `TreeView.SelectedItemActive`  
  
 Foreground (Text)  
  
 `TreeView.SelectedItemActive`  
  
 Foreground (Glyph)  
  
 `TreeView.SelectedItemActiveGlyph`  
  
 Border  
  
 `TreeView.FocusVisualBorder`  
  
 ![Tree view unfocused](../extensibility/media/0303-152_treeviewunfocused.png "0303-152_TreeViewUnfocused")  
  
 **Unfocused**  
  
 Background  
  
 `TreeView.SelectedItemInactive`  
  
 Foreground (Text)  
  
 `TreeView.SelectedItemInactive`  
  
 Foreground (Glyph)  
  
 `TreeView.SelectedItemInactiveGlyph`  
  
 Border  
  
 None  
  
 **Hover over selected**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Tree view focused on hover](../extensibility/media/0303-153_treeviewfocusedhover.png "0303-153_TreeViewFocusedHover")  
  
 **Focused**  
  
 Background  
  
 `TreeView.SelectedItemActive`  
  
 Foreground (Text)  
  
 `TreeView.SelectedItemActive`  
  
 Foreground (Glyph)  
  
 `TreeView.SelectedItemActiveGlyphMouseOver`  
  
 Border  
  
 None`TreeView.FocusVisualBorder`  
  
 ![Tree view unfocused on hover](../extensibility/media/0303-154_treeviewunfocusedhover.png "0303-154_TreeViewUnfocusedHover")  
  
 **Unfocused**  
  
 Background  
  
 `TreeView.SelectedItemInactive`  
  
 Foreground (Text)  
  
 `TreeView.SelectedItemInactive`  
  
 Foreground (Glyph)  
  
 `TreeView.SelectedItemActiveGlyphMouseOver`  
  
 Border  
  
 None  
  
### Button controls  
 ![Button control redline](../extensibility/media/0303-155_buttoncontrolredline.png "0303-155_ButtonControlRedline")  
  
 Use …  
 for buttons in the document well that you want to integrate with Visual Studio themes (Light, Dark, Blue, or a system High Contrast theme).  
  
 Do not use …  
 for buttons that will display against a custom background that is not part of a Visual Studio theme.  
  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Button](../extensibility/media/0303-156_button.png "0303-156_Button")  
  
 Button  
  
 `CommonControls.Button`  
  
 Button border  
  
 `CommonControls.ButtonBorder`  
  
 **Disabled**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Button disabled](../extensibility/media/0303-157_buttondisabled.png "0303-157_ButtonDisabled")  
  
 Button  
  
 `CommonControls.ButtonDisabled`  
  
 Button border  
  
 `CommonControls.ButtonBorderDisabled`  
  
 **Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Button on hover](../extensibility/media/0303-158_buttonhover.png "0303-158_ButtonHover")  
  
 Button  
  
 `CommonControls.ButtonHover`  
  
 Button border  
  
 `CommonControls.ButtonBorderHover`  
  
 **Pressed**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Button pressed](../extensibility/media/0303-159_buttonpressed.png "0303-159_ButtonPressed")  
  
 Button  
  
 `CommonControls.ButtonPressed`  
  
 Button border  
  
 `CommonControls.ButtonBorderPressed`  
  
 **Focused**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Button focused](../extensibility/media/0303-160_buttonfocused.png "0303-160_ButtonFocused")  
  
 Button  
  
 `CommonControls.ButtonFocused`  
  
 Button border  
  
 `CommonControls.ButtonBorderFocused`  
  
### Check box controls  
 ![Check box redline](../extensibility/media/0303-161_checkboxredline.png "0303-161_CheckboxRedline")  
  
 Use …  
 for check box controls contained within the document well.  
  
 Do not use …  
 for any UI that is not a check box control.  
  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Check box](../extensibility/media/0303-162_checkbox.png "0303-162_Checkbox")  
  
 Background  
  
 `CommonControls.CheckBoxBackground`  
  
 Border  
  
 `CommonControls.CheckBoxBorder`  
  
 Text  
  
 `CommonControls.CheckBoxText`  
  
 Glyph  
  
 `CommonControls.CheckBoxGlyph`  
  
 **Disabled**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Check box disabled](../extensibility/media/0303-163_checkboxdisabled.png "0303-163_CheckboxDisabled")  
  
 Background  
  
 `CommonControls.CheckBoxBackgroundDisabled`  
  
 Border  
  
 `CommonControls.CheckBoxBorderDisabled`  
  
 Text  
  
 `CommonControls.CheckBoxTextDisabled`  
  
 Glyph  
  
 `CommonControls.CheckBoxGlyphDisabled`  
  
 **Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Check box on hover](../extensibility/media/0303-164_checkboxhover.png "0303-164_CheckboxHover")  
  
 Background  
  
 `CommonControls.CheckBoxBackgroundHover`  
  
 Border  
  
 `CommonControls.CheckBoxBorderHover`  
  
 Text  
  
 `CommonControls.CheckBoxTextHover`  
  
 Glyph  
  
 `CommonControls.CheckBoxGlyphHover`  
  
 **Pressed**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Check box pressed](../extensibility/media/0303-165_checkboxpressed.png "0303-165_CheckboxPressed")  
  
 Background  
  
 `CommonControls.CheckBoxBackgroundPressed`  
  
 Border  
  
 `CommonControls.CheckBoxBorderPressed`  
  
 Text  
  
 `CommonControls.CheckBoxTextPressed`  
  
 Glyph  
  
 `CommonControls.CheckBoxGlyphPressed`  
  
 **Focused**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Check box focused](../extensibility/media/0303-166_checkboxfocused.png "0303-166_CheckboxFocused")  
  
 Background  
  
 `CommonControls.CheckBoxBackgroundFocused`  
  
 Border  
  
 `CommonControls.CheckBoxBorderFocused`  
  
 Text  
  
 `CommonControls.CheckBoxTextFocused`  
  
 Glyph  
  
 `CommonControls.CheckBoxGlyphFocused`  
  
### Drop box/combo box controls  
 ![Drop&#45;down&#47;combo box redline](../extensibility/media/0303-167_dropdowncomboboxredline.png "0303-167_DropDownComboBoxRedline")  
  
 Use …  
 for drop-downs and combo boxes that are part of the document well.  
  
 Do not use …  
 -   for any UI that is not a drop-down or combo box.  
  
-   for a [Drop-down](../misc/shared-colors.md#BKMK_CommandDropDown) or [Combo box](../misc/shared-colors.md#BKMK_CommandComboBox) in the command bar.  
  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Drop&#45;down&#47;combo box](../extensibility/media/0303-168_dropdowncombobox.png "0303-168_DropDownComboBox")  
  
 Background  
  
 `CommonControls.ComboBoxBackground`  
  
 Border  
  
 `CommonControls.ComboBoxBorder`  
  
 Text  
  
 `CommonControls.ComboBoxText`  
  
 Separator  
  
 `CommonControls.ComboBoxSeparator`  
  
 Glyph  
  
 `CommonControls.ComboBoxGlyph`  
  
 Glyph background  
  
 `CommonControls.ComboBoxGlyphBackground`  
  
 **Disabled**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Drop&#45;down&#47;combo box disabled](../extensibility/media/0303-169_dropdowncomboboxdisabled.png "0303-169_DropDownComboBoxDisabled")  
  
 Background  
  
 `CommonControls.ComboBoxBackgroundDisabled`  
  
 Border  
  
 `CommonControls.ComboBoxBorderDisabled`  
  
 Text  
  
 `CommonControls.ComboBoxTextDisabled`  
  
 Separator  
  
 `CommonControls.ComboBoxSeparatorDisabled`  
  
 Glyph  
  
 `CommonControls.ComboBoxGlyphDisabled`  
  
 Glyph background  
  
 `CommonControls.ComboBoxGlyphBackgroundDisabled`  
  
 **Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Drop&#45;down&#47;combo box on hover](../extensibility/media/0303-170_dropdowncomboboxhover.png "0303-170_DropDownComboBoxHover")  
  
 Background  
  
 `CommonControls.ComboBoxBackgroundHover`  
  
 Border  
  
 `CommonControls.ComboBoxBorderHover`  
  
 Text  
  
 `CommonControls.ComboBoxTextHover`  
  
 Separator  
  
 `CommonControls.ComboBoxSeparatorHover`  
  
 Glyph  
  
 `CommonControls.ComboBoxGlyphHover`  
  
 Glyph background  
  
 `CommonControls.ComboBoxGlyphBackgroundHover`  
  
 **Pressed**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Drop&#45;down&#47;combo box pressed](../extensibility/media/0303-171_dropdowncomboboxpressed.png "0303-171_DropDownComboBoxPressed")  
  
 Background  
  
 `CommonControls.ComboBoxBackgroundPressed`  
  
 Border  
  
 `CommonControls.ComboBoxBorderPressed`  
  
 Text  
  
 `CommonControls.ComboBoxTextPressed`  
  
 Separator  
  
 `CommonControls.ComboBoxSeparatorPressed`  
  
 Glyph  
  
 `CommonControls.ComboBoxGlyphPressed`  
  
 Glyph background  
  
 `CommonControls.ComboBoxGlyphBackgroundPressed`  
  
 **Focused**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Drop&#45;down&#47;combo box focused](../extensibility/media/0303-172_dropdowncomboboxfocused.png "0303-172_DropDownComboBoxFocused")  
  
 Background  
  
 `CommonControls.ComboBoxBackgroundFocused`  
  
 Border  
  
 `CommonControls.ComboBoxBorderFocused`  
  
 Text  
  
 `CommonControls.ComboBoxTextFocused`  
  
 Separator  
  
 `CommonControls.ComboBoxSeparatorFocused`  
  
 Glyph  
  
 `CommonControls.ComboBoxGlyphFocused`  
  
 Glyph background  
  
 `CommonControls.ComboBoxGlyphBackgroundFocused`  
  
 **Text input selection**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Drop&#45;down&#47;combo box text input](../extensibility/media/0303-173_dropdowncomboboxtextinput.png "0303-173_DropDownComboBoxTextInput")  
  
 Highlight  
  
 `CommonControls.ComboBoxTextInputSelection`  
  
 **Pressed – List item view**  
  
 ![Drop&#45;down&#47;combo box list view](../extensibility/media/0303-174_dropdowncomboboxlistview.png "0303-174_DropDownComboBoxListView")  
  
 Background  
  
 `CommonControls.ComboBoxListBackground`  
  
 `CommonControls.ComboBoxListBackgroundHover`  
  
 `CommonControls.ComboBoxListItemBackgroundPressed`  
  
 `CommonControls.ComboBoxListItemBackgroundFocused`  
  
 Border  
  
 `CommonControls.ComboBoxListBorder`  
  
 `CommonControls.ComboBoxListBorderHover`  
  
 `CommonControls.ComboBoxListBorderPressed`  
  
 `CommonControls.ComboBoxListBorderFocused`  
  
 Item text  
  
 `CommonControls.ComboBoxListItemText`  
  
 `CommonControls.ComboBoxListItemTextHover`  
  
 `CommonControls.ComboBoxListItemTextPressed`  
  
 `CommonControls.ComboBoxListItemTextFocused`  
  
 Background shadow  
  
 `CommonControls.ComboBoxListBackgroundShadow`  
  
### Tabular data (grid) controls  
 Tabular data controls, also known as grid controls, are common controls for Visual Studio that can be used to present large amounts of data in multiple columns. Standard tabular data controls can be found in multiple places within Visual Studio: the Error List tool window, IntelliTrace reports, and memory heap view, among others. Always use the standard tabular data controls provided. In some rare instances, you might not have access to the standard tabular data controls. In these situations, use the following token names to ensure that your UI is consistent with other tabular data controls in Visual Studio.  
  
 ![Tabular data &#40;grid control&#41; redline](../extensibility/media/0303-197_tabulardatagridcontrolredline.png "0303-197_TabularDataGridControlRedline")  
  
 Use …  
 for tabular or grid controls.  
  
 Do not use …  
 for any UI that is not a tabular or grid control.  
  
#### Column headers  
 Column headers consist of a background, a border, the title text, and an optional glyph usually used when a grid is sorted by that column.  
  
 State  
  
 Element  
  
 Token name: Category.color  
  
 Default  
  
 Background  
  
 `Header.Default`  
  
 Foreground (Text)  
  
 `Environment.CommandBarTextActive`  
  
 Foreground (Glyph)  
  
 `Header.Glyph`  
  
 Border  
  
 `Header.SeparatorLine`  
  
 Hover  
  
 Background  
  
 `Header.MouseOver`  
  
 Foreground (Text)  
  
 `Environment.CommandBarTextHover`  
  
 Foreground (Glyph)  
  
 `Header.MouseOverGlyph`  
  
 Border  
  
 `Header.SeparatorLine`  
  
 Pressed  
  
 Background  
  
 `CommonControls.CheckBoxBackgroundPressed`  
  
 Foreground (Text)  
  
 `CommonControls.CheckBoxBorderPressed`  
  
 Foreground (Glyph)  
  
 `CommonControls.CheckBoxTextPressed`  
  
 Border  
  
 `CommonControls.CheckBoxGlyphPressed`  
  
#### List view items  
 List view items consist of a background and the content. The content can be text, an icon, or both.  
  
 State  
  
 Element  
  
 Token name: Category.color  
  
 Default  
  
 Background  
  
 Transparent  
  
 Foreground (Text)  
  
 `Environment.CommandBarTextActive`  
  
 Border  
  
 None  
  
 Selected (active)  
  
 Background  
  
 `TreeView.SelectedItemActive`  
  
 Foreground (Text)  
  
 `TreeView.SelectedItemActiveText`  
  
 Border  
  
 None  
  
 Selected (inactive)  
  
 Background  
  
 `TreeView.SelectedItemInactive`  
  
 Foreground (Text)  
  
 `TreeView.SelectedItemInactiveText`  
  
 Border  
  
 None  
  
## Manifest Designer  
 The Manifest Designer was designed as a way to make it easier to edit the manifest file in Windows 8 and Windows Phone 8 projects. While there is no shared framework available for consumption, it might be appropriate for you to match the design layout and colors of the orientation/navigation tabs and overall structure. For more information about layout details, see [Layout for Visual Studio](../extensibility/layout-for-visual-studio.md).  
  
 ![Manifest Designer redline](../extensibility/media/0303-175_manifestdesignerredline.png "0303-175_ManifestDesignerRedline")  
  
 Use …  
 -   for designers that are similar to the Manifest Designer.  
  
-   in place of using common tab controls at the top of an editor within the document well.  
  
 Do not use …  
 -   if you have more than six tabs.  
  
-   for any UI that is not structured like the Manifest Designer.  
  
 State  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 Default (selected)  
  
 Tab  
  
 Background  
  
 `ManifestDesigner.TabActive`  
  
 Border  
  
 None  
  
 Description pane  
  
 Background  
  
 `ManifestDesigner.DescriptionPane`  
  
 Content page  
  
 Background  
  
 `ManifestDesigner.Background`  
  
 Dialog helper text  
  
 `ManifestDesigner.WatermarkText`  
  
 This token name does not match its function.  
  
 Non-selected  
  
 Tab  
  
 Background  
  
 `ManifestDesigner.Tab.Inactive`  
  
 Hover  
  
 Tab  
  
 Background  
  
 `ManifestDesigner.Tab.Mouseover`  
  
## Tagging  
 Visual Studio supports tagging, which allows a user to declare searchable keywords for tracking purposes. For example, project managers and developers can use Team Foundation Server (TFS) to tag work items. The tables below give color names for both the tag itself and the "close icon" glyph that appears in hover and selected states.  
  
 ![Tagging redline](../extensibility/media/0303-176_taggingredline.png "0303-176_TaggingRedline")  
  
 Use …  
 for UI that supports tagging.  
  
 Do not use …  
 for any other type of UI.  
  
### Tag  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Tag](../extensibility/media/0303-177_tag.png "0303-177_Tag")  
  
 **Default**  
  
 Background  
  
 `Tag.Background`  
  
 Foreground (Text)  
  
 `Tag.Background`  
  
 ![Tag on hover](../extensibility/media/0303-178_taghover.png "0303-178_TagHover")  
  
 **Hover**  
  
 Background  
  
 `Tag.HoverBackground`  
  
 Foreground (Text)  
  
 `Tag.HoverBackgroundText`  
  
 ![Tag pressed](../extensibility/media/0303-179_tagpressed.png "0303-179_TagPressed")  
  
 **Pressed**  
  
 Background  
  
 `Tag.PressedBackground`  
  
 Foreground (Text)  
  
 `Tag.PressedBackgroundText`  
  
 ![Tag selected](../extensibility/media/0303-180_tagselected.png "0303-180_TagSelected")  
  
 **Selected**  
  
 Background  
  
 `Tag.SelectedBackground`  
  
 Foreground (Text)  
  
 `Tag.SelectedBackgroundText`  
  
### Glyph (close icon)  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Tag &#40;glyph&#41;](../extensibility/media/0303-181_tagglyph.png "0303-181_TagGlyph")  
  
 **Default (tag default)**  
  
 Background  
  
 N/A  
  
 Foreground (Glyph)  
  
 `Tag.TagHoverGlyph`  
  
 **Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Tag &#40;glyph&#41; on hover](../extensibility/media/0303-182_tagglyphhover.png "0303-182_TagGlyphHover")  
  
 **Hover (tag default)**  
  
 Background  
  
 `Tag.TagHoverGlyphHoverBackground`  
  
 Foreground (Glyph)  
  
 `Tag.TagHoverGlyphHover`  
  
 Border  
  
 `Tag.TagHoverGlyphHoverBorder`  
  
 **Pressed**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Tag &#40;glyph&#41; pressed](../extensibility/media/0303-183_tagglyphpressed.png "0303-183_TagGlyphPressed")  
  
 **Pressed (tag default)**  
  
 Background  
  
 `Tag.TagHoverGlyphPressedBackground`  
  
 Foreground (Glyph)  
  
 `Tag.TagHoverGlyphPressed`  
  
 Border  
  
 `Tag.TagHoverGlyphPressedBorder`  
  
 **Tag selected/glyph default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Tag selected](../extensibility/media/0303-184_tagselected.png "0303-184_TagSelected")  
  
 **Default (tag selected)**  
  
 Background  
  
 N/A  
  
 Foreground (Glyph)  
  
 `Tag.TagSelectedGlyph`  
  
 **Tag selected/glyph hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Tag selected on hover](../extensibility/media/0303-185_tagselectedhover.png "0303-185_TagSelectedHover")  
  
 **Hover (tag selected)**  
  
 Background  
  
 `Tag.TagSelectedGlyphHoverBackground`  
  
 Foreground (Glyph)  
  
 `Tag.TagSelectedGlyphHover`  
  
 Border  
  
 `Tag.TagSelectedGlyphHoverBorder`  
  
 **Tag selected/glyph pressed**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Tag selected pressed](../extensibility/media/0303-186_tagselectedpressed.png "0303-186_TagSelectedPressed")  
  
 **Pressed (tag selected)**  
  
 Background  
  
 `Tag.TagSelectedGlyphPressedBackground`  
  
 Foreground(Glyph)  
  
 `Tag.TagSelectedGlyphPressed`  
  
 Border  
  
 `Tag.TagSelectedGlyphPressedBorder`  
  
## Shell  
  
### Background  
 The environment background consists of two layers. The bottom layer is a solid color that covers the entire IDE. The top layer fits under the command shelf and between the tool window auto-hide channels on the left and right edges of the IDE. As of Visual Studio 2013, the top and bottom background layers are set to the same color in the Light and Dark themes.  
  
 ![Shell background redline](../extensibility/media/0303-187_shellbackgroundredline.png "0303-187_ShellBackgroundRedline")  
  
 Use …  
 for places that you want to match the background of the Visual Studio environment.  
  
 Do not use …  
 -   as a fill for places that are not background surfaces.  
  
-   as a background on which you wish to place foreground elements.  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 Bottom layer  
  
 Background  
  
 `Environment.EnvironmentBackground`  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 Top layer  
  
 Background  
  
 *Gradient stops set to the same color value in Visual Studio 2013 Light and Dark themes.*  
  
 `Environment.EnvironmentBackgroundGradientBegin`  
  
 `Environment.EnvironmentBackgroundGradientEnd`  
  
 `Environment.EnvironmentBackgroundGradientMiddle1`  
  
 `Environment.EnvironmentBackgroundGradientMiddle2`  
  
### Command shelf  
 Two sets of token names are used for the command shelf backgrounds: one set for where the menu bar sits and one for where the command bars sit. An individual command bar group has its own background color values, which are discussed in more detail in the "command bar" section. Menu bar and command bar text is discussed in the menu and command bar sections, respectively.  
  
 ![Command shelf redline](../extensibility/media/0303-188_commandshelfredline.png "0303-188_CommandShelfRedline")  
  
 Use …  
 -   for areas where you place menus or toolbars.  
  
-   with the correct background/?foreground token name combination.  
  
 Do not use …  
 for areas that are not similar to a command shelf.  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 Menu bar  
  
 Background  
  
 *Gradient stops set to the same color value in Visual Studio 2013 Light and Dark themes.*  
  
 `Environment.CommandShelfHighlightGradientBegin`  
  
 `Environment.CommandShelfHighlightGradientMiddle`  
  
 `Environment.CommandShelfHighlightGradientEnd`  
  
 Command bar  
  
 Background  
  
 *Gradient stops set to the same color value in Visual Studio 2013 Light and Dark themes.*  
  
 `Environment.CommandShelfBackgroundGradientBegin`  
  
 `Environment.CommandShelfBackgroundGradientMiddle`  
  
 `Environment.CommandShelfBackgroundGradientEnd`  
  
## Toolbox  
 The toolbox is one of the common tool windows that is most frequently used in Visual Studio. It is essentially a tree control with a special theme and styling applied.  
  
 ![Toolbox redline](../extensibility/media/0303-189_toolboxredline.png "0303-189_ToolboxRedline")  
  
 Use …  
 when you are designing a tool window that you want to always be consistent with the shell toolbox.  
  
 Do not use …  
 for anything that is not similar to the toolbox UI, or if you are unsure whether your UI will have problems if the shell toolbox colors change.  
  
 **Default**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Toolbox parent node](../extensibility/media/0303-190_toolboxparentnode.png "0303-190_ToolboxParentNode")  
  
 **Parent node**  
  
 ![Toolbox child node](../extensibility/media/0303-191_toolboxchildnode.png "0303-191_ToolboxChildNode")  
  
 **Child node**  
  
 Background  
  
 `Environment.ToolboxContent`  
  
 Headings  
  
 `Environment.ToolWindowBackground`  
  
 Individual items, or entire window if no available controls  
  
 Border  
  
 None  
  
 Foreground (Glyph)  
  
 `Environment.ToolboxContent`  
  
 Foreground (Text)  
  
 `Environment.ToolboxContent`  
  
 **Hover**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Toolbox child node on hover](../extensibility/media/0303-192_toolboxchildnodehover.png "0303-192_ToolboxChildNodeHover")  
  
 **Toolbox hover on child node**  
  
 Background  
  
 `Environment.ToolboxContentMouseOver`  
  
 Individual items only  
  
 Border  
  
 None  
  
 Foreground (Text)  
  
 `Environment.ToolboxContentMouseOver`  
  
 Individual items only  
  
 **Selected**  
  
 Component  
  
 Element  
  
 Token name: Category.color  
  
 ![Toolbox parent node focused](../extensibility/media/0303-193_toolboxparentnodefocused.png "0303-193_ToolboxParentNodeFocused")  
  
 **Focused parent node**  
  
 ![Toolbox child node focused](../extensibility/media/0303-194_toolboxchildnodefocused.png "0303-194_ToolboxChildNodeFocused")  
  
 **Focused child node**  
  
 Background  
  
 `TreeView.SelectedItemActive`  
  
 From [Tree view](../extensibility/shared-colors-for-visual-studio.md#BKMK_TreeView) category  
  
 Border  
  
 `TreeView.FocusVisualBorder`  
  
 From [Tree view](../extensibility/shared-colors-for-visual-studio.md#BKMK_TreeView) category  
  
 Foreground (Glyph)  
  
 `TreeView.SelectedItemActive`  
  
 From [Tree view](../extensibility/shared-colors-for-visual-studio.md#BKMK_TreeView) category  
  
 Foreground (Text)  
  
 `TreeView.SelectedItemActive`  
  
 From [Tree view](../extensibility/shared-colors-for-visual-studio.md#BKMK_TreeView) category  
  
 ![Toolbox parent node unfocused](../extensibility/media/0303-195_toolboxparentnodeunfocused.png "0303-195_ToolboxParentNodeUnfocused")  
  
 **Unfocused parent node**  
  
 ![Toolbox child node unfocused](../extensibility/media/0303-196_toolboxchildnodeunfocused.png "0303-196_ToolboxChildNodeUnfocused")  
  
 **Unfocused child node**  
  
 Background  
  
 `TreeView.SelectedItemInactive`  
  
 From [Tree view](../extensibility/shared-colors-for-visual-studio.md#BKMK_TreeView) category  
  
 Border  
  
 None  
  
 Foreground (Glyph)  
  
 `TreeView.SelectedItemInactive`  
  
 From [Tree view](../extensibility/shared-colors-for-visual-studio.md#BKMK_TreeView) category  
  
 Foreground (Text)  
  
 `TreeView.SelectedItemInactive`  
  
 From [Tree view](../extensibility/shared-colors-for-visual-studio.md#BKMK_TreeView) category