用python自带的turtle画出自己的名字，然后移动，同时清屏
# 源代码
    import turtle
    for i in range(20):
        turtle.forward(5*i)
        turtle.right(5*i)
        turtle.clear()
        turtle.write("康杰航",font=("Times",30,"bold"))
