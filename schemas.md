---
title: Schemas
description: 
published: true
date: 2023-01-05T09:53:37.888Z
tags: schema, quick-start
editor: markdown
dateCreated: 2023-01-05T09:43:18.382Z
---

## Defining a Schema

Let's get into some more details about the different syntaxes that are supported when defining a schema. It's probably best to start with the simplest syntax. Here's an example:

### Shorthand Definitions

```js
import SimpleSchema from "simpl-schema";

const schema = new SimpleSchema({
  name: String,
  age: SimpleSchema.Integer,
  registered: Boolean,
});
```

This is referred to as "shorthand" syntax. You simply map a property name to a type. When validating, SimpleSchema will make sure that all of those properties are present and are set to a value of that type.

### Longhand Definitions

In many cases, you will need to use longhand in order to define additional rules beyond what the data type should be.

```js
import SimpleSchema from "simpl-schema";

const schema = new SimpleSchema({
  name: {
    type: String,
    max: 40,
  },
  age: {
    type: SimpleSchema.Integer,
    optional: true,
  },
  registered: {
    type: Boolean,
    defaultValue: false,
  },
});
```
