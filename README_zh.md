## 三方开源软件 reqwest

### 1. Reqwest 简介

Reqwest 是一个 Rust 编写的第三方库，提供了一个符合人体工学的、强大的 Rust HTTP 客户端，并提供了如下功能：

- 多种 body 可选：纯文本、JSON 格式、URL 格式、Multipart 格式
- 可自定义的重定向策略
- HTTP 代理配置
- 可自选的底层 TLS 库
- Cookie
- WASM

Reqwest 基于 Rust 异步语义实现，具有高性能、高吞吐量等特点。

### 2. 引入背景简述

OpenHarmony 需要引入 Rust 的 HTTP 客户端能力。

### 3. 使用场景

任何 Rust 语言编写的组件且需要使用 HTTP 客户端的场景均可使用。

### 4. 为 OpenHarmony 带来的价值

借助于 Reqwest 的 HTTP 客户端功能，提高 OpenHarmony 各组件在进行 HTTP 请求交互时的吞吐量，降低时延。

### 5. 如何使用

在您的 BUILD.gn 需要的地方添加依赖即可。

```json
 deps += [ "//third_party/rust/crate/reqwest" ]
```