---
title: Validate an Array of Objects and Throw an Error
description: 
published: true
date: 2023-01-05T09:55:15.883Z
tags: validation
editor: markdown
dateCreated: 2023-01-05T09:38:03.008Z
---

### Validate an Array of Objects and Throw an Error

An error is thrown for the first invalid object found.

```js
import SimpleSchema from "simpl-schema";

new SimpleSchema({
  name: String,
}).validate([{ name: "Bill" }, { name: 2 }]);
```