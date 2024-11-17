+++
title = 'Qt主题oneDark设置'
date = 2024-10-09T23:14:12+08:00

categories = ["Qt"] 
tags = ["主题设置"]

+++

参考链接:  CSDN  [Qt Creator打造VScode one dark pro主题配色](https://blog.csdn.net/qq_41980754/article/details/119861293)

代码部分

```
<?xml version="1.0" encoding="UTF-8"?>
<style-scheme version="1.0" name="One Dark">
  <style name="Text" foreground="#abb2bf" background="#282c34"/>
  <style name="Link" underlineStyle="SingleUnderline"/>
  <style name="Selection" background="#3e4451"/>
  <style name="LineNumber" foreground="#4b5363"/>
  <style name="SearchResult" background="#324365"/>
  <style name="SearchScope" background="#3e4451"/>
  <style name="Parentheses" underlineColor="#61afef" underlineStyle="SingleUnderline"/>
  <style name="ParenthesesMismatch" foreground="#000000" background="#c678dd"/>
  <style name="AutoComplete" background="#3e4451"/>
  <style name="CurrentLine" background="#3a3f4b"/>
  <style name="CurrentLineNumber" foreground="#777c87"/>
  <style name="Occurrences" background="#324365"/>
  <style name="Occurrences.Unused" underlineColor="#d19a66" underlineStyle="DashUnderline"/>
  <style name="Occurrences.Rename" background="#e06c75"/>
  <style name="Number" foreground="#d19a66"/>
  <style name="String" foreground="#98c379"/>
  <style name="Type" foreground="#61afef"/>
  <style name="Local"/>
  <style name="Global"/>
  <style name="Field" foreground="#e06c75"/>
  <style name="Static" foreground="#61afef" italic="true"/>
  <style name="VirtualMethod" foreground="#61afef" italic="true"/>
  <style name="Function" foreground="#61afef"/>
  <style name="Keyword" foreground="#c678dd"/>
  <style name="PrimitiveType" foreground="#c678dd"/>
  <style name="Operator" foreground="#c678dd"/>
  <style name="Overloaded Operator" foreground="#c678dd"/>
  <style name="Punctuation"/>
  <style name="Preprocessor" foreground="#c678dd"/>
  <style name="Label" foreground="#e06c75" bold="true"/>
  <style name="Comment" foreground="#5c6370" italic="true"/>
  <style name="Doxygen.Comment" foreground="#5c6370" italic="true"/>
  <style name="Doxygen.Tag" foreground="#61afef"/>
  <style name="VisualWhitespace" foreground="#3c4049"/>
  <style name="QmlLocalId" foreground="#61afef"/>
  <style name="QmlExternalId"/>
  <style name="QmlTypeId" foreground="#61afef"/>
  <style name="QmlRootObjectProperty" foreground="#61afef"/>
  <style name="QmlScopeObjectProperty" foreground="#61afef"/>
  <style name="QmlExternalObjectProperty"/>
  <style name="JsScopeVar"/>
  <style name="JsImportVar" foreground="#d19a66"/>
  <style name="JsGlobalVar" foreground="#d19a66"/>
  <style name="QmlStateName" foreground="#61afef"/>
  <style name="Binding" foreground="#c678dd"/>
  <style name="DisabledCode" foreground="#5c6370"/>
  <style name="AddedLine" foreground="#98c379"/>
  <style name="RemovedLine" foreground="#e06c75"/>
  <style name="DiffFile" foreground="#61afef"/>
  <style name="DiffLocation" foreground="#d19a66"/>
  <style name="DiffFileLine" foreground="#000000" background="#e5c07b"/>
  <style name="DiffContextLine" foreground="#000000" background="#56b6c2"/>
  <style name="DiffSourceLine" foreground="#000000" background="#be5046"/>
  <style name="DiffSourceChar" foreground="#000000" background="#e06c75"/>
  <style name="DiffDestLine" foreground="#000000" background="#789353"/>
  <style name="DiffDestChar" foreground="#000000" background="#98c379"/>
  <style name="LogChangeLine" foreground="#e06c75"/>
  <style name="LogAuthorName" foreground="#61afef"/>
  <style name="LogCommitDate" foreground="#98c379"/>
  <style name="LogCommitHash" foreground="#e06c75"/>
  <style name="LogCommitSubject"/>
  <style name="LogDecoration" foreground="#c678dd"/>
  <style name="Warning" underlineColor="#d19a66" underlineStyle="SingleUnderline"/>
  <style name="WarningContext" underlineColor="#d19a66" underlineStyle="DotLine"/>
  <style name="Error" underlineColor="#e06c75" underlineStyle="SingleUnderline"/>
  <style name="ErrorContext" underlineColor="#e06c75" underlineStyle="DotLine"/>
  <style name="Declaration"/>
  <style name="FunctionDefinition"/>
  <style name="OutputArgument" italic="true"/>
  <style name="LastStyleSentinel"/>
</style-scheme>
```
主题设置
```
[General]
ThemeName=One Dark
PreferredStyles=Fusion
DefaultTextEditorColorScheme=onedark.xml

[Palette]
shadowBackground=ff21252b
text=ffabb2bf
textDisabled=99abb2bf
textHighlighted=ffd7dae0
toolBarItem=ffabb2bf
toolBarItemDisabled=99abb2bf
fancyBarsNormalTextColor=ffabb2bf
fancyBarsBoldTextColor=ffabb2bf
hoverBackground=ff31363f
selectedBackground=ff3a3f4b
selectedBackgroundText=ffd7dae0
normalBackground=ff282c34
alternateBackground=ff31363f
error=ffe06c75
warning=ffe5c07b
success=ff98c379
message=ff61afef
splitter=ff181a1f
textColorLink=61afef
textColorLinkVisited=c678dd
backgroundColorDisabled=ff21252b

[Colors]

;DS controls theme START
DScontrolBackground=normalBackground
DScontrolOutline=splitter
DStextColor=text
DSdisabledTextColor=textDisabled
DSpanelBackground=ff454444
DShoverHighlight=hoverBackground
DScolumnBackground=ff363636
DSfocusEdit=normalBackground
DSfocusDrag=ff565656
DScontrolBackgroundPressed=selectedBackground
DScontrolBackgroundChecked=selectedBackground
DSinteraction=selectedBackground
DSsliderActiveTrack=ff7a7a7a
DSsliderInactiveTrack=ff4d4d4d
DSsliderHandle=ff4b5362
DSsliderActiveTrackHover=ff7f7f7f
DSsliderInactiveTrackHover=ff505050
DSsliderHandleHover=ff7a7a7a
DSsliderActiveTrackFocus=ffaaaaaa
DSsliderInactiveTrackFocus=ff7a7a7a
DSsliderHandleFocus=ff1d545c
DSerrorColor=error
DScontrolBackgroundDisabled=backgroundColorDisabled
DScontrolOutlineDisabled=ff4d4d4d
DStextColorDisabled=textDisabled
DStextSelectionColor=selectedBackground
DStextSelectedTextColor=selectedBackgroundText
DSscrollBarTrack=ff4d4d4d
DSscrollBarHandle=ff4b5362
DScontrolBackgroundInteraction=ff4d4d4d
DStranslationIndicatorBorder=splitter
DSsectionHeadBackground=alternateBackground
DSchangedStateText=message
DS3DAxisXColor=error
DS3DAxisYColor=success
DS3DAxisZColor=message
;DS controls theme END

BackgroundColorAlternate=alternateBackground
BackgroundColorDark=shadowBackground
BackgroundColorHover=hoverBackground
BackgroundColorNormal=normalBackground
BackgroundColorDisabled=backgroundColorDisabled
BackgroundColorSelected=selectedBackground
BadgeLabelBackgroundColorChecked=text
BadgeLabelBackgroundColorUnchecked=text
BadgeLabelTextColorChecked=normalBackground
BadgeLabelTextColorUnchecked=normalBackground
CanceledSearchTextColor=error
ComboBoxArrowColor=toolBarItem
ComboBoxArrowColorDisabled=toolBarItemDisabled
ComboBoxTextColor=fancyBarsNormalTextColor
DetailsButtonBackgroundColorHover=hoverBackground
DetailsWidgetBackgroundColor=shadowBackground
DockWidgetResizeHandleColor=splitter
DoubleTabWidget1stSeparatorColor=splitter
DoubleTabWidget1stTabActiveTextColor=text
DoubleTabWidget1stTabBackgroundColor=normalBackground
DoubleTabWidget1stTabInactiveTextColor=text
DoubleTabWidget2ndSeparatorColor=toolBarItemDisabled
DoubleTabWidget2ndTabActiveTextColor=text
DoubleTabWidget2ndTabBackgroundColor=selectedBackground
DoubleTabWidget2ndTabInactiveTextColor=text
EditorPlaceholderColor=shadowBackground
FancyToolBarSeparatorColor=toolBarItemDisabled
FancyTabBarBackgroundColor=shadowBackground
FancyTabBarSelectedBackgroundColor=selectedBackground
FancyTabWidgetDisabledSelectedTextColor=toolBarItemDisabled
FancyTabWidgetDisabledUnselectedTextColor=toolBarItemDisabled
FancyTabWidgetEnabledSelectedTextColor=fancyBarsBoldTextColor
FancyTabWidgetEnabledUnselectedTextColor=fancyBarsBoldTextColor
FancyToolButtonHoverColor=hoverBackground
FancyToolButtonSelectedColor=selectedBackground
FutureProgressBackgroundColor=shadowBackground
IconsBaseColor=toolBarItem
IconsDisabledColor=toolBarItemDisabled
IconsInfoColor=message
IconsInfoToolBarColor=message
IconsWarningColor=warning
IconsWarningToolBarColor=warning
IconsErrorColor=error
IconsErrorToolBarColor=error
IconsRunColor=success
IconsRunToolBarColor=success
IconsStopColor=error
IconsStopToolBarColor=error
IconsInterruptColor=message
IconsInterruptToolBarColor=message
IconsDebugColor=toolBarItem
IconsNavigationArrowsColor=warning
IconsBuildHammerHandleColor=b06112
IconsBuildHammerHeadColor=toolBarItem
IconsModeWelcomeActiveColor=success
IconsModeEditActiveColor=message
IconsModeDesignActiveColor=warning
IconsModeDebugActiveColor=message
IconsModeProjectActiveColor=success
IconsModeAnalyzeActiveColor=message
IconsModeHelpActiveColor=warning
IconsCodeModelKeywordColor=ff777777
IconsCodeModelClassColor=ffc0b550
IconsCodeModelStructColor=ff53b053
IconsCodeModelFunctionColor=ffd34373
IconsCodeModelVariableColor=ff2bbbcc
IconsCodeModelEnumColor=ffc0b550
IconsCodeModelMacroColor=ff476ba0
IconsCodeModelAttributeColor=ff316511
IconsCodeModelUniformColor=ff994899
IconsCodeModelVaryingColor=ffa08833
IconsCodeModelOverlayBackgroundColor=normalBackground
IconsCodeModelOverlayForegroundColor=text
InfoBarBackground=shadowBackground
InfoBarText=text
MenuBarEmptyAreaBackgroundColor=shadowBackground
MenuBarItemBackgroundColor=shadowBackground
MenuBarItemTextColorDisabled=textDisabled
MenuBarItemTextColorNormal=text
MenuItemTextColorDisabled=textDisabled
MenuItemTextColorNormal=text
MiniProjectTargetSelectorBackgroundColor=shadowBackground
MiniProjectTargetSelectorBorderColor=shadowBackground
MiniProjectTargetSelectorSummaryBackgroundColor=normalBackground
MiniProjectTargetSelectorTextColor=fancyBarsNormalTextColor
PanelStatusBarBackgroundColor=shadowBackground
PanelsWidgetSeparatorLineColor=splitter
PanelTextColorDark=text
PanelTextColorMid=text
PanelTextColorLight=textHighlighted
ProgressBarColorError=error
ProgressBarColorFinished=success
ProgressBarColorNormal=message
ProgressBarTitleColor=text
ProgressBarBackgroundColor=alternateBackground
SplitterColor=splitter
TextColorDisabled=textDisabled
TextColorError=error
TextColorHighlight=textHighlighted
TextColorHighlightBackground=hoverBackground
TextColorLink=textColorLink
TextColorLinkVisited=textColorLinkVisited
TextColorNormal=text
ToggleButtonBackgroundColor=shadowBackground
ToolBarBackgroundColor=shadowBackground
TreeViewArrowColorNormal=hoverBackground
TreeViewArrowColorSelected=text

OutputPanes_DebugTextColor=text
OutputPanes_ErrorMessageTextColor=error
OutputPanes_MessageOutput=message
OutputPanes_NormalMessageTextColor=text
OutputPanes_StdErrTextColor=error
OutputPanes_StdOutTextColor=text
OutputPanes_WarningMessageTextColor=warning
OutputPanes_TestPassTextColor=success
OutputPanes_TestFailTextColor=error
OutputPanes_TestXFailTextColor=error
OutputPanes_TestXPassTextColor=message
OutputPanes_TestSkipTextColor=message
OutputPanes_TestWarnTextColor=warning
OutputPanes_TestFatalTextColor=error
OutputPanes_TestDebugTextColor=text
OutputPaneButtonFlashColor=error
OutputPaneToggleButtonTextColorChecked=fancyBarsNormalTextColor
OutputPaneToggleButtonTextColorUnchecked=fancyBarsNormalTextColor

Debugger_LogWindow_LogInput=ff56b6c2
Debugger_LogWindow_LogStatus=message
Debugger_LogWindow_LogTime=error

Debugger_WatchItem_ValueNormal=text
Debugger_WatchItem_ValueInvalid=textDisabled
Debugger_WatchItem_ValueChanged=error

Debugger_Breakpoint_TextMarkColor=message

Welcome_TextColor=text
Welcome_ForegroundPrimaryColor=text
Welcome_ForegroundSecondaryColor=text
Welcome_BackgroundColor=normalBackground
Welcome_ButtonBackgroundColor=normalBackground
Welcome_DividerColor=splitter
Welcome_HoverColor=hoverBackground
Welcome_LinkColor=textColorLink
Welcome_DisabledLinkColor=textDisabled

Timeline_TextColor=text
Timeline_BackgroundColor1=normalBackground
Timeline_BackgroundColor2=shadowBackground
Timeline_DividerColor=splitter
Timeline_HighlightColor=selectedBackground
Timeline_PanelBackgroundColor=alternateBackground
Timeline_PanelHeaderColor=normalBackground
Timeline_HandleColor=ff4b5362
Timeline_RangeColor=selectedBackground

VcsBase_FileStatusUnknown_TextColor=text
VcsBase_FileAdded_TextColor=success
VcsBase_FileModified_TextColor=warning
VcsBase_FileDeleted_TextColor=error
VcsBase_FileRenamed_TextColor=message
VcsBase_FileUnmerged_TextColor=error

Bookmarks_TextMarkColor=message

TextEditor_SearchResult_ScrollBarColor=success
TextEditor_CurrentLine_ScrollBarColor=message

ProjectExplorer_TaskError_TextMarkColor=error
ProjectExplorer_TaskWarn_TextMarkColor=warning

CodeModel_Error_TextMarkColor=error
CodeModel_Warning_TextMarkColor=warning

QmlDesigner_BackgroundColor=normalBackground
QmlDesigner_HighlightColor=selectedBackground
QmlDesigner_FormEditorSelectionColor=message
QmlDesigner_FormEditorForegroundColor=normalBackground
QmlDesigner_BackgroundColorDarkAlternate=shadowBackground
QmlDesigner_BackgroundColorDarker=splitter
QmlDesigner_BorderColor=splitter
QmlDesigner_ButtonColor=normalBackground
QmlDesigner_TabDark=shadowBackground
QmlDesigner_TabLight=text
QmlDesigner_FormeditorBackgroundColor=normalBackground
QmlDesigner_AlternateBackgroundColor=alternateBackground
QmlDesigner_ScrollBarHandleColor=ff4b5362

PaletteWindow=shadowBackground
PaletteWindowText=text
PaletteBase=normalBackground
PaletteAlternateBase=alternateBackground
PaletteButton=shadowBackground
PaletteBrightText=error
PaletteText=text
PaletteButtonText=text
PaletteButtonTextDisabled=textDisabled
PaletteToolTipBase=hoverBackground
PaletteHighlight=selectedBackground
PaletteDark=shadowBackground
PaletteHighlightedText=selectedBackgroundText
PaletteToolTipText=text
PaletteLink=textColorLink
PaletteLinkVisited=textColorLinkVisited
PaletteWindowDisabled=backgroundColorDisabled
PaletteWindowTextDisabled=textDisabled
PaletteBaseDisabled=backgroundColorDisabled
PaletteTextDisabled=textDisabled

[Flags]
ComboBoxDrawTextShadow=false
DerivePaletteFromTheme=true
DrawIndicatorBranch=true
DrawSearchResultWidgetFrame=false
DrawTargetSelectorBottom=false
DrawToolBarHighlights=false
DrawToolBarBorders=false
ApplyThemePaletteGlobally=true
FlatToolBars=true
FlatSideBarIcons=true
FlatProjectsMode=true
FlatMenuBar=true
ToolBarIconShadow=true
WindowColorAsBase=true
DarkUserInterface=true

[Gradients]
DetailsWidgetHeaderGradient\1\color=normalBackground
DetailsWidgetHeaderGradient\1\pos=1
DetailsWidgetHeaderGradient\size=1

```

