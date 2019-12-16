# java集合

## HashSet

​		HashSet 实现 Set 接口，由哈希表（实际上是 HashMap ）实现，但不保证 set  的迭代顺序，并允许使用 null 元素。HashSet 的时间复杂度跟 HashMap 一致，如果没有哈希冲突则时间复杂度为 O(1) ，如果存在哈希冲突则时间复杂度不超过 O(n) 。所以，在日常编码中，可以使用 HashSet 判断主键是否存在。

​		Set 的 add 函数有个特性——如果添加的元素已经再集合中存在，则会返回 false 。