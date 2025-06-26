# OpenDDOS - 开源网络压力测试工具集

[中文说明](/README.zh-CN.md)

**一个基于Bash的交互式菜单工具，用于快速执行网络侦察和压力测试**


## 项目简介

OpenDDOS 是一个功能强大的网络测试工具集，提供直观的交互式菜单界面，集成了多种网络侦察和压力测试功能。工具采用模块化设计，支持TCP/UDP/ICMP等多种协议测试。

## 功能特性

### 侦察模块
- **网络接口检测**：显示本地和公网IP信息
- **DNS侦查**：执行DNS查询和WHOIS查找
- **主机发现**：ICMP Ping扫描网络段
- **端口扫描**：快速扫描和全面扫描选项
- **服务识别**：检测服务版本和操作系统
- **VPN检测**：识别IPsec VPN服务器

### 压力测试模块
- **ICMP洪水**：传统ICMP Echo洪水攻击
- **TCP洪水**：SYN/ACK/RST/XMAS多种标志位攻击
- **UDP洪水**：高带宽UDP数据包洪水
- **SSL/TLS攻击**：握手过程资源耗尽攻击
- **Slowloris**：低速HTTP头攻击
- **DNS缓存攻击**：NXDOMAIN查询洪水

### 数据传输
- **文件传输**：通过TCP/UDP发送文件
- **网络监听**：建立接收文件的监听服务

## 系统要求

- **操作系统**：Linux (Debian/Arch测试通过)
- **依赖工具**：
  - bash
  - sudo
  - curl
  - netcat (支持-k选项)
  - hping3/nping
  - openssl
  - stunnel
  - nmap
  - whois
  - nslookup/host
  - ike-scan
  - bind-tools

## 安装使用

### 快速安装
```bash
git clone https://github.com/HaoTang9878/OpenDDOS.git
cd OpenDDOS
chmod +x OpenDDOS
sudo ./OpenDDOS
```

### 或下载发布版
从[Releases页面](https://github.com/HaoTang9878/OpenDDOS/releases)下载最新版本

## 模块详解

### 侦察功能
- **网络接口检测**：使用curl查询公网IP，ip/ifconfig显示本地IP
- **DNS侦查**：执行正向/反向DNS查询和WHOIS查找
- **快速扫描**：使用nmap扫描1000个常见TCP端口
- **全面扫描**：扫描所有TCP端口并识别服务/OS
- **UDP扫描**：扫描所有UDP端口
- **服务检测**：通过TCP时间戳估算服务器运行时间
- **VPN检测**：使用ike-scan检测IPsec VPN服务器

### 压力测试
- **ICMP洪水**：可配置源IP和数据包大小
- **TCP SYN洪水**：可配置源IP、端口和数据内容
- **SSL攻击**：通过大量SSL握手消耗资源
- **Slowloris**：低速HTTP头攻击，支持SSL加密
- **DNS洪水**：发送大量NXDOMAIN查询

## 免责声明

⚠ **重要法律声明** ⚠

1. 本工具仅限**合法授权**的安全测试使用
2. 使用者需确保已获得目标系统的**书面授权**
3. 开发者不对任何滥用行为负责
4. 禁止用于非法网络活动

使用本工具即表示您同意承担全部责任。

## 许可证

GNU General Public License v3.0

## 贡献指南

欢迎提交Pull Request和Issue报告问题或建议新功能。

## 联系方式

- 作者：Hao Tang
- GitHub：[@HaoTang9878](https://github.com/HaoTang9878)
- 项目主页：https://github.com/HaoTang9878/OpenDDOS

---

*"With great power comes great responsibility."* - 请负责任地使用本工具。
