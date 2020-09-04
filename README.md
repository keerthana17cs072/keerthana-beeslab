# keerthana-beeslab

3.swap between two numbers without using third variables:-
#include <stdio.h>
int main()
{
  int x, y, third variable;

  printf("Enter two integers\n");
  scanf("%d%d", &x, &y);

  printf("Before Swapping\nFirst integer = %d\nSecond integer = %d\n", x, y);

  third variable = x;
  x = y;
  y = thirdvariable;

  printf("After Swapping\nFirst integer = %d\nSecond integer = %d\n", x, y);

  return 0;
}


6.Java program to find angle between hour and minute hands
import java.io.*;
import math.io.*;
 
class John
{
    
    static int handsofclock(hour h, minute m)
    {
        
        if (h <0 || m < 0 || h >12 || m > 60)
            System.out.println("Wrong input");
 
        if (h == 12)
            h = 0;
             if (m == 60)
       {
        m = 0;
        h += 1;
        if(h>12)
          h = h-12;
        }
        int hour_angle = (int)(0.5 * (h*60 + m));
        int minute_angle = (int)(6*m);
 
        
        int angle = Math.abs(hour_angle - minute_angle);
 
        
        angle = Math.min(360-angle, angle);
 
        return angle;
         }
     
  
    public static void main (String[] args)
    {
        System.out.println(handsofclock(9, 60)+" degree");
        System.out.println(handsofclock(3, 30)+" degree");
    }
}


5.weekends:-
import java.util.*;
class Calender
public int saturdaysunday(Date d1, Date d2) {
                Calendar c1 = Calendar.getInstance();
                c1.setTime(d1);

                Calendar c2 = Calendar.getInstance();
                c2.setTime(d2);

                int sundays = 0;
                int saturday = 0;

                while (c1.after(c2)) {
                    if (c2.get(Calendar.DAY_OF_WEEK) == Calendar.SUNDAY || c2.get(Calendar.DAY_OF_WEEK) == Calendar.SUNDAY)
                        sundays++;
                    saturday++;
                    c2.add(Calendar.DATE, 1);
                    c2.add(Calendar.DATE, 1);
                }
                System.out.println(sundays);

                return saturday + sundays;
            }
            
            
   2.find the missing number:
  #include <stdio.h>
 int missingnumber(int a[], int n)
{
    int i, total;
    total = (n + 1) * (n + 2) / 2;
    for (i = 0; i < n; i++)
        total -= a[i];
    return total;
}
 

7.sum of digits of no until sum becomes single digit:-
import java.util.*; 
  
 class Digit { 
      
    static int singleDigit(int n) 
    { 
        int sum = 0; 
        while (n > 0 || sum > 9)  
        { 
            if (n == 0) { 
                n = sum; 
                sum = 0; 
            } 
            sum += n % 10; 
            n /= 10; 
        } 
        return sum; 
    } 
      
    
    public static void main(String args[]) 
    { 
        int n = 1234; 
        System.out.println(singleDigit(n)); 
    } 
} 
int main()
{
    int a[] = { 1, 2, 4, 5, 6 };
    int miss = missingnumber(a, 5);
    printf("%d", miss);
    getchar();
}



8.Average Marks:-
class AverageMarks
{
   public static void main(String args[])
  {
    int i;
    System.out.println("Enter number of subjects");
    Scanner sc=new Scanner(System.in);
    int n=sc.nextInt();
    int[] a=new int[n];
    double average=0;
    System.out.println("Enter marks");
    for( i=0;i<n;i++)
    {
       a[i]=sc.nextInt();
    }
    for( i=0;i<n;i++)
    {
      average=average+a[i];
    }
    System.out.print("Average of (");
    for(i=0;i<n-1;i++)
    {
      System.out.print(a[i]+",");
    }
    System.out.println(a[i]+") ="+average/n);
  }
}
 
