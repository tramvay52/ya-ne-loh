# ya-ne-loh
#lol pididi in prison im f**** his mother
from pygame import *
from random import randint
from time import time as timer  
import sys 
WIDTH, HEIGHT = 600,800
display.set_caption("чувырла")
window = display.set_mode((WIDTH, HEIGHT))

while True:
    for e in event.get():
      if e.type == QUIT:
        raise SystemExit("QUIT")


    WHITE = (255, 255, 255)
    BLACK = (0, 0, 0)


    PADDLE_WIDTH, PADDLE_HEIGHT = 10, 100
    PADDLE_SPEED = 7


    BALL_SIZE = 20
    BALL_SPEED_X = 5
    BALL_SPEED_Y = 5


    font = font.SysFont("Arial", 30)


    left_paddle = Rect(10, HEIGHT//2 - PADDLE_HEIGHT//2, PADDLE_WIDTH, PADDLE_HEIGHT)
    right_paddle = Rect(WIDTH - 20, HEIGHT//2 - PADDLE_HEIGHT//2, PADDLE_WIDTH, PADDLE_HEIGHT)


    ball = Rect(WIDTH//2 - BALL_SIZE//2, HEIGHT//2 - BALL_SIZE//2, BALL_SIZE, BALL_SIZE)
    ball_speed_x = BALL_SPEED_X
    ball_speed_y = BALL_SPEED_Y

    score_left = 0
    score_right = 0

    display.update()
