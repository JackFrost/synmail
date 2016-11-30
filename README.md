# synmail

Модуль для работы с почтовой системой контактных форм.

* Страница настроек /admin/config/synapse/synmail
* Страница настроек в меню находится в подпапке модуля synapse (https://github.com/politsin/synapse), поэтому модуль synapse - зависимость.
 * synmail.links.menu.yml - тут прописан parent synapse.page
 * Если данная иситуация не устраивает - в качестве парента можно использовать system.admin_config_system

## Возможности:
* Своя функция phpMail, которая правильнее чем роднаяя друпаловская, т.к. родная друпаловская неправильно прогоняет через юникод поле "фром" если название сайта на кирилице. Эту галочку всегда хорошо ткнуть если сайт крутится на osLinux.
* подставление поля "from", чтобы удобно указать от кого приходят письма, если это не должно совпадать с SEOшным названием сайта
* пропускать html - эта кнопка позволяет "своей функции phpMail" не обрезать html теги. полезно в сочетании с галочкой тут: /admin/structure/contact/settings, без этой галочки бесполезна. 
* кому полсылать: - разом добавляет получателей, чтобы не нужно было в каждую вебформу редактировать
* режим отладки - выводит в dsm() информацию которая прилетела в модуль, и информацию которая ушла письмом
* использовать свой шаблон для исходящих писем - позволяет скопировать в тему synmail.tpl.twig и настроить его как надо. 


## Как слать красивые письма:
1. Включаем галочку "Send HTML" в настройках контактных форм
2. Ставим галочку "Своя функция phpMail"
3. Ставим галочку "пропускать html"
4. Ставим галочку "использовать шаблон"
5. Копируем файл synmail.tpl.twig в свою тему оформления и верстаем его как надо.

<img src="https://github.com/politsin/help/blob/master/synmail.png?raw=true">
 
