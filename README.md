# programmer-tips


## 问题与工具
* 程序员常见问题与相关工具
* 黑盒方式，实验推理方式，用各种工具探测系统行为，做出推理。
* 白盒方式： 看活的系统在各个层次的数据状态，或则看静态的代码，做出分析。
* 性能问题分析
  * 内存： VSS,RSS
  * CPU?
  * 网络: TCP/IP
  * IPC: Unix Socket,
  * Algorithm
  * Serialization/Deserialization.
* 并发问题分析
* Hack的方式解决问题
* 进出各个系统组件的数据: HTTPS (wireshark), HTTP, SOAP, REST, gpb, others.
* 分析Log: timeline, tools: grep, less, keywords: exception, can't, fail,caught,
* 分析dump: core dump, heap dump
* 字符问题：特殊字符，字符集
* 各个操作系统（Windows, Linux)掌握各种搜索工具，文件搜索，程序搜索。

## 常见问题
* 连不上 (Protocl, IP, Port). SSH, DB Server, Web Server and so on.
    * 网络畅通：ping <IP>
    * 端口开放：telnet IP Port.  Check it on server: netstat -tuanp |grep XXX to make sure BInd Address is open enough.
    * 其他？traceroute?
