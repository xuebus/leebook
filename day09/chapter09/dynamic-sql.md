# 动态 SQL

---

动态 SQL，主要用于解决查询条件不确定的情况：在程序运行期间，根据用户提交的查询条件进行查询。提交的查询条件不同，执行的 SQL 语句不同。若将每种可能的情况均逐一列出，对所有条件进行排列组合，将会出现大量的 SQL 语句。此时，可使用动态 SQL 来解决这样的问题。

![](/assets/Lusifer1514409215.png)

动态 SQL，即通过 MyBatis 提供的各种标签对条件作出判断以实现动态拼接 SQL 语句。

这里的条件判断使用的表达式为 OGNL 表达式。常用的动态 SQL 标签有`<if>`、`<where>`、`<choose>`、`<foreach>` 等。