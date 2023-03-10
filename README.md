# Лабораторная работа #3
#### Вариант 676455
## Разработать приложение на базе JavaServer Faces Framework, которое осуществляет проверку попадания точки в заданную область на координатной плоскости.

Приложение должно включать в себя 2 facelets-шаблона - стартовую страницу и основную страницу приложения, а также набор управляемых бинов (managed beans), реализующих логику на стороне сервера.

### Стартовая страница должна содержать следующие элементы:

"Шапку", содержащую ФИО студента, номер группы и номер варианта.
Интерактивные часы, показывающие текущие дату и время, обновляющиеся раз в 9 секунд.
Ссылку, позволяющую перейти на основную страницу приложения.

### Основная страница приложения должна содержать следующие элементы:

<ul>
<li>Набор компонентов для задания координат точки и радиуса области в соответствии с вариантом задания. Может потребоваться использование дополнительных библиотек компонентов - <a href="http://www.icesoft.org/java/projects/ICEfaces/overview.jsf">ICEfaces</a> (префикс "ace") и <a href="http://www.primefaces.org/">PrimeFaces</a> (префикс "p"). Если компонент допускает ввод заведомо некорректных данных (таких, например, как буквы в координатах точки или отрицательный радиус), то приложение должно осуществлять их валидацию.</li>
<li>Динамически обновляемую картинку, изображающую область на координатной плоскости в соответствии с номером варианта и точки, координаты которых были заданы пользователем. Клик по картинке должен инициировать сценарий, осуществляющий определение координат новой точки и отправку их на сервер для проверки её попадания в область. Цвет точек должен зависить от факта попадания / непопадания в область. Смена радиуса также должна инициировать перерисовку картинки.</li>
<li>Таблицу со списком результатов предыдущих проверок.</li>
<li>Ссылку, позволяющую вернуться на стартовую страницу.</li>
</ul>

### Дополнительные требования к приложению:

<ul>
<li>Все результаты проверки должны сохраняться в базе данных под управлением СУБД <strike>Oracle</strike> <b>PostgreSQL</b>.</li>
<li>Для доступа к БД необходимо использовать <b>ORM EclipseLink</b>.</li>
<li>Для управления списком результатов должен использоваться <b>Application-scoped Managed Bean</b>.</li>
<li>Конфигурация управляемых бинов должна быть задана <b>с помощью аннотаций</b>.</li>
<li>Правила навигации между страницами приложения должны быть заданы <b>в отдельном конфигурационном файле</b>.</li>
</ul>

<img style="border: 1px solid;" src="https://i.ibb.co/27fjGFn/areas.png" alt="areas">

### Вопросы к защите лабораторной работы:

<ol>
<li>Технология JavaServer Faces. Особенности, отличия от сервлетов и JSP, преимущества и недостатки. Структура JSF-приложения.</li>
<li>Использование JSP-страниц и Facelets-шаблонов в JSF-приложениях.</li>
<li>JSF-компоненты - особенности реализации, иерархия классов. Дополнительные библиотеки компонентов. Модель обработки событий в JSF-приложениях.</li>
<li>Конвертеры и валидаторы данных.</li>
<li>Представление страницы JSF на стороне сервера. Класс UIViewRoot.</li>
<li>Управляемые бины - назначение, способы конфигурации. Контекст управляемых бинов.</li>
<li>Конфигурация JSF-приложений. Файл faces-config.xml. Класс FacesServlet.</li>
<li>Навигация в JSF-приложениях.</li>
<li>Доступ к БД из Java-приложений. Протокол JDBC, формирование запросов, работа с драйверами СУБД.</li>
<li>Концепция ORM. Библиотеки ORM в приложениях на Java. Основные API. Интеграция ORM-провайдеров с драйверами JDBC.</li>
<li>Библиотеки ORM Hibernate и EclipseLink. Особенности, API, сходства и отличия.</li>
<li>Технология JPA. Особенности, API, интеграция с ORM-провайдерами.</li>
</ol>
