# CG Sem-3 Mini Project
## Analog clock animation

•This is our basic analog clock using COS, SIN,
THETA, and the form's aspect ratio to draw the
circles and gather the placement of the markers and
hands.

•This project shows an animation of an analog clock which
shows the system time

### Functions used along with syntax
•initwindow(int width,int height,const char* title)

•setcolor(color)

•outtextxy(int x,int y, char *string)

•setactivepage(int page)

•setvisualpage(int page)

•time(int time in seconds)

•localtime(time-t *timer)

•delay(int time in seconds)

•closegraph()


### About Code

•initwindow (500, 500, "ANALOG CLOCK") makes a window of height and width of 5oopx with the window title as "ANALOG CLOCK"

•circle (250, 250, 200) will create a circle with centre(250,250) and radius of 200 

•circle (250, 250, 5) will create a small dial at the centre


<img width="575" alt="2023-01-12 (12)" src="https://user-images.githubusercontent.com/111975032/212147999-06fc6e56-4c88-45fc-b4a8-01bbb7f147a1.png">

The distance between each number is 30°

Co-ordinates of print C = (250+ BC, 250-AB)

Define π as 3.1415, make sure to include math class


•outtextxy (250 + 180 * sin(π/6), 250-180 *cos(π/6),"1")

This function will print "1" at the above mentioned x and у co-ordinates

Similarly, print all other numbers with a gap of π/6 between every two numbers.

To get system time, include ctime or time.h library

time_t now= time (0)

where time_t is a structure
and time() is a method

To bring the time in readable format,

tm *ltm=localtime(&now)

This time is in а 24 hour format and is stored in a readable format in ltm


ltm->tm_hour  //gets hours

ltm->tm_min  //gets minutes

ltm->tm_sec  //gets seconds


Finally,use double buffering to avoid flickering of the hands of the
clock using setactivepage() and setvisualpage()

### Output
<img width="616" alt="2023-01-12 (11)" src="https://user-images.githubusercontent.com/111975032/212131185-092ca8b0-c80f-4991-a8e9-a64680c09645.png">


### Authors
- [@SiddhantKodolkar](https://www.github.com/SiddhantKodolkar)
- [@Divesh Mangtani](https://www.github.com/Divesh-Mangtani)

