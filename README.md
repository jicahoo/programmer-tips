# programmer-tips
* 很明显，解决这些问题需要基础知识，但更重要的是处理过相关问题，才能习得这些能力。大家都知道，基础知识就是计算机专业课：数据结构与算法，操作系统，网络TCP/IP，数据库系统，分布式系统。对我而言，前三个的知识都不太充足，要继续深入研究，差缺补漏，现在的目标就是学习Linux内核，以Linux内核学习，作为自己的一个核心竞争力。在此基础上，学C, 学透JVM, Java, 但这只能是Java语言本身；对于语言如何使用，还是要写，读，调过足够多的Java代码。 如何驯服各种Java构造的产品，还需要有实际经验。数据结构算法也需加强。
* 可能最简单的方法就是根据要学的知识，买对应领域经典的书籍，通读，反复阅读，实践课后习题。这样知识体系就不会学得乱七八糟，不扎实，不全面。有些时候，你可能工作中遇到一些知识点，google一下可能更快，如果，查阅自己读过的书籍，可能印象更深刻，因为你以前看过这本书的内容，脑海中已有印象。所以，我的方法可能就是通过管理我的技术书籍，管理我的知识体系；这是第一步，然后，可能通过博客，记录我的经验体会，整理我的知识体系。我有个books github repo.
* 一招鲜。某种技术做到极致很重要。我们是分工社会，一招鲜才能立足，才能体现价值。一种语言？一种软件？一种设计能力？做PPT? 画图？shell工具？ wireshark? Linux 进程内存分析? 算法? 流行的数据库、基础软件产品？如果没有机会重度使用比较流行的开源软件，把某种语言搞到极致，是我的出路，立我的标签。或者面向问题学习，网络问题经常在软件开发中出现，网络问题解决小能手。TCP/IP/HTTP-Web，JVM/Java大神，Scala大神，C语言大神，Linux大神，其他够用即可。最终要落实到各种工具解决问题，tcpdump, wireshark, telnet, ping,traceroute, ip cmd, firewall, netstat,rpc perf analysis,netty, nginx; jstack, jmap, heap dump, thread dump, GC, jstat, NMT, Class loading, JIT, JVM code, JDK core: collection, conrruency, IO/NIO; My Scala tools; glibc: malloc, pthread; /proc, pmap, top, io, free, signal, shell, cpu time, interrupts.既然说的分工，就要沟通，我要努力耐心地锻炼快速地理解别人的意思，然后清楚地有逻辑地表达我的意思，并推动进程，达到沟通的目标：需要别人做什么，解决问题，下一步如何做，而不仅仅是探讨个技术问题，没有action item.

* 当然了，有些东西也不能花太多的精力深入，因为软件事件纷繁复杂，不可能什么都专。挑方向专。更重要的还是要能产生价值，产生战斗力。我们重要的是如何利用已有的好轮子造一部好车子。重点在于**用好轮子**. 有个整体的正确的把握, 或者把握其中的道，而不是仅仅是术。
* 有一个心得，网上各种技术博客讲得不准确，不清晰，甚至还有错误。如果你能快速看懂相关的源代码，你就更快地获取最准确的系统行为。而不是被各种博客误导。任何一个复杂的软件系统，在每个程序员的心中都有不同的理解，就像一千个人心中就会有一千个哈姆雷特。但是源代码不会说谎，描述也不会有歧义，程序员通过代码取得一致的观点。其他的画图，自然语言，也很重要，但肯定没有代码准确。不同的沟通方式有不同的优缺点。

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
