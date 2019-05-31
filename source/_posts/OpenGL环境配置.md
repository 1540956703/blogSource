---
layout: port
title: OpenGL环境配置
date: 2019-05-30 20:26:35
tags: OpenGL
---

<div id="topics">
	<div class = "post">
		<h1 class = "postTitle">
			<a id="cb_post_title_url" class="postTitle2" href="https://www.cnblogs.com/lichuangblog/p/10920592.html">环境搭建</a>
		</h1>
		<div class="clear"></div>
		<div class="postBody">
			<div id="cnblogs_post_body" class="blogpost-body"><p>首先说一下自学的网址：&nbsp;<a href="https://learnopengl-cn.github.io/">https://learnopengl-cn.github.io/</a>&nbsp;这个也是主要资料。</p>
<p>1.GLFW下载与配置：</p>
<p>下载地址：<a href="https://www.glfw.org/download.html">https://www.glfw.org/download.html</a></p>
<p><img src="https://img2018.cnblogs.com/blog/1064759/201905/1064759-20190524221536458-315242762.png" alt="" width="612" height="212" /></p>
<p>建议下载32位的，据说64位会有很多问题所以我就先不用了。</p>
<p>下载后里面有很多VS版本的类库，至于用哪一个就看使用的VS版本了。</p>
<p>打开VS创建一个空的C++项目，然后再解决方案中右击项目打开属性页。</p>
<p><img src="https://img2018.cnblogs.com/blog/1064759/201905/1064759-20190524222246229-459948353.png" alt="" width="700" height="464" /></p>
<p>&nbsp;</p>
<p>2.GLAD下载与配置:</p>
<p>打开网址&nbsp;<a href="http://glad.dav1d.de/">http://glad.dav1d.de/</a>&nbsp;按以下配置进行选择:</p>
<p><img src="https://img2018.cnblogs.com/blog/1064759/201905/1064759-20190524222834187-1392052658.png" alt="" width="684" height="268" /></p>
<p>选完后</p>
<p><img src="https://img2018.cnblogs.com/blog/1064759/201905/1064759-20190524223030815-240527541.png" alt="" width="755" height="188" /></p>
<p>在生成后的页面下载生成后.zip文件:</p>
<p><img src="https://img2018.cnblogs.com/blog/1064759/201905/1064759-20190524223124684-1140134663.png" alt="" width="281" height="173" /></p>
<p>把解压后的include里面的两个文件夹复制到glfw的include文件夹下，当然你也可以再创建个项目进行外链。</p>
<p>把src下的文件glad.c复制到自己的项目中去.按以下步骤把glfw3.lib和opengl32.lib加入链接器。</p>
<p><img src="https://img2018.cnblogs.com/blog/1064759/201905/1064759-20190524223608305-708627247.png" alt="" width="728" height="472" /></p>
<p>&nbsp;</p>
<p>&nbsp;3.测试:</p>
<p>创建.cpp文件把下面代码复制进去，看是否出现了窗口。</p>
<div class="cnblogs_Highlighter">
<pre class="brush:cpp;gutter:true;">#include &lt;glad/glad.h&gt;
#include &lt;GLFW/glfw3.h&gt;
#include&lt;iostream&gt;
using namespace std;
void framebuffer_size_callback(GLFWwindow* window, int width, int height);
void processInput(GLFWwindow *window);
int main()
{
	glfwInit();
	//设置glfw的版本为3.3
	glfwWindowHint(GLFW_CONTEXT_VERSION_MAJOR, 3);
	glfwWindowHint(GLFW_CONTEXT_VERSION_MINOR, 3);

	glfwWindowHint(GLFW_OPENGL_PROFILE, GLFW_OPENGL_CORE_PROFILE);

	//创建窗体
	GLFWwindow* window = glfwCreateWindow(800, 600, "LearnOpenGL", NULL, NULL);
	if (window == NULL)
	{
		std::cout &lt;&lt; "Failed to create GLFW window" &lt;&lt; std::endl;
		glfwTerminate();
		return -1;
	}
	glfwMakeContextCurrent(window);
	if (!gladLoadGLLoader((GLADloadproc)glfwGetProcAddress))
	{
		std::cout &lt;&lt; "Failed to initialize GLAD" &lt;&lt; std::endl;
		return -1;
	}
	glViewport(0, 0, 800, 600);
	glfwSetFramebufferSizeCallback(window, framebuffer_size_callback);

	// 渲染循环
	while (!glfwWindowShouldClose(window))
	{
		glClearColor(0.2f, 0.3f, 0.3f, 1.0f);
		glClear(GL_COLOR_BUFFER_BIT);
		// 输入
		processInput(window);

		// 渲染指令


		// 检查并调用事件，交换缓冲
		glfwPollEvents();
		glfwSwapBuffers(window);
	}
	glfwTerminate();
	return 0;
}
//当窗口改变时调用
void framebuffer_size_callback(GLFWwindow* window, int width, int height)
{
	glViewport(0, 0, width, height);
}
//给窗体注册输入事件
void processInput(GLFWwindow *window)
{
	if (glfwGetKey(window, GLFW_KEY_ESCAPE) == GLFW_PRESS)
	{
		glfwSetWindowShouldClose(window, true);
	}	
}
</pre>
</div>
</div>