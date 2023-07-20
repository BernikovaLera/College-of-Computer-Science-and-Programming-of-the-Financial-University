# Работа с MS Office в WPF (часть 3)
-------
**Цель работы:** цель данной программы - показать легкость доступа к функциям MS Excel.

--------

Ниже на рисунках представлены фрагменты проекта


<img src="" width="500" height="300" >



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
