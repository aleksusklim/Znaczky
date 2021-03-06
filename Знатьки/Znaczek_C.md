﻿### Znaczek #C:

Я спаял себе пианино!

<http://klimaleksus.narod.ru/Files/REPEAT/piano_01.jpg>

Вернее, это старый советский электромузыкальный инструмент:

<http://klimaleksus.narod.ru/Files/REPEAT/piano_02.jpg>

Там было несколько плат, куча проводов и самое главное – тяжеленная, смонтированное на металле, пиано-клавиатура! На три октавы:

<http://klimaleksus.narod.ru/Files/REPEAT/piano_03.jpg>

Изначально я его проверил, то там работала максимум цепь питания, но никакого звука не было.

Я нашёл драйвер, программу и схему для подключения пиано-клавиатуры (фактически, набора кнопочек) к параллельному LPT порту компьютера:

<http://klimaleksus.narod.ru/Files/REPEAT/piano_00.png>

Купил LPT-шнур (для принтера, отпаяв второй конец) и включил сам порт в BIOS. Позамыкал пины – работает! Получаю миди-ноты. Даже без диодов.

Изучил, как на моём устройстве подключены клавиши. Оказалось, разводка не подходит: пришлось запаять общую шину по каждой октаве отдельно:

<http://klimaleksus.narod.ru/Files/REPEAT/piano_04.jpg>

На картинке: диагональные перемычки уже были, я же соединил красным проводом их все между собой.

Зато, одноимённые ноты разных октав уже любезно скручены и выведены в жгут:

<http://klimaleksus.narod.ru/Files/REPEAT/piano_05.jpg>

На картинке: синие провода уже были, соединяют тройки нот; красные (и тонкий белый слева) – мои шины на каждую октаву; толстые белые – выходы с двенадцати нот, жгут.

На самом деле, на схему мне нужно ещё 36 диодов – припаять к каждой клавише, чтобы компьютер смог отличать более двух одновременно зажатых клавиш, вроде бы. Но пока что и так работает (один фиг я двумя руками играть не умею):

<http://klimaleksus.narod.ru/Files/REPEAT/piano_06.jpg>

Всё инсталляцию придётся вернуть в оригинальный корпус, потому что клавиши своими пазами упираются в поверхность, на которой инструмент лежит:

<http://klimaleksus.narod.ru/Files/REPEAT/piano_07.jpg>

Кстати, мне пришлось отвернуть эти накладки (на трёх винтах каждая), чтобы добраться до клемм кнопок и зачистить их все шкуркой. Я шкурил, шкурил, шкурил… а то половина нот барахлила:

<http://klimaleksus.narod.ru/Files/REPEAT/piano_08.jpg>

И подрегулировать винты на кнопках, ведь несколько клавиш давали короткое замыкание:

<http://klimaleksus.narod.ru/Files/REPEAT/piano_09.jpg>

С обратной стороны были ещё три кнопочных детектора – для октав. На оригинальной разводке они соединялись достаточно странно, я потом что-то замутил с проводами, но потом вовсе отрезал всё:

<http://klimaleksus.narod.ru/Files/REPEAT/piano_10.jpg>

(Этот один общий провод не нужен, просто не убрал пока).

Раз я три своих провода непосредственно на клавиши провёл, эти контакты для октав в моей схеме не нужны:

<http://klimaleksus.narod.ru/Files/REPEAT/piano_11.jpg>

Таким образом, от клавиш выходит просто пучок проводов:

<http://klimaleksus.narod.ru/Files/REPEAT/piano_12.jpg>

Правда, дальше эти 15 проводков надо прикрутить к LPT шнуру… Можно конечно напрямую, но что-то я побоялся такую кипу скотчем скручивать.

Подыскал пустую плату с одним хорошим выводом, к которому можно было удобно припаяться с двух сторон:

<http://klimaleksus.narod.ru/Files/REPEAT/piano_13.jpg>

Не обращайте внимания на дорожки на самой плате, там всё равно нет деталей (и до кучи я перерезал все пути от контакта). Толстые провода я припаял как есть к выводным контактам платы:

<http://klimaleksus.narod.ru/Files/REPEAT/piano_14.jpg>

Она конечно прям здоровенная, хотя это просто способ соединить пятнадцать пар проводов.

Тоненькие проводки из шнура – припаял к контактам на плате. Замаялся, но получилось; лишние заизолировал отдельно:

<http://klimaleksus.narod.ru/Files/REPEAT/piano_15.jpg>

Итак, ещё раз: я разобрал старое нерабочее электронное пианино, вытащил из него музыкальную клавиатуру, соединил по схеме контакты кнопок, подключил в параллельный порт компьютера, и при помощи программы-драйвера получил внешнее устройство midi-ввода!

Правда как таковым вводом я и не пользовался, просто прямое воспроизведение нажимаемых нот. Осталось лишь диоды приделать, и закрыть чем-то поприличнее разводку к шнуру.

---

[Назад](./)
