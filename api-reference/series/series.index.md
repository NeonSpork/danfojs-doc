---
description: Obtain the index of a Series
---

# Series.index

> danfo.Series.index&#x20;

**Returns**: Array

**Example**

{% tabs %}
{% tab title="Node" %}
```javascript
const dfd = require("danfojs-node")

let data1 = [30.21091, 40.190901, 3.564, 5.0212]
let sf1 = new dfd.Series(data1)

console.log(sf1.index)
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Output" %}
```
[ 0, 1, 2, 3 ]
```
{% endtab %}
{% endtabs %}
