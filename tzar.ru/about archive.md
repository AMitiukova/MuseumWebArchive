# Архив сайта ГМЗ "Царское Село" [https://tzar.ru/](https://tzar.ru/)

### Оглавление:

- [*описание архива*](#описание) 
- [*анализ архивабилити*](#анализ-архивабилити) 
- [*анализ архива*](#анализ-архива)
- [*просмотр архива*](#просмотр-архива)

## Описание
Архив должен был содержать снимок всех страниц сайта ГМЗ "Царское Село" по состоянию на 12.12.2023
Размер архивного файла составляет **19 Кб**. Очевидно, что архивация не сработала и архив сайта не сохранился.
Кроме самого архивного файла при создании архива записаны файлы индексов, логов и файл базы данных 
сайта, но размер файлов говорит об ошибках сохранения:

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\tzar.ru\images\tzar.ru.jpg"/>

___
## Анализ архивабилити
Перед архивацией с помощью инструмента [ArchiveReady](https://archiveready.com/) был проведен анализ сайта.
При предварительной оценке архивабилити перед архивацией были определены потенциально проблемные 
моменты. Надо сказать, что при первоначальном анализе сайт показывал высокие потенциальные проценты архивабилити.

Общая оценка архивабилити сайта составила **82%**;

Cамый низкий процент у показателя **доступности (Accessibility) - 44%**
Показатель снижен из-за 
    
- нехватки файла с картой сайта (sitemap),  защиты доступа для автоматических систем (роботов):

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\tzar.ru\images\ArchiveReady.com Sitemap httptzar.ru.jpg"/>

- низкой скорости ответа сайта:

 <img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\tzar.ru\images\ArchiveReady_response.jpg"/>

- неработающих ссылок на внешние ресурсы: 

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\tzar.ru\images\ArchiveReady.com InvalidLinks.jpg"/>

Процент **согласованности (Cohetion)** снижен очень незначительно и составляет **96%**
Основные причины:

- ссылки на внешние скрипты, изображения, размещенные на внешних ресурсах и ошибки кода CSS:

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\tzar.ru\images\ArchiveReadyRemoteImages.jpg"/>

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\tzar.ru\images\ArchiveReadyRemoteScript.jpg"/>

Процент **соответствия стандартам (Standards Compliance)** составляет **86%**
Снижение процентов происходит из-за несоответствия кода страницы принятым стандартам. 
- В случае с сайтом ГМЗ "Царское Село" несоответствие выявлено и в коде CSS, и HTML, множество ошибок при загрузке изображений:

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\tzar.ru\images\ArchiveReadyImageErrors.jpg"/>

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\tzar.ru\images\ArchiveReadyInvalidHTML.jpg"/>

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

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\tzar.ru\images\CWindowssystem32cmd.exe.jpg"/>

Судя по анализу сайта можно сказать, что данные архива не сохранились, кроме небольшого фрагмента текстовых данных в формате HTML.

[К оглавлению](#оглавление)
___
## Просмотр архива

При просмотре архива с помощью расширения [Replay Web Page](https://replayweb.page/) подтверждаются данные анализа архивного сайта:

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\tzar.ru\images\Archive of Home.jpg"/>

Отображается лишь меню сайта в текстовом режиме.
При попытке пройти по ссылкам в разделы сайта возникает ошибка.

<img src="C:\Users\Aleksandra\Documents\GitHub\MuseumWebArchive\tzar.ru\images\Archive of Home_.jpg"/>

что подтверждает предусмотренные анализом ошибки сохранения архива.
Для понимания причин неполного скачивания сайта необходимо изучить файл логов.

[К оглавлению](#оглавление)