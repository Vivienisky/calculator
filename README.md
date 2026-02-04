# calculator

**Homework 2 switch**
```
using System;

class Program
{
    static void Main(string[] args)
    {
        Console.WriteLine("Выберите операцию:");
        Console.WriteLine("1. Сложение");
        Console.WriteLine("2. Вычитание");
        Console.WriteLine("3. Умножение");
        Console.WriteLine("4. Деление");

        Console.Write("Введите номер операции которую хотите совершить (1/2/3/4): ");
        string choice = Console.ReadLine();

        Console.Write("Введите первое число: ");
        double num1 = Convert.ToDouble(Console.ReadLine());

        Console.Write("Введите второе число: ");
        double num2 = Convert.ToDouble(Console.ReadLine());

        double result;

        switch (choice)
        {
            case "1":
                result = Add (num1, num2);
                Console.WriteLine($"{num1} + {num2} = {result}");
                break;
            case "2":
                result = Subtract(num1, num2);
                Console.WriteLine($"{num1} - {num2} = {result}");
                break;
            case "3":
                result = Multiply(num1, num2);
                Console.WriteLine($"{num1} * {num2} = {result}");
                break;
            case "4":
                if (num2 != 0)
                {
                    result = Divide(num1, num2);
                    Console.WriteLine($"{num1} / {num2} = {result}");
                }
                else
                {
                    Console.WriteLine("Ошибка: деление на ноль!");
                }

                break;
            default:
                Console.WriteLine("Неверный ввод. Пожалуйста, выберите операцию от 1 до 4.");
                break;
        }
    }
    static double Add(double x, double y)
    {
        return x + y;
    }

    static double Subtract(double x, double y)
    {
        return x - y;
    }

    static double Multiply(double x, double y)
    {
        return x * y;
    }

    static double Divide(double x, double y)
    {
        return x / y;
    }
}
