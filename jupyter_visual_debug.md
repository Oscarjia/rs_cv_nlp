## jupyter 不能图形化debug 这点很烦人。
#### 介绍一个PixieDebugger工具，可以图形化。
使用方法：
```
pip install pixiedust
安装好后，可以在相应的方法里面引入
-------------------------------------
import pixiedust
-------------------------------------
%%pixie_debugger or %%pixie_debugger -b method name ##但是%%pixe_debugger 必需在单元格的最前方。注释之类的不可以在最前方。
def search(start,end,linedata,transferinfo):
   pass
----------正确的写法-----------------
%%pixie_debugger
def test():
      pass
test()
-----------------------------

----------错误的写法-----------------
##comment
%%pixie_debugger
def test():
      pass
test()
-----------------------------
```
另外一个很有用的功能是当错误发生的时候，仍然可以调用debugger,要少一个%分号。
重新启动一个cell
```
%pixie_debugger
```
![](https://miro.medium.com/max/1840/1*neCV-jBrj28sD8yad3qE0w.png)
Invoking the PixieDebugger post-mortem (after an exception has happened) is also possible with the line magic %pixie_debugger. (Notice the difference between the cell magic, which has two % symbols, and the line magic, which has only one and no argument.) This is useful to troubleshoot hard-to-reproduce errors.
参考链接(https://medium.com/@chrieke/jupyter-tips-and-tricks-994fdddb2057)
