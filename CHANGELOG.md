# Release notes

<!-- do not remove -->

## 0.0.5

### New Features

- User defined group name parsing ([#2](https://github.com/AnswerDotAI/fastspec/issues/2))



## 0.0.4

### New Features

- Preserve OpenAPI request content type and encode bodies accordingly ([#1](https://github.com/AnswerDotAI/fastspec/issues/1))
  - ## Problem

`fastspec` currently sends request bodies as JSON for generated OpenAPI calls. This works for JSON-first APIs, but not for Stripe v1 write endpoints, which expect `application/x-www-form-urlencoded`.

Stripe v1 also expects nested structures to be flattened:

- `metadata={"kind": "subscription"}` -> `metadata[kind]=subscription`
- `items=[{"price": "price_..."}]` -> `items[0][price]=price_...`


