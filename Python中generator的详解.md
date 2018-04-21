# python-

generator使用场景：

　　1  当我们需要一个公用的，【按需生成】的数据

　　2  某个事情执行一部分，另一部分在【某个事件发生后再执行下一部分】，实现异步。

注意事项：

    1  yield from generator_obj 本质上类似于 for item in generator_obj: yield item

    2  generator函数中允许使用return，但是return 后不允许有返回值
    
https://www.cnblogs.com/MnCu8261/p/6410594.html

