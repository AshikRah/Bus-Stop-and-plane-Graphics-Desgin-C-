# Bus-Stop-and-plane-Graphics-Desgin-C-
#include<iostream>
#include<graphics.h>
#include<stdlib.h>

int main()
{
    int a=DETECT;
    int b,i=0,j=1;
    initgraph(&a,&b,"C:\\TC\\BGI");



    for(i=0;i<=700;i++)
    {

        circle(40+i,390,10);
        circle(80+i,390,10);                //Bus
        rectangle(10+i,340,110+i,380);

        rectangle(10+i,345,40+i,365);
        rectangle(40+i,345,70+i,365);           //Bus window
        rectangle(70+i,345,100+i,365);
        rectangle(100+i,345,110+i,365);
        outtextxy(30+i,368,"City Bus");

        if(i>420)
        {
            circle(25+i,355,7);                   //Passenger1 inside bus
            line(25+i,362,25+i,365);

            circle(55+i,355,7);                   //Passenger2 inside bus
            line(55+i,362,55+i,365);

            circle(85+i,355,7);                   //Passenger3 inside bus
            line(85+i,362,85+i,365);
        }


        if(i<425)
        {
            circle(530,360,7);
            line(530,367,530,382);
            line(530,369,525,377);              //Passenger1 in bus stop
            line(530,369,535,377);
            line(530,382,525,400);
            line(530,382,535,400);

            circle(500,360,7);
            line(500,367,500,382);
            line(500,369,495,377);              //Passenger2 in bus stop
            line(500,369,505,377);
            line(500,382,495,400);
            line(500,382,505,400);

            circle(470,360,7);
            line(470,367,470,382);
            line(470,369,465,377);              //Passenger3 in bus stop
            line(470,369,475,377);
            line(470,382,465,400);
            line(470,382,475,400);
        }

        if(i==420)
        {
                delay(5000);                    //Bus delay for 10 second
        }
        delay(10);
        cleardevice();

        line(1,400,639,400);

        rectangle(550,300,555,400);
        rectangle(500,250,600,300);
        outtextxy(520,270,"Bus Stop");

        circle(100,100,30);
        line(30,100,70,100);
        line(100,30,100,70);                //Sun
        line(130,100,170,100);
        line(100,130,100,170);


        rectangle(200,100,300,150);
        rectangle(220,120,320,170);         //Cloud
        rectangle(150,70,250,110);

        setcolor(j);
        setfillstyle(SOLID_FILL,j);
        line(400-i*2,50,450-i*2,50);
        line(380-i*2,70,400-i*2,50);
        line(380-i*2,70,400-i*2,90);
        line(400-i*2,90,450-i*2,90);
        line(450-i*2,50,450-i*2,10);
        line(450-i*2,10,470-i*2,10);
        line(470-i*2,10,470-i*2,50);         //Plane
        line(470-i*2,50,550-i*2,50);
        line(550-i*2,50,570-i*2,30);
        line(570-i*2,30,570-i*2,110);
        line(570-i*2,110,550-i*2,90);
        line(550-i*2,90,470-i*2,90);
        line(470-i*2,90,470-i*2,130);
        line(470-i*2,130,450-i*2,130);
        line(450-i*2,90,450-i*2,130);
        floodfill(455-i*2,55,j);
        j++;
        if(j==16)
        {
            j=1;
        }

   }
    getch();
    closegraph();
}
