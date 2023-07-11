# Работа с делегатами (часть 1)
-------
**Цель работы:** Изучить теоретический материал и выполнить консольный проект, демонстрирующий работу с делегатами.

--------

Ниже на рисунках представлены фрагменты проекта

<img src="https://github.com/BernikovaLera/College-of-Computer-Science-and-Programming-of-the-Financial-University/blob/main/Projects%20in%20C%23/Working%20with%20Delegates%20(Part%201)/%D0%A0%D0%B8%D1%81%D1%83%D0%BD%D0%BE%D0%BA1.png" width="500" height="300" >

Часть программного кода:

using System;
namespace pr_up4
{
    class Math
    {
        public int Sum(int x, int y) { return x + y; }
    }
    class Program
    {
        delegate int Operation(int x, int y);
        delegate int OperationForClass(int x, int y);
        delegate void Message(); 
        static void Main(string[] args)
        {
            // делегата Message()
            Console.WriteLine("\t\t 1. Создание делегата и добавление в него метода, в зависимости от времени суток:");
            Message mes; 
            if (DateTime.Now.Hour < 12) {
                mes = GoodMorning; }
            else {
                mes = GoodEvening; }
            mes();
            Console.WriteLine("\n");
            // делегата Перопределение делегата: делегат указывает на метод Add
            Console.WriteLine("\t\t 2. Перопределение делегата:");
            Console.WriteLine("\t\t делегат указывает на метод Add");
            Console.WriteLine("Operation del = Add;");
            Console.WriteLine("int result = del(4, 5);");
            Console.WriteLine("Console.WriteLine(Результат:  + result);");
            Operation del = Add; 
            int result = del(4, 5); 
            Console.WriteLine("\t Результат: " + result);
            Console.WriteLine("\n");
            // делегата Переопределение делегата: делегат указывает на метод Multiply
            Console.WriteLine("\t\t делегат указывает на метод Multiply");
            Console.WriteLine("del = Multiply;");
            Console.WriteLine("result = del(4, 5);");
            Console.WriteLine("Console.WriteLine(Результат:  + result);");
            del = Multiply; 
            result = del(4, 5);
            Console.WriteLine("\t Результат: " + result);
            Console.WriteLine("\n");
            // Присвоение делегату метода из другого класса: делегату присваивается метод Sum из класса Math
            Console.WriteLine("\t\t 3. Присвоение делигату метода из другого класса:");
            Console.WriteLine("\t\t делегату присваивается метод Sum из класса Math");
            Console.WriteLine("Math math = new Math();");
            Console.WriteLine("OperationForClass delSum = math.Sum;");
            Console.WriteLine("int resultSum = delSum(10, 100);");
            Console.WriteLine("Console.WriteLine(Результат:  + resultSum);");
            Math math = new Math();
            OperationForClass delSum = math.Sum;
            int resultSum = delSum(10, 100);
            Console.WriteLine("\t Результат: " + resultSum);  
            Console.Read();
        }
        private static void GoodMorning()
        {
            Console.WriteLine("Good Morning");
        }
        private static void GoodEvening()
        {
            Console.WriteLine("Good Evening");
        }
        private static int Add(int x, int y)
        {
            return x + y;
        }
        private static int Multiply(int x, int y)
        {
            return x * y;
        }
        private static int delSum(int x, int y)
        {
            return x + y;
        }
    }
}


--------

**Язык программирования**
![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=c-sharp&logoColor=white)
![XAML](https://img.shields.io/badge/XAML-%23239120.svg?style=for-the-badge&logo=xaml&logoColor=white)
