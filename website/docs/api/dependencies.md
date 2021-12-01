# NoneBot.handler 模块

## 依赖注入处理模块

该模块实现了依赖注入的定义与处理。


## `Depends(dependency=None, *, use_cache=True)`


* **说明**

    参数依赖注入装饰器



* **参数**

    
    * `dependency: Optional[Callable[..., Any]] = None`: 依赖函数。默认为参数的类型注释。


    * `use_cache: bool = True`: 是否使用缓存。默认为 `True`。


```python
def depend_func() -> Any:
    return ...

def depend_gen_func():
    try:
        yield ...
    finally:
        ...

async def handler(param_name: Any = Depends(depend_func), gen: Any = Depends(depend_gen_func)):
    ...
```