# Прокрутка

<<<<<<< HEAD
Событие прокрутки `scroll` позволяет реагировать на прокрутку страницы или элемента. Есть много хороших вещей, которые при этом сделать.
=======
The `scroll` event allows to react on a page or element scrolling. There are quite a few good things we can do here.
>>>>>>> 8c30654f694fe8682f5631809980be931ee4ed72

Например:
- Показать/скрыть дополнительные элементы управления или информацию, основываясь на том, в какой части документа находится пользователь.
- Подгрузить данные, когда пользователь прокручивает страницу вниз до конца.

Вот небольшая функция для отображения текущей прокрутки:

```js autorun
window.addEventListener('scroll', function() {
  document.getElementById('showScroll').innerHTML = pageYOffset + 'px';
});
```

```online
В действии:

Текущая прокрутка = <b id="showScroll">прокрутите окно</b>
```

Событие `scroll` работает как на `window`, так и на других элементах, на которых включена прокрутка.

## Предотвращение прокрутки

<<<<<<< HEAD
Как можно сделать что-то непрокручиваемым?

Нельзя предотвратить прокрутку, используя `event.preventDefault()` в обработчике `onscroll`, потому что он срабатывает *после* того, как прокрутка уже произошла.

Но можно предотвратить прокрутку, используя `event.preventDefault()` на событии, которое вызывает прокрутку, например, на событии `keydown` для клавиш `key:pageUp` и `key:pageDown`.
=======
How do we make something unscrollable?

We can't prevent scrolling by using `event.preventDefault()` in `onscroll` listener, because it triggers *after* the scroll has already happened.

But we can prevent scrolling by `event.preventDefault()` on an event that causes the scroll, for instance `keydown` event for `key:pageUp` and `key:pageDown`.
>>>>>>> 8c30654f694fe8682f5631809980be931ee4ed72

Если поставить на них обработчики, в которых вызвать `event.preventDefault()`, то прокрутка не начнётся.

<<<<<<< HEAD
Способов инициировать прокрутку много, поэтому более надёжный способ -- использовать CSS, свойство `overflow`.
=======
There are many ways to initiate a scroll, so it's more reliable to use CSS, `overflow` property.
>>>>>>> 8c30654f694fe8682f5631809980be931ee4ed72

Вот несколько задач, которые вы можете решить или просмотреть, чтобы увидеть применение `onscroll`.
