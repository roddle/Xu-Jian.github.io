---
layout: post
title: Socks & Http
tags: 
categories: IT-Admin
---

## Proxy : Socks & Http  …

- 代理解释 :
	1. 找别人去做 本该自己亲自去做的某件事.
		2. 客户端 通过代理服务器 与 服务器 进行非直接的连接.
		3. 一堵外网和客户端(电脑) 之间的墙. 提供流量和安全管理.
		4. 比如A要访问C网站，但A到C网络出现问题.可以通过绕道，  
			假设B是代理服务器，A可通过B， 再由B到C。

- 网络代理(一种服务) :     保护隐私或者安全 防止攻击.

	客户端 ⟺ 代理服务器 ⟺ 服务器    进行非直接的连接.

网关 路由器有代理功能. 保证安全 防止攻击.

## 翻墙 :
\*绕过 IP 封锁, 端口封锁 , 内容过滤 , 域名劫持 等等.....

中国封锁力度最大. 草榴 / BBC / Facebook / Twitter ….

中国有技术 切断所有的代理服务器 和 VPN 连接. 
但是: 大量的国外银行 和 企业在跨国通讯时 都必须用 VPN 来传输数据.

## 代理功能:

1. 提高访问速度：
	通常代理服务器都设置一个较大的缓冲区，当有外界的信息通过时，同时也将其保存到缓冲区中，当其他用户再访问相同的信息时， 则直接由缓冲区中取出信息，传给用户，以提高访问速度。

	2. 控制对内部资源的访问：
		如某大学FTP（前提是该代理地址在该资源的允许访问范围之内），使用教育网内地址段免费代理服务器，就可以用于对教育网开放的各类FTP下载上传，以及各类资料查询共享等服务。

	3. 过滤内容：
		例如限制对特定计算机的访问，将一种语言的数据翻译成另一种语言，或是防御代理服务器两边的攻击性访问。

	4. 隐藏真实IP：
		上网者也可以通过代理服务器隐藏自己的IP，免受攻击。但是只一个代理很难保证安全，更安全的方法是利用特定的工具创建代理链（如：Tor）。

	5. 访问国外站点。
		中国教育网和169网等网络用户可以通过代理访问国外网站。

	6. 突破内容过滤机制限制，访问被过滤网站。
		如防火长城对中国境内互联网访问的限制可通过使用代理服务器浏览而突破。但是每到国庆、两会等敏感时期，防火长城的封锁力度会大大加强，大多数代理服务器和代理软件都会无法连接。（如：Tor、自由门、无界浏览等


## 代理链:

用好几台代理. + After invasion 清除代理服务器日志. 缓存. 


代理中转功能时: 所有数据基本全部明文. 间谍代理 能记录所有的数据(包括用户名+密码). 
所以 使用代理服务器 尽量用 SSL / TLS 先加密.


代理服务器: 网络代理.   网络安全用.

分布式代理:
利用私立的域名解析系统, 如 TOR.

## 代理分类
 - HTTP 代理  *应用层* *明文传输!!! URL 可以被检测到* 80/8080/3128/8081/9080
	WWW 连接请求 . 浏览网页 . 下载数据（也可采用ftp协议)

HTTP 代理可以中断连接.( 也就是 *可以截留+修改数据.* )
HTTP 代理是以 HTTP 请求为基础的. 这些请求 大多以明文存在!


- Socks 代理 *会话层 / 传输层 * 1080
	只是简单的传递数据包. 不用关心是什么协议( FTP HTTP )  所以比 HTTP 代理速度快很多

	传输虽然是加密的.但是原则上可以还原真实数据的.所以不是很可靠.

	电子邮件 等软件.

	Socks 4 → 只支持 TCP
	Socks 5 → TCP / UDP
	> QQ 使用 UDP 所以不能用 Socks 4 . 


- Ftp 代理 :     21 / 2121 端口. 访问 FTP 服务器.

- SSL / TLS 代理 :    访问加密网站. 443端口.

- Telnet 代理 23
	telnet 远程控制. Hack someone. hide yourself.

- Pop3 / SMTP 代理 :    邮件收发.

- 高度匿名代理:
	*转发原封数据包* . 就像普通用户在访问.

- 普通匿名代理:
	*修改数据包*  服务端有可能发现这是个代理服务器. *有可能查到你的真实 IP*

- 透明代理:
	*修改数据包 + 主动透露你的真实 IP * 
	作用: 除了用缓存技术 提高浏览速度.+ 内容过滤 提高一定的安全性 . 无别的作用.
	内网中的硬件防火墙 就是这个用的.

- 间谍代理:
	组织/个人 创建的 用于 *记录用户传输数据,进行研究 监控* 等目的.



## 代理选择 :  

浏览器: 支持 Socks 代理.
浏览器上网 需要与目标主机建立 TCP 连接.

- 浏览器,下载软件 → HTTP or Socks 
- 上传软件             → FTP or Socks 
- 聊天/游戏            → Socks 


网络协议  客户端与外网服务器之间的通讯.

HTTP 代理: 浏览器




## Proxy  代理服务器:

用代理服务器上网  有黑客攻击 就会攻击到代理服务器 不会攻击你的实际电脑.
 
设置用户验证和记账功能，可按用户进行记账，没有登记的用户无权通过代理服务器访问

Internet网。并对用户的访问时间、访问地点、信息流量进行统计。

充当防火墙（Firewall）：
连接内网与Internet，
因为所有内部网的用户通过代理服务器访问外界时，只映射为一个IP地址，
所以外界不能直接访问到内部网；同时可以设置IP地址过滤，限制内部网对外部的访问权限。


## VPN代理

指在共用网络上建立专用网络的技术。



共享网络

代理服务器
代理服务器
最常见的可能是用代理服务器共享上网，很多人不知不觉中就在用，比如通过sygate，wingate，isa，ccproxy，NT系统自带的网络共享等，可以提供企业级的文件缓存、复制和地址过滤等服务，充分利用局域网出口的有限带宽，加快内网用户的 访问速度，可以解决仅仅有一条线路一个IP，IP资源不足，带局域网很多用户上网的功能，同时可以做为一个防火墙，隔离内网与外网，并且能提供监控网络和记录传输信息的功能，加强了局域网的安全性，又便于对上网用户进行管理。[1]() 
访问代理



防止攻击

隐藏自己的真实地址信息，还可隐藏自己的IP，防止被黑客攻击。通过分析指定IP地址，可以查询到网络用户的所在地。例如，大家在一些论坛上看到，论坛中明确标出了发帖用户所在地，这就是根据论坛会员登录时的IP地址解析的。还有平日里我们最为常 用的显IP版QQ，在“发送消息”窗口中，可以查看对方的IP及解析出的地理位置。而当我们使用相应协议的代理服务器后，就可以达到隐藏自己当前所在地地址的目的了。[1]() 
突破限制

代理服务器还可以突破网络限制。比如局域网对上网用户的端口、目的网站、协议、游戏、即时通讯软件等的限制，都可以突破这些限制，可参见我这篇帖子，如何突破局域网对上网用户的一些限制 不再重复。举个例子：GOOGLE我们都喜欢用，其实GOOGLE有一个功能就有点类似于代理服务器的功能，就是网页快照，网站经常发生变动，地址或者网站关了，网站服务器发生故障了，或者已经更新了，但我们仍然要查以前非常有用的资料，网页快照就排 上用场了，Google以其复杂而全自动的搜索方法排除了任何人为因素对搜索结果的影响，保证了网页排名的客观公正，Google可以方便、诚实、客观地帮您在网上找到有价值的资料。GOOGLE有一个海量的数据库，如果找不到服务器，Google储存的网页快照也可救急。虽然网页快照中的信息可能不是最新的，但在网页快照中查找资料要比在实际网页中快得多，这时可以通过加密代理访问Google，再访问其网页快照来救急。[1]() 
掩藏身份

代理服务器知识是黑客基本功，黑客的很多活动都是通过代理服务器，比如扫描、刺探，对局域网内机器进行渗透，黑客一般攻击的时候都是中转了很多级跳板，才攻击目标机器。隐藏了身份，保证了自己的安全。[1]() 


提高速度

提高下载速度，突破下载限制。比如有的网站提供的下载资源，做了一IP一线程的限制，这时候可以用影音传送带，设置多线程，为每个线程设置一个代理。对于限制一个IP的情况很好突破，只要用不同的代理服务器，就可同时下载多个资源，适用于从WEB和FTP 上下载的情况。不过如果是论坛里面的资源，每个用户一个账号，并且限制一账号一IP，代理服务器就突破不了。还有一种情况，比如我们这里，电信的用户上不了联通的电影网站，联通的用户上不了的电信电影网站，这种情况只要电信的找一个联通地代理，IP地址属联通就行。联通找一个电信代理。就可以去电影网站下载其电影。教育网还可以通过代理服 务器可使无出国权限或无访问某IP段权限的计算机访问相关资源。[1]() 
充当防火墙

[1]()  因为所有使用代理服务器的用户都必须通过代理服务器访问远程站点，因此在代理服务器上就可以设置相应的限制，以过滤或屏蔽某些信息。
用户管理

[1]()  通过代理服务器，管理员可以设置用户验证和记账功能，对用户进行登记，并对用户的访问时间、访问地点、信息浏览进行统计。没有登记的用户无权通过代理服务器访问Internet





什么是代理服务器及其作用？代理服务器是网上提供转接功能的服务器，比如你想访问的目的网站是A，由于某种原因你不能访问到网站A或者你不想直接访问网站A（这样通过代理服务器网站A，对网站A而已可以隐藏你自己的身份 ，也就是不知道是谁访问的网站，而认为是代理服务器访问的），此时你就可以使用代理服务器，在实际访问网站的时候，你在浏览器的地址栏内和你以前一样输入你要访问的网站，浏览器会自动先访问代理服务器，然后代理服务器会自动给你转接到你的目标网站。简单而言，代理服务器可以隐藏你的身份。[1]() 
为什么有的代理服务器不能使用？代理服务器是有很强的时效性的，原因是由于大家可以理解的原因，代理服务器有时候运行一段时间，就被迫关闭了，这时候你需要再找新的代理服务器使用了。[1]() 
使用代理服务器能够提高访问速度还是降低访问速度？不一定，要视具体情况而定，如果你是这个代理服务器上第一个访问目的网站的用户，那么，使用代理服务器的访问速度会降低；如果你不是第一个访问目的网站的用户，速度有可能提高，原因是在第一个用户访问代理服务器以后，目标网站的内容就保存在代理服务器上了，你要访问目的网站，此时的网页是从道理服务器直接取的，速度有可能提高，但是由于有些代理服务器的带宽比较窄或者访问的人数比较多，即使你不是第一个访问用户速度也可能降低的。[1]() 
怎样使用代理服务器？使用代理服务器的步骤是（我们以IE5为例）：a.打开浏览器IE5；b.选择“工具”--“Internet选项[1]() 
===================================

在IE等浏览器中使用HTTP代理服务器
IE5.0以上版本中设置代理：菜单栏“工具”-\>；下拉菜单“Internet选项”-\>；选项卡“连接”-\>；在“局域网设置”中选中您使用的连接，然后点击右侧的“设置”-\>；在中间的“代理服务器”栏选中“使用代理服务器”-\>；在“地址” 和“端口”栏输入本站提供的HTTP代理服务器-\>；确定-\>；确定。[1]() 
MyIE2中设置代理服务器：菜单栏“选项”——》“代理服务器”——》“代理设置”——》在输入框中输入标准格式的代理服务器，如XXX.XXX.XXX.XXX：端口，然后“确定”并退出，继续，菜单栏“选项”——》“代理服务器”——》然后选择刚才输入的代理服务器[1]() 
腾讯浏览器（TT浏览器）中设置代理服务器：菜单栏“工具”——》“WWW代理”——》“设置代理”——》在代理设置对话框中，点击“新增”——》在代理设置区中，输入代理，然后“确定”并退出，继续，菜单栏“工具”——》“WWW代理”——》然后选择刚才输入的代理服务器[1]() 
使用SOCKS代理服务器上QQ的方法
用SOCKS代理上QQ，可隐藏真实IP地址，方法如下：
启动QQ，登陆后右击下方开始菜单处的QQ小图标，选择“系统参数”==》“网络设置”
在服务器地址与端口处填QQ服务器地址，最好数字的。如5202.104.129.2515端口：8000
在“使用SOCKS5代理服务器”前打上勾，在“代理服务器地址”与“端口号”处，（QQ代理的端口号一般为1080） 分别填上最新SOCKS代理（SOCKS4也可用）
在“校验用户名”与“校验用户密码”处全部删空，然后点“测试”，如能通过，则说明代理服务器工作正常，否则换一个。[1]() 
按“确定”，点击任务栏的QQ小图标，先离线再上线即可.
在FTP中使用SOCKS代理服务器的方法
在FTP软件中我们可以使用SOCKS4/SOCKS5代理服务器，常见的FTP工具中的代理设置方法如下：
FlashFXP3.0以前版本中设置代理：菜单栏“选项”——》参数设置——》代理和防火墙，然后在“代理服务器”项中选择代理类型，填写代理
FlashFXP3.0以后版本中设置代理：菜单栏“选项”——》参数设置——》连接，然后在“代理服务器”项中选择代理类型，填写代理
CuteFTP XP 5.0.2 中文版中设置代理：菜单栏“编辑”——》设置——》连接——》SOCKS--》选择代理类型，如SOCKS4或者SOCKS5，并填写代理
LeapFtp中设置代理：菜单栏“选项”——》参数设置——》常规——》代理，将“使用代理”前面的方框钩上，然后填写代理，并将下面的SOCKS防火墙钩上



