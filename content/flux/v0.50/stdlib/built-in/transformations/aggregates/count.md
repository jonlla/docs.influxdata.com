---
title: count() function
description: The count() function outputs the number of non-null records in each aggregated
  column.
aliases:
  - /flux/v0.50/functions/transformations/aggregates/count
  - /flux/v0.50/functions/built-in/transformations/aggregates/count/
menu:
  flux_0_50:
    name: count
    parent: Aggregates
    weight: 1
---

The `count()` function outputs the number of records in each aggregated column.
It counts both null and non-null records.

_**Function type:** Aggregate_  
_**Output data type:** Integer_

```js
count(column: "_value")
```

## Parameters

### column
Column on which to operate.
Defaults to `"_value"`.

_**Data type:** String_

## Examples
```js
from(bucket: "telegraf/autogen")
  |> range(start: -5m)
  |> count()
```

```js
from(bucket: "telegraf/autogen")
  |> range(start: -5m)
  |> count(column: "_value")
```

<hr style="margin-top:4rem"/>

##### Related InfluxQL functions and statements:
[COUNT()](/influxdb/latest/query_language/functions/#count)
