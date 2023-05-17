## 系统优势：设计器刻度尺与真实打印纸张0误差！（可以根据设计器刻度值完美设计）

# printDesign简介
- ptDesign是基于HTML5的打印设计器
- demo地址:[https://desktool.flyscloud.com/ptDesign/index.html](https://desktool.flyscloud.com/ptDesign/index.html)
- 打印需要搭配desktool产品使用

# desktool简介

- desktool是基于自动化运维、监控、网页打印一体的插件
- desktool官网：[https://desktool.flyscloud.com/](https://desktool.flyscloud.com/)
- 目前打印部分开源免费。欢迎大家提出意见


# 如何开始：
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
# The following translation is provided by ChatGPT -3.5

## System Advantages: Zero Deviation Between Designer Ruler and Actual Printed Paper! (Perfect Design Based on Designer Scale Values)

# Introduction to printDesign
- ptDesign is a print designer based on HTML5.
- Demo link: [https://desktool.flyscloud.com/ptDesign/index.html](https://desktool.flyscloud.com/ptDesign/index.html)
- Printing requires the use of desktool product.

# Introduction to desktool

- desktool is a plugin that combines automation operation and maintenance, monitoring, and web printing.
- desktool official website: [https://desktool.flyscloud.com/](https://desktool.flyscloud.com/)
- Currently, the printing part is open source and free. Suggestions are welcome from everyone.


# Getting Started
- 1. Integrate the ptDesign project from GitHub or Gitee into your own project.
- 2. Save the template code edited in the designer to your server and database (using ptDesign.getTemplate()).
- 3. Call the JavaScript print function where printing is needed (using desktool('print', {}) to print).


`Basic APIs of ptDesign.js`
```javascript
ptDesign.init(data); // Initialize the template
ptDesign.setTheme(data); // Set the skin
ptDesign.getTemplate(); // Get the designed template
ptDesign.setTemplate(data); // Initialize the editor template
ptDesign.setSize(width, height); // Set the paper width and height
ptDesign.setBgImage(url); // Set the template background
ptDesign.clearBgImage(); // Remove the template background
ptDesign.clear(); // Remove all elements
```

--------------------------------------------
# How to Implement Web Printing
* 1. To use the printing function, please download desktool.exe from the official website first.
* 2. Download link: [https://desktool.flyscloud.com/download.html](https://desktool.flyscloud.com/download.html)
* 3. The free version currently supports all printing functions.
* 4. Start desktool.exe on Windows/linux.
* 5. Include the JavaScript in the web page: `<script async type="text/javascript" src="http://localhost:11027/desktool.js"></script>`
* 6. Use desktool('print', {}) to print.

`Tip: When desktool.exe starts normally, Windows will open port 11027 locally. Please include this JavaScript (i.e., localhost:11027/desktool.js) to achieve native printing.`


# Others, API for desktool.exe
desktool js demo: [https://desktool.flyscloud.com/example.html](https://desktool.flyscloud.com/example.html)
Main APIs:
```javascript
desktool('print', {}); // Use native printing (no pop-ups, can print continuously, high performance)
desktool('get', { mem: {}, cpu: {}, disk: {}, network:{}}); // Return performance parameters of this Windows system: memory, CPU, disk read/write, network bandwidth
desktool('get', { printer: {}); // Return all printers on this Windows system
desktool('screenshot', { scale: 0.8 }); // Take a screenshot of the screen (PNG image scaled by 0.8)
desktool('powerShell1', {}); // Execute native PowerShell1 command and return the result
desktool('powerShell2', {}); // Execute native PowerShell2 command and return the result
```
`Tip: For security reasons, powerShell 1 or 2 does not support calling with parameters. You can only configure it in config.txt for initialization. PowerShell commands can solve the following scenarios:`
- 1. For fruit stores or fresh food stores, retrieve the values from a USB weighing scale using JavaScript (you can configure the PowerShell1 script to retrieve the values from a USB weighing scale and return them to the web page).
- 2. If a Windows computer is equipped with special USB devices such as ID card readers, multiple cameras, or fingerprint scanners, you can retrieve the values using native PowerShell and return them to the web page.
- 3. In certain situations, you can also configure it to clear the Chrome cache or create desktop shortcuts, and then call them through the web page.
