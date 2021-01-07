# ocean-navigation-system-in-C-

#include<iostream>
#include<conio.h>
using namespace std;
class Angle
{ 
  private:
  	int degree;
	float minutes;
	char direction;
   public:
   	
      Angle(int d,float m,char r): degree(d),minutes (m),direction (r){}
  void setdata()
  {
  	cout<<degree<<"\xF8"<<minutes<<"'"<<direction;
  }
     void obtain()
	   {
	   	cout<<"\n Enter an Angle in Degree  ";
	   	cin>>degree;
	   	cout<<"\n Enter Minutes ";
	   	cin>>minutes;
	   	if (minutes>60)
	   	{
	   		minutes=minutes-60;
	   		degree=degree+1;
		   }
	   	cout<< "\n Enter Direction As N,E,W,S : " ;
	   	cin>>direction;
	   	
		} 
		void display()
		{
			cout<<"\n The angel Value is "<<degree<<"\xF8"<<minutes<<"'" <<direction;
		if(direction=='E'||direction=='W')
		{
		cout<<"\n \n You Are in Longitude \n ";
		}
		else
		{
		  cout<<" \n \n You Are in Latitude \n ";
		}
	 }
  };
		
  int main( )
{
int option;
cout<< "Initial Values are : ";
Angle a1(35,20.2,'w');
a1.setdata();

while(1)
{	cout<<"\n Press 1 for input Values and 2 for Exit : ";
	cin>>option;
	switch(option)
     {
	     case 1:
	     
     	  a1.obtain();
	 	  a1.display();
	 	  break;
         
	    case 2:
     	     exit(0);	
     	    
     }
}
return 0;
}

