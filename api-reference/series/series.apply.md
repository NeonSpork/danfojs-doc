---
description: invoke a function on Series Value
---

# Series.apply

> danfo.series.**apply**\(callable\) \[[source](https://github.com/opensource9ja/danfojs/blob/master/danfojs/src/core/series.js#L718)\]

| Parameters | Type | Description | Default |
| :--- | :--- | :--- | :--- |
| callable | Function | Function \(can be anonymous\) to apply |  |

**Returns:**

       ****return **Series**

\*\*\*\*

**Example**

{% tabs %}
{% tab title="Node" %}
```javascript
const dfd = require("danfojs-node")

let sf = new dfd.Series([1, 2, 3, 4, 5, 6, 7, 8])

let apply_func = (x) => {
    return x + x
}
sf.apply(apply_func).print()
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
║ 0 │ 2                    ║
╟───┼──────────────────────╢
║ 1 │ 4                    ║
╟───┼──────────────────────╢
║ 2 │ 6                    ║
╟───┼──────────────────────╢
║ 3 │ 8                    ║
╟───┼──────────────────────╢
║ 4 │ 10                   ║
╟───┼──────────────────────╢
║ 5 │ 12                   ║
╟───┼──────────────────────╢
║ 6 │ 14                   ║
╟───┼──────────────────────╢
║ 7 │ 16                   ║
╚═══╧══════════════════════╝
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Node" %}
```javascript
const dfd = require("danfojs-node")

let sf = new dfd.Series([1, 2, 3, 4, 5, 6, 7, 8])

sf.apply(Math.log).print()
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
║ 0 │ 0                    ║
╟───┼──────────────────────╢
║ 1 │ 0.6931471805599453   ║
╟───┼──────────────────────╢
║ 2 │ 1.0986122886681096   ║
╟───┼──────────────────────╢
║ 3 │ 1.3862943611198906   ║
╟───┼──────────────────────╢
║ 4 │ 1.6094379124341003   ║
╟───┼──────────────────────╢
║ 5 │ 1.791759469228055    ║
╟───┼──────────────────────╢
║ 6 │ 1.9459101490553132   ║
╟───┼──────────────────────╢
║ 7 │ 2.0794415416798357   ║
╚═══╧══════════════════════╝
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Node" %}
```javascript
const dfd = require("danfojs-node")

let sf = new dfd.Series(["Rice","Beans","Yam","Banana","Wheat"])

sf.apply((x)=>{
    return x.toLocaleLowerCase()
}).print()
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
║ 0 │ rice                 ║
╟───┼──────────────────────╢
║ 1 │ beans                ║
╟───┼──────────────────────╢
║ 2 │ yam                  ║
╟───┼──────────────────────╢
║ 3 │ banana               ║
╟───┼──────────────────────╢
║ 4 │ wheat                ║
╚═══╧══════════════════════╝
```
{% endtab %}
{% endtabs %}



