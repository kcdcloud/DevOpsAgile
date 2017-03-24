# WordPress

## Теги WordPress

* [Справочник wordpress ru](wp-kama.ru)
* [Справочник wordpress en](https://codex.wordpress.org/Создание_тем)

&lt;?php bloginfo\(`name`\); ?&gt; - данная функция с параметром name передает имя темы сайта \(название сайта\)  
параметры bloginfo:

* name
* description
* stylesheet\_url
* template\_url - выводит путь
  &lt;?php echo home\_url\(\); ?&gt; - ссылка на домен сайта оператор echo отобразит данные наэкране
  &lt;?php the\_title\(\); ?&gt; - выводит заголовок статьи
  &lt;?php the\_content\(\); ?&gt; - вывод контента используется только внутри цикла wordpress theloop
  &lt;?php have\_posts\(\); ?&gt;
  &lt;?php the\_post\(\); ?&gt;
  &lt;?php the\_excerpt\(\); ?&gt;
  &lt;?php the\_permalink\(\); ?&gt;
  &lt;?php var\_dump\($post\); ?&gt; - получить объект post есть еще объект posts это массив его можно использовать для создание своего цикла вместо стандартного theloop
  &lt;?php echo $post-&gt;post\_title ?&gt; - тоже самое что и ф-ия the\_title только напрямую свойство post\_title из объекта post
  &lt;?php get\_header\(\); ?&gt;
  &lt;?php get\_sidebar\(\); ?&gt;
  &lt;?php get\_footer\(\); ?&gt;
  &lt;?php wp\_title\(\); ?&gt; - выводит название страницы
  &lt;?php wp\_head\(\); ?&gt; - включение админ бара
  &lt;?php wp\_footer\(\); ?&gt;
  &lt;?php ?&gt;

файл функций functions.php - все стили и скрипты постановка в очередь  
&lt;?php add\_action\('wp\_enqueue\_sripts', 'user\_function\_load\_script'\); ?&gt; - ф-ия add\_action осуществляет привязку нашей функции к действию или hook крючкам \(хуки это ф-ии к которым можно прицепиться и что выполнить или изменить в их работе\) цепляемся к ф-ии wp\_enqueue\_scripts которая ставит в очередь на подгрузку скрипты в том числе пользовательские

function user\_function\_load\_script\(\){  
  wp\_enqueue\_script\('name\_script', 'get\_template\_directory\_url\(\)ж'\);  
}

