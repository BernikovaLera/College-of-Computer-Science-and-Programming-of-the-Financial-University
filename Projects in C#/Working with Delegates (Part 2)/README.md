# Работа с делегатами (часть 2)
-------
**Цель работы:** Изучить теоретический материал и выполнить консольный проект, демонстрирующий работу с делегатами.

--------

Ниже на рисунках представлены фрагменты проекта

<img src="https://github.com/BernikovaLera/College-of-Computer-Science-and-Programming-of-the-Financial-University/blob/main/Projects%20in%20C%23/Working%20with%20Delegates%20(Part%202)/%D0%A0%D0%B8%D1%81%D1%83%D0%BD%D0%BE%D0%BA1.png" width="500" height="300" >

Часть программного кода:

    using System;
    namespace up_pr5
    {
        class First
        {
            public static string str { get; set; }
            public static void fun1()
            {
                Console.WriteLine("Берникова 3ПКС-118");
                Console.WriteLine("Практическая работа №5\n");
                Console.WriteLine("В простанстве имен Му создаются 2 класса - First и Second.");
                Console.WriteLine("В классе First");
                Console.WriteLine("\t 1. создается закрытое поле str. Показан пример передачи значения закрытому полю.");
                Console.WriteLine("\t 2. создаются 5 функций для их дальнейшей привязки к делегату.");
                Console.WriteLine("В классе Second");
                Console.WriteLine("\t 1. рассмотрены различные способы добавления методов в делегат.\n");
                str = "###########1";
                Console.WriteLine("Работает fun1:");
            }
            public static void fun2()
            {
                str = "************2";
                Console.WriteLine("Работает fun2:");
            }
            public static void fun3()
            {
                str = "*************23";
                Console.WriteLine("Работает fun3:");
            }
        }
        class Second
        {
            public static void fun4()
            {
                Console.WriteLine("Работает статестическая функция");
                Console.WriteLine("\n");
                First.str = "~~~~~~~~~~~~~~~4";
                Console.WriteLine("Работает fun5 класса Second:");
            }
            public static void fun5()
            {
                First.str = "~~~~~~~~~~~~~~~51";
                Console.WriteLine("Работает fun6:");
            }
        }
        class Rechenie
        {
            delegate void Report();
            static void Main(string[] args)
            {
                Report del;
                del = First.fun1;
                del += ReportD;
                del();
                del = First.fun2;
                del += ReportD;
                del();
                del = First.fun3;
                del += ReportD;
                del();
                del = Second.fun4;
                del += ReportD;
                del();
                del = Second.fun5;
                del += ReportD;
                del();
                Console.ReadKey();
            }
            public static void ReportD()
            {
                Console.WriteLine("Работает функция Report. Значение str: " + First.str);
            }
        }
    }



--------

**Язык программирования**
![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=c-sharp&logoColor=white)
![XAML](https://img.shields.io/badge/XAML-%23239120.svg?style=for-the-badge&logo=xaml&logoColor=white)
