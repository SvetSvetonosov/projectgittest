#  Создаем туториал по GIT

## Инициализация репозитория

Создать пустой репозиторий Git или вновь инициализировать существующий можно параметром init:
```
git init
```

## Добавление отдельных файлов или всех файлов в область подготовленных файлов

Добавить отдельный файл в область подготовленных файлов можно параметром add с указанием имени файла. Просто замените name.md на актуальное имя:
```
git add name.md
```

## Проверка статуса репозитория

Просмотреть статус нужного репозитория можно по ключевому слову status :
```
git status
```

## Внесение изменений однострочным сообщением или через редактор

При создании коммита в репозитории можно добавить однострочное сообщение с помощью параметра commit с флагом -m . Само сообщение вводится непосредственно после флага, в кавычках:
```
git commit -m "Your short summary about the commit"
```

## Просмотр истории коммитов с изменениями

Просматривать изменения, внесённые в репозиторий, можно с помощью параметра log . Он отображает список последних коммитов в порядке выполнения. Кроме того, добавив флаг -p , вы можете подробно изучить изменения, внесённые в каждый файл.
```
git log -p
```

## Создание новой ветки и переход в неё
Создать новую ветку можно с помощью параметра branch , указав имя ветки:
```
git branch new_branch_name
```

## Изменение последнего коммита
Внести изменения в последний коммит можно параметром commit с флагом --amend . Например, вы записали изменения, внесённые в ряд файлов, и поняли, что допустили ошибку в сообщении коммита. В этом случае можете воспользоваться указанной командой, чтобы отредактировать сообщение предыдущего коммита, не изменяя его снимок:
```
git commit --amend -m "Updated message for the previous commit"
```

# Краткая инструкция по MarkDown

## Списки

Для разметки неупорядоченных списков можно использовать или `*`, или `-`, или `+`:

 * элемент 1
 - элемент 2
 + элемент ...

Вложенные пункты создаются четырьмя пробелами перед маркером пункта:

 * элемент 1
 * элемент 2
     * вложенный элемент 2.1
     * вложенный элемент 2.2
 * элемент ...

 Упорядоченный список:
 1. элемент 1
 2. элемент 2
    1. вложенный
    2. вложенный
  3. элемент ...
  4. Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse id sem consectetuer libero luctus adipiscing.

  На самом деле не важно как в коде пронумерованы пункты, главное, чтобы перед элементом списка стояла цифра любая) с точкой. Можно сделать и так:

  1. элемент 1
  0. элемент 2
  0. элемент 3
  0. элемент 4

Список с абзацами:

* Раз абзац. Lorem ipsum dolor sit amet, consectetur adipisicing elit.

* Два абзац. Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse id sem consectetuer libero luctus adipiscing.

* Три абзац. Ea, quis, alias nobis porro quos laborum minus sed fuga odio dolore natus quas cum enim necessitatibus magni provident non saepe sequi?

    Четыре абзац (Четыре пробела в начале или один tab).
    
## Горизонтальная черта

"hr" создается тремя дефисами:

---

"hr" создается тремя звездочками: 

***

## Ссылки

Это встроенная [ссылка с title элементом] (http://example.com/link "Я ссылка"). Это — [без title] (http://example.com/link).

А вот [пример][1] [нескольких][2] [ссылок][id] с разметкой как у сносок. Прокатит и [короткая запись][] без указания id.

[1]: http://example.com/ "Optional Title Here"
[2]: http://example.com/some
[id]: http://example.com/links (Optional Title Here)
[короткая запись]: http://example.com/short

Вынос длинных урлов из предложения способствует сохранению читабельности исходника. Сноски можно располагать в любом месте документа.

## Зачеркивание

В GFM добавлено зачеркивание текста: две тильды `~` до и
после текста:

~~зачеркнуто~~

## Картинки

 Чтобы вставить изображение в текст, выполните следующее:

 ![текст](имя.расширение)

 Например:

![Привет](1.jpeg)

## Цитаты

Цитаты оформляются как в емейлах, с помощью символа `>`. 
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
>
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
 > id sem consectetuer libero luctus adipiscing.

 Или более ленивым способом, когда знак `>` ставится перед каждым элементом цитаты, будь то абзац, заголовок или пустая строка:

 > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
 >
 > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
 id sem consectetuer libero luctus adipiscing.

 В цитаты можно помещать всё что угодно, в том числе вложенные цитаты:

 > ## This is a header.
 >
 > 1. This is the first list item.
 > 2. This is the second list item.
 >
 > Вложенная цитата.
 >
 > Here's some example code:
 >
 > return shell_exec("echo $input |
$markdown_script").
