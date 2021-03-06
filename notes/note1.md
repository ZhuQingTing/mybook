> https://mp.weixin.qq.com/s?__biz=MjM5ODYxMDA5OQ==&mid=2651961720&idx=1&sn=94d1e2b253b715368e6424ec37cd3a1a&chksm=bd2d0ca48a5a85b21d9e7a7e54d69734d8d845ed085393246f2732f9154a145b8a71b6feecac&scene=21#wechat_redirect
>
> 痛点： 代码到处拷贝，复杂性扩散
>
> **库的复用与耦合**
>
> 服务化并不是唯一的解决上述两痛点的方法，抽象出统一的“库”是最先容易想到的解决（1）代码拷贝；（2）复杂性扩散；的方法。
>
> 
>
> 抽象出一个user.so，负责整个用户数据的存取，从而避免代码的拷贝。至于复杂性，也只有user.so这一个地方需要关注了。
>
>  
>
> 解决了旧的问题，会引入新的问题，库的版本维护会导致业务线之间的耦合。
>
> 
>
> 业务线A将user.so由版本1升级至版本2，如果不兼容业务线B的代码，会导致B业务出现问题。
>
> 
>
> 业务线A如果通知了业务线B升级，则是的业务线B会无故做一些“自身业务无关”的升级，非常郁闷。当然，如果各个业务线都是拷贝了一份代码则不存在这个问题。
>
> *画外音：有时候拷贝代码也是有好处的。*