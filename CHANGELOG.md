# Release notes

<!-- do not remove -->

## 0.1.3

### New Features

- Move API surface helpers (snake, `sanitized_params`, `mk_sig`, `mk_doc`, OpGroup, group building, `full_docs`) to fastcore.apisurface ([#21](https://github.com/AnswerDotAI/fastspec/issues/21))
- Include raw field in APIError string representation ([#19](https://github.com/AnswerDotAI/fastspec/pull/19)), thanks to [@kafkasl](https://github.com/kafkasl)

### Bugs Squashed

- Fix `_schema_py_type` for OpenAPI 3.1 nullable type lists ([#18](https://github.com/AnswerDotAI/fastspec/pull/18)), thanks to [@kafkasl](https://github.com/kafkasl)


## 0.1.2

### New Features

- Add `__dir__` to OpGroup and OpenAPIClient to control attribute discovery ([#17](https://github.com/AnswerDotAI/fastspec/issues/17))


## 0.1.1

### Bugs Squashed

- fix: walk anyOf/oneOf in `_schema_props_required` ([#14](https://github.com/AnswerDotAI/fastspec/pull/14)), thanks to [@jackhogan](https://github.com/jackhogan)


## 0.1.0

### New Features

- Add sync client support (SyncTransport/SyncOpFunc) ([#15](https://github.com/AnswerDotAI/fastspec/issues/15))
- Add `__allow__` protocol to OpGroup and OpenAPIClient for simpler `allow()` usage ([#16](https://github.com/AnswerDotAI/fastspec/issues/16))

### Bugs Squashed

- fix: walk anyOf/oneOf in `_schema_props_required` ([#14](https://github.com/AnswerDotAI/fastspec/pull/14)), thanks to [@jackhogan](https://github.com/jackhogan)


## 0.0.11

### Bugs Squashed

- Adding suffixes to duplicated sanitized param names ([#7](https://github.com/AnswerDotAI/fastspec/pull/7)), thanks to [@kafkasl](https://github.com/kafkasl)


## 0.0.9


### Bugs Squashed

- guard against empty response body in _decode ([#6](https://github.com/AnswerDotAI/fastspec/pull/6)), thanks to [@ncoop57](https://github.com/ncoop57)

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
- `metadata={"kind": "subscription"}` -> `metadata[kind]=subscription`
- `items=[{"price": "price_..."}]` -> `items[0][price]=price_...`
