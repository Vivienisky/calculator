#Calculator int
**Homework 2 int**
```
using System;

class Calculator
{
    static void Main(string[] args)
    {
        // Подсказка для пользователя
        Console.WriteLine("Добро пожаловать в калькулятор!");
        Console.WriteLine("Выберите операцию:");
        Console.WriteLine("1. Сложение");
        Console.WriteLine("2. Вычитание");
        Console.WriteLine("3. Умножение");
        Console.WriteLine("4. Деление");

        // Считывание выбора операции
        Console.Write("Введите номер операции (1/2/3/4): ");
        string selectedOperation = Console.ReadLine();

        // Считывание первого числа
        Console.Write("Введите первое целое число: ");
        int firstOperand = Convert.ToInt32(Console.ReadLine());

        // Считывание второго числа
        Console.Write("Введите второе целое число: ");
        int secondOperand = Convert.ToInt32(Console.ReadLine());

        // Переменная для хранения результата
        int result;

        // Выполнение операции в зависимости от выбора пользователя
        switch (selectedOperation)
        {
            case "1":
                result = Add(firstOperand, secondOperand);
                Console.WriteLine($"{firstOperand} + {secondOperand} = {result}");
                break;
            case "2":
                result = Subtract(firstOperand, secondOperand);
                Console.WriteLine($"{firstOperand} - {secondOperand} = {result}");
                break;
            case "3":
                result = Multiply(firstOperand, secondOperand);
                Console.WriteLine($"{firstOperand} * {secondOperand} = {result}");
                break;
            case "4":
                if (secondOperand != 0)
                {
                    result = Divide(firstOperand, secondOperand);
                    Console.WriteLine($"{firstOperand} / {secondOperand} = {result}");
                }
                else
                {
                    Console.WriteLine("Ошибка");
                }
                break;
            default:
                Console.WriteLine("Ошибка: неверный ввод выберите операцию от 1 до 4.");
                break;
        }

        // Завершение программы
        Console.WriteLine("Нажмите любую клавишу для выхода.");
        Console.ReadKey();
    }

    // Метод для сложения
    static int Add(int a, int b)
    {
        return a + b;
    }

    // Метод для вычитания
    static int Subtract(int a, int b)
    {
        return a - b;
    }

    // Метод для умножения
    static int Multiply(int a, int b)
    {
        return a * b;
    }

    // Метод для деления
    static int Divide(int a, int b)
    {
        return a / b;
    }
}
