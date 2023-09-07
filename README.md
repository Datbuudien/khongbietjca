#include<graphics.h>
#include<conio.h>
#include<string>
#include<math.h>
#define PI 3.14582
#define step 1







void ve(int &x1,int &y1,int &x2,int &y2)
{
		line(x1+31,y1+31,632,31);// ve duong thang noi tu vat den rong roc
    	line(100,625,450,275);//ve canh huyen cua mat phang nghieng
    	line(x1,y1,x2+13,y2+13);//canh ngan o ben phai
    	line(x1-101,y1+99,x2-88,y2+112);//canh ngan o ben trai
    	line(x1-101,y1+99,x2-50,y2-50);//canh dai o tren
    	line(x2+13,y2+13,x2-88,y2+112);// canh dai o duoi
}
void xe(int &pos_Car)
{    //ve theo chieu ngc chieu kim dong ho
	
	line(pos_Car+375,405,pos_Car+375,350);//canh so 1
	line(pos_Car+375,350,pos_Car+475,350);// canh so2
	line(pos_Car+475,350,pos_Car+505,380);//canh so 3
	line (pos_Car+505,380,pos_Car+505,405);// canh so4
	line (pos_Car+505,405,pos_Car+495,405);// canh so 5
	line  (pos_Car+455,405,pos_Car+430,405);// canh so 6
	line (pos_Car+375,405,pos_Car+390,405);// canh so 7
	
	
	
	circle(pos_Car+335+25+25+25,405,20);// ve hinh tron tam (662,50) ban kinh 20
	circle(pos_Car+400+25+25+25,405,20);// ve hinh tron tam (662,50) ban kinh 20
	line(pos_Car+410,350,pos_Car+410,325);//ve cot doc tren o to
	circle(pos_Car+410,325,6);
	line(pos_Car+410,325,662+29,30); // ve day tren oto


    
}
void vanhxe1(int &x1,int &y1,int &x2,int &y2,int &x3,int &y3,int &x,int centerY)
{
		line(x+410,centerY,x1,y1);//ve 3 canh cua vanh xe 
        line(x+410,centerY,x2,y2);//ve 3 canh cua vanh xe
        line(x+410,centerY,x3,y3);//ve 3 canh cua vanh xe
        
        
      
}
void vanhxe2(int &x1,int &y1,int &x2,int &y2,int &x3,int &y3,int &x,int centerY)
{
	line(x+475,centerY,x1,y1) ;
	line(x+475,centerY,x2,y2) ;
	line(x+475,centerY,x3,y3) ;
	
}
void vanhrongroc(int &x1,int &y1,int &x2,int &y2,int &x3,int &y3,int &x4,int &y4)
{
	line(662,50,x1,y1);
	line(662,50,x2,y2);
	line(662,50,x3,y3);
	line(662,50,x4,y4);
	
}




int main()
{ 





	
    // Creating Graphics Window
    DWORD screenwidth=GetSystemMetrics(SM_CXSCREEN);
    DWORD screenHeight=GetSystemMetrics(SM_CYSCREEN);
    int x1=150;
	int y1=450;
	int x2=200;
	int y2=500;
	int k=500;
	int radius=20;// ban kinh vanh xe
	int r=35;// ban kinh rong roc
	double angle = 0;            
    char c;
	int pos_Car=500;
    initwindow(screenwidth,screenHeight, "Cool Programming Projects",-3);
	int x=500,y=400;
	//----------------- trang tri----------------------//
	
	//-------------Thong tin thanh vien nhom----------//
		setcolor(11);
		line(40,35,350,35);
		line(40,35,40,185);
		line(40,185,350,185);
		line(350,185,350,35);
		settextstyle(4,0,1);
		outtextxy(46,40," C++ Project - Group 3");
		settextstyle(3,0,1);
		setcolor(12);
		outtextxy(55,70,"Trinh Quang Lam");
		outtextxy(55,96,"Nguyen Duc Dat");
		outtextxy(55,122,"Luu Minh Hien");
		setcolor(YELLOW);
		outtextxy(55,148,"Topic: Physics experiment");
	//------------------------------------------------//
	
			//------------------ Nut di chuyen ----------------//
			
			 	//-------------- Left -------------------//
			 		setcolor(10);
			 		line(600,675,700,675);
			 		line(600,675,600,725);
			 		line(600,725,700,725);
			 		line(700,725,700,675);
			 		line(625,700,675,700);
			 		line(625,700,635,710);
			 		line(625,700,635,690);
				//---------------------------------------//	 	
			 
			 	//-------------- Right ------------------//
			 		setcolor(10);
			 		line(800,675,900,675);
			 		line(800,675,800,725);
			 		line(800,725,900,725);
			 		line(900,725,900,675);
			 		line(825,700,875,700);
			 		line(875,700,865,690);
			 		line(875,700,865,710);
				//---------------------------------------//
				settextstyle(4,0,1);
				setcolor(YELLOW);
			 	outtextxy(610,750,"Click to move the Car!");
			
			//-------------------------------------------------//
	
	
	//----------Thong so van toc cua vat va xe--------//
	
			setcolor(11);
			rectangle(609,126,709,221);
			settextstyle(1,0,1);
			setcolor(12);
			outtextxy(618,130,"Speed");
			setcolor(WHITE);
			outtextxy(638,190,"m/s");
	
	//-------------------------------------------------------//
	
	
	//-------------------------------------------------//
	setcolor(WHITE);
	
	
	
	
	
	
	int centerX=910,centerY=405;
    int maxX = 1500; // chieu rong man hinh
    int maxY = 850; // chieu cao man hinh
    line(maxX/2,maxY/2,maxX/2,maxY/2+200);// canh ben trai chua o to


    
    
    

    	line(maxX/2, maxY / 2, maxX, maxY / 2);//duong chua o to
    	
    	line(0, maxY / 2+100+100, maxX, maxY / 2+100+100);// duong chua mat phang nghieng
    	
    	/*ve rong roc*/
	    line(662,0,662,50); // ve gia do rong roc
	    
	    circle(662,50,35);// ve hinh tron tam (662,50) ban kinh 35
    	/*------------*/
    
    	/* ve mat phang nghieng */
		line(450,275,450,625);// ve chieu cao cua mat phang nghieng
		line(100,625,450,275);//ve canh huyen cua mat phang nghieng
    	/*----------------------*/
    	setcolor(WHITE);
    /*ve hinh chu nhat */
    	ve(x1,y1,x2,y2);
    	xe(pos_Car);
     delay(0);
    	int x11,y11,x21,y21,x31,y31;
    	int x12,y12,x22,y22,y32,x32;
    	int xr1,yr1,xr2,yr2,xr3,yr3,xr4,yr4;
    while(1)
    {	
   
    	if(x2+13>450) // restart vitri
    	{
    		 x1=150;
			 y1=450;
			 x2=200;
			 y2=500;
			 k=500;
			 
			radius=20;
			 angle = 0;            
		     
			 pos_Car=500;
			  x=500,y=400;
			 centerX=910,centerY=405;
		}
		/* thay doi vi tri cua vanh xe 1 */
    	 x11=x+410+radius*cos(angle);
		 y11=centerY+radius*sin(angle);
		 x21=x+410+radius*cos(angle+2*PI/3);
		 y21=centerY+radius*sin(angle+2*PI/3);
		 x31=x+410+radius*cos(angle+4*PI/3);
		 y31=centerY+radius*sin(angle+4*PI/3);
		 /*******/
		
		
		
		 /* thay doi vi tri cua vanh xe 2*/
		 x12=x+475+radius*cos(angle);         //vi x,y la tam, x12 y12 chi can cho khoang cach bang r thi thuoc duong tron
		 y12=centerY+radius*sin(angle);
		 x22=x+475+radius*cos(angle+2*PI/3);
		 y22=centerY+radius*sin(angle+2*PI/3);
		 x32=x+475+radius*cos(angle+4*PI/3);
		 y32=centerY+radius*sin(angle+4*PI/3);
		 
		 
		 
		 
		 
		  /*****************/
		  
		  
		  
		  /* thay doi vi tri cua vanh rong roc  */
		  
		 xr1=662+r*cos(angle);
		 yr1=50+r*sin(angle);
		 xr2=662+r*cos(angle+PI/2);
		 yr2=50+r*sin(angle+PI/2);
		 xr3=662+r*cos(angle+PI);
		 yr3=50+r*sin(angle+PI);
		 xr4=662+r*cos(angle+3*PI/2); 
		 yr4=50+r*sin(angle+3*PI/2); 
		  
		  
		  
		  /********************/
		 /* vi tri xe o cho moi */
    	setcolor(WHITE);
    	vanhxe1(x11,y11,x21,y21,x31,y31,x,centerY);
    	vanhxe2(x12,y12,x22,y22,x32,y32,x,centerY);
    	vanhrongroc(xr1,yr1,xr2,yr2,xr3,yr3,xr4,yr4);
    	circle(662,50,35);// ve lai hinh tron rong roc
    	ve(x1,y1,x2,y2);
    	xe(pos_Car);
    	delay(1);
    	/***********/
    	/*  xoa vi tri xe o cho cu di */
     	setcolor(BLACK);
     	vanhxe1(x11,y11,x21,y21,x31,y31,x,centerY);
     	vanhxe2(x12,y12,x22,y22,x32,y32,x,centerY);
     	vanhrongroc(xr1,yr1,xr2,yr2,xr3,yr3,xr4,yr4);
     	ve(x1,y1,x2,y2);
     	xe(pos_Car);
     	/************/
	    /* toc do di chuyen cua xe va toc do quay cau vanh xe*/
	     x1+=step;
	     y1-=step;
	     x2+=step;
	     y2-=step;
	     pos_Car+=step;
	     
	     
	     
	     
	     
	     angle+=0.05;
	     /****************/
     	
     	x+=step;
     	
	}



	
	
    
    




    getch();
    closegraph();
    return 0;

}
