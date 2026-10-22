# 微云盘

基于 Qt 与 C++ 实现的客户端/服务器云盘项目，提供文件管理、好友互动、私聊和文件分享等功能。

## 功能概览

- 用户注册、登录与在线用户查看
- 好友管理和私聊
- 文件上传、下载、删除与目录管理
- 文件分享
- SQLite 数据持久化

## 技术栈

- C++ / Qt Widgets
- TCP Socket 通信
- SQLite
- qmake

## 目录结构

```text
.
├── TcpClient/    # Qt 客户端、业务页面和网络协议
├── TcpServer/    # TCP 服务、连接管理和数据库访问
└── sqlite/       # SQLite 相关文件
```

## 快速开始

1. 安装 Qt 和对应的 C++ 编译工具链。
2. 使用 Qt Creator 打开 `TcpServer/TcpServer.pro` 并构建服务器。
3. 检查 `TcpServer/server.config`，前两行分别为监听地址和端口。
4. 启动服务器。
5. 使用 Qt Creator 打开 `TcpClient/TcpClient.pro` 并构建客户端。
6. 让 `TcpClient/client.config` 的服务器地址、端口与服务端配置保持一致，然后启动客户端。

默认示例配置使用 `127.0.0.1:8888`。跨主机运行时，请将客户端配置改为服务器可访问的 IP 地址。
