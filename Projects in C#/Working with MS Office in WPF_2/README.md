# Работа с MS Office в WPF (часть 2)
-------
**Цель работы:** разработать программу, которая предлагает пользователю ввести какие-либо слова, предложения в текстовое поле и после нажатия соответствующей кнопки проверить орфографию введенного текста.

--------

Ниже на рисунках представлены фрагменты проекта


<img src="https://github.com/BernikovaLera/College-of-Computer-Science-and-Programming-of-the-Financial-University/blob/main/Projects%20in%20C%23/Working%20with%20MS%20Office%20in%20WPF_1/%D0%A0%D0%B8%D1%81%D1%83%D0%BD%D0%BE%D0%BA1.png" width="500" height="300" >

<img src="https://github.com/BernikovaLera/College-of-Computer-Science-and-Programming-of-the-Financial-University/blob/main/Projects%20in%20C%23/Working%20with%20MS%20Office%20in%20WPF_1/%D0%A0%D0%B8%D1%81%D1%83%D0%BD%D0%BE%D0%BA2.png" width="500" height="300" >

Часть программного кода:

    public partial class MainWindow : Window
    {
        public MainWindow()
        {
            InitializeComponent();
        }
        private void Button_Click(object sender, RoutedEventArgs e)
        {
            TextBox_vvod.SpellCheck.IsEnabled = true;
        } 
    }

--------

    <Grid Background="LimeGreen">
        <Label Content="Введите текст" HorizontalAlignment="Left" Height="36" Margin="26,10,0,0" VerticalAlignment="Top" Width="217" FontSize="20"/>
        <TextBox Name="TextBox_vvod" SpellCheck.IsEnabled="False" Language="ru-ru" AcceptsReturn="True" HorizontalAlignment="Left" Height="245" Margin="26,62,0,0" TextWrapping="Wrap" Text="" VerticalAlignment="Top" Width="471"/>
        <Button Content="Проверка орфографии текста" HorizontalAlignment="Left" Height="42" Margin="130,342,0,0" VerticalAlignment="Top" Width="271" FontSize="18" Click="Button_Click" Background="Gold"/>
    </Grid>


--------

**Язык программирования**
![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=c-sharp&logoColor=white)
![XAML](https://img.shields.io/badge/XAML-%23239120.svg?style=for-the-badge&logo=xaml&logoColor=white)
