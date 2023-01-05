---
title: Validate a MongoDB Update Document
description: 
published: true
date: 2023-01-05T09:54:54.127Z
tags: validation
editor: markdown
dateCreated: 2023-01-05T09:39:01.715Z
---

### Validate a MongoDB Update Document

```js
import SimpleSchema from "simpl-schema";

const validationContext = new SimpleSchema({
  name: String,
}).newContext();

validationContext.validate(
  {
    $set: {
      name: 2,
    },
  },
  { modifier: true }
);

console.log(validationContext.isValid());
console.log(validationContext.validationErrors());
```