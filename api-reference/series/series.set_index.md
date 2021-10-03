---
description: Assign new Index to Series
---

# Series.set\_index

> danfo.series.**set\_index\(**kwargs**\)** \[[source](https://github.com/opensource9ja/danfojs/blob/master/danfojs/src/core/series.js#L635)\]

| Parameters | Type | Description | Default |
| :--- | :--- | :--- | :--- |
| kwargs\["index"\] | Array | index to replace the former index  |  |
| kwargs\["inplace"\] | Boolean | return new series or not | false |

**Returns:** Series

**Example**

{% tabs %}
{% tab title="Node" %}
```javascript
const dfd = require("danfojs-node")

let data = [{ alpha: "A", count: 1 }, { alpha: "B", count: 2 }, { alpha: "C", count: 3 }]
let sf = new dfd.Series(data)
let sf_new = sf.set_index({ "index": ["one", "two", "three"] })
sf_new.print()
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
╔═══════╤══════════════════════╗
║       │ 0                    ║
╟───────┼──────────────────────╢
║ one   │ {"alpha":"A","cou... ║
╟───────┼──────────────────────╢
║ two   │ {"alpha":"B","cou... ║
╟───────┼──────────────────────╢
║ three │ {"alpha":"C","cou... ║
╚═══════╧══════════════════════╝
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Node" %}
```javascript
const dfd = require("danfojs-node")

let data = ["Humans","Life","Meaning","Fact","Truth"]
let sf = new dfd.Series(data)
let sf_new = sf.set_index({ "index": ["H", "L", "M","F","T"] })
sf_new.print()
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
║ H │ Humans               ║
╟───┼──────────────────────╢
║ L │ Life                 ║
╟───┼──────────────────────╢
║ M │ Meaning              ║
╟───┼──────────────────────╢
║ F │ Fact                 ║
╟───┼──────────────────────╢
║ T │ Truth                ║
╚═══╧══════════════════════╝
```
{% endtab %}
{% endtabs %}

set index without creating a new series by using `inplace = true`

{% tabs %}
{% tab title="Node" %}
```javascript
const dfd = require("danfojs")

let data = [1,2,3,4,5,6]
let sf = new dfd.Series(data)
sf.set_index({ "index": ["one", "two", "three", "four", "five", "six"], "inplace": true })
sf.print()
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
╔═══════╤══════════════════════╗
║       │ 0                    ║
╟───────┼──────────────────────╢
║ one   │ 1                    ║
╟───────┼──────────────────────╢
║ two   │ 2                    ║
╟───────┼──────────────────────╢
║ three │ 3                    ║
╟───────┼──────────────────────╢
║ four  │ 4                    ║
╟───────┼──────────────────────╢
║ five  │ 5                    ║
╟───────┼──────────────────────╢
║ six   │ 6                    ║
╚═══════╧══════════════════════╝
```
{% endtab %}
{% endtabs %}

