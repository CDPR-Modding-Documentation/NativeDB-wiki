---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# inkWidget

## Description

See [wiki](https://github.com/psiberx/cp2077-codeware/wiki#user-interface) of Codeware to learn more about creating a UI. You should install [RedHotTools](https://github.com/psiberx/cp2077-red-hot-tools/) too. It provides a powerful `InkInspector` tool to help you design a UI while in-game.

## Functions

#### BindProperty(propertyName: CName, stylePath: CName) -> Bool

Bind a style to a property of a widget, based on the current theme of the game. You must define a style resource using \[this.SetStyle], otherwise this function will have no effect.

Example to use the red color of the game on a widget: `BindProperty(n"tintColor", n"MainColors.Red")`.

#### SetStyle(styleResPath: redResourceReferenceScriptToken) -> Void

You must define an `.inkstyle` file to use \[this.BindProperty]. When you add a widget with a script, this call is required on each widget you create.

A common `styleResPath` used to define colors is: `r"base\\gameplay\\gui\\common\\main_colors.inkstyle"`. You can see a Json representation of this file on [Discord](https://discord.com/channels/717692382849663036/1036574451237662780/1287833757449060444).

You can find other styles using WolvenKit.
