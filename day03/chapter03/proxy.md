# 代理模式

---

> 代理模式是指，为其他对象提供一种代理以控制对这个对象的访问。在某些情况下，一个对象不适合或者不能直接引用另一个对象，而代理对象可以在客户类和目标对象之间起到中介的作用。

使用代理对象，是为了在不修改目标对象的基础上，增强主业务逻辑。

客户类真正的想要访问的对象是目标对象，但客户类真正可以访问的对象是代理对象。客户类对目标对象的访问是通过访问代理对象来实现的。当然，代理类与目标类要实现同一个接口。