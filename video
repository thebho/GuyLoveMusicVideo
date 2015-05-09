import pygame
import random
from pygame import gfxdraw
 
# Define some colors
BLACK    = (   0,   0,   0)
WHITE    = ( 255, 255, 255)
GREEN    = (   0, 255,   0)
RED      = ( 255,   0,   0)
TEAL     = (   0, 212, 187)
BLUE     = (   0,   0, 255)
LTBLUE   = ( 207, 252, 248)
LTBLUE2  = ( 116, 176, 165)
SKYBLUE  = ( 145, 240, 255)
CHOC     = ( 189, 119,  70)
BROWN    = ( 120,  75,  43)
VANILLA  = ( 255, 227, 191)
PURPLE   = ( 191,   0, 255)
ORANGE   = ( 255, 255,   0)
SILVER   = ( 153, 153, 153)
BACKGROUND=( 219, 204, 191)
BEDFRAME = ( 186, 153, 127)
DOORSHADOW=(  96,  96, 214)

PI       = 3.141592653
COLOR_LIST=[RED,BLUE,GREEN,TEAL,PURPLE,ORANGE]

guyFont='americantypewriter'
guySize=25

#Base Print Functin
def basicText(lyrics,x,y,color):
    font = pygame.font.SysFont(guyFont, guySize, False, False)
    text = font.render(lyrics,True,color)
    screen.blit(text, [x, y])

def bigText(lyrics,x,y,color,rectColor):
    pygame.draw.rect(screen,rectColor,[150,10,400,90])
    font = pygame.font.SysFont(guyFont, 75, False, False)
    text = font.render(lyrics,True,color)
    screen.blit(text, [x, y])


 
pygame.init()
 
# Set the width and height of the screen [width, height]
size = (700, 450)
screen = pygame.display.set_mode(size)
 
pygame.display.set_caption("Guy Love")
 
# Loop until the user clicks the close button.
done = False
frameCount=00
 
# Used to manage how fast the screen updates
clock = pygame.time.Clock()

# Setting starting points for Turk and JD
turkX=700
jdX=1100
turk_move=0
jd_move=0

# Drawing set up
animate=True
if animate==False:
    turkX=200
    jdX=400
    frameCount=1000

# -------- Main Program Loop -----------
while not done:
    # --- Main event loop
    for event in pygame.event.get(): # User did something
        if event.type == pygame.QUIT: # If user clicked close
            done = True # Flag that we are done so we exit this loop
    if animate==True: frameCount+=1

    screen.fill(LTBLUE2)

    # Draws back wall and door
    pygame.draw.rect(screen,BACKGROUND,[0,0,700,340])
    pygame.draw.rect(screen,WHITE,[275,100,150,240])
    pygame.draw.rect(screen,DOORSHADOW,[280,105,140,235])
    pygame.draw.rect(screen,WHITE,[420,100,100,240])
    pygame.draw.rect(screen,BACKGROUND,[430,120,80,80])

    backgroundSurface=pygame.Surface((700,340))
    backgroundSurface.set_alpha(180)
    backgroundSurface.fill(BLACK)
    screen.blit(backgroundSurface,(0,0,))

    # Horizontal movement commands by frameCount
    if frameCount<=50:
        turk_move=-8
        jd_move=-7
    elif frameCount<=110:
        turk_move=0
        jd_move=-5
    elif frameCount>305 and frameCount<350:
        turk_move=-3
    elif frameCount>650 and frameCount<720:
        turk_move=1
        jd_move=-1
    elif frameCount>900 and frameCount<950:
        turk_move=-1
    elif frameCount>950 and frameCount<1000:
        jd_move=1
    elif frameCount>1160 and frameCount<1205:
        turk_move=1
    elif frameCount>1270 and frameCount<1335:
        jd_move=-1
    elif frameCount>1700 and frameCount<1760:
        jd_move=1
    elif frameCount>1750 and frameCount<1810:
        turk_move=-1
    elif frameCount>2010 and frameCount<2080:
        turk_move=1
        jd_move=-1
    else:
        turk_move=0
        jd_move=0
    turkX+=turk_move
    jdX+=jd_move

    # Text commands by fameCount
    if 70<=frameCount<120:
        basicText("Let's face the facts",400,50,WHITE)
        if frameCount>90:
            basicText("about me and you",450,80,WHITE)

    if 120<=frameCount<160:
        basicText("a love unspecified",400,50,WHITE)

    if 160<=frameCount<235:
        basicText("though I'm proud",400,50,WHITE)
        if frameCount>185:
            basicText("to call you",450,80,WHITE)
        if frameCount>205:
            basicText("Chocolate Bear!",480,110,WHITE)
            
    if 235<=frameCount<305:
        basicText("the crowd will always",400,50,WHITE)
        if frameCount>265:
            basicText("stop and stare",450,80,WHITE)
            
    if 305<=frameCount<390:
        basicText("I feel exactly",100,50,WHITE)
        if frameCount>340:
            basicText("those feelings too",150,80,WHITE)
            
    if 390<=frameCount<440:
        basicText("and that's why I keep them inside",100,50,WHITE)
        
    if 440<=frameCount<540:
        basicText("Cause this bear",100,50,WHITE)
        if frameCount>470:
            basicText("can't bear the world's disdane",150,80,WHITE)
            
    if 540<=frameCount<610:
        basicText("and sometimes it's easier to hide",100,50,WHITE)

    if 610<=frameCount<640:
        basicText("than explain our",80,80,WHITE)
        basicText("than explain our",400,80,WHITE)

    if 640<=frameCount<740:
        bigText("GUY LOVE",160,16,WHITE,BLUE)
        if frameCount>690:
            basicText("that's all it is",260,100,WHITE)
            
    if 740<=frameCount<820:
        bigText("GUY LOVE",160,16,WHITE,PURPLE)
        if frameCount>760:
            basicText("He's mine",350,110,WHITE)
        if frameCount>780:
            basicText("I'm his",240,110,WHITE)
            
    if 820<=frameCount<900:
        basicText("There's nothing gay about it",100,30,WHITE)
        if frameCount>860:
            basicText("in our eyes...",350,70,WHITE)
            
    if 900<=frameCount<1020:
        basicText("You ask me bout this thing we share...",20,30,WHITE)
        if frameCount>950:
            basicText("and he tenderly replies...",380,80,WHITE)

    if 1020<=frameCount<1070:
        basicText("It's Guy Love!",120,80,WHITE)

    if 1070<=frameCount<1160:
        basicText("between two guys...",80,80,WHITE)
        basicText("between two guys...",400,80,WHITE)

    if 1170<=frameCount<1270:
        basicText("we're closer than the average",80,50,WHITE)
        if frameCount>1210:
            basicText("man and wife",130,80,WHITE)

    if 1270<=frameCount<1370:
        basicText("thats why our matching bracelets say",180,50,WHITE)
        if frameCount>1300:
            basicText("Turk and JD",300,80,WHITE)

    if 1370<=frameCount<1480:
        basicText("you know I'll stick by you",80,50,WHITE)
        if frameCount>1420:
            basicText("for the rest of my life",130,80,WHITE)

    if 1480<=frameCount<1580:
        basicText("you're the only man",360,50,WHITE)
        if frameCount>1520:
            basicText("who's ever been inside of me",320,80,WHITE)

    if 1590<=frameCount<1680:
        basicText("whoa...,whoa...",120,50,WHITE)
        if frameCount>1620:
            basicText("I just took out his appendix",90,80,WHITE)

    if 1700<=frameCount<1760:
        basicText("There's no need to clarify",300,50,WHITE)

    if 1750<=frameCount<1780:
        basicText("oh, no?",180,50,WHITE)

    if 1780<=frameCount<1860:
        basicText("Just let it grow",360,50,WHITE)
        if frameCount>1800:
            basicText("more and more each day",320,80,WHITE)

    if 1860<=frameCount<1950:
        basicText("It's like I married my best friend",290,50,WHITE)

    if 1950<=frameCount<2000:
        basicText("But in a TOTALLY MANLY WAY!",80,50,WHITE)

    if 2000<=frameCount<2040:
        basicText("Let's GO!",150,80,WHITE)
        basicText("Let's GO!",380,80,WHITE)

    if 2040<=frameCount<2200:
        bigText("GUY LOVE",160,16,WHITE,BLUE)

    if 2080<=frameCount<2120:
            basicText("don't compromise",260,110,WHITE)

    if 2120<=frameCount<2160:
            basicText("the feeling of",260,110,WHITE)

    if 2160<=frameCount<2200:
            basicText("some other guy",260,110,WHITE)
               
    if 2200<=frameCount<2300:
        basicText("Holding up your heart",180,40,WHITE)
        if frameCount>2250:
            basicText("into the sky...",350,70,WHITE)
    

    # Drawing figures
    # Draw Turk
    pygame.draw.rect(screen,TEAL,[turkX,200,80,110])
    pygame.gfxdraw.filled_polygon(screen,[[turkX+31,200],[turkX+49,200],[turkX+40,220]],CHOC)
    # Arms
    pygame.draw.rect(screen,TEAL,[turkX-22,200,22,40])
    pygame.draw.rect(screen,TEAL,[turkX+80,200,22,40])
    pygame.draw.rect(screen,CHOC,[turkX-22,240,20,50])
    pygame.draw.rect(screen,CHOC,[turkX+82,240,20,50])
    # Hands
    pygame.draw.ellipse(screen,CHOC,[turkX-22,280,20,25])
    pygame.draw.ellipse(screen,CHOC,[turkX+82,280,20,25])
    # Legs
    pygame.draw.rect(screen,TEAL,[turkX,290,35,90])
    pygame.draw.rect(screen,TEAL,[turkX+45,290,35,90])
    # Shoes
    pygame.draw.ellipse(screen,BLUE,[turkX,370,35,20])
    pygame.draw.ellipse(screen,BLUE,[turkX+45,370,35,20])
    # ID
    pygame.draw.rect(screen,WHITE,[turkX+55,230,10,8])
    pygame.draw.rect(screen,RED,[turkX+55,230,10,3])

    # Head
    pygame.draw.ellipse(screen,CHOC,[turkX+22,148,40,50])
    # Neck
    pygame.draw.rect(screen,CHOC,[turkX+33,190,17,10])
    # Clipboard
    if frameCount>50:
        pygame.draw.rect(screen,SILVER,[turkX-25,280,30,48])
        pygame.draw.rect(screen,WHITE,[turkX-23,288,26,37])
    else:
        pygame.draw.rect(screen,SILVER,[276,282,30,48])
        pygame.draw.rect(screen,WHITE,[278,290,26,37])

    # Draw JD
    pygame.draw.rect(screen,BLUE,[jdX,200,80,110])
    pygame.gfxdraw.filled_polygon(screen,[[jdX+31,200],[jdX+49,200],[jdX+40,220]],SKYBLUE)
    # Arms
    pygame.draw.rect(screen,BLUE,[jdX-22,200,22,40])
    pygame.draw.rect(screen,BLUE,[jdX+80,200,22,40])
    pygame.draw.rect(screen,SKYBLUE,[jdX-22,240,20,50])
    pygame.draw.rect(screen,SKYBLUE,[jdX+82,240,20,50])
    # Hands
    pygame.draw.ellipse(screen,VANILLA,[jdX-22,280,20,25])
    pygame.draw.ellipse(screen,VANILLA,[jdX+82,280,20,25])
    # Legs
    pygame.draw.rect(screen,BLUE,[jdX,290,35,90])
    pygame.draw.rect(screen,BLUE,[jdX+45,290,35,90])
    # Shoes
    pygame.draw.ellipse(screen,RED,[jdX,370,35,20])
    pygame.draw.ellipse(screen,RED,[jdX+45,370,35,20])
    # ID
    pygame.draw.rect(screen,WHITE,[jdX+55,230,10,8])
    pygame.draw.rect(screen,RED,[jdX+55,230,10,3])
    # Hair
    pygame.draw.ellipse(screen,BROWN,[jdX+21,141,42,53])
    # Head
    pygame.draw.ellipse(screen,VANILLA,[jdX+22,148,40,50])
    # Neck
    pygame.draw.rect(screen,VANILLA,[jdX+33,190,17,10])
    # Stethoscope
    pygame.draw.arc(screen, BLACK, [jdX+21,198,30,70],PI/1.75,PI,2)
    pygame.draw.arc(screen, BLACK, [jdX+24,198,40,60],0,PI/2.54,2)
    pygame.draw.arc(screen, BLACK, [jdX+24,200,50,55],0,PI/2.34,2)

    # Draw bed
    pygame.draw.rect(screen,BEDFRAME,[200,290,300,210])
    pygame.draw.rect(screen,LTBLUE,[210,380,280,120])
    
    pygame.display.flip()  #Updates screen
 
    # --- Limit to 60 frames per second
    clock.tick(50)
 
# Close the window and quit.
# If you forget this line, the program will 'hang'
# on exit if running from IDLE.
pygame.quit()
