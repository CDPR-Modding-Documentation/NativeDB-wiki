---
description: >-
  This guide explains what syntax you can use to format the documentation for
  NativeDB.
---

# Format and syntax

🟢 fully supported

🟠 partially supported

🔴 not supported

<table data-full-width="true"><thead><tr><th width="165" align="right">Blocks</th><th width="57" align="center"></th><th width="201">Markdown</th><th>Description</th></tr></thead><tbody><tr><td align="right">Paragraph</td><td align="center">🟢​​</td><td>Some text</td><td>Basic block to show text.</td></tr><tr><td align="right">Code</td><td align="center">🟢​​</td><td><code>`content`</code></td><td>Useful to highlight arguments of a function.<br>Note: it doesn't support complex code block with a language (like <code>```lua ```</code>).</td></tr><tr><td align="right">URL</td><td align="center">🟢</td><td>[label](https://)</td><td>You can add URL link with a label. URL must starts with <code>https://</code>.</td></tr><tr><td align="right">Lists</td><td align="center">🟠​</td><td><ul><li>- Item A</li><li>- Item B</li></ul><ol><li>1. Item 1</li><li>2. Item 2</li></ol><ul class="contains-task-list"><li><input type="checkbox">[ ] Item T</li><li><input type="checkbox" checked>[x] Item D</li></ul></td><td>You can add ordered lists, unordered lists and tasks lists. In all cases, they will be visible as unordered lists using <code>-</code> as a prefix. Markdown example will look like this:<br>- Item A<br>- Item B<br><br>- Item 1<br>- Item 2<br><br>- Item T<br>- Item D</td></tr><tr><td align="right">Bold / Italic</td><td align="center">🔴​</td><td><p>**<strong>bold**</strong></p><p>*<em>italic</em>*</p></td><td></td></tr><tr><td align="right">Headers</td><td align="center">🔴</td><td># H1<br>## H2<br>### H3</td><td></td></tr><tr><td align="right">Hint</td><td align="center">🔴</td><td>{% hint %}<br>{% endhint %}</td><td></td></tr><tr><td align="right"></td><td align="center"></td><td></td><td></td></tr><tr><td align="right">Class reference</td><td align="center">🟢</td><td>[ClassName]</td><td>Write the native name / alias name of a class between brackets (<code>[]</code>). NativeDB will automatically format it as a link to navigate to the class.</td></tr><tr><td align="right">Property reference</td><td align="center">🟢</td><td>[this.prop]<br>[ClassName.prop]</td><td><p>When documenting a class, you can reference its own properties using <code>this.</code> followed by the name of the property.</p><p>You can also reference properties of other classes using <code>ClassName.</code> instead of <code>this.</code>.</p><p>It must be surrounded by brackets (<code>[]</code>) in both cases.</p></td></tr><tr><td align="right">Function reference</td><td align="center">🟢</td><td>[this.GetStuff]<br>[ClassName.SetStuff]</td><td>When documenting a class, you can reference its own functions using <code>this.</code> followed by the name of the function.<br>You can also reference functions of other classes using <code>ClassName.</code> instead of <code>this.</code>.<br>It must be surrounded by brackets (<code>[]</code>) in both cases.</td></tr><tr><td align="right">Enum / Bitfield<br>reference</td><td align="center">🟢</td><td>[Enum.Value]<br>[Bitfield.Value]</td><td>You can reference value of an enum and value of a bitfield.</td></tr></tbody></table>

{% hint style="info" %}
Don't hesitate to look at other classes to see how the syntax is used, and how it looks like in NativeDB. If you are not sure, you can always come and ask on Discord.
{% endhint %}
