实现原理
/*******
   拖拽原理：
   拖拽状态 = 0 
   鼠标在元素上按下的时候 {
      拖拽状态 = 1
      记录下鼠标的x和y坐标
      记录下元素的x和y坐标
      元素的偏移值X=元素的X-元素的offsetLeft
      元素的偏移值Y=元素的Y-元素的offsetTop
   }
   鼠标在元素上移动的时候 {
      如果拖拽状态是0就什么也不做。
      如果拖拽状态是1， 那么
      元素y = 现在鼠标y -元素的偏移值X
      元素x = 现在鼠标x -元素的偏移值Y
   }
   鼠标在任何时候放开的时候 {
      拖拽状态 = 0
   }
   将以上思路翻译成JS代码就可以实现拖拽的效果了。
*******/