# Работа с MS Office в WPF (часть 3)
-------
**Цель работы:** цель данной программы - показать легкость доступа к функциям MS Excel.

--------

Ниже на рисунках представлены фрагменты проекта


<img src="https://github.com/BernikovaLera/College-of-Computer-Science-and-Programming-of-the-Financial-University/blob/main/Projects%20in%20C%23/Working%20with%20MS%20Office%20in%20WPF_3/%D0%A0%D0%B8%D1%81%D1%83%D0%BD%D0%BE%D0%BA1.png" width="500" height="300" >



Часть программного кода:

    public partial class MainWindow : Window
    {
        public MainWindow()
        {
            InitializeComponent();
        }

        private void Button_Pi_Click(object sender, RoutedEventArgs e)
        {
            var XL = new Microsoft.Office.Interop.Excel.Application();
            var PI = XL.WorksheetFunction.Pi();

            TextBlock_Pi.Text = Math.PI.ToString();

            XL.Quit();
        }
    }




--------

**Язык программирования**
![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=c-sharp&logoColor=white)
![XAML](https://img.shields.io/badge/XAML-%23239120.svg?style=for-the-badge&logo=xaml&logoColor=white)
