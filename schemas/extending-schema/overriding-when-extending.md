---
title: Overriding When Extending
description: 
published: true
date: 2023-01-05T09:59:47.994Z
tags: schema
editor: markdown
dateCreated: 2023-01-05T09:46:42.927Z
---

## Overriding When Extending

If the key appears in both schemas, the definition will be extended such that the result is the combination of both definitions.

```js
import SimpleSchema from "simpl-schema";
import { idSchema, addressSchema } from "./sharedSchemas";

const schema = new SimpleSchema({
  name: {
    type: String,
    min: 5,
  },
});
schema.extend({
  name: {
    type: String,
    max: 15,
  },
});
```

The above will result in the definition of the `name` field becoming:

```js
{
  name: {
    type: String,
    min: 5,
    max: 15,
  },
}
```

Note also that a plain object was passed to `extend`. If you pass a plain object, it is converted to a `SimpleSchema` instance for you.
