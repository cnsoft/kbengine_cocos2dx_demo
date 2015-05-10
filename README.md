kbengine_cocos2dx_demo
======================

kbengine_cocos2dx_demo



##What is KBEngine?

An open source MMOG server engine, Using a simple protocol will be able to make the client and server interaction,
To use the KBEngine-plugins quick combine with (Unity3D, OGRE, Cocos2d, HTML5, etc.) to form a complete client.

Engine framework written using c++, Game logic layer using Python, 
developers do not need to re-implement some common server-side technology,
Allows developers to concentrate on the game logic development, quickly create a variety of games.

(Frequently asked load-limit, kbengine is designed to be multi-process distributed dynamic load balancing scheme, 
In theory only need to expand hardware can increase load-limit, The complexity of the single machine 
load-limit depends on the logic of the game itself.)

## 什么是KBEngine?
一款开源的游戏服务端引擎，使用简单的约定协议就能够使客户端与服务端进行交互，
使用KBEngine插件能够快速与(Unity3D, OGRE, Cocos2d, HTML5, 等等)技术结合形成一个完整的客户端。

服务端底层框架使用c++编写， 游戏逻辑层使用Python， 开发者无需重复的实现一些游戏服务端通用的底层技术，
将精力真正集中到游戏开发层面上来，快速的打造各种网络游戏。

(经常被问到承载上限, kbengine底层架构被设计为多进程分布式动态负载均衡方案， 理论上只需要不断扩展硬件就能够
不断增加承载上限, 单台机器的承载上限取决于游戏逻辑本身的复杂度。)


KBEngine Homepage

http://www.kbengine.org

sources     : https://github.com/kbengine/kbengine/

##Demo sources

      unity3d     : https://github.com/kbengine/kbengine_unity3d_demo
      unity3d     : https://github.com/kbengine/kbengine_unity3d_warring
      ogre        : https://github.com/kbengine/kbengine_ogre_demo
      html5       : https://github.com/kbengine/kbengine_html5_demo
      cocos2dx    : https://github.com/kbengine/kbengine_cocos2dx_demo
      	

## KBEngine-cocos2dx 

   会实现KBEngine Cocos2dx 版本. 重点是客户端框架封装. 提供和KBE相似的开发流程. 可能无python脚本.但用CPP写逻辑也不错吧.
   地址在  https://github.com/cnsoft/kbengine-cocos2dx/tree/cocos2dx-cnsoft/kbe/src/client/cocos2dx 目录下.
   有建议欢迎mail cnsoft#gmail.com 

   2014-07-01 PreAlpha is ready. Now, cocos2dx client can chat with unity3d client in the KBE same game server . by cnsoft
   
   2014-07-02 create submodule and moved here :  https://github.com/cnsoft/kbengine_cocos2dx_demo/ 
   
   2014-08-03 next branch: add in game chat kit with seemless integratation. e.g: player broad msg to others. change single player game to multiply player internal-chat game . like a mmorpg. chat in some channel. 工会.好友.交易.组队.
   
 ![screenshots1](https://raw.githubusercontent.com/cnsoft/kbengine-cocos2dx/cocos2dx-cnsoft/kbe/src/client/cocos2dx/snapshots/u_cocos2d_chat.PNG)
 
   2014-08-23 fellow thie url: https://github.com/cnsoft/kbengine-cocos2dx/commit/10f00267523e21fb4c971c3a6dc51b8a860444ab you need this patch for server side. it will enable chat demo feature.  
   
   2014-09-20. it should works on ios platform . no code needed to be change. you only need to create your ios project. 
![screenshots1] ( https://raw.githubusercontent.com/cnsoft/kbengine_cocos2dx_demo/master/kbedemo/snapshots/ios_cocos2d_chat_unity.png )  

   some preview video link: 
        Win: http://v.youku.com/v_show/id_XNzM0MzE2NzE2.html 
		ios: http://v.youku.com/v_show/id_XNzg2Nzk4NjI4.html

   until now, you can extend your system according this demo. e.g: define more system and implemented it in server side and client side. that's the start kit. next update, i want to create a more powerful demo.  
   
   
##Q&A
	This demo is used cocos2dx 2.2.3. cocos2dx files are not stored in this repository. you should prepare it locally. 
	After configure cocos2dx. place the kbedemo folder into Projects folder. open the kbedemo.sln and  can build it yourself.
	
##Install
	Install KBE Server 0.1.5 - 0.1.7 .( or you can download kbengine-cocos2dx, it is my debug server version. with it you can got the chat patch server side also. ) 
		It seems that we should upgrade this library to support latest KBE v0.1.13. 
	Until that, you should use correct version to test this demo. it should works on ios and andriod also.  

	if you fork this project and contribute back, you are welcomed! 
	Sorry for can not upgrade this project in time with offical kbengine. because i have no much time can be assigned to it, for i am freelancer at the begin of this year, it meaning no salary for half past year.
	i have to working hard on my indie game project first. so if someone like, you can buy some time from me. LOL :) 
	Of course, i will try my best to upgrade this project soon or later. 

  
  2015-05-10
        create v3 branch for prepare upgraded to cocos2dx 3.x . even include WP8 support. native socket testing.
