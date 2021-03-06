13. Применение необычных типов данных
==============

### Контрольный список

#### Структуры 

+ Используете ли вы структуры вместо отдельных переменных для организации и манипуляции группами взаимосвязанных данных? 
+ Рассматривали ли вы создание класса как альтернативу использованию структуры? 

#### Глобальные данные 

+ Действительно ли все переменные объявлены локально или в области видимости класса, если только они не обязательно должны быть глобальными? 
+ Различаются ли в соглашениях по именованию переменных локальные, классовые и глобальные данные? 
+ Документированы ли все глобальные переменные? 
+ Свободен ли код от псевдоглобальных данных — мамонтообразных объектов, содержащих мешанину из данных, передающихся в каждый метод? 
+ Используются ли методы доступа вместо глобальных данных? 
+ Организованы ли данные и методы доступа к ним в классы? 
+ Предоставляют ли методы доступа уровень абстракции, независимый от реализации используемого типа данных? 
+ Находятся ли все методы доступа на одном уровне абстракции? 

#### Указатели 

+ Изолированы ли операции с указателями в методах? 
+ Корректны ли обращения к указателям или они могут быть «висячими»? 
+ Проверяет  ли  код  корректность  указателей  перед  их  использованием?
+ Проверяется ли корректность переменной, на которую ссылается указатель, перед  ее  использованием?
+ Присваивается  ли  указателям  пустое  значение  после  их  освобождения?
+ Использует  ли  код  все  необходимые  для  читабельности  переменные-указатели?
+ Освобождаются  ли  указатели  в  связных  списках  в  правильном  порядке?
+ Выделяет  ли  программа  «резервный  парашют»  памяти,  чтобы  иметь  возможность  аккуратно  завершить  выполнение  в  случае  нехватки  памяти?
+ Используются  ли  указатели  только  как  последнее  средство,  когда  другие методы  неприменимы?

### Ключевые моменты

+ Структуры  могут  помочь  сделать  программы  менее  сложными,  упростить  их понимание  и  сопровождение.
+ Принимая решение использовать структуру, подумайте, не будет ли класс подходить  лучше.
+ Работа  с  указателями  чревата  ошибками.  Обезопасьте  себя,  используя  методы или  классы  для  доступа  к  ним  и  практику  защитного  программирования.
+ Избегайте  глобальных  переменных  не  только  потому,  что  они  опасны,  но  и потому  что  их  можно  заменить  чем#то  лучшим.
+ Если  вы  не  можете  отказаться  от  глобальных  переменных,  работайте  с  ними через методы доступа. Эти методы предоставляют все то же и даже больше, что и  глобальные  переменные