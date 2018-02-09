[![voltNik YouTube](http://voltnik.ru/voltnik-banner.jpg)](https://www.youtube.com/channel/UC4s13gPVOMQVX3P1ZpdUwjA?sub_confirmation=1)
# Часы с датчиком давления, температуры и адаптивной подсветкой
* [Описание проекта](#chapter-0)
* [Папки проекта](#chapter-1)
* [Схема подключения](#chapter-2)
* [Материалы и компоненты](#chapter-3)
* [Как скачать и прошить](#chapter-4)
* [FAQ](#chapter-5)
* [Полезная информация](#chapter-6)

<a id="chapter-0"></a>
## Описание проекта
Это полностью законченный проект настольных часов на платформе Arduino Nano. Внутри корпуса установлен модуль BMP180 с барометром и термометром.
Реализована адаптивная подсветка экрана в зависимости от внешнего освещения чтобы часы не слепили ночью. Есть будильник и установка времени с кнопок.

Для сборки используется следующий набор комлпектующих:
- контроллер Arduino Nano
- экран 2004 с модулем I2C
- модуль времени DS1302
- модуль барометра BMP180
- 3шт кнопки
- фоторезистор
- 1шт резистор 10 кОм

еще понадобится: Цветной монтажный провод, макетнная плата.

Подробности сборки в ВИДЕО на канале voltNik:

<a id="chapter-1"></a>
## Папки
- **libraries** - библиотеки для работы с проектом
- **RBGflashlight** - прошивка для Arduino
- **3d-printer** - корпус для печати на 3D принтере

<a id="chapter-2"></a>
## Схема подключения
![СХЕМА2](https://github.com/voltNik/WeatherClock-2004/blob/master/weather-clock_bb.jpg.jpg)

<a id="chapter-3"></a>
## Материалы и компоненты
- Контроллер Arduino Nano: http://ali.pub/28sn0v резерв: http://ali.pub/2351o1
- Экран LCD 1602 с модулем I2C: http://ali.pub/28sn2m резерв: http://ali.pub/241bmo
- Кнопки 25шт: http://ali.pub/28sn4y резерв: http://ali.pub/235230
- Набор резисторов 600шт: http://ali.pub/28smng 

<a id="chapter-4"></a>
## Как скачать и прошить
* Скачать архив с проектом
> На этой странице сверху справа зелёная кнопка **Clone or download**, жми её, там будет **Download ZIP**
* Установить библиотеки в:  
`C:\Program Files (x86)\Arduino\libraries\` (Windows x64)  
`C:\Program Files\Arduino\libraries\` (Windows x86) 
* Подключить Ардуино к компьютеру
* Запустить файл прошивки .ino
* Настроить COM порт и модель Arduino
* Настроить что нужно по проекту в файле прошивке
* Нажать загрузить

## Настройки в коде
     Особого смысла менять код не вижу. Но он хорошо откомментирован. 
     Возможно вам понадобится изменить адрес экрана выбрав 0x27, либо 0x3f. 
     Переназначить пины подключения кнопок:
     - R_BTN 10 
     - G_BTN 9
     - B_BTN 8
     - MODE_BTN 11   // кнопка смены режима работы
     - POT_BTN 7   // потенциометр А7! (не 7, а именно А7!)
     - MODE_CNT 5              // количество режимов работы

<a id="chapter-5"></a>
## FAQ
### Основные вопросы
В: Как скачать с этого сайта?  
О: Вверху вверху справа зелёная кнопка **Clone or download**, её жми, там будет **Download ZIP**  

В: Скачался какой то файл .zip, куда его теперь?  
О: Это архив. Надо распаковать.  

В: Компьютер никак не реагирует на подключение Ардуины!  
О: Возможно у тебя зарядный USB кабель, а нужен именно data-кабель, по которому можно данные передавать  

В: Можно сделать по другому?  
О: Можно.  

В: Сколько стоит?  
О: Фонарь не продается и на заказ не иготавливается. Его можно только сделать самому по инструкции и видеогайду.  

### Вопросы по этому проекту
В: Как добавить свои режимы?  
О: Увеличиваете MODE_CNT и дописываете в массив modes название ваших режимов. Далее в коде добавляете CASE с номером вашего режима описывая алгоритм работы.  

В: Какой термодатчик можно использовать для подключения к Ардуино?  
О: Проще всего подключить DS18B20.  

В: Можно использовать аккумуляторы 18650?  
О: Да, делаете из них сборку 3S или 4S и будет работать.  

В: Как сделать чтобы Ардуино включал вентилятор?  
О: Нужно добавить четвертый транзистор и дописать код под его работу.  

В: Как заряжать аккумулятор?  
О: Зарядка в фонаре не предусмотрена. По моему опыту для многобаночного лития оптимально использовать балансировочные устройства. Самым популярным и бюджетным является IMAX B6.  

<a id="chapter-6"></a>
## Полезная информация
* [Мой сайт VOLTNIK.RU](http://voltnik.ru/)
* [Мой YouTube канал VOLTNIK](https://www.youtube.com/channel/UC4s13gPVOMQVX3P1ZpdUwjA?sub_confirmation=1)