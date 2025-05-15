# 介绍
![GitHub License](https://img.shields.io/github/license/LesBoys43/TimeLimitPro?style=plastic) ![GitHub branch status](https://img.shields.io/github/checks-status/LesBoys43/TimeLimitPro/master?style=plastic)
这是一个简单的 Python 任务时间限制工具 可以轻松限制复杂任务的最高用时
# 使用
```python
# 首先，初始化一个 TimeLimit 对象，并传入最高用时（毫秒）
limit = TimeLimit(1000)  # 1 秒
# 然后，使用 with 语句来限制任务的执行时间
with limit:
    time.sleep(1500) # 模拟长时间操作
    try:
        # 在任务中插入一些检查点
        limit.checkpoint()
    except TimeoutError:
        print("任务超时！")
        # 在这里处理超时后的逻辑
    # 在这里编写需要限制时间的代码
```
