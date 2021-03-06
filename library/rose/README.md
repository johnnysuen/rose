## 说明文档

### 概述：
 * 初始化流程：store => service => modular
 
### 基础核心层 - 模块modular、服务service、数据store

#### UI 模块 - modular
  * 登记模块方法
  * 运行模块方法
  * 单独模块验证
  * 显示 show 加载界面
  * 主子模块区分
  * 关闭 close 老的场景（判断新模块是否为主模块“isSubModule”，判断是否现在关闭“isHideUnder”）
  * 加载资源（待定。。。需进度条功能）
  * 创建新模块
  * 设置新模块数据 moduleParam 
  * 执行新场景 init 方法
  * 执行新场景 show 方法
  * 关闭 close 老的场景（判断新模块是否为主模块“isSubModule”，判断是否现在关闭“isHideUnder”）
  * 关闭 close 加载界面
  * 加载模块完成，成功执行 resolve

#### 服务 - service - 在复杂业务场景下用于做业务逻辑封装的一个抽象层
 * 使用场景：保持业务逻辑的独立性，抽象出来的 service 可以被多个模块复用，将逻辑和展现分离。
   * 复杂的模块跳转、验证、登录等操作
   * 周期运行的方法，例如全局的倒计时等功能
   * 复杂数据的处理，例如展现的数据从 store 中获取后需要经过一定的计算处理，才能展示。
   * 更新 store 需要一定量的计算才能更新到 store 中。
 * serviceContainer 服务容器，主要存储所有 service 类
 * service 服务基类 

#### 数据 - store
 * 动态数据：redux 形式管理 store 
   * 数据不可变 immutable
 * 静态数据：

------

### 辅助模块

#### 网络处理 net 包
 * http 请求
  * 请求分为有登录状态和无登录
  * get 请求，命名 request
  * post 请求格式有json、FormData，命名 post4Json post4FormData

#### 资源管理
 * 

#### 声音管理
 * 提供管理声音和声音组的功能。

#### 本地化
 * 提供本地化功能，多语言等。

#### 各平台 SDK
 * 封装各个常用平台 SDK 接口
 * 微信
 * 

#### 常用工具方法 -- 推荐使用函数式编程，工具方法属于无状态
 * 行为树
 * 有限状态机，[参考](https://github.com/jakesgordon/javascript-state-machine)
 * 对象池
   * 提供基础对象池功能。
   * 需要对象池功能的对象自己维护一个对象池，根据基础对象池生成自己特定的池子。
 * 常用数据结构
 * 数学工具
 * 图像处理工具

#### 动画特效系统
 * 使用 action 模式

---

### 注意事项：
 * 非常不推荐使用反射机制
 * 处理异步推荐使用 promise 方式

---

### 待解决问题：
 * 封装 eui 按钮自动添加事件
 * 添加 dialog 无皮肤基类
 * 优化模块、ui 界面类的继承
 * 添加 ui 面板管理类
 * 模块系统验证模块是否已经存在，如果存在设置参数，然后调用刷新接口
 * 优化模块加载类和管理
 * 资源管理进一步优化
 * 加入扩展功能 extend
 * 扩展 extend http 请求处理

---

![](./logo.jpg)
