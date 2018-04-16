# service-worker-test
test service worker function

---

### service worker
* javascript本身是单线程的, js代码用户层无法创建多线程
* 所有代码都在主线程执行
* 如果要进行非常大的运算, 严重阻碍相关页面的渲染
* 现代前端大规模的运算越来越常见
* 使用service worker, 在后台线程进行相关的大规模数据的运算和获取, 将结果返回到主线程, 由主线程进行渲染
* 避免了主线程被巨大的代码逻辑所阻塞, 大大提升了浏览器在处理大规模运算的性能

---
### PWA
###### 定义
* 不是指一种新技术
* 通过一系列的web特性, 配合优秀的UI交互设计, 逐步增强web app的用户体验
  * 弱网环境下, app的内容能否快速加载出来
  * 离线环境能够加载
  * ...

###### 技术指标
  * 可靠性: 没有网络的环境下能够显示
  * 快速: 针对网页渲染和网络数据访问有比较好的优化
  * 融入: app可以添加到用户桌面, 不依赖浏览器, 有全屏, 推送等特性

###### 工具检测
* lighthouse chrome插件的形式
* generate report
  * progress web app
  * performance
  * accessibility
  * best practice

---
### service worker的特性
* 拦截和处理网络请求的能力, 所有从页面上发送的ajax请求都可以被拦截, 在这个层面就可以做缓存和离线应用了, 以编程的方式管理被缓存的响应
* 可以和主线程之间进行通信, 实现大规模数据的后台处理

---
### service worker的生命周期
