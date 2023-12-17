# Архив сайта ГМЗ "Павловск" [https://pavlovskmuseum.ru/](https://pavlovskmuseum.ru/)

### Оглавление:

- [*описание архива*](#описание) 
- [*анализ архивабилити*](#анализ-архивабилити) 
- [*анализ архива*](#анализ-архива)
- [*просмотр архива*](#просмотр-архива)

## Описание
Архив содержит снимок всех страниц сайта ГМЗ "Павловск" по состоянию на 11.12.2023
Размер архивного файла составляет **144975 Кб**
Кроме самого архивного файла при создании архива записаны файлы индексов, логов и файл базы данных сайта.
___
## Анализ архивабилити
Перед архивацией с помощью инструмента [ArchiveReady](https://archiveready.com/) был проведен анализ сайта.
При предварительной оценке архивабилити перед архивацией были определены потенциально проблемные моменты. 
Общая оценка архивабилити сайта составила **78%**;

Cамый низкий процент у показателя **доступности (Accessibility) - 47%**
Показатель снижен из-за 
    
- нехватки файла с картой сайта (sitemap):

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\pavlovskmuseum.ru\images\ArchiveReady_sitemaps.jpg"/>

- недостаточно высокой скорости ответа сайта:

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\pavlovskmuseum.ru\images\ArchiveReady.com response httpspavlovskmuseum.ru.jpg"/>

- неработающих ссылок на внешние ресурсы: 

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\pavlovskmuseum.ru\images\ArchiveReady_invalid links.jpg"/>

- защиты доступа для автоматических систем (роботов):

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\pavlovskmuseum.ru\images\ArchiveReady_robots_pavlovsk.jpg"/>

Процент **согласованности (Cohetion)** снижен незначительно и составляет **87%**
Основные причины:

- ссылки на внешние скрипты:

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\pavlovskmuseum.ru\images\ArchiveReadyRemoteScripts.jpg"/>

- использование изображений, размещенных на внешних ресурсах:

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\pavlovskmuseum.ru\images\ArchiveReady_remote image.jpg"/> 

Процент **соответствия стандартам (Standards Compliance)** составляет **79%**
Снижение процентов происходит из-за несоответствия кода страницы принятым стандартам. 
- В случае с сайтом ГМЗ "Павловск" несоответствие выявлено и в коде CSS, и HTML:

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\pavlovskmuseum.ru\images\ArchiveReadyHTML.jpg"/>

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\pavlovskmuseum.ru\images\ArchiveReadyCSS.jpg"/>

- кроме того, найдены ошибки воспроизведения изображений:

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\pavlovskmuseum.ru\images\ArchiveReady_standards.jpg"/>

Показатель по **метаданным (Metadata)** составляет **100%**

[К оглавлению](#оглавление)
___
## Анализ архива

Архивный файл был проанализирован с помощью утилиты командной строки, созданной 
для задач цифрового дознания, сбора данных из архивов веб-сайтов - [Metawarc](https://github.com/datacoon/metawarc)

Архив был проанализирован с помощью команды `-analyze`
в полученном ответе команды в последней строке подсчитывается общее количество файлов, 
размер архива в байтах. В перечне типов файлов перечислены все встречающиеся в архиве 
типы данных, указано количество файлов каждого типа, их общий размер и процент от общего объема.

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\pavlovskmuseum.ru\images\CWindowssystem32cmd.exe.jpg"/>

Судя по анализу сайта можно сказать, что большую часть архива ~ 95% составляют изображения разных форматов, 
Практически весь остальной контент составляет текст - 4.2%

С помощью утилиты Metawarc была также команда `-index`, записывающая все метаданные в базу данных. 
Однако записано меньше 60% файлов.

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\pavlovskmuseum.ru\images\CWindowssystem32cmd.exe_index.jpg"/>

из-за значительного перекоса по типу контента, с помощью команды `metawarc stats -m mimes` 
проанализирован размер и количество каждого типа [маймов](https://ru.wikipedia.org/wiki/MIME).

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\pavlovskmuseum.ru\images\CWindowssystem32cmd.exe_stats.mimes.jpg"/>

по саммари видно, что большую часть архива составляют изображения, причем большая часть это `.jpeg`,  а остальные - это `.png` 
всего один элемент `x-icon`. Типы текстовых данных расписаны не только по форматам, но указаны также кодировки текста, 
что может быть полезно в случае извлечения и сохранения текста отдельно от контента сайта.

при анализе архива с помощью команды `metawarc stats -m exts`, видим, что показатели не отличаются:

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\pavlovskmuseum.ru\images\CW stats.jpg"/>

[К оглавлению](#оглавление)
___
## Просмотр архива

При просмотре архива с помощью расширения [Replay Web Page](https://replayweb.page/) открывается главная страница, 
корректно работает переход по разделам сайта. При переходе по разделам меню сталкиваемся с тем, 
что многие картинки не отображаются:
<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\pavlovskmuseum.ru\images\Archive of История  ReplayWeb.page.jpg"/>

Возникает ошибка при переходе в раздел "Специалистам", "Вакансии" и отсутствует корректный переход на внешние сайты, где размещен
представленный контент:

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\pavlovskmuseum.ru\images\Archive of  ReplayWeb.page.jpg"/>

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\pavlovskmuseum.ru\images\Archive of Обзорные экскурсии  ReplayWeb.page.jpg"/>

что подтверждает предусмотренные анализом ошибки при архивировании сайтов со ссылками на контент, размещенный на внешних источниках.

[К оглавлению](#оглавление)