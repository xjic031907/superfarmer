面试高频指数：★ ★ ★ ★ ★

（1）什么是 HTML5？

HTML5 是定义 HTML 标准的组新版本，具有两个不同的概念：

HTML5 是一个新版本的 HTML 语言，具有新的元素，属性和行为
HTML5 有更大的技术集，允许构建多样化和更强大的网站和应用程序
（2）HTML5 有哪些新特性 ？
根据功能，HTML5 新特性可以分为：

语义：能够更恰当地描述内容是什么
新的区块和段落元素
举例：
<section> 表示一个包含在 HTML 文档的独立部分
<article> 表示文档、页面、应用或网站中的独立结构
<nav> 表示页面的一部分，其目的是在当前文档或其他文档提供导航链接
<header> 用于展示介绍性内容辅助导航。包含标题，Logo，搜索框和作者名称
<footer> 表示最近一个章节或根节点元素的页脚，包含作者，版权，相关链接
<aside> 表示一个和其余页面内容几乎无关的部分，通常是侧边栏或标注框
<hgroup>代表文档章节所属的多级别目录
嵌入和允许操作新的多媒体内容
举例：
<audio> 用于在文档中嵌入音频内容
<video> 用于再文档嵌入媒体播放器，支持视频及音频播放
表单的改进
强制性校验 API
举例：
required 必填属性
pattern 声明正则校验规则属性
minlength 和 maxlength 限制输入的长度
constraint validation API 检测和自定义表单元素的状态
新 <input> 元素的 type 属性值
举例：
color 取色器
date 日期控件
detetime-local 不包括时区的日期控件
month 输入年和月的控件，没有时区
range 输入不需要精确地数字空间
search 搜索字符串的单行文字区域
tel 输入电话号码的控件
time 输入时间的控件
url 输入并校验 URL 的控件
其它新的语义元素
举例：
<mark> 为表示引用或符号目的而标记或突出显示的文本
<figure> 常与 <figcaption> 配合使用，表示独立的说明内容
<data> 将一个指定内容和机器可读的翻译联系在一起
<time> 表示机器可读的 24 小时制的时间或者公历日期
<progress> 显示一项任务的完成进度
<meter> 用来显示已知范围的标量值或者分数值
<main> 呈现了文档的 <body> 或应用的主体部分
output 表示计算或用户操作的结果
<iframe> 的改进
精确控制 <iframe> 元素的安全级别和期望的渲染
举例：
sandbox 对呈现在 iframe 框架中的内容启用一些额外的限制条件
srcdoc 支持的浏览器优先使用 srcdoc 代替 src
MathML
用于描述数学公式、符号的一种标记语言，允许直接嵌入数学公式
连通性：能够通过创新的新技术方法进行通信
Web Sockets
允许在页面和服务器之间建立持久连接，并通过这种方法来交换非 HTML 数据
Server-sent events
允许服务器向客户端推送事件
WebRTC
支持在浏览器客户端之间语音 / 视频交流和数据分享的技术
浏览器原生支持点对点的分享应用数据和进行电话会议
离线 & 存储：能够让网页再客户端本地存储数据并且更高效地离线运行
离线资源：应用程序缓存
缓存 .manifest 上的资源，离线或资源没有更新时，浏览器会加载缓存的离线资源
在线和离线事件
navigator.onLine 返回在线 true 或离线 false
online 和 offline 事件
window document document.body 使用 addEventListener
document document.body 的 .ononline 或 .onoffline 属性设为一个 JavaScript Function 对象
<body> 标签上指定 ononline="..." 或 onoffline="..." 属性
WHATWG 客户端会话和持久化存储（又名 DOM 存储）
Storage
DOM 存储被设计为用户提供一个更大存储量，更安全，更便捷的存储方法
代替掉将一些不需要让服务器知道的信息存储到 cookies 里的这种传统方法
构造函数 Storage 及其实例
seesionStorage 全局对象，维护着页面会话期间有效的存储空间，重新载入或从崩溃中恢复不会丢失
localStorage 全局对象，本次持久化存储，隐身模式下关闭浏览器会丢弃
IndexedDB
用于在客户端存储大量的结构化数据，包括文件 / 二进制大型对象（blobs）
使用索引实现对数据的高性能搜索
在 Web 应用程序中使用文件
File API：可以访问 FileList，包含表示用户所选择的 File 对象
name 文件名称，只读字符串，只包含文件名，不包含任何路径信息
size 以字节数为单位的文件大小，只读的 64 位整数
type 文件的 MIME 类型，只读字符串，当类型不能确定为 ""
通过 change 事件访问被选择的文件
this.files
通过 drogenter dragover drag 的 dataTransfer 的 files 中获取文件列表
对象 URL window.URL.createObjectURL() 和 window.URL.revokeObjectURL()
多媒体：加快普及 video 和 audio 应用，丰富 web 表现力
HTML5 音视频
<video> 和 <audio> 标签以及 JavaScript 和 APIs 用于对其进行控制
WebRTC
支持在浏览器客户端之间语音 / 视频交流和数据分享的技术
浏览器原生支持点对点的分享应用数据和进行电话会议
Camera API
使用手机的摄像头拍照，然后把拍到的照片发送给当前网页
Track 和 WebVTT
<track> 元素怒被当作媒体元素 <audio> 和 <video> 的子元素
WebVTT（Web 视频文本跟踪格式）使用 <track> 元素现实定时文本轨道（如字幕或标题）的格式化，支持 VTTCue 和 VTTRegion 接口
2D/3D 绘图 & 效果：提供定制图形、动画界面的新选择
Canvas
<canvas> 元素被用来通过 JavaScript （Canvas API 或 WebGL API）绘制图形及图形动画
HTML5 文本 API 由 <canvas> 支持
fillText(text, x, y, [, maxWidth]) 在指定的 (x, y) 位置填充指定的文本
strokeText(text, x, y, [, maxWidth] 在指定的 (x, y) 位置绘制文本边框
WebGL
WebGL （Web 图形库） 是一个 JavaScript API，可在任何兼容的 Web 浏览器中渲染高性能的交互式 3D 和 2D 图形，无需使用插件
WebGL 引入 OpenGL ES 2.0，通过 canvas.getContext('webgl') 使用
WebGL 2 引入 OpenGL ES 3.0，通过 canvas.getContext('webgl2') 使用
SVG
SVG （可缩放矢量图形）是一种描述二维的矢量图形，基于 XML 的标记语言
优雅而简洁地渲染不同大小的图形，并和 CSS，DOM，JavaScript 和 SMIL 等其他网络标准无缝衔接
可以搜索、索引、编写脚本和压缩，也可以使用任何文本编辑器和绘图软件来创建和编辑 SVG
性能 & 集成：提供作用显著的性能优化方案，更有效地使用设备硬件
Web Workers
为 Web 内容在后台线程中运行脚本提供一种简单方法
线程可以执行任务而不干扰用户界面
专用 worker
new Worker() 构建
通过 postMessage() 和 onmessage 事件函数发送和接收消息
共享 worker
new SharedWorker() 构建
通过 po``r``t``.``postMessage() 和 po``r``t.onmessage 事件函数发送和接收消息
worker 中需先使用 onconnect 获取 port
XMLHttpRequest Level 2
可以设置 HTTP 请求的时限
可以使用 FormData 对象管理表单数据
可以上传文件
可以请求不同域名下的数据（跨域请求）
可以获取服务器端的二进制数据
可以获得数据传输的进度信息
即时编译的 JavaScript 引擎
新一代的 JavaScript 引擎更强大，性能更杰出
History API
History 接口允许操作浏览器的曾经在标签页或者框架里访问的会话历史记录
属性
History.length 返回一个整数，该整数表示会话历史中元素的数目，包括当前加载的页
History.scrollRestoration 允许 Web 应用程序在历史导航上显式地设置默认滚动恢复行为。此属性可以是自动的（auto）或者手动的（manual）
History.state 返回一个表示历史堆栈顶部的状态的值。这是一种可以不必等待 popstate 事件而查看状态的方式
方法
History.back() 在浏览器历史记录里前往上一页，用户可以点击浏览器左上角的返回按钮模拟此方法，等价于 history.go(-1)
History.forward() 在浏览器历史记录中前往下一页，用户可以点击浏览器左上角的前进按钮模拟此方法，等价于 history.go(1)
History.go() 通过当前页面的相对位置从浏览器历史记录（会话记录）加载页面
History.pushState() 按指定的名称和 URL（如果提供该参数）将数据 push 进会话历史栈，数据被 DOM 进行不透明处理，你可以指定任何可以被序列化的 JavaScript 对象
History.replaceState() 按指定的数据，名称和 URL（如果提供该参数）更新历史栈上最新的入口。这个数据被 DOM 进行了不透明处理。您可以指定任何可以被序列化的 JavaScript 对象
Content Editable
HTML 中任何元素都可以被编辑，设置 contenteditable 属性为 true 即可
HTML5 将此属性标准化
HTML 拖放 API
HTML 拖放（Drag and Drop）接口使应用程序能够在浏览器中私用拖放功能
引入拖放功能的基本步骤
确定可拖拽元素
给元素添加 draggable 属性，添加全局事件处理函数 ondragstart
定义拖拽数据
通过 drag event 的 dataTransfer 属性访问事件数据
通过 dataTransfer 的 setData() 方法为拖拽数据添加一个项
通过 dataTransfer 的 setDrageImage 方法定义拖拽图像
通过 dataTransfer 的 dropEffect 属性定义拖拽效果
copy 表明拖拽的数据将从它原本的位置拷贝到目标的位置
move 表明被拖拽的数据将被移动
link 表明拖拽源位置和目标之间将会创建一些关系表格或是连接
确定放置区域
给元素添加 ondragover 和 ondrop 事件处理程序属性
定义放置效果
通过 dataTransfer 的 dropEffect 属性定义拖拽效果
拖拽结束
拖拽操作结束时，在源元素（开始拖拽时的目标元素）上触发 dragend 事件
不管拖拽是完成还是取消，这个事件都会被触发
HTML 焦点管理
DOM 属性 activeElement 与方法 hasFocus() 为程序按提供了更好的控制页面交互的能力，特别是丢与用户行为引发的交互
activeElement 只读属性，用来返回当前在 DOM 或者 shadow DOM 树中处于聚焦状态的 Element
Do``cumen``t.hasFocus() 方法返回一个 Boolean，表明当前文档或者文档内的节点是否获得了焦点。该方法可以用来判断当前文档中的活动元素是否获得了焦点
两者关系
获得焦点的元素一定是当前文档的活动元素
一个文档中的活动元素不一定获得了焦点
基于 Web 的协议处理程序
使用 navigator.registerProtoolHandler(sch``em``e,``ur``l``, tit``le) 方法把 web 应用程序注册成一个协议处理程序
requestAnimationFrame
传入一个回调函数，该回调函数会在浏览器下一次重绘之前执行
全屏 API
全屏 API 为使用用户的整个屏幕展现网络内容提供了一种简单的方式，不需要时退出全屏模式
方法
Document.exitFullscreen() 用于请求从全屏模式切换到窗口模式，会返回一个 Promise，会在全屏模式完全关闭的时候，被重置为 resolved 状态
Element.requestFullscreen() 请求浏览器将特定元素置为全屏模式，隐去屏幕上的浏览器所有 UI 元素，以及其它应用
属性
DocumentOrShadowRoot.fullscreenElement fullscreenElement 属性提供了当前在 DOM（或者 shadow DOM）里被展示为全屏模式的 Element，如果这个值为 null，文档不处于全屏模式
Document.fullscreenEnabled fullscreenEnabled 属性提供了启用全屏模式的可能性。当它的值是 false 的时候，表示全屏模式不可用
事件处理程序
Document 事件处理程序 onfullscreenchange 和 onfullscreenerror
Element 事件处理程序 onfullscreenchange 和 onfullscreenerror
指针锁定 API
光标移到浏览器或者屏幕区域之外，指针锁定也能够让你访问鼠标事件
指针锁定是持久性的。指针锁定不释放鼠标，直到作出一个显式的 API 调用或者用户使用一个专门的释放手势
指针锁定不局限于浏览器或者屏幕边界
指针锁定持续发送事件，而不管鼠标按钮状态如何
指针锁定隐藏光标
指针锁定目前需要先进入全屏模式 requestFullscreen() 然后执行 requestPointerLock() 方法
在线和离线事件
navigator.onLine 返回在线 true 或离线 false
online 和 offline 事件
window document document.body 使用 addEventListener
document document.body 的 .ononline 或 .onoffline 属性设为一个 JavaScript Function 对象
<body> 标签上指定 ononline="..." 或 onoffline="..." 属性
设备访问 ：能够处理各种输入和输出设备
Camera API
使用手机的摄像头拍照，然后把拍到的照片发送给当前网页
触摸事件
触摸事件提供了在触摸屏或触控板商解释手指（或触控笔）活动的能力
触摸事件接口可为程序提供多点触控交互的支持，分为开始、移动、结束三个阶段
接口
TouchEvent 接口将当前所有活动的触摸点封装起来
Touch 接口表示单独一个触摸点，其中包括浏览器视角的相对坐标
TouchList 表示一组 Touch，用于多点触控的情况
使用地理位置定位
地理位置 API 允许用户向 Web 应用程序提供他们的位置
出于隐私考虑，报告地理位置和前会先请求用户许可
方法，通过 navigator.geolocation 提供
getCurrentPosition(success[, error[, options]]) 用来获取设备当前位置
watchPosition(success[, error, options]]) 用于注册监听器，在设备的地理位置发生改变的时候自动被调用，返回一个 id
clearWatch(id) 清除注册的位置及错误监听器
检测设备方向
DeviceOrientationEvent 它会在加速度传感器检测到设备在方向上产生变化时触发
DeviceMotionEvent 它会在加速度发生改变时触发
指针锁定 API
光标移到浏览器或者屏幕区域之外，指针锁定也能够让你访问鼠标事件
指针锁定是持久性的。指针锁定不释放鼠标，直到作出一个显式的 API 调用或者用户使用一个专门的释放手势
指针锁定不局限于浏览器或者屏幕边界
指针锁定持续发送事件，而不管鼠标按钮状态如何
指针锁定隐藏光标
指针锁定目前需要先进入全屏模式 requestFullscreen() 然后执行 requestPointerLock() 方法
