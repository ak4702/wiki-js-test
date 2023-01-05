---
title: home
description: 
published: true
date: 2023-01-05T09:34:00.378Z
tags: 
editor: markdown
dateCreated: 2023-01-05T09:26:18.414Z
---

# SimpleSchema (simpl-schema NPM package)

[![Lint, Test, and (Maybe) Publish](<https://github.com/longshotlabs/simpl-schema/workflows/Lint,%20Test,%20and%20(Maybe)%20Publish/badge.svg?event=push>)](https://github.com/longshotlabs/simpl-schema/actions?query=workflow%3A%22Lint%2C+Test%2C+and+%28Maybe%29+Publish%22)

SimpleSchema validates JavaScript objects to ensure they match a schema. It can also clean the objects to automatically convert types, remove unsupported properties, and add automatic values such that the object is then more likely to pass validation.

There are a lot of similar packages for validating objects. These are some of the features of this package that might be good reasons to choose this one over another:

- Written in TypeScript and published with support for both CommonJS and ESM.
- Isomorphic. Works in NodeJS and modern browsers.
- Package has been maintained for 10 years and is mature
- Has nearly 500 tests and is used in production apps of various sizes
- The object you validate can be a MongoDB [update document](https://www.mongodb.com/docs/drivers/node/current/fundamentals/crud/write-operations/change-a-document/) (also known as "modifier" object). SimpleSchema understands how to properly validate it such that the object in the database, after undergoing modification, will be valid.
- Object cleaning feature can fix potential validation errors automatically, avoiding unnecessary errors for your users. Cleaning also supports MongoDB update documents.
- Powerful customizable error message system with decent English language defaults and support for localization, which makes it easy to drop this package in and display the validation error messages to end users.
- Used by [Mailchimp Open Commerce](https://mailchimp.com/developer/open-commerce/)
- Used by the [Collection2](https://github.com/Meteor-Community-Packages/meteor-collection2) and [AutoForm](https://github.com/Meteor-Community-Packages/meteor-autoform) Meteor packages.

There are also reasons not to choose this package. Because of all it does, this package is more complex than (but still "simple" :) ) and slower than some other packages. Based on your needs, you should decide whether these tradeoffs are acceptable. Other packages you might consider:

- [simplecheck](https://www.npmjs.com/package/simplecheck)
- [joi](https://joi.dev/)
- [yup](https://www.npmjs.com/package/yup)