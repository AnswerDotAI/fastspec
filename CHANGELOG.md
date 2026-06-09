# Release notes

<!-- do not remove -->



## 0.0.8

### New Features

- Return request response and stream events as `AttrDict` ([#5](https://github.com/AnswerDotAI/fastspec/pull/5)), thanks to [@KeremTurgutlu](https://github.com/KeremTurgutlu)


## 0.0.7

- revert dict2obj resp which was causing issues in fastllm


## 0.0.6

### New Features

- op/path tags in `group_func`, dedupe route/body/query params ([#4](https://github.com/AnswerDotAI/fastspec/issues/4))

- Handle httpx.RequestError as retryable APIError ([#3](https://github.com/AnswerDotAI/fastspec/pull/3)), thanks to [@ncoop57](https://github.com/ncoop57)

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


