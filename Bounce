#LIBRARY
#Screen Resolution Variables (ResolutionX,ResolutionY)
# x and y coordinates are x and y
# Movement along x and y is MoveX and MoveY respectively
# radius = 50


import pygame
pygame.init()
ResolutionX= 1000
ResolutionY= 500
win = pygame.display.set_mode((ResolutionX,ResolutionY))
pygame.display.set_caption('aman')
# Initialiied Pygame & Resolution SET

#variables
x,y  = 100,100 # and y coordinates
MoveX, MoveY = 1,1
velocity = 1
jump= 0

run = True
while run:
    for event in pygame.event.get():
        #print(event)
        if event.type == pygame.QUIT:
            run = False
            pygame.quit()
            quit()
    win.fill((255,0,0))
    pygame.draw.circle(win, (0,0,0), (x,y),50) #radius = 50

    # x+=MoveX
    # y+=MoveY

    keys = pygame.key.get_pressed()
    if keys[pygame.K_RIGHT] and x < ResolutionX - 50:
        x += velocity
    elif keys[pygame.K_LEFT] and x > 50:
        x -= velocity

    #Jump
    if keys[pygame.K_SPACE] and y == ResolutionY -50:
        jump = 300
    if jump > 0:
        y -= velocity
        jump -= velocity
    elif y < ResolutionY - 50:
        y += velocity

    pygame.display.update()
