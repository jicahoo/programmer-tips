# programmer-tips
* 很明显，解决这些问题需要基础知识，但更重要的是处理过相关问题，才能习得这些能力。大家都知道，基础知识就是计算机专业课：数据结构与算法，操作系统，网络TCP/IP，数据库系统，分布式系统。对我而言，前三个的知识都不太充足，要继续深入研究，差缺补漏，现在的目标就是学习Linux内核，以Linux内核学习，作为自己的一个核心竞争力。在此基础上，学C, 学透JVM, Java, 但这只能是Java语言本身；对于语言如何使用，还是要写，读，调过足够多的Java代码。 如何驯服各种Java构造的产品，还需要有实际经验。数据结构算法也需加强。

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
    * 心中要有网络结构
     * 192 vs 10 vs 172 ?
        * http://www.ietf.org/rfc/rfc1918.txt
        * https://superuser.com/questions/146194/why-are-home-networks-prefixed-with-192-168
     
    * 网络畅通：ping <IP>
    * 端口开放：telnet IP Port.  Check it on server: netstat -tuanp |grep XXX to make sure BInd Address is open enough.
    * 其他？traceroute?
