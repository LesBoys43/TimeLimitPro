# Introduction  
![GitHub License](https://img.shields.io/github/license/LesBoys43/TimeLimitPro?style=plastic) ![GitHub branch status](https://img.shields.io/github/checks-status/LesBoys43/TimeLimitPro/master?style=plastic)  

This is a simple Python task time-limiting tool that can easily enforce a maximum time limit for complex tasks.  

# Usage  
```python  
# First, initialize a TimeLimit object with the maximum time limit (in milliseconds)  
limit = TimeLimit(1000)  # 1 second  
# Then, use a with statement to constrain task execution time  
with limit:  
    time.sleep(1500) # Simulate a long operation  
    try:  
        # Insert checkpoints within the task  
        limit.checkpoint()  
    except TimeoutError:  
        print("Task timed out!")  
        # Handle post-timeout logic here  
    # Write time-constrained code here  
```
