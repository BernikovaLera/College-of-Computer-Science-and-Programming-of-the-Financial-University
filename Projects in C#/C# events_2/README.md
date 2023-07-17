# Калькулятор С#
-------
**Цель работы:** разработать калькулятор на языке С#. В проекте использовать прием создания одного обработчика для нескольких событий.

--------

Ниже на рисунках представлены фрагменты проекта

**Главная**

<img src="https://github.com/BernikovaLera/calculator/blob/main/C%23%20events_2/%D0%A0%D0%B8%D1%81%D1%83%D0%BD%D0%BE%D0%BA5.png" width="500" height="300" >

<img src="https://github.com/BernikovaLera/calculator/blob/main/C%23%20events_2/%D0%A0%D0%B8%D1%81%D1%83%D0%BD%D0%BE%D0%BA6.png" width="500" height="300" >

--------
public MainWindow()
```С#
InitializeComponent();
foreach (UIElement el in Calculyator.Children)
    {
        if (el is Button)
            {
                ((Button)el).Click += Button_Click;
            }
    }
```
private void Button_Click
```С#
string vvod = (string)((Button)e.OriginalSource).Content;
switch (vvod)
    {
        case "CE":
            {
                TextBox_Vichislenie.Text = "";
                break;
            }
        case "=":
            {
                string chislo = new DataTable().Compute(TextBox_Vichislenie.Text, null).ToString();
                TextBox_Vichislenie.Text = chislo;
                break;
            }
        case "x²":
            {
                string chislo = new DataTable().Compute(TextBox_Vichislenie.Text, null).ToString();
                var kvadrat = Convert.ToDouble(chislo);
                kvadrat = Math.Pow(kvadrat, 2);
                chislo = Convert.ToString(kvadrat);
                TextBox_Vichislenie.Text = chislo;
                break;
            }
        case "x³":
            {
                string chislo = new DataTable().Compute(TextBox_Vichislenie.Text, null).ToString();
                var kub = Convert.ToDouble(chislo);
                kub = Math.Pow(kub, 3);
                chislo = Convert.ToString(kub);
                TextBox_Vichislenie.Text = chislo;
                break;
            }
        case "±":
            {
                string chislo = new DataTable().Compute(TextBox_Vichislenie.Text, null).ToString();
                var plus_minus = Convert.ToDouble(chislo);
                plus_minus = -plus_minus;
                chislo = Convert.ToString(plus_minus);
                TextBox_Vichislenie.Text = chislo;
                break;
            }
        case ".":
            {
                string chislo = new DataTable().Compute(TextBox_Vichislenie.Text, null).ToString();
                chislo = TextBox_Vichislenie.Text + '.';
                TextBox_Vichislenie.Text = chislo;
                break;
            }
        case "√":
            {
                string chislo = new DataTable().Compute(TextBox_Vichislenie.Text, null).ToString();
                var koren = Convert.ToDouble(chislo);
                koren = Math.Sqrt(koren);
                chislo = Convert.ToString(koren);
                TextBox_Vichislenie.Text = chislo;
                break;
            }
        default:
            {
                TextBox_Vichislenie.Text += vvod;
                break;
            }
```
--------
**Язык программирования**
![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=c-sharp&logoColor=white)
![XAML](https://img.shields.io/badge/XAML-%23239120.svg?style=for-the-badge&logo=xaml&logoColor=white)
