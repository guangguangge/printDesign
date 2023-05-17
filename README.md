## 系统优势：设计器刻度尺与真实打印纸张0误差！（可以根据设计器刻度值完美设计）

# printDesign简介
- ptDesign是基于HTML5的打印设计器
- demo地址:[https://desktool.flyscloud.com/ptDesign/index.html](https://desktool.flyscloud.com/ptDesign/index.html)
- 打印需要搭配desktool产品使用

# desktool简介

- desktool是基于自动化运维、监控、网页打印一体的插件
- desktool官网：[https://desktool.flyscloud.com/](https://desktool.flyscloud.com/)
- 目前打印部分开源免费。欢迎大家提出意见


#如何开始：
- 1.将github或gitee ptDesign项目整合到您的项目中
- 2.将设计器编辑好的模板代码，保存到您的服务器和数据库中（使用ptDesign.getTemplate()）
- 3.在需要打印的地方调用js打印（使用desktool('print',{})来打印）


`关于ptDesign.js基本API`
```javascript
ptDesign.init(data);//初始化模版
ptDesign.setTheme(data);//设置皮肤
ptDesign.getTemplate();//拿到已设计好的模版
ptDesign.setTemplate(data);//初始化编辑器模版
ptDesign.setSize(width,height);//设置纸张宽度和高度
ptDesign.setBgImage(url);//设置模版背景
ptDesign.clearBgImage();//删除模版背景
ptDesign.clear();//删除所有元素
```

--------------------------------------------
# 如何实现网页打印
* 1.使用打印功能，请先官网下载 desktool.exe
* 2.下载地址：[https://desktool.flyscloud.com/download.html](https://desktool.flyscloud.com/download.html)
* 3.目前免费版即可使用所有打印功能
* 4.在windows上启动desktool.exe
* 5.网页中引入js ```<script async type="text/javascript" src="http://localhost:11027/desktool.js"></script>```
* 6.使用desktool('print',{})即可打印

`小提示：当desktool.exe正常启动后，windows会本地开启11027端口，请引入这个js（即：localhost:11027/desktool.js）实现原生打印`


# 其他，关于desktool.exe的api
desktool js demo：[https://desktool.flyscloud.com/example.html](https://desktool.flyscloud.com/example.html)
主要API：
```javascript
desktool('print',{});//使用原生打印（不弹窗，可连打，性能高。）
desktool('get',{mem:{},cpu:{},disk:{},network{});//返回该windows的性能参数，内存，cpu,硬盘读写，网络带宽
desktool('get',{printer:{});//返回该windows上所有打印机
desktool('screenshot',{scale:0.8});//屏幕截图，（根据0.8倍缩放PNG图片）
desktool('powerShell1',{});//执行原生powerShell1命令并返回
desktool('powerShell2',{});//执行原生powerShell2命令并返回
```
`小提示：powerShell 1或2，为了安全，不支持调用传参，只能在config.txt去配置初始化，powerShell命令能解决下面一些场景`
- 1.水果店，生鲜店，通过js获取usb称重器的值（可以将powerShell1的脚本配置成获取usb称重器并返回给网页）
- 2.windows电脑接入了一些特殊usb设备，身份证读卡器，多摄像头，指纹等（可以通过原生powerShell获取值，给到网页返回）
- 3.某种情况下，也可以配置成清理chrome缓存或者创建桌面快捷方式，让后通过网页调用

-------------------------------------------------------
#The following content is from google translation.

## System advantage: Zero error between the designer scale and the real printing paper! (It can be perfectly designed according to the designer scale value)

#Introduction to printDesign
- ptDesign is a print designer based on HTML5
- demo address: [https://desktool.flyscloud.com/ptDesign/index.html](https://desktool.flyscloud.com/ptDesign/index.html)
- Printing needs to be used with desktool products

#desktoolIntroduction

- desktool is a plug-in based on automated operation and maintenance, monitoring, and web page printing
- desktool official website: [https://desktool.flyscloud.com/](https://desktool.flyscloud.com/)
- Currently the printing part is open source and free. We welcome your comments


#How to get started:
- 1. Integrate the github or gitee ptDesign project into your project
- 2. Save the template code edited by the designer to your server and database (use ptDesign.getTemplate())
- 3. Call js to print where it needs to be printed (use desktool('print',{}) to print)


`About ptDesign.js basic API`
```javascript
ptDesign.init(data);//initialize the template
ptDesign.setTheme(data);//set skin
ptDesign.getTemplate();//Get the designed template
ptDesign.setTemplate(data);//Initialize editor template
ptDesign.setSize(width,height);//Set paper width and height
ptDesign.setBgImage(url);//Set template background
ptDesign.clearBgImage();//Delete template background
ptDesign.clear();//Delete all elements
```

--------------------------------------------
# How to implement web page printing
* 1. To use the printing function, please download desktool.exe from the official website first
* 2. Download link: [https://desktool.flyscloud.com/download.html](https://desktool.flyscloud.com/download.html)
* 3. All printing functions can be used in the current free version
* 4. Start desktool.exe on windows
* 5. Introduce js into the webpage ```<script async type="text/javascript" src="http://localhost:11027/desktool.js"></script>```
* 6. Use desktool('print',{}) to print

`Tips: When desktool.exe starts normally, windows will open port 11027 locally, please import this js (ie: localhost:11027/desktool.js) to realize native printing`


# Others, about the api of desktool.exe
desktool js demo: [https://desktool.flyscloud.com/example.html](https://desktool.flyscloud.com/example.html)
Main APIs:
```javascript
desktool('print',{});//Use native printing (no pop-up window, continuous typing, high performance.)
desktool('get',{mem:{},cpu:{},disk:{},network{});//Return the performance parameters of the windows, memory, cpu, hard disk read and write, network bandwidth
desktool('get',{printer:{});//return all printers on this windows
desktool('screenshot',{scale:0.8});//Screenshot, (scale PNG image according to 0.8 times)
desktool('powerShell1',{});//Execute the native powerShell1 command and return
desktool('powerShell2',{});//Execute the native powerShell2 command and return
```
`Tips: powerShell 1 or 2, for security reasons, does not support calling parameters, and can only be configured and initialized in config.txt, powerShell commands can solve some of the following scenarios`
- 1. Fruit shop, fresh store, get the value of the usb scale through js (you can configure the script of powerShell1 to get the usb scale and return it to the webpage)
- 2. The windows computer is connected to some special usb devices, ID card readers, multi-cameras, fingerprints, etc.
- 3. In some cases, it can also be configured to clear the chrome cache or create a desktop shortcut, and then call it through the web page
