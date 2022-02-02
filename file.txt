using System;

namespace SimpleCalc
{
    class Program
    {
        static void Main(string[] args)
        {
            int num1, num2, ope;
            Console.WriteLine("Choose operation to perfom (+,-,*,/)");
            ope = Console.ReadLine()[0];
            Console.WriteLine("Enter 1st number");
            num1 = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Enter 2nd number");
            num2 = Convert.ToInt32(Console.ReadLine());
            switch (ope)
            {
                case '+':
                    Console.WriteLine("{0}+{1}={2}", num1, num2, (num1 + num2));
                    break;
                case '-':
                    Console.WriteLine("{0}-{1}={2}", num1, num2, (num1 - num2));
                    break;
                case '*':
                    Console.WriteLine("{0}*{1}={2}", num1, num2, (num1 * num2));
                    break;
                case '/':
                    if (num2 == 0)
                        Console.WriteLine("Not possible");
                    else
                        Console.WriteLine("{0}/{1}={2}", num1, num2, (num1 / num2));
                    break;
            }
            Console.ReadKey();
        }
    }
}
