# NDS_Layton_Pandora_RU
В данном репозитории выкладываю наработки по переводу на русский язык Professor Layton and Pandora's Box для Nintendo DS.

# Ром на основе которого производились работы:
- 4213 - Professor Layton and Pandora's Box (Europe)
- Размер: 134 217 728 bytes
- CRC32: 27AD5247

Каждый желающий может продолжить перевод игры, для этого достаточно владеть минимальными знаниями в ромхакинге.

В папке !test_build лежит патч публичной демки версии 0.01 в которой уже вставлено:
1. Русские шрифты с исправленными таблицами ширины. Поддерживают кодировку win1251.
2. Русская клавиатура ввода имени / названия профиля.
3. Перерисованная графика главного меню и титульного экрана.
4. Плашки с именами персонажей, отображаемые на экранах диалогов (согласно глоссарию).
5. Переведены около 250 текстовых файлов из папки data_lt2\txt\en\txt.plz
	- вступительная часть игры
	- имена персонажей, название событий и прочий текст в меню бонусов
	- описание некоторых событий

Все дальнейшие работы можно производить на основе рома с утановленным по инструкции патчем.

Редактирование текста
===========================================
Тектст в роме хранится в двух форматах:
простой .txt - можно работать в блокноте или лубом другом удобном текстовом редакторе, например notepad++.
скрипты событий в .gds - есть плагин для autodump.

Где лежит внутри рома:
- data_lt2\event	- скрипты в формате .gds, упакованы в архивы .plz
- data_lt2\nazo	- головоломки и всё, что связано с ними. Формат .txt, упакованы в архивы .plz
- data_lt2\place	- текст. Формат .txt, упакованы в архивы .plz
- data_lt2\rc	- текст. Формат .txt, упакованы в архивы .plz
- data_lt2\script	- скрипты в формате .gds, упакованы в архивы .plz
- data_lt2\txt	- текст. Формат .txt, упакованы в архивы .plz / частично переведён


Редактирование графики:
===========================================
Вся графика хранится в двух основных форматах - .arc и .arj. Зачастую в одном и том же файле содержится несколько изображений.
Графические форматы полноценно поддерживаются Tinke (экспорт и импорт в/из .bmp и .png)
Практически вся графика, требующая редактирования вынута и лежит отдельным архивом в папке GFX.

Шрифты:
===========================================
Расположение внутри рома:
- data_lt2\font

Шрифты fontevent.nftr и fontq.nftr сгенерированы с нуля, есть поддержкой кириллицы в формате Windows1251.
Таблица ширины глифов отредактирована как внутри самих .nftr, так и в оверлее overlay09_0002.bin.

Расположение таблиц в распакованном оверлее (обратно сжимать перед вставкой в ром не обязательно):
- fontevent.ntft	- overlay09_0002.bin /unp 0x01f1158 - ABCD...
- fontq.ntft	- overlay09_0002.bin /unp 
