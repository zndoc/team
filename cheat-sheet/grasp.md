GRASP
===

**GRASP** — шаблоны, используемые в объектно-ориентированном проектировании для решения общих задач по назначению ответственностей классам и объектам. 

## Информационный эксперт (Information Expert)

Шаблон определяет базовый принцип распределения ответственностей:

> Ответственность должна быть назначена тому, кто владеет максимумом необходимой информации для исполнения — информационному эксперту.

Локализация же ответственностей, проводимая согласно шаблону:

* Повышает
	* Инкапсуляцию;
	* Простоту восприятия;
	* Готовность компонентов к повторному использованию; 
* Снижает
	* степень связности.

## Создатель (Creator)

Класс должен создавать экземпляры тех классов, которые он может:

* Содержать или агрегировать
* Записывать
* Использовать
* Инициализировать, имея нужные данные

Альтернатива — шаблон «Фабрика» (создание объектов концентрируется в отдельном классе).

## Контроллер (Controller)

Отвечает за операции, запросы на которые приходят от пользователя, 
и может выполнять сценарии одного или нескольких вариантов использования (например, создание и удаление);

Не выполняет работу самостоятельно, а делегирует компетентным исполнителям;

Может представлять собой:

* Систему в целом
* Подсистему
* Корневой объект
* Устройство

## Слабое зацепление (Low Coupling)

«Степень зацепления» — мера неотрывности элемента от других элементов (либо мера данных, имеющихся у него о них).

«Слабое» зацепление является оценочной моделью, которая диктует, как распределить обязанности, которые необходимо поддерживать.

«Слабое» зацепление — распределение ответственностей и данных, обеспечивающее взаимную независимость классов. Класс со «слабым» зацеплением:

* Имеет слабую зависимость от других классов
* Не зависит от внешних изменений (изменение в одном классе оказывает слабое влияние на другие классы)
* Прост для повторного использования

## Высокая связность (High Cohesion)

Связность класса — это оценочная модель, направленная на удержание объектов должным образом сфокусированными, управляемыми и понятными. Высокая связанность обычно используется для поддержания низкого зацепления. Высокая связанность означает, что обязанности данного элемента тесно связаны и сфокусированы. Разбиение программ на классы и подсистемы является примером деятельности, которая увеличивает связанность системы.

И наоборот, низкая связанность — это ситуация, при которой данный элемент имеет слишком много несвязанных обязанностей. Элементы с низкой связанностью часто страдают от того, что их трудно понять, трудно использовать, трудно поддерживать.

Связность класса — мера сфокусированности предметных областей его методов:

«Высокая» связность — сфокусированные подсистемы (предметная область определена, управляема и понятна);
		
«Низкая» связность — абстрактные подсистемы. 

Затруднены:

* Восприятие
* Повторное использование
* Поддержка
* Устойчивость к внешним изменениям

## Полиморфизм (Polymorphism)

Устройство и поведение системы:

* Определяется данными
* Задано полиморфными операциями её интерфейса

## Чистая выдумка (Pure Fabrication)

Не относится к предметной области, но:

* Уменьшает зацепление
* Повышает связность
* Упрощает повторное использование

«Pure Fabrication» отражает концепцию сервисов в модели проблемно-ориентированного проектирования.

Пример задачи: Не используя средства класса «А», внести его объекты в базу данных.

Решение: Создать класс «Б» для записи объектов класса «А» (смотрите также: «Data Access Object»).

## Посредник (Indirection)

Слабая связность между элементами системы (и возможность повторного использования) обеспечивается назначением промежуточного объекта их посредником.

Пример: В архитектуре Model-View-Controller, контроллер (англ. controller) ослабляет связность данных (англ. model) с их представлением (англ. view).

## Устойчивость к изменениям (Protected Variations)

Шаблон защищает элементы от изменения другими элементами (объектами или подсистемами) с помощью вынесения взаимодействия в фиксированный интерфейс, через который (и только через который) возможно взаимодействие между элементами. Поведение может варьироваться лишь через создание другой реализации интерфейса. 