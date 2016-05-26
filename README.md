kbengine_cocos2dx_demo
======================

kbengine_cocos2dx_demo

## KBEngine-cocos2dx 

   会实现KBEngine Cocos2dx 版本. 重点是客户端框架封装. 提供和KBE相似的开发流程. 暂时无python脚本.但用CPP写逻辑也不错吧.
   
   地址在  https://github.com/cnsoft/kbengine-cocos2dx/tree/cocos2dx-cnsoft/kbe/src/client/cocos2dx 目录下.
   有建议欢迎mail cnsoft#gmail.com 

   2014-07-01 PreAlpha is ready. Now, cocos2dx client can chat with unity3d client in the KBE same game server . by cnsoft
   
   2014-07-02 create submodule and moved here :  https://github.com/cnsoft/kbengine_cocos2dx_demo/ 
   
   2014-08-03 next branch: add in game chat kit with seemless integratation. e.g: player broad msg to others. change single player game to multiply player internal-chat game . like a mmorpg. chat in some channel. 工会.好友.交易.组队.
   
   
 ![screenshots1](https://raw.githubusercontent.com/cnsoft/kbengine-cocos2dx/cocos2dx-cnsoft/kbe/src/client/cocos2dx/snapshots/u_cocos2d_chat.PNG)
 
   2014-08-23 fellow thie url: https://github.com/cnsoft/kbengine-cocos2dx/commit/10f00267523e21fb4c971c3a6dc51b8a860444ab you need this patch for server side. it will enable chat demo feature.  
   
   2014-09-20. it should works on ios platform . no code needed to be change. you only need to create your ios project. 
![screenshots1] ( https://raw.githubusercontent.com/cnsoft/kbengine_cocos2dx_demo/master/kbedemo/snapshots/ios_cocos2d_chat_unity.png )  


   2015-05-30
      The new updated version is under testing. 
      
      Check the preview snapshot demo first.
      
![screenshots2](https://github.com/cnsoft/kbengine_cocos2dx_demo/raw/v3/kbedemo/snapshots/OtherAvatar_with_weapon_walk1.gif)
   
  2016-05-26 
      Prepare ipv6 support 
      

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

##How to
	connect to server :  
		check the testKBE function. in the function, create connection with server.
        
	demo code: 
	
	     call send chat msg:
	    
        	KAccount* account = (KAccount*) KBEngineClient::ClientApp::getInstance().pPlayer();
        	account->sendMsg(" cocos2dx coming! "); 
       
        implement more logic:
        	
              handle method call like KAccount 
        	
        	void onRemoteMethodCall( std::string methodname,MemoryStream& s )
		{
			if( methodname == "receiveMsg")
			{
				string who;
				string msg;
				s.readBlob ( who );
				s.readBlob ( msg );

				this->receiveMsg( who, msg ) ;
				//
			}
        	
                

Get more detail read the source code.		

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/cnsoft/kbengine_cocos2dx_demo/trend.png)](https://bitdeli.com/free "Bitdeli Badge")
