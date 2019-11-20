#### jupyter 重要的使用
##### 1、查看method,用?

Because finding help on an object is so common and useful, IPython introduces the ? character as a shorthand for accessing this documentation and other relevant information:
```python
In [2]: len?
Type:        builtin_function_or_method
String form: <built-in function len>
Namespace:   Python builtin
Docstring:
len(object) -> integer
Return the number of items of a sequence or mapping.
```

##### 2、查看python代码的源码用??

比如随便定义一个python方法，abc,可以查看abc的源码。但是如果该方法是非python写的就无法查看。
```python
In [8]: abc??
```

##### 3、自动补全用tab 按键
```python
In[9]  a[TAB]
In[10] a.[TAB]
In[11] a.co[TAB]
```
##### 4、自动匹配用*
比如我想找一下a类下面的中间包含get字符的方法，可以用如下的方法
In[12] a.*get*?
