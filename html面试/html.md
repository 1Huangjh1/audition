1、src和href的区别
 src：指向外部资源，指向的内容将会嵌套到文档中当前标签所在位置；在请求src资源是会将其指向的资源下载并应用到文档
 当浏览器解析到该元素时，会暂停其他资源的瞎子啊和处理，直到该资源加载、编译、执行完毕，图片和框架等元素也如此，类似于蒋所指向资源嵌入到当前标签内，这也是为什么将js脚本放在底部而不是头部

 href： 指向网络字眼梭子啊位置，简历和当前元素或当前文档之间的连接
<link href="common.css" rel="stylesheet"/>
浏览器会识别该文档为css文件，就会并行下载资源，并且不会停止对档期那文档的处理，这也是为什么建议使用link方式架子啊css而不是使用@import方式

2、html语义化的理解
    语义化是指根据内容结构，选择合适的标签

    语义化的优点：
        对机器友好，带有语义化的文字表现力丰富，更适合搜索引擎的爬虫爬取有效信息，有利于seo
        对开发者友好，使用语义化标签增强了可读性，结构更加清晰，开发者能清晰的看出网页的结构，便于团队的开发与维护

    常见的语义化标签
        <header></header> 头部
        <nav<</nav>  导航栏
        <section></section>  区块，文档的某个区域
        <artical></artical> 主要内容
        <aside></aside>  侧边栏
        <footer></footer> 底部

3、DOCUTYPE 的作用
    目的是告诉浏览器应该使用什么样（html或者xhtml）的文档类型定义来解析文档

    浏览器渲染页面的两种模式（document.compatMode获取）
        css1compat：标准模式
        backcompat：怪异模式，该模式，页面以一种标胶宽松的向后兼容的方式显示

4、script标签中defer和async的区别
    如果没有defer或者async属性，浏览器会料理机加载并执行相应的脚本，他不会等待后续加载的文档元素，读取到就开始加载和执行，这样就组赛了后续文档的加载

    defer和async都是异步加载外部的js脚本文件，他们都不会阻塞页面的解析，区别：
        执行顺序： 多个带async属性大的标签，不能保证加载的舒徐；多个带defer属性的标签，按照加载顺序执行
        脚本是否并行执行： async属性，表述后续文档的加载和执行与js脚本的加载和执行是并行进行的，即有异步执行； defer属性，加载后续问的过程和js脚本的加载（此时仅加载不执行）是并行的（异步),js
        脚本需要等到文档所有元素解析完成之后v爱执行，domcontentLoader时间触发执行之前


5、html5有哪些更新？
    1、语义化标签
        header、article、aside、section、footer、nav
    2、媒体标签
        audio
            control控制面板
            autoplay 自动播放
            loop 循环播放
        video
            poster：指定视频没有下载完毕之前，或者用户没有点击播放之前显示的封面，默认当前视频的第一帧画面
            width、height、autoplay
        source
            因为浏览器对视频格式支持成都不同，为了能够兼容不同的浏览器，可以使用source来指定视频源

    3、表单
    4、进度条、度量条
    5、dom查询
        dociment.querySelector()
        docunent.querySeelectAll()
        他们选择的对象可以是标签、类、id

    web存储
        localStroage - 没有时间夏至的数据存储方式
        sessionStorage -- 针对一个session的数据存储

    6、其他
        拖放、画布、svg、地理定位
    
    移除的元素
        纯表现的元素“ basefont、big、center、font、s、strike、tt、u
        对可用性产生负面影响的元素：frame、frameset、noframes
    

6、对web worker的理解
    web worker是运行在后天的js，独立于其他脚本，不会影响页面的性能，并且通过postMessage将结果回传到主线程

    如何创建web worker
        检测浏览器对应web worker的支持性
        创建web worker问价
        创建web worker对象
    
7、html5的离线存储怎么使用，它的工作原理是什么
    离线存储： 在用户没有联网时，可以正常访问站点或者应用，在联网时，更新缓存文件按


8、title和h1的区别、b和strong的区别、i和em的区别
    strong标签有语义，起到加重语气的效果
    title属性没有明确意只表示标题，h1则标识层次明确的标题，对页面信息的抓取有很大的影响
    i内容展示为斜体，em表示强调文本

9、iframe的优缺点
    优点：
        用来架子啊速度较慢的内容（广告）
        可以使脚本并行下载
        可以实现跨自域通信
    
    缺点：
        阻塞也买你的onLoad事件
        无法被一些搜索引擎识别
        会产生很多页面，不容易管理

10、svg 和 canvas
    svg特点：
        不依赖分辨率
        支持事件处理器
        最适合带有大型渲染区域的应用程序
        复杂度高会减慢渲染速度
        不适合游戏应用
    
    canvas：
        依赖分辨率
        不支持事件处理器
        弱的文本渲染
        能够以png、jpg格式保存图像
        最合适体香密集型游戏，其中的许多u第项会被频繁重绘
    

11、html5 drag API
    dragStart： 事件主体被拖放元素，在开始拖放被拖放元素时触发
    drag： 事件主体是被拖放元素，在正在脱饭被拖放元素时触发
    dragenter： 事件主体时目标元素，在被拖放元素进入某元素时触发
    dragover：事件主体时目标元素，移动目标元素触发
    dragleve： 移出
    drop： 完全接受
    dragend： 拖放结束

    

        


 