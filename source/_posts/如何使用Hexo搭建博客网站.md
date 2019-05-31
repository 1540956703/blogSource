---
title: 如何使用Hexo搭建博客网站(转)
date: 2019-05-29 17:24:08
tags: Hexo
categories: Hexo
---

<p>原文连接: www.cnblogs.com/fengxiongZz/p/7707219.html</p>
<div id="cnblogs_post_body" class="blogpost-body"><p>前言：电脑系统为window 10专业版，64位</p>
<p><strong>相关步骤：</strong></p>
<p>1、安装Node.js和配置好Node.js环境，打开cmd命令行，成功界面如下</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021222335756-1508643846.png" alt="" /></p>
<p>&nbsp;</p>
<p>&nbsp;2、安装Git和配置好Git环境，安装成功的象征就是在电脑上任何位置<strong>鼠标右键</strong>能够出现如下两个选择</p>
<p>&nbsp;<img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021222542474-1351750125.png" alt="" /></p>
<p>注意：一般出于安全考虑，只有在Git Bash Here中才能进行Git的相关操作。如果需要在cmd命令行里调用Git，那么就要配置电脑的环境变量Path，或者在安装的时候选择use Git from the Windows Command Prompt。这个可有可无，影响不大，成功配置的界面如图</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021223101193-1524328031.png" alt="" /></p>
<p>&nbsp;</p>
<p>&nbsp;3、Github账户注册和新建项目，项目必须要遵守格式：账户名.github.io，不然接下来会有很多麻烦。并且需要勾选Initialize this repository with a README</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021223639881-1998790649.png" alt="" /></p>
<p>&nbsp;</p>
<p>在建好的项目右侧有个settings按钮，点击它，向下拉到GitHub Pages，你会看到那边有个网址，访问它，你将会惊奇的发现该项目已经被部署到网络上，能够通过外网来访问它。&nbsp;</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021223928802-1978574025.png" alt="" /></p>
<p>&nbsp;</p>
<p>&nbsp;4、安装Hexo，在自己认为合适的地方创个文件夹，我是在D盘建了一个blog文件夹。然后通过命令行进入到该文件夹里面</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021224442443-1196707159.png" alt="" /></p>
<p>&nbsp;</p>
<p>输入npm install hexo -g，开始安装Hexo</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021224910568-2096615217.png" alt="" /></p>
<p>&nbsp;</p>
<p>输入hexo -v，检查hexo是否安装成功</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021225015224-1426206003.png" alt="" /></p>
<p>&nbsp;</p>
<p>输入hexo init，初始化该文件夹（有点漫长的等待。。。）</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021230203912-509196411.png" alt="" /></p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021230241646-1660449756.png" alt="" /></p>
<p>看到后面的&ldquo;Start blogging with Hexo！&rdquo;，激动有木有！！！！！</p>
<p>&nbsp;</p>
<p>输入npm install，安装所需要的组件</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021231521646-1099473727.png" alt="" /></p>
<p>&nbsp;</p>
<p>输入hexo g，首次体验Hexo</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021231705474-1404994153.png" alt="" /></p>
<p>&nbsp;</p>
<p>&nbsp;输入hexo s，开启服务器，访问该网址，正式体验Hexo</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021231833912-663774637.png" alt="" /></p>
<p>问题：假如页面一直无法跳转，那么可能端口被占用了。此时我们ctrl+c停止服务器，接着输入&ldquo;hexo server -p 端口号&rdquo;来改变端口号</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021232311912-1198771378.png" alt="" /></p>
<p>那么出现如下图就成功了</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021232413224-1288183746.png" alt="" /></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;5、将Hexo与Github page联系起来，设置Git的user name和email（如果是第一次的话）</p>
<p>&nbsp;<img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021233157224-1386748377.png" alt="" /></p>
<p>上图是在其文件夹里面鼠标右键，点击Git Base Here。这里&ldquo;feng&rdquo;可以替换成自己的用户名，邮箱可以替换成自己的邮箱</p>
<p>&nbsp;</p>
<p>输入cd ~/.ssh，检查是否由.ssh的文件夹</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021233543052-76995831.png" alt="" /></p>
<p>&nbsp;</p>
<p>输入ls，列出该文件下的内容。下图说明存在</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021233630568-279882178.png" alt="" /></p>
<p>&nbsp;</p>
<p>&nbsp;输入ssh-keygen -t rsa -C &ldquo;929762930@qq.com&rdquo;，连续三个回车，生成密钥，最后得到了两个文件：id_rsa和id_rsa.pub（默认存储路径是：C:<span class="hljs-command">\Users<span class="hljs-command">\Administrator<span class="hljs-command">\.ssh）</span></span></span>。</p>
<p>&nbsp;<img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021234107209-1205335399.png" alt="" /></p>
<p>&nbsp;</p>
<p>&nbsp;输入eval "$(ssh-agent -s)"，添加密钥到ssh-agent</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021234314146-695835137.png" alt="" /></p>
<p>&nbsp;</p>
<p>&nbsp;再输入ssh-add ~/.ssh/id_rsa，添加生成的SSH key到ssh-agent</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021234528552-610835964.png" alt="" /></p>
<p>&nbsp;</p>
<p>&nbsp;登录Github，点击头像下的settings，添加ssh</p>
<p>&nbsp;<img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021234636834-426105098.png" alt="" /></p>
<p>&nbsp;</p>
<p>新建一个new ssh key，将id_rsa.pub文件里的内容复制上去</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021234906724-1938556332.png" alt="" /></p>
<p>&nbsp;</p>
<p>输入ssh -T git@github.com，测试添加ssh是否成功。如果看到Hi后面是你的用户名，就说明成功了</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021235116271-1521882533.png" alt="" /></p>
<p><span style="color: #993300;"><strong>问题：</strong></span>假如ssh-key配置失败，那么只要以下步骤就能完全解决</p>
<div>
<div>
<p>首先，清除所有的key-pair<br />ssh-add -D<br />rm -r ~/.ssh<br />删除你在github中的public-key</p>
<p>重新生成ssh密钥对<br />ssh-keygen -t rsa -C "xxx@xxx.com"</p>
<p>接下来正常操作<br />在github上添加公钥public-key:<br />1、首先在你的终端运行 xclip -sel c ~/.ssh/id_rsa.pub将公钥内容复制到剪切板<br />2、在github上添加公钥时，直接复制即可<br />3、保存</p>


测试：<br />在终端 ssh -T git@github.com</div>


</div>
<p>&nbsp;</p>
<p>6、配置Deployment，在其文件夹中，找到_config.yml文件，修改repo值（在末尾）</p>
<p>&nbsp;<img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021235812974-84318377.png" alt="" /></p>
<p>&nbsp;</p>
<p>repo值是你在github项目里的ssh（右下角）</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171021235722365-818312042.png" alt="" /></p>
<p>&nbsp;</p>
<p>7、新建一篇博客，在cmd执行命令：hexo new post &ldquo;博客名&rdquo;</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171022000227834-1991784353.png" alt="" /></p>
<p>&nbsp;</p>
<p>&nbsp;这时候在文件夹_posts目录下将会看到已经创建的文件</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171022000508865-46787156.png" alt="" /></p>
<p>&nbsp;</p>
<p>在生成以及部署文章之前，需要安装一个扩展：npm install hexo<span class="hljs-attribute">-deployer<span class="hljs-attribute">-git <span class="hljs-subst">--save</span></span></span></p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171022001237943-657272339.png" alt="" /></p>
<p>&nbsp;</p>
<p>使用编辑器编好文章，那么就可以使用命令：hexo d -g，生成以及部署了</p>
<p>&nbsp;<img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171022001410662-1611125904.png" alt="" /></p>
<p>&nbsp;</p>
<p>部署成功后访问你的地址：http://用户名.github.io。那么将看到生成的文章</p>
<p><img src="https://images2017.cnblogs.com/blog/1108615/201710/1108615-20171022001738037-1195721153.png" alt="" /></p>
<p>&nbsp;</p>
<p>&nbsp;好了，到此为止，最基本的也是最全面的hexo+github搭建博客完结。接下来是进阶的操作</p>
