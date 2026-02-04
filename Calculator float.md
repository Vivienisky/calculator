#calculator

**Homework 2 метод float**
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
        Console.Write("Введите первое число: ");
        float firstOperand = Convert.ToSingle(Console.ReadLine());

        // Считывание второго числа
        Console.Write("Введите второе число: ");
        float secondOperand = Convert.ToSingle(Console.ReadLine());

        // Переменная для хранения результата
        float result;

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
                    Console.WriteLine("Ошибка: деление на ноль невозможно!!!");
                }
                break;
            default:
                Console.WriteLine("Ошибка: неверный ввод");
                break;
        }

        // Завершение программы
        Console.WriteLine("Нажмите любую клавишу для выхода, хорошего дня:).");
        Console.ReadKey();
    }

    // Метод для сложения
    static float Add(float a, float b)
    {
        return a + b;
    }

    // Метод для вычитания
    static float Subtract(float a, float b)
    {
        return a - b;
    }

    // Метод для умножения 
    static float Multiply(float a, float b)
    {
        return a * b;
    }

    // Метод для деления
    static float Divide(float a, float b)
    {
        return a / b;
    }
}
