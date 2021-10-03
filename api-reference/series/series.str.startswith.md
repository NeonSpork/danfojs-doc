---
description: Test whether a string begins with specified characters
---

# Series.str.startsWith

> danfo.Series.str.**startsWith**\(str\)     \[[source](https://github.com/opensource9ja/danfojs/blob/master/danfojs/src/core/strings.js#L119)\]

| Parameters | Type | Description | Default |
| :--- | :--- | :--- | :--- |
| str | string | the character\(s\) to check | "" |

**Returns:**  Series \(Boolean element\)

**Examples**

{% tabs %}
{% tab title="Node" %}
```javascript
const dfd = require("danfojs-node")

let data = ['lower', 'CAPITALS', 'this is a sentence', 'SwApCaSe']
let sf = new dfd.Series(data)
sf.str.startsWith("S").print()
```
{% endtab %}

{% tab title="Browser" %}
```

```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Output" %}
```text
╔═══╤══════════════════════╗
║   │ 0                    ║
╟───┼──────────────────────╢
║ 0 │ false                ║
╟───┼──────────────────────╢
║ 1 │ false                ║
╟───┼──────────────────────╢
║ 2 │ false                ║
╟───┼──────────────────────╢
║ 3 │ true                 ║
╚═══╧══════════════════════╝
```
{% endtab %}
{% endtabs %}

