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

# inkTextWidget

## Functions

#### SetFontFamily(fontFamilyPath: String, opt fontStyle: CName) -> Void

Known relative paths for `fontFamilyPath`, in root path `base\gameplay\gui\fonts\`:

* foreign\chinese\_traditional\ar\_fang\_xing\_run\_yuan\ar\_fang\_xing\_run\_yuan.inkfontfamily
* foreign\arabic\ara\_es\_nawar\ara\_es\_nawar.inkfontfamily
* arame\arame.inkfontfamily
* arial\arial.inkfontfamily
* blender\blender.inkfontfamily
* digital\_readout\digitalreadout.inkfontfamily
* industry\industry.inkfontfamily
* foreign\chinese\_traditional\jing\_xi\_heig\_b5\jing\_xi\_heig\_b5.inkfontfamily
* foreign\chinese\jing\_xi\_heig\jing\_xi\_heig.inkfontfamily
* foreign\korean\kbiz\_go\kbiz\_go.inkfontfamily
* foreign\japanese\mgenplus\mgenplus.inkfontfamily
* foreign\korean\nanum\_square\nanum\_square.inkfontfamily
* orbitron\orbitron.inkfontfamily
* foreign\thai\printable4u\printable4u.inkfontfamily
* foreign\russian\raj\_rus.inkfontfamily
* raj\raj.inkfontfamily
* foreign\japanese\smart\_font\_ui\smart\_font\_ui.inkfontfamily
* foreign\thai\th\_sarabun\_new\th\_sarabun\_new.inkfontfamily

#### SetFontStyle(fontStyle: CName) -> Void

This call is not enough to redraw the widget with the new font style. You can trigger a redraw by calling another function too, for example using \[this.SetText] or \[this.SetFontSize] with the same current value.

`fontStyle` values are unique per font family, you can find them in `.inkfontfamily` files using WolvenKit. List of known values: `Regular`, `Light`, `Medium`, `Heavy`, `Semi-Bold`, `Bold`, `Extra Bold`, `Italic`, `Bold Italic`, `Black`, `Demi`, `Book`, `Book Italic`.
