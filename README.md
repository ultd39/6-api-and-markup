# Работа с API, верстка и анимации

Особенности:
* Выпадающий список более крупных фотографий - обычным списком;
* Переключение стрелками (без Ctrl). Закрытие предпросмотра по Esc;
* Переключение на другие страницы - под поисковой строкой;
* «Раздвижные двери».

Баги:
* Пока нет возможности протестить под браузеры, отличные от Chrome;
* Предпросмотр закрывается, если на первом изображении нажать стрелку вправо. То же самое с последним;
* При выборе картинки внизу страницы, при уже открытом предпросмотре, страница «дергается» во время его «схлопывания» и плавному переходу к новому предпросмотру. Пока для этого установлен тысячепиксельный костыль.

Доделать:
* Прелоалер на изображение в предпросмотре;
* Адекватную анимацию к предпросмотру;
* Поддержку остальных браузеров;
* Сделать какой-нибудь футер;
* Кнопку «крест» в предпросмотре сделать картинкой.

Вопросы:
* Использовал два разных метода для создания шаблонов:
1. Генерация средствами jQuery ( $(&rsquo;&lt;tag/&gt;) ).
2. Использование скрытого шаблона в разметке и последующая вставка в него данных.
Как было бы лучше генерировать разметку на клиенте? Понятно, что «серебряной пули» не существует, — в том и другом методе есть свои преимущества и недостатки, касаемые скорости работы, «замусоренности» кода и др. Или, может быть, есть еще методы генерации разметки из шаблонов на клиенте?

* Как можно избавиться от «передергивания» страницы при скрытии прежнего предпросмотра? Может у кого-нибудь будут какие-нибудь идеи?
Потратил на это три дня — так ничего не смог придумать. В принципе, можно обойтись без анимации, и мгновенно  переходить к предпросмотру, но так получается не очень красиво.

* Стрелки в&nbsp;предпросмотре сделаны &lt;i&gt; вложенным&nbsp;в &lt;div&gt;. Вопрос в&nbsp;том, правильнее было&nbsp;бы, со&nbsp;стороны семантики, использовать для этих целей тег &lt;button&gt;? Или это не&nbsp;имеет никакого значения? Ведь, на&nbsp;самом деле, этот элемент здесь играет роль кнопки.

* Ну, и по организации кода — очень хочу услышать какие-либо рекомендации.