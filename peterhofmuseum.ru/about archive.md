# Архив сайта ГМЗ "Петергоф" [https://peterhofmuseum.ru/](https://peterhofmuseum.ru/)

### Оглавление:

- [*описание архива*](#описание) 
- [*анализ архивабилити*](#анализ-архивабилити) 
- [*анализ архива*](#анализ-архива)
- [*просмотр архива*](#просмотр-архива)

## Описание
Архив содержит снимок всех страниц сайта ГМЗ "Петергоф" по состоянию на 11.12.2023
Размер архивного файла составляет **181207 Кб**
Кроме самого архивного файла при создании архива записаны файлы индексов, логов и файл базы данных сайта.
___
## Анализ архивабилити
Перед архивацией с помощью инструмента [ArchiveReady](https://archiveready.com/) был проведен анализ сайта.
При предварительной оценке архивабилити перед архивацией были определены потенциально проблемные моменты. 
Общая оценка архивабилити сайта составила **72%**;

Cамый низкий процент у показателя **доступности (Accessibility) - 41%**
Показатель снижен из-за 
    
- нехватки файла с картой сайта (sitemap):

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\peterhofmuseum.ru\images\ArchiveReady.com sitemap pspeterhofmuseum.ru.jpg"/>

- низкой скорости ответа сайта:

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\peterhofmuseum.ru\images\ArchiveReady.com response peterhofmuseum.ru.jpg"/>

- неработающих ссылок на внешние ресурсы: 

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\peterhofmuseum.ru\images\ArchiveReadyInvalidLinks.jpg"/>

- ошибки кэширования заголовков:

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\peterhofmuseum.ru\images\ArchiveReadyCachingHeaders.jpg"/>

Процент **согласованности (Cohetion)** снижен и составляет **76%**
Основные причины:

- ссылки на внешние скрипты, изображения, размещенные на внешних ресурсах и ошибки кода CSS:

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\peterhofmuseum.ru\images\ArchiveReady.com images peterhofmuseum.ru.jpg"/>

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\peterhofmuseum.ru\images\ArchiveReady.comHTML+CSS2peterhofmuseum.ru.jpg"/>

Процент **соответствия стандартам (Standards Compliance)** составляет **90%**
Снижение процентов происходит из-за несоответствия кода страницы принятым стандартам. 
- В случае с сайтом ГМЗ "Петергоф" несоответствие выявлено и в коде CSS, и HTML:

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\peterhofmuseum.ru\images\ArchiveReady.com HTML+CSS httpspeterhofmuseum.ru.jpg"/>

Показатель по **метаданным (Metadata)** составляет **80%**

снижение процента по метаданным вызвано 
также [ошибкой кэширования заголовков](<img%20src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\peterhofmuseum.ru\images\ArchiveReadyCachingHeaders.jpg"/>).

[К оглавлению](#оглавление)
___
## Анализ архива

Архивный файл был проанализирован с помощью утилиты командной строки, созданной 
для задач цифрового дознания, сбора данных из архивов веб-сайтов - [Metawarc](https://github.com/datacoon/metawarc)

Архив был проанализирован с помощью команды `-analyze`
в полученном ответе команды в последней строке подсчитывается общее количество файлов, 
размер архива в байтах. В перечне типов файлов перечислены все встречающиеся в архиве 
типы данных, указано количество файлов каждого типа, их общий размер и процент от общего объема.

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\peterhofmuseum.ru\images\CWindowssystem32cmd.exe.jpg"/>

Судя по анализу сайта можно сказать, что данные архива распределяются между изображениями, 
приложениями и текстом в соотношении **~60% / ~26% / ~11%**

С помощью утилиты Metawarc была также команда `-index`, записывающая все метаданные в базу данных. 
Записано более 93% файлов.
При анализе их с помощью команды `stats -mimes`, данные объединены по типам с указанием кодировок.

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\peterhofmuseum.ru\images\CWindowssystem32cmd.exeindex&amp;mimes.jpg"/>

при анализе архива с помощью команды `metawarc stats -m exts`, можно проанализировать количество и размеры файлов по расширениям:

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\peterhofmuseum.ru\images\CWindowssystem32cmd.exe_stats.jpg"/>

[К оглавлению](#оглавление)
___
## Просмотр архива

При просмотре архива с помощью расширения [Replay Web Page](https://replayweb.page/) открывается главная страница, 
корректно работает переход по разделам сайта. При переходе по разделам меню сталкиваемся с тем, 
что многие картинки не отображаются:

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\peterhofmuseum.ru\images\Archive objects.jpg"/>

Не работает модуль онлайн трансляции:

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\peterhofmuseum.ru\images\Archive online_image.jpg"/>

Возникает ошибка при переходе в некоторые разделы сайта.

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\peterhofmuseum.ru\images\Archive_plan.jpg"/>

что подтверждает предусмотренные анализом ошибки кэширования заголовков, сохранения изображений, 
скриптов и объектов, размещенных на внешних источниках.

[К оглавлению](#оглавление)