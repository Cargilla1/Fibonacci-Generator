# Fibonacci-Generator
This program will generate a sequence in the Fibonacci equation. 
namespace Fibonacci_Sequence
{
    class Program
    {
        static void Main(string[] args)
        {
            
            Console.WriteLine("What number in the fibonacci sequence do you wish to call?");
         
            string userinput = Console.ReadLine();
            int a = Convert.ToInt32(userinput);
            int[] fibonacci = new int[a + 1];

            int ticker = 0;
            
                Console.WriteLine("I've returned from the method your number is "+Fibonacci(a,ticker, fibonacci));           
        } 
        static int Fibonacci(int a, int ticker, int[] fibonacci)
        {                                       
                fibonacci[0] = 1;
                fibonacci[1] = 1;                      
          
            if (ticker > 1)
            {
                fibonacci[ticker] = fibonacci[ticker-1] + fibonacci[ticker - 2];
                          
            }
                    
                if (ticker == a)
                {
                return fibonacci[ticker-1];
                }                                  
            
            return Fibonacci(a,ticker+1,fibonacci);           
        }

        
    }
}
