Jekyll

#### Условные конструкции:

{% if var <= 1 %}...{% elsif var > 1 and var < 5%}...{% else %}...{% endif %}

if x.array contains y - содержит ли массив. Работает также и со строчками.

{% case var %} - проверка переменной
    {% when 'x' %} - если переменная равна x
        ...
    {% when 'y' %}
        ...
    {% else %}
        ...
{% endcase %}

#### Массивы

.size - размер массива.

#### Циклы
{% for item in array %}
    {% if item.x %}
        {% continue %} //Переход на следующую интерацию
    {% endif %}
    ...
{% endfor %}

{% for item in array limit:2 offset:2 %} - лимит интераций (от 1), стартовая интерация (от 0)

forloop.length - длинна цикла
forloop.index - индекс текущей интерации (отсчёт от единицы)

#### Переменные
{% assign var = 'text, text, text' %} - создание текстовой переменной
{% assign var = false %} - создание булевой переменной
{% capture var %}{{ item.title | handleize }}-{{ i }}-color{% endcapture %} - продвинутое присвоение значения
