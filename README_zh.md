# 三方开源软件 reqwest

## Reqwest 简介

Reqwest 是一个 Rust 编写的第三方库，提供了一个符合人体工学的、强大的 Rust HTTP 客户端，并提供了如下功能：

- 多种 body 可选：纯文本、JSON 格式、URL 格式、Multipart 格式
- 可自定义的重定向策略
- HTTP 代理配置
- 可自选的底层 TLS 库
- Cookie
- WASM

Reqwest 基于 Rust 异步语义实现，具有高性能、高吞吐量等特点。

## 引入背景简述

OpenHarmony 需要引入 Rust 的 HTTP 客户端能力。借助于 Reqwest 的 HTTP 客户端功能，可以提高 OpenHarmony 各组件在进行 HTTP 请求交互时的吞吐量，并降低时延。

任何 Rust 语言编写的组件且需要使用 HTTP 客户端的场景均可使用 Reqwest 来发送 HTTP 请求。

## 如何使用

在您的 BUILD.gn 需要的地方添加依赖即可。

```json
 deps += [ "//third_party/rust/crate/reqwest" ]
```

如果您需要使用 Cargo 的方式进行依赖，可以在自己的 Rust 工程的 Cargo.toml 下添加如下字段：

如果您的本地环境上存在 reqwest 库，您可以使用路径依赖：
```
[dependencies]
reqwest = { path = "(reqwest 的具体路径)" }
```

您也可以依赖 Reqwest 的具体版本。如果您使用该方式，该三方库会在您的 Rust 工程编译时自动从 crates.io 下载。
```
[dependencies]
reqwest = { version = "0.11.13" } 
```