### API на примере user

Не работает из коробки, необходимо как минимум правильно прописать namespace и разместить в правильных папках

Схема работы:
0. Компонент получает запрос
1. В классе компонента определяется сущность запроса, метод и передаваемые данные
2. В зависимости от настроек Mapping и наличия неORM и ORM классов происходит передача запроса соответствующим функциям
3. При получении ответа при необходимости логируется и отдается в виде JSON  
4. Отрисовывается ответ. В зависимости от типа шаблона с отладочной инфой или чистый

При правильных настройках и заполнении Mapping ORM-часть не требует создания файлов (как User). 
Все отрабатывает в OrmModules/Base.

Необходимо учитывать, что некоторые сущности Битрикс в ORM работают только на получение. 
В этом случае изменения и добавление надо обрабатывать в Modules/<Entity>.  