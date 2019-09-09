# 网络协议
## 基础概念

请求过程**

```mermaid
graph LR
A[浏览器输入域名] --> B[NDS服务器查询域名对应的IP地址并返回给浏览器]
B --> C[浏览器拿到IP地址后与WEB服务器建立TCP连接]
C --> D[浏览器向WEB服务器发起HTTP请求]
D --> F[WEB服务器向浏览器返回HTML]
```

**IP**

IPv4地址格式：`211.161.170.115` ，这是一个32位的2进制

IP分为动态IP、静态IP，绝大部分用户使用的是动态IP，一段时间后会被运营商收回，重新分配。

**url协议**

url格式：`http://www.example.com:80/path/to/file.html?key1=value1&key2=value2#link`

`http://` 协议

`www.example.com` 域名

`:80` 端口

`/path/to/file.html` 路径

`?key1=value1&key2=value2` 参数

`#link` 锚点

**url的绝对路径与相对路径**

如 `http://www.example.com/path` 的路径资源中有一段跳转的代码  `href='/commond/user'` 。

`/commond/user` 最终的url是 `http://www.example.com/commond/user`

`commond/user` 最终的url是 `http://www.example.com/path/commond/user`

## 七层网络协议模型

标准的七层网络协议

```mermaid
graph LR
A[应用层] --> B[表示层]
B --> C[会话层]
C --> D[传输层]
D --> F[网络层]
F --> G[数据链路层]
G --> H[物理层]
```

常用的五层网络协议

```mermaid
graph LR
A[应用层] --> B[传输层]
B --> C[网络层]
C --> D[数据链路层]
D --> F[物理层]
```

**应用层协议**

Http、ftp、pop3、DNS

**传输层**

TCP、UDP

**网络层**

ICMP、IP、IGMP

**数据链路层**

ARP、RARP

**物理层**

物理传输介质

### 五层常用网络协议层中数据流动

**应用层协议**

Http、ftp、pop3、DNS

**传输层**

TCP、UDP

**网络层**

ICMP、IP、IGMP

**数据链路层**

ARP、RARP

**物理层**

物理传输介质