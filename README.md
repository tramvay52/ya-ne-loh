# ya-ne-loh
#lol pididi in prison im f**** his mother
from pygame import *
from random import randint
from time import time as timer  
import sys 
WIDTH, HEIGHT = 600,800
display.set_caption("чувырла")
window = display.set_mode((WIDTH, HEIGHT))


racket1 = Player("коты.jpg", 30, 200, 4, 50, 150)
racket2 = Player("коты.jpg", 520, 200, 4, 50, 150)
ball = GameSprite("шар.lpg",200, 200, 4, 50, 50)

font.init()
font = font.Font(None,35)
lose1 = font.render('PLAYER 1 LOHHHH!!!!!!!!!!!!!!!', True, (180,0,0))
lose2 = font.render('PLAYER 2 LOHHHH!!!!!!!!!!!!!!!', True, (180,0,0))

speed_x = 3
speed_y = 3






class Player(GameSprite):
  def update_r(self):
    keys = key.get_pressed()
    if keys[K_UP] and self.rect.y > 5:
      self.rect.y -= self.speed
    if keys[K_DOWN] and self.rect.y < win_height -  80:
      self.rect.y += self.speed
  def update_1(self):
    keys = key.get_pressed()
    if keys[K_w] and self.rect.y > 5:
      self.rect.y -= self.speed
    if keys[K_s] and self.rect.y < win_height -80:


while True:
    for e in event.get():
      if e.type == QUIT:
        raise SystemExit("QUIT")
    if finish != True:
      ball.rect.x = speed_x
      ball.rect.y = speed_y
    if ball.rect.y > win_height-50 or ball.rect.y < 0:
      speed_y *= -1
    if sprite.collide_rect(racket1, ball) or sprite.collide_rect(racket2, ball):
      speed_x *= -1 
    if ball.rect.x < 0:
      finish = True
      window.blit(lose1, (200, 200))
    if ball.rect.x > 600 :
      finish = True
      window.blit(lose2, (200, 200))





    display.update()
