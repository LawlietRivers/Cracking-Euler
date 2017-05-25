# Cracking-Euler
Solving Project Euler programs
Initial code for Problem 601 of project euler

public class Divisibilitystreak 
{
    
    public int streak(int x)
    {
        int t;
        for(int i=1;;i++)
        {
            if(((x+i) % (i+1))!=0)
            {
                t=i;
                break;
            }
        }

        return t;
    }
    
    public int P(int s, int N)
    {
        int x = 0;
        for(int n = 2;n<N;n++)
        {
            if(streak(n)==s)
                x++;
        }
        return x;
    }
    
    public static void main(String args[])
    {
        Divisibilitystreak d1 = new Divisibilitystreak();
        int s = 0;
       for(int i =1;i<=31;i++)
       {
           s+= new Divisibilitystreak().P(i, (int)Math.pow(4, i));
       }
        System.out.println("SUM = " + s);
    }
}
