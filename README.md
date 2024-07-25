import turtle
import time

# Set up the screen
screen = turtle.Screen()
screen.setup(width=360, height=120)  # 8x2cm in pixels (assuming 40 pixels/cm)
screen.title("I Love You Animation")
screen.bgcolor("black")

# Create a turtle for drawing the heart
heart = turtle.Turtle()
heart.speed(3)
heart.color("red")
heart.pensize(3)

def draw_heart():
    heart.begin_fill()
    heart.left(140)
    heart.forward(80)
    heart.circle(-40, 200)
    heart.left(120)
    heart.circle(-40, 200)
    heart.forward(80)
    heart.end_fill()

# Create a turtle for writing text
text = turtle.Turtle()
text.hideturtle()
text.speed(1)
text.color("white")

def write_message(message, x, y, font_size):
    text.penup()
    text.goto(x, y)
    text.write(message, align="center", font=("Burgues Script", font_size, "normal"))

# Draw the heart
heart.penup()
heart.goto(0, -70)
heart.pendown()
draw_heart()

# Write "I Love You"
write_message("I", -50, 30, 14)
time.sleep(1)
text.clear()
write_message("Love", 0, 30, 14)
time.sleep(1)
text.clear()
write_message("You", 50, 30, 14)

# Additional message
time.sleep(1)
text.clear()
write_message("Let's be together again till the end,", 0, 10, 10)
time.sleep(3)
text.clear()
write_message("I'm sorry for everything", 0, 10, 10)
time.sleep(3)
text.clear()
write_message("and let's just forget",0,10,10)
time.sleep(3)
text.clear()
write_message("everything that happened", 0, 10, 10)
time.sleep(3)
text.clear()
write_message(" and light up a new candle",0,10,10)
time.sleep(3)
text.clear()
write_message("of our love.", 0, 10, 10)
time.sleep(3)
text.clear()
write_message("i really really really",0,10,10)
time.sleep(3)
text.clear()
write_message("love you my AB(my wife)",0,10,10)

# Hide the heart turtle
heart.hideturtle()

# Keep the window open until clicked
screen.exitonclick()
