# Требования к проекту checkers_game

# <h1>1 Введениe</h1>
<p align="justify"> Игра Шашки – логическая игра для двух игроков, заключающаяся в передвижении определённым образом фишек-шашек по клеткам шашечной доски. Цель игры — взять все шашки соперника.</p>
Программа состоит из:
<ol> 
<li><p align="justify">Основное меню программы. Данное окно создается сразу после запуска приложения, служит для навигации по основным модулям программы, а также выхода из неё.</p></li>
<li><p align="justify">Окно настроек. Данное окно создаётся сразу после выбора соответствующего пункта основного меню программы. Данное окно служит для настроек внешнего вида игрового объекта шашка, а именно выбора короны для “дамки”.</p></li>
<li><p align="justify">Окно игры одного пользователя против другого пользователя. Данное окно создаётся сразу после выбора соответствующего пункта основного меню программы. Данное окно служит для игры одного пользователя с другим пользователем, где один пользователь играет за белые шашки, а другой за черные шашки.</p></li>
</ol>

# <h1>2 Требования пользователя </h1>
<h2>2.1 Программные интерфейсы </h2>
<p align="justify">Графическая библиотека SFML содержит следующие модули: System, Window, Graphics, Audio и Network. На первых четырёх остановимся подробнее, т.к. только они были использованы при написании программы.</p>
<ol>
<p align="justify"><li>Модуль System является основным модулем, без которого работа всех прочих невозможна. В нём осуществляется управление временем и потоками, реализованы такие основополагающие классы как:</li></p>
<ul>
<li><p align="justify">sfml_string для работы со строками.</p></li>
<li><p align="justify">Vector2 и Vector3 для хранения двумерных и трёхмерных векторов.</p></li>
<li><p align="justify">FileInputStream для работы с файлами.</p></li>
</ul>

<p align="justify"><li>Модуль Window необходим для работы с оконными приложениями, созданием окон и взаимодействием с пользователем посредством их. Этот модуль содержит в себе классы:</li></p>
<ul>
<li><p align="justify">RenderWindow – используется для создания окна, а также обработку пользовательского ввода и отображения элементов интерфейса.</p></li>
<li><p align="justify">Event – событие, которое можно получить вызовом метода pollevent класса RenderWindow.</p></li>
<li><p align="justify">VideoMode – служит для задания характеристик окна, таких как, например, ширина и высота.</p></li>
</ul>

<p align="justify"><li>Модуль Graphics специально оптимизирован для работы с двумерной графикой. Данный модуль содержит в себе такие классы как:</li></p>
<ul>
<li><p align="justify">Image – предназначен для работы с изображениями. В данной программе используется для изменения иконки приложения в левом верхнем углу окна.</p></li>
<li><p align="justify">Font – предназначен для работы с пользовательскими шрифтами. В программе нужен для улучшения дизайна с помощью использования шрифта «Proxima-nova extrabold», который как нельзя лучше вписывается в общий стиль приложения.</p></li>
<li><p align="justify">RectangleShape – предназначен для создания, изменения и отображения на экран прямоугольных форм. На его основе реализованы все элементы интерфейса в программе.</p></li>
</ul>

<p align="justify"><li>Модуль Audio используется для работы со звуком. Данный модуль содержит в себе такие классы как:</li></p>
<ul>
<li><p align="justify">Music – предназначен для воспроизведения из аудиофайла потоковой музыки.</p></li>
<li><p align="justify">Sound - предназначен для работы с обычным звуком, который можно воспроизводить в звуковой среде.</p></li>
</ul>

<p align="justify"><li>Модуль Network предназначен для работы с TCP и UDP сокетами (межсетевыми протоколами), HTTP и FTP протоколами.</li></p>
</ol>

<h2> 2.2 Интерфейс пользователя</h2>
<p align="justify">В данном приложении пользователь будет взаимодействовать с приложением только при помощи мышки компьютера. После запуска приложения будет открыто игровое меню данного приложения которое будет содержать две кнопки для выбора дальнейших действий пользователя: “Игра с другом” и “Настройки”. При наведении курсора мыши на кнопку, она подсветится, тем самым акцентируя внимание пользователя на пункте меню игры которое он собирается выбрать. В пункте меню “Настройки” пользователю будет предоставлена возможность выбрать корону для дамки. В окне “Настройки” перед пользователем появятся две дамки с наборами корон изображенных на них. После выбора пользователем пункта меню “Игра с другом” пользователь перейдет в новое окно. В котором будет проходить сам игровой процесс. В ходе игры при нажатии на шашку будет происходить подсветка возможных её ходов. Будет присутствовать кнопка чтения правил игры и также информация о том чей сейчас ход, а также кнопка “Сдаться”.</p>
 
<h2> 2.3 Характеристики пользователей</h2>
<p align="justify">Данное приложение рассчитано на пользователей любого возраста, любого уровня образования и с минимальным уровнем владения ПК. Но стоит отметить, что оно требует наличие минимальных знаний игры, но при этом не требует наличие опыта игры.</p>

<h2> 2.4 Предположения и зависимости</h2>
<p align="justify">Так как приложение компьютерное и не требует интернет соединения, то ограничений в использовании данного приложения нету.</p>

# <h1>3 Системные требования</h1>
<h2> 3.1 Функциональные требования</h2>
<ol>
<li><p align="justify">Качественное оформление приложения, включающее в себя понятный пользовательский интерфейс, красивые текстуры и подходящая цветовая гамма;</p></li>
<li><p align="justify">Наличие возможности играть локально с другим игроком;</p></li>
<li><p align="justify">Наличие возможности графических настроек шашек ранга “дамка”;</p></li>
<li><p align="justify">Адекватная реакция приложения на различные ненормальные ситуации;</p></li>
</ol>
<h2> 3.2 Нефункциональные требования</h2>
<p align="justify">Приложение будет располагаться локально и соответственно, не требует повышенной степени безопасности. Для целостности работы приложения необходима защита данных приложения от несанкционированных действий, т.к. удаление какого либо файла из папки приложения приведет к критическим ошибкам приложения. Приложение будет работать только на ПК с операционной системой Windows. Минимальная версия будет дополнена позже.</p>
