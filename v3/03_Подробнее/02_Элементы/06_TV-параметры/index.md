TV-параметр в Evolution CMS - элемент (поле), который содержит определенную информацию для текущей страницы.

TV-параметры позволяют добавить к документу дополнительную информацию, которую затем можно использовать наравне с основными параметрами. Они имеют различные типы и в зависимости от этого меняется их поведение и внешний вид. Значение параметра можно вывести на страницу или передать сниппету для дальнейшей обработки.

## Для чего нужен TV-параметр?

TV-параметр нужен для упорядочненного и логичного хранения информации на сайте. 

Представьте, что на сайте есть 2 типа материалов - товары и новости. Для товара можно создать параметры, в одном из которых будет храниться цена, а в другом фотография. А для новостей создать другие параметры - теги и сюжет.

Зачастую TV-параметры используются для создания SEO-полей наподобие meta description, keywords и т.д.

## Гибкость и простота ##
Параметры привязываются к шаблонам, и это позволяет в зависимости от типа материала задавать абсолютно разные поля для контента.

### Пример параметра:

[\*pagetitle\*]  -  вызов параметра в шаблоне, который вернет заголовок страницы. Чаще всего он используется для вывода title:
```
<head>
<title>[*pagetitle*]</title>
</head>
```

Все параметры можно разделить на основные, системные и пользовательские.

## Основные параметры: ##

Список основных параметров заранее определен в Evolution CMS  и содержит основную информацию о документе. Большую часть из них можете увидеть при создании и редактировании любого документа.

### Наиболее часто используемые: ###

- **[\*pagetitle\*]** - заголовок документа
- **[\*longtitle\*]** - расширенный заголовок документа
- **[\*description\*]** - описание документа
- **[\*introtext\*]** - аннотация документа
- **[\*content\*]** - содержимое документа
- **[\*id\*]** - идентификатор (номер) документа
- **[\*parent\*]** - номер (ID) родительского документа
- **[\*pub_date\*]** - дата публикации дкоумента
- **[\*unpub_date\*]** - дата завершения публикации
- **[\*createdby\*]** - Идентификатор пользователя создавшего документ
- **[\*createdon\*]** - Дата создания документа
- **[\~идентификатор\~]** - URL документа по указанному идентификатору

Стоит отдельно упомянуть о том, что параметры можно сочетать. В особенности это актуально для создания ссылок на разные документы с помощью параметра **[\~идентификатор\~]**. В качестве идентификатора можно также задать параметр.

**[\~[\*id\*]\~]** -Вывести ссылку на текущий документ.

**[\~[\*parent\*]\~]** - Вывести ссылку на родителя текущего документа.

### Дополнительные

- **[\*alias\*]** - псевдоним документа
- **[\*editedby\*]** - идентификатор пользователя, редактировавшего документ
- **[\*editedon\*]** - дата редактирования документа
- **[\*type\*]** - тип ресурса (документ, папка или ссылка)
- **[\*contentType\*]** - тип содержимого (например, text/html)
- **[\*published\*]** - опубликован ли документ (1|0)
- **[\*isfolder\*]** - является ли документа папкой (1|0)
- **[\*richtext\*]** - используется ли при редактировании документа визуальный редактор
- **[\*template\*]** - номер (ID) используемого шаблона для документа
- **[\*menuindex\*]** - порядковый номер отображения в меню
- **[\*searchable\*]** - доступен ли документ для поиска (1|0)
- **[\*cacheable\*]** - Кэшируется ли документ (1|0)
- **[\*deleted\*]** - документ удален (1|0)
- **[\*deletedby\*]** - идентификатор пользователя удалившего документ
- **[\*menutitle\*]** - заголовок меню.
- **[\*donthit\*]** - Слежение за количеством посещений отключено (1|0)
- **[\*haskeywords\*]** - Документ содержит ключевые слова (1|0)
- **[\*hasmetatags\*]** - Документ имеет метатеги (1|0)
- **[\*privateweb\*]** - Документ входит в частную группу пользовательских документов (1|0)
- **[\*privatemgr\*]** - Документ входит в частную группу менеджерских документов (1|0)
- **[\*content_dispo\*]** - Вариант выдачи содержимого (1 - для отображения | 0 - для скачивания)
- **[\*hidemenu\*]** - Документ не отображается в меню (1|0)
- **[\*alias_visible\*]** - Участвует ли документ в формировании URL(1|0)

### Системные параметры

Параметры, которые отображают системные данные

- **[^qt^]** - время на запросы к базе данных
- **[^q^]** - запросов к базе данных
- **[^p^]** - время на работу PHP скриптов
- **[^t^]** - общее время на генерацию страницы
- **[^s^]** - источник содержимого (база или кэш)
- **[^m^]** - количество потребляемой памяти 

#### Пример: 

```
Memory : [^m^], 
MySQL: [^qt^], [^q^] request(s), 
PHP: [^p^], 
Total time: [^t^], 
Document from [^s^]. 
```

### Пользовательские TV-параметры

Пользовательские параметры создаются программистом вручную, исходя из опыта и структуры сайта.

## Создание и редактирование TV-параметра

Для создания параметра необходимо нажать на ссылку "Элементы - Параметры (TV)" и выбрать "Новый параметр (TV)".

![пример](https://raw.githubusercontent.com/0test/evo-newdocs/main/v3/03_%D0%9F%D0%BE%D0%B4%D1%80%D0%BE%D0%B1%D0%BD%D0%B5%D0%B5/02_%D0%AD%D0%BB%D0%B5%D0%BC%D0%B5%D0%BD%D1%82%D1%8B/06_TV-%D0%BF%D0%B0%D1%80%D0%B0%D0%BC%D0%B5%D1%82%D1%80%D1%8B/tv_create.png)

### Назначение полей

- **Имя параметра** - используется для вызова TV-параметра. Можно использовать как английский так и русский язык, а также дефис и знак подчеркивания. Пробел использовать нельзя!
- **Заголовок** - используется для названия TV-параметра в документе при редактировании.
- **Описание** - используется для более расширенной информации о параметре в документе при редактировании, а также в общем списке TV-параметров.
- **Тип ввода** - определяет вид получаемой информации. В зависимости от выбранного типа интерфейс меняется. Более подробно смотрите "Типы ввода".
- **Значение по умолчанию** - определеяет значение TV-параметра по умолчанию при редактировании документа.
- **Возможные значения** - используются в некоторых типах ввода (например Radio Options, Check Box) для предоставления вариантов выбора. Более подробно смотрите Определение значений TV-параметра.
- **Визуальный компонент** - определеяет вариант вывода TV-параметра на страницу сайта. Более подробно смотрите Вид TV-параметра.
- **Порядок в списке** - определяет порядок TV-параметра в документе.
- **"Замок" в имени параметра** - если включить флажок, то никто, кроме администраторов не сможет редактировать этот TV-параметр.

### Типы ввода ###

- **Text** - поле ввода.
Возможные значения не используются. Значение по умолчанию автоматически записывается в поле при первом редактировании.

- **Raw Text, Raw Textarea** - устарели и не рекомендуются к использованию. 
Вместо них рекомендуется использовать Textarea и Textarea (Mini).

- **Textarea и Textarea (Mini)** - текстовое поле. Возможные значения не используются. Значение по умолчанию автоматически записывается в поле при первом редактировании.

- **RichText** - поле с визуальным редактором.
Возможные значения не используются. Значение по умолчанию автоматически записывается в поле при первом редактировании.

- **DropDown List Menu** - раскрывающийся список.
Поле "Возможные значения" задает список значений и определеляется специальным форматом. Более подробно смотрите Определение значений TV-параметра. Значение по-умолчанию определяет выбранный пункт при первом редактировании.

- **Listbox (Single-Select) и Listbox (Multi-Select)** - список множественного выбора.
Single-Select и Multi-Select отличаются только тем, что в первом варианте можно выбрать одно значение, а во втором несколько (с использование Ctrl).
Поле "Возможные значения" задает конечный список значений и определеляется специальным форматом. Более подробно смотрите Определение значений TV-параметра. Значение по умолчанию определяет выбранный пункт при первом редактировании.

- **Radio Options** - переключатели.
Поле Возможные значения задает конечный список значений и определеляется специальным форматом. Более подробно смотрите Определение значений TV-параметра. Значение по умолчанию определяет выбранный пункт при первом редактировании.

- **Check Box** - флажки.
Поле Возможные значения задает конечный список значений и определеляется специальным форматом. Более подробно смотрите Определение значений TV-параметра. Значение по умолчанию определяет выбранный пункт при первом редактировании.

- **Image** - изображение.
При нажатии кнопки "Вставить" открывается файловый менеджер, который позволяет выбрать необходимое изображение и загрузить его.
Возможные значения не используются. Значение по умолчанию автоматически записывается в поле при первом редактировании. 

- **File** - файл.
При нажатии кнопки "Вставить" открывается файловый менеджер, который позволяет выбрать необходимый файл и загрузить его.
Возможные значения не используются. Значение по умолчанию автоматически записывается в поле при первом редактировании.

- **URL** - ссылка.
Возможные значения не используются. Значение по умолчанию автоматически записывается в поле при первом редактировании.

- **Email** - электронная почта.
Возможные значения не используются. Значение по умолчанию автоматически записывается в поле при первом редактировании.

- **Number** - число.
Возможные значения не используются. Значение по умолчанию автоматически записывается в поле при первом редактировании.

- **Date** - дата.
Первая кнопка вызывает календарик, с помощью которого можно выбрать дату. Вторая кнопка стирает дату.
Возможные значения не используются. Значение по умолчанию автоматически записывается в поле при первом редактировании.

### Определение значений TV-параметра ###

Настройкой "Возможные значения" определяются варианты для таких параметров как DropDown List Menu, Listbox,Check Box и Radio Options.

Формат определения значений следующий:
```
параметр1==значение1||параметр2==значение2||параметр3==значение3
```
Разделитель "==" используется для разделения отображаемого и фактического значения, а разделитель "||" разделяет значения между собой.

Если фактические и отображаемые значения совпадают, то можно использовать упрощенный вариант записи:
```
значение1||значение2||значение3
```
### Пример ###

Тип ввода: DropDown List Menu
Возможные значения:
```
Красный==#FF0000||Зеленый==#00FF00||Синий==#0000FF
```

Когда пользователь будет редактировать документ, то увидит выпадающий список со значениями "Красный, Зеленый, Синий". При выборе значения и сохранения документа в базу сохранится одно из значений - #FF0000, #00FF00 или #0000FF.
