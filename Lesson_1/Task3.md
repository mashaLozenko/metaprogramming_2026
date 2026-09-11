# Task 3
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
            const double USD_TO_UAH = 40;
            const double EUR_TO_UAH = 45;

            double amount;
            int from;
            int to;
            double result;

            Console.WriteLine("Enter amount:");
            string amount_str = Console.ReadLine();
            amount = Convert.ToDouble(amount_str);

            if (amount < 0)
            {
                Console.WriteLine("Amount cannot be negative");
                return;
            }

            Console.WriteLine("Choose the currency:");
            Console.WriteLine("1 - USD");
            Console.WriteLine("2 - EUR");
            Console.WriteLine("3 - UAH");

            string from_str = Console.ReadLine();
            from = Convert.ToInt32(from_str);

            if (from < 1 || from > 3)
            {
                Console.WriteLine("Invalid source currency");
                return;
            }

            Console.WriteLine("Choose the target currency:");
            Console.WriteLine("1 - USD");
            Console.WriteLine("2 - EUR");
            Console.WriteLine("3 - UAH");

            string to_str = Console.ReadLine();
            to = Convert.ToInt32(to_str);

            if (to < 1 || to > 3)
            {
                Console.WriteLine("Invalid target currency");
                return;
            }

            if (from == 1 && to == 3)
            {
                result = amount * USD_TO_UAH;
                Console.WriteLine($"Your result: {result}");
            }
            else if (from == 2 && to == 3)
            {
                result = amount * EUR_TO_UAH;
                Console.WriteLine($"Your result: {result}");
            }
            else if (from == 3 && to == 1)
            {
                result = amount / USD_TO_UAH;
                Console.WriteLine($"Your result: {result}");
            }
            else if (from == 3 && to == 2)
            {
                result = amount / EUR_TO_UAH;
                Console.WriteLine($"Your result: {result}");
            }
            else if (from == 1 && to == 2)
            {
                result = amount * USD_TO_UAH;
                result = result / EUR_TO_UAH;
                Console.WriteLine($"Your result: {result}");
            }
            else if (from == 2 && to == 1)
            {
                result = amount * EUR_TO_UAH;
                result = result / USD_TO_UAH;
                Console.WriteLine($"Your result: {result}");
            }
            else if (from == to)
            {
                result = amount;
                Console.WriteLine($"Your result: {result}");
            }

            Console.WriteLine("Press any key");
            Console.ReadKey();

        }
    }
}
