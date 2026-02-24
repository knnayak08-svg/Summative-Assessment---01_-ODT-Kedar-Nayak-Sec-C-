# Summative-Assessment---01_-ODT-Kedar-Nayak-Sec-C-
The First Summative Assessment for Open Design and Technology
Work-in-Progress Pictures: file:///C:/Users/Kedar%20Nayak/Downloads/Workinprogress_ODT.pdf
Presentation: file:///C:/Users/Kedar%20Nayak/Downloads/ODT%20PRESENTATION%20FINAL.pdf
YouTube Video Link: https://youtube.com/shorts/b4FsV_x7oaU?feature=share
Code: 
from machine import PWM, Pin
import time
import neopixel
import random

n=neopixel.NeoPixel(Pin(21),16)
b=Pin(18, Pin.OUT)
pb=Pin(19,Pin.IN,Pin.PULL_UP)

while True:
    pb_val=pb.value()
    for r in range(0,16,1):
        r=random.randint(0,15)
        n[r]=(225,4,0)
        n.write()
        time.sleep(0.05)
        n[r]=(0,0,0)
        if pb_val==0:
            if r==8:
                b.value(1)
                time.sleep(0.05)
                b.value(0)
                print("Success!")
                break
            elif r!=8:
                b.value(1)
                print("Better Luck Next Time!")
                time.sleep(0.05)
                break
        time.sleep(0.05)

Code .py file: "C:\Users\Kedar Nayak\Downloads\ODT_Assignment.py"
