# Tast 4
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
            string text;
            int spaces = 0;
            Console.WriteLine("Enter tour text:");
            text = Console.ReadLine();
            int lines = 1;
            Console.WriteLine($"Number of lines: {lines}");
            int characters = text.Length;
            Console.WriteLine($"Number of characters: {characters}");
            for (int i = 0; i < text.Length; i++)
            {
                if (text[i] == ' ')
                {
                    spaces++;
                }
            }
            Console.WriteLine($"Number of spaces: {spaces}");

            int words = 1;

            for (int i = 0; i < text.Length - 1; i++)
            {
                if (text[i] == ' ' && text[i + 1] != ' ')
                {
                    words++;
                }
            }
            Console.WriteLine($"Number of words: {words}");




            Console.WriteLine("Press any key to exit");
            Console.ReadKey();
        }
    }
}

