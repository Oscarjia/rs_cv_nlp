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
参考链接(https://medium.com/@chrieke/jupyter-tips-and-tricks-994fdddb2057)
