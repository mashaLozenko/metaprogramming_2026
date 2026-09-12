# Task 5
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    class Book
    {
        public string Title { get; set; }
        public string Author { get; set; }
        public int Year { get; set; }

        public string GetDescription()
        {
            return $"Назва: {Title}, Автор: {Author}, Рік: {Year}";
        }
    } 
    internal class Program
    {
        static void Main(string[] args)
        {
                Book[] books =
                {
                new Book { Title = "Harry Potter", Author = "J.K. Rowling", Year = 1997 },
                new Book { Title = "The Hobbit", Author = "J.R.R. Tolkien", Year = 1937 },
                new Book { Title = "1984", Author = "George Orwell", Year = 1949 },
                new Book { Title = "Animal Farm", Author = "George Orwell", Year = 1945 }
            };

                Console.WriteLine("Books:");
                for (int i = 0; i < books.Length; i++)
                {
                    Console.WriteLine(books[i].GetDescription());
                }

                Console.WriteLine();
                Console.WriteLine("Search by:");
                Console.WriteLine("1 - Year");
                Console.WriteLine("2 - Author");
                Console.WriteLine("3 - Title");

                int choice = Convert.ToInt32(Console.ReadLine());

                Console.Write("Enter search value: ");
                string search = Console.ReadLine();

                Console.WriteLine();
                Console.WriteLine("Search results:");

                for (int i = 0; i < books.Length; i++)
                {
                    if (choice == 1)
                    {
                        if (books[i].Year.ToString() == search)
                        {
                            Console.WriteLine(books[i].GetDescription());
                        }
                    }
                    else if (choice == 2)
                    {
                        if (books[i].Author.ToLower() == search.ToLower())
                        {
                            Console.WriteLine(books[i].GetDescription());
                        }
                    }
                    else if (choice == 3)
                    {
                        if (books[i].Title.ToLower() == search.ToLower())
                        {
                            Console.WriteLine(books[i].GetDescription());
                        }
                    }
                }

                Console.WriteLine();
                Console.WriteLine("Press any key to exit");
                Console.ReadKey();
            }
    }
}
