#include<conio.h>
#include<stdio.h>


// FUNCTION TO CHECK LEAP YEAR
void leapyear()
{
 int year;
 printf("****YOU SELECTED 2 CHOICE**** ");
 printf("\n\nEnter a year\n\t\t\t");
 scanf("%d", &year);
   if ( year%400 == 0)
     printf("%d is a leap year.\n", year);
   else if ( year%100 == 0)
     printf("%d is not a leap year.\n", year);
   else if ( year%4 == 0 )
     printf("%d is a leap year.\n", year);
   else
     printf("%d is not a leap year.\n", year);
}



int day(int m1,int y1)  // FUNCTION TO FIND NO OF DAYS
{
  int d;
  if(m1==1 || m1==3 || m1==5 || m1==7 || m1==8 || m1==10 || m1==12)
 d=31;
  else if(m1==4 || m1==6 || m1==9 || m1==11)
 d=30;
  else if((y1%100!=0 && y1%4==0) || y1%400==0)
 d=29;
  else
 d=28;
  return d;
}




// TO SHOW CALENDAR
void showcalendar()
{
  int t;
  int y,y1,m,m1,d,da,i,j,k;
     char a[12][20]={"January","February","March","April","May","June","July","August","September","October","November","December"};

  printf("****YOU SELECTED 1 CHOICE****");
      printf("\n\nEnter the year: ");
      scanf("%d",&y);
      if(y<0)
 y=-y;
       printf("\n\nEnter the month(NUMERIC): ");
       scanf("%d",&m);
       if(m<=0 || m>=13)
       {
        printf("month cant exceed 12 so by default jan is taken\\n");
         m=1;
       }
       printf("Calendar\n");
        y1=0;
        t=0;
        while(y1<y)
  {
 if((y1%100!=0 && y1%4==0) || y1%400==0)
   t=t+366;
 else
   t=t+365;
 y1++;
  }
  m1=1;
  while(m1<m)
  {
 d=day(m1,y);
 t=t+d;
 m1++;
  }
  d=t%7;
  printf("\nYear: '%u'",y);
  printf("\nMonth: '%s'",a[m-1]);
  printf("\n\n");
  printf("%6s%6s%6s%6s%6s%6s%6s","Sun","Mon","Tue","Wed","Thu","Fri","Sat");
  printf("\n");
  k=1;
  for(i=1;i<=day(m,y);i++,k++)
  {
 if(i==1)
 {
   if(d==0)
   {
     for(j=1;j<7;j++,k++)
       printf("%6s","");
   }
   else
   {
      for(j=1;j<d;j++,k++)
   printf("%6s","");
           }
         }
 printf("%6d",i);
 if(k%7==0)
 {
   printf("   ");
   printf("\n");
         }
  }
}


//FUNCTION TO DETERMINE THE DAY ON SELECTED DATE MONTH AND YEAR
void determineday()
{
int d,m,i,y,r=0,r1=0,r2=0,s=0;
printf("****YOU SELECTED 3 CHOICE****");
input:
printf("\nEnter the DATE : ");
scanf("%d",&d);
printf("\nEnter the MONTH(numeric): ");
scanf("%d",&m);
printf("\nEnter the YEAR : ");
scanf("%d",&y);
 if(m==2)
 {
   if((d>28)&&(y%4!=0)){
   printf("\n Invalid date in February of non leap year.\nThe maximum value is 28 !!!!");
     goto input;
     }
     if((d>29)&&(y%4==0)){
     printf("\n Invalid date in February of leap year.\nThe maximum value is 29 !!!!");
     goto input;
     }
     }
 else if((m==1)||(m==3)||(m==5)||(m==7)||(m==8)||(m==10)||(m==12)){
    if(d>31)
{
     printf("\n Invalid date in %d th month.\nThe maximum value is 31 !!!!",m);
     goto input;
    }
    }
 else if(((m==4)||(m==6)||(m==9)||(m==11))&&(d>30)){
      printf("\n Invalid date in the %d th month.\nThe maximum value is 30 !!!!",m);
      goto input;
      }
 else if((d>31)){
printf("\n @@ Enter valid date @@");
goto input;
}
if((d<1)||(m<1)){
printf("\nEnter positive valid data!!!! ");
goto input;
}
 else  {

switch(m){
case 1:
case 10:
       r1=d+2;
       break;
case 2:
case 3:
case 11:
       r1=d+5;
       break;
case 4:
case 7:
       r1=d+1;
       break;
case 9:
case 12:
        r1=d;
        break;
case 5:
        r1=d+3;
        break;
case 6:
        r1=d+6;
        break;
case 8:
        r1=d+4;
        break;
default:
{
  printf("\n No month greater than 12.\nEnter valid month Once again enter the Date Month Year!!!!");
  goto input;
}
 }
  }
if(y<2003){
  for(i=2002;i>=y;i--){
    if((i==y)&&(i%4==0)){
      if(m>2) s=s+1;
      else if(m<=2) s=s+2;
       break;
       }

       else if(i%4==0){
       if(i%100==0){
         if(i%400==0)
         s=s+2;
         else s=s+1;
         }
       else s=s+2;
        }
       else s=s+1;
       }
       r2=7-s%7;
       }
else if(y>2003){
 for(i=2004;i<=y;i++){
  if((i==y)&&(i%4==0)){
    if(m>2) s=s+2;
    else if(m<=2) s=s+1;
    break;
    }
     else if(i%4==0){
      if(i%100==0){
      if(i%400==0)
      s=s+2;
      else s=s+1;
      }
      else s=s+2;
      }
     else s=s+1;
     }
     r2=s%7;
     }
else r2=0;
r=(r1+r2)%7;
printf(" ");
switch(r){
case 0:
    printf("\nThe Day is SUNDAY");
    break;
case 1:
    printf("\nThe Day is MONDAY");
    break;
case 2:
    printf("\nThe Day is TUESDAY");
    break;
case 3:
    printf("\nThe Day is WEDNESDAY");
    break;
case 4:
    printf("\nThe Day is THURSDAY");
    break;
case 5:
    printf("\nThe Day is FRIDAY");
    break;
case 6:
    printf("\nThe Day is SATURDAY");
    break;
}
}



//MAIN MENU
void main()
{
  int choice;
  char n;

  // INTRODUCTION
   printf("This is program of CALENDER \n\n");
   printf("\n\t\tMENU\n\n choice 1: show calender of specific month\n choice 2: check the leap year\n choice 3: check the day on specific date-month-year\n choice 4: exit");
   printf("\n\nEnter your choice: ");
   scanf("%d",&choice);
   switch(choice)
   {
    case 1:
        showcalendar();
        break;
     case 2:
           leapyear();
           break;

     case 3:
            determineday();
        break;
     case 4:
            exit(0);

     default:
               printf("\n\n !!!!WRONG CHOICE!!!!");

   }
printf("\n\nthank you");

  getch();
}





