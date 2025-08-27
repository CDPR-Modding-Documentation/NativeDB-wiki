# inkWidget

## Description

See [wiki](https://github.com/psiberx/cp2077-codeware/wiki#user-interface) of Codeware to learn more about creating a UI. You should install [RedHotTools](https://github.com/psiberx/cp2077-red-hot-tools/) too. It provides a powerful `InkInspector` tool to help you design a UI while in-game.

## Functions

#### BindProperty(propertyName: CName, stylePath: CName) -> Bool

Bind a style to a property of a widget, based on the current theme of the game. You must define a style resource using \[this.SetStyle], otherwise this function will have no effect.

Example to use the red color of the game on a widget: `BindProperty(n"tintColor", n"MainColors.Red")`.

#### RegisterToCallback(eventName: CName, object: handle:IScriptable, functionName: CName) -> Void

You need to setup your widget to listen for events and trigger callbacks. You can do so using \[this.SetInteractive] on the widget.

You can listen to the following common events (see also the [full list](https://github.com/psiberx/cp2077-cet-kit/blob/f64c837e589ffffc030e79ed0123688eb3091098/EventProxy.lua#L28)):

* `n"OnEnter"`: when cursor enters the widget (hover in)
* `n"OnLeave"`: when cursor leaves the widget (hover out)
* `n"OnPress"`: when mouse left button is pressed inside the widget
* `n"OnRelease"`: when mouse left button is released inside the widget

You must declare your callback method with `cb` qualifier, and with one argument of type ref<\[inkPointerEvent]>.

#### SetStyle(styleResPath: redResourceReferenceScriptToken) -> Void

You must define an `.inkstyle` file to use \[this.BindProperty]. When you add a widget with a script, this call is required on each widget you create.

A common `styleResPath` used to define colors is: `r"base\\gameplay\\gui\\common\\main_colors.inkstyle"`. You can see a Json representation of this file on [Discord](https://discord.com/channels/717692382849663036/1036574451237662780/1287833757449060444).

You can find other styles using WolvenKit.
