# MuseumWebArchive
### Проект по архивации сайтов пригородных музеев Санкт-Петербурга
Архив содержит сайты музеев:
1. ГМЗ "Гатчина": [https://gatchinapalace.ru](https://gatchinapalace.ru
)
2. ГМЗ "Павловск": [https://pavlovskmuseum.ru/](https://pavlovskmuseum.ru/
)
3. ГМЗ "Петергоф": [https://peterhofmuseum.ru/](https://peterhofmuseum.ru/)
4. ГМЗ "Царское Село": [http://tzar.ru](http://tzar.ru)

Файлы с архивами доступны по [ссылке](https://cloud.mail.ru/public/6D4F/uurvpWRH4) в облаке.

Для анализа выбраны сайты пригородных музеев и дворцов Санкт-Петербурга, сотрудником одного из которых я являюсь. 
Так как сайты различные по качеству и количеству контента, уровню дизайна, анализ с точки зрения их архивабилити – 
задача интересная для понимания технической стороны этих сайтов и их возможного воспроизведения в случае необходимости.

В целом структура сайтов одинакова: они содержат новостной блок, информацию для посетителей, включая модуль продажи 
онлайн-билетов, раздел с информацией о детских мероприятиях, раздел для специалистов. Чаще всего пригородные 
музеи-заповедники имеют в своей юрисдикции несколко объектов, например, **ГМЗ "Петерегоф"**, в состав которого входят также 
дворцы и парки "Ораниенбаум" и "Александрия", **ГМЗ "Царское Село"**, включающий Александровский дворец, Приоратский дворец 
и парк в **ГМЗ "Гатчина"**, имеют подразделы этих объектов с описанием и информацией о посещении.

Контент сайтов содержит в основном изображения и текст. Лишь на сайте **ГМЗ "Петергоф"** имеется раздел с медиа-контентом, 
где представлены видеобзоры, фильмы и мультимедийные проекты.

Архивация всех сайтов произведена с помощью утилиты [wpull](https://wpull.readthedocs.io/en/master/install.html)

Для сохранения архивов сайтов запускалась команда, содержащая идентичные опции; заменялись лишь наименования папок, файлов и url:
```
wpull http://tzar.ru/ --strip-session-id --no-check-certificate --no-robots --span-hosts --page-requisites 
--sitemaps --inet4-only --timeout 20 --tries 3 --waitretry 5 --recursive 
--level inf --retry-connrefused --retry-dns-error --delete-after 
--warc-append --warc-cdx -U "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:101.0) 
Gecko/20100101 Firefox/101.0" -d -a tzar.ru.log --database sitearchive-tzar.ru.db 
--warc-file "tzar.ru" --warc-header "operator: Aleksandra Mityukova" --warc-header "downloaded-by: student" 
--domains tzar.ru --concurrent 4
```
в результате работы команды для каждого архива сохранился архивный файл `.warcz`,
содержащий архив сайта, файл `.db` с базой данных сайта, файл `.log`, 
содержащий строки логов и индекс-файл `.cdx`.

Непосредственно перед архивацией был проведен анализ сайтов на их архивабилити. По результатам
анализа мы можем сделать предварительные выводы, о том, какие компоненты сайта могут быть сохранены
некорректно или потеряны при сохранении.

URL | Overall Rating | Accessibility | Cohesion | Metadata | Standards Compliance
:--- |---:|----:|---------:|----:|---:
https://pavlovskmuseum.ru/ | 78% |    47% |   87% |   100% | 79% |
http://tzar.ru | 82% |    44% |    96% | 100% | 86% |
https://peterhofmuseum.ru/ | 72% |    41% |  76% | 80% | 90% |
https://gatchinapalace.ru | 76% |     41% |    84% | 100% | 80% |

По основным показателям общего рейтинга, видим, что сайты довольно близки: данные колеблются в пределах 10%. 
Лидирует сайт ГМЗ "Царское Село". Лучший показатель по согласованности также у него. По доступности данных три из 
четырех показывают абсолютные значения. По показателю соответствия стандартам наивысший результат у Петергофа. 
Царское на втором месте.
Если рассматривать более подробно причины снижения оценок, однако, мы увидим, что они практически у всех сайтов одинаковы:
снижение Доступности вызвано чаще всего долгим ответом сервера, соответственно для Петергофа, Гатчины и Павловска.

Подробные описания архивов и их метеданных доступны в папках репозитория.

---
<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/AMitiukova/MuseumWebArchive.git">MuseumWebArchive</a> by <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://github.com/AMitiukova">Aleksandra Mitiukova</a> is licensed under <a href="http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"></a></p>
