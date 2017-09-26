
# 方法一 turtle
## 用python自带的turtle画出自己的名字，然后移动，同时清屏
* 源代码
```   
   import turtle
    for i in range(20):
        turtle.forward(5*i)
        turtle.right(5*i)
        turtle.clear()
        turtle.write("康杰航",font=("Times",30,"bold"))
```

# 方法二 pygame
* ![效果演示]()
* 源代码
```
import pygame
pygame.init()
size = width, height = 600, 400
speed = [-2,1]
bg = (255,255,255)
screen = pygame.display.set_mode(size)
pygame.display.set_caption("KJH Moves")
car = pygame.image.load("KJH.png")
position = car.get_rect()

while True:
	for event in pygame.event.get():
		if event.type == pygame.QUIT:
			sys.exit()
	position = position.move(speed)
	if position.left<0 or position.right>width:
		speed[0] = -speed[0]
	if position.top<0 or position.bottom>height:
		speed[1] = -speed[1]
	screen.fill(bg)
	screen.blit(car,position)
	pygame.display.flip()
	pygame.time.delay(10)
```    
