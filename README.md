# Print-triangle---and-allow-user-to-set-height-of-it-in
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Enter the height of the triangle:");
        int height;
        if (int.TryParse(Console.ReadLine(), out height))
        {
            PrintTriangle(height);
        }
        else
        {
            Console.WriteLine("Invalid input. Please enter a valid integer.");
        }
    }

    static void PrintTriangle(int height)
    {
        for (int i = 0; i < height; i++)
        {
            Console.Write(new string(' ', height - i - 1));
            Console.WriteLine(new string('*', 2 * i + 1)); 
        }
    }
}
