# Task 2
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {

            int x;
            int y;
            int z;
            int number;

            Console.WriteLine("Enter the first number:");
            string x_str = Console.ReadLine();
            x = Convert.ToInt32(x_str);

            Console.WriteLine("Enter the second number:");
            string y_str = Console.ReadLine();
            y = Convert.ToInt32(y_str);

            Console.WriteLine("Enter the number of the operation you want to perform");
            Console.WriteLine("1 - multiplication");
            Console.WriteLine("2 - division");
            Console.WriteLine("3 - addition");
            Console.WriteLine("4 - subtraction");

            number = Convert.ToInt32(Console.ReadLine());

            if (number == 1)
            {
                z = x * y;
                Console.WriteLine($"{x} * {y} = {z}");
            }
            else if (number == 2)
            {
                if (y == 0)
                {
                    Console.WriteLine("You cannot divide by zero");
                    return;
                }

                z = x / y;
                Console.WriteLine($"{x} / {y} = {z}");
            }
            else if (number == 3)
            {
                z = x + y;
                Console.WriteLine($"{x} + {y} = {z}");
            }
            else if (number == 4)
            {
                z = x - y;
                Console.WriteLine($"{x} - {y} = {z}");
            }
            else
            {
                Console.WriteLine("Invalid operation number");
            }

            Console.WriteLine("Press any key");
            Console.ReadKey();

        }
    }
}
