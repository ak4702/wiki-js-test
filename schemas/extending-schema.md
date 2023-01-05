---
title: Extending Schemas
description: 
published: true
date: 2023-01-05T09:59:22.470Z
tags: schema
editor: markdown
dateCreated: 2023-01-05T09:44:40.915Z
---

## Extending Schemas

If there are certain fields that are repeated in many of your schemas, it can be useful to define a SimpleSchema instance just for those fields and then merge them into other schemas:

```js
import SimpleSchema from "simpl-schema";
import { idSchema, addressSchema } from "./sharedSchemas";

const schema = new SimpleSchema({
  name: String,
});
schema.extend(idSchema);
schema.extend(addressSchema);
```