🛠 Благодаря return можно использовать результат работы функции где угодно, например в условиях или формировании новых значений. Пример ниже использует функцию с return для проверки условия — действительно ли счёт игрока больше 100:

```js
function checkScore(score) {
  return score > 100
}
var s1 = 10
var s2 = 15
var s3 = 20
if (checkScore(s1)) alert("игрок 1 проходит")
if (checkScore(s2)) alert("игрок 2 проходит")
if (checkScore(s3)) alert("игрок 3 проходит")
```

Чем вот такой вариант:

```js
var s1 = 10
var s2 = 15
var s3 = 20
if (s1 > 100) alert("игрок 1 проходит")
if (s2 > 100) alert("игрок 2 проходит")
if (s3 > 100) alert("игрок 3 проходит")
```

**Почему эффективнее?**

- если условие проверки очков изменится — его придётся писать в нескольких местах
- если условие будет состоять более чем из одной проверки? Тогда `if` усложнится и его будет сложнее понимать. Функцию, дающую ответ true или false легче читать в условном операторе.

Необходимо помнить, если выполнение функции завершилось не через `return`, то возвращаемое значение будет `undefined`;

Самый простой способ этого избежать — __всегда__ добавлять `return` с каким-либо значением перед концом функции.

<iframe title="Название — return — Дока" src="../demos/vindi-r-oVPReL/" height="150" sandbox></iframe>

- Ещё `return` останавливает выполнение функции. Обычно это ожидаемое поведение, но если про это забыть — возможны баги.

<iframe title="Название — return — Дока" src="../demos/vindi-r-aMagpW/" height="300" sandbox></iframe>