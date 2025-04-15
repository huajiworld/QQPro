### QQPro
基于NWear-QQ最终版2（这个版本的qq是爅峫手改smali实现，所以无法开源）

https://www.123865.com/s/jzH1jv-w9Gwh?notoken=1

https://bke.lanzoub.com/iq6QW2spsowf

☆☆地表最强表Q改版 震撼推出☆☆

### 关于ApkMixin工具
```
@Mixin
class ExampleHook : TargetClass() { ... }
```
会将`ExampleHook`类内所有`override`的方法的方法体替换到hook的`TargetClass`内，使用`super.fun(...)`可以调用类内原有的方法
你可以在src内的其他任意地方把任意`TargetClass`对象**强转**为`ExampleHook`并调用`ExampleHook`类内定义的其他方法或是字段。非`override`的方法和字段会被复制进hook后的TargetClass内。但是要注意目前**不支持构造函数Hook**，这意味着**添加字段不能有初始值**

我不建议在Hook类内添加过多的东西，建议仅添加必要的代码。

静态方法Hook使用：
```
@Mixin
object ExampleStatic : TargetClass() {
  @StaticHook
  @JvmStatic
  fun targetMethod_(...) {...}
}
```
要点：定义为`object`类，方法带上`JvmStatic`注解，方法名后添加**一个下划线**（否则重复声明无法通过编译）

### 更新日志
- v1.2 2025/04.12
  回复消息定位
  修复回复显示bug
  消息长按菜单背景透明
  聊天记录图片加载失败提示
  移除超级表情放大动画
  调整气泡文本大小和边距
  圆屏查看图片时添加边距 
  新设置：气泡文本缩放
  新设置：平滑表冠滚动（by dudu）

- v1.1 2025/04/06
  添加页面缩放设置
  尝试修复回复显示的bug但是没修好

- v1.0 2025/04/05
  现在可以查看转发的聊天记录
  现在可以看见引用消息的发送者昵称
  表冠滚动适配
  修复了回复带图看不见的问题
  限制了表情包的最大大小（unstable）
  页面缩放至90%
