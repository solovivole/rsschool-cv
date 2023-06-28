# **Ivan Solovey**

![Моё фото](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSpRWMmhdZR82GUCkWccw1Pc4_m4N1MLS9f1w&usqp=CAU)

***

### Контакты
* **Почта**: l3aho98@gmail.com
* **Телефон**: +7 (654) 321-09-87
* **Телеграм**: @telegramtest

***

### Обо мне
Мне *25 лет*, *инженер* по образованию. Благодаря университетскому курсу информатики открыл для себя программирование. После окончания университета неоднократно возвращался к самостоятельному изучению то вёрстки, то пайтона, то ещё чего-то, даже записывался на *stage1* два года назад, но тогда в себя не поверил и заочно решил, что не справлюсь. Серьёзно заниматься программированием начал год назад с курса по SQL на степике. Затем перешел на серию курсов с того же степика по пайтону и вот последние 6 месяцев проходил их. Заниматься самостоятельно по мини-курсам мне нравится, но я понимаю, что этого недостаточно, чтобы стать программистом, а начать свой проект всё никак не хватало воли. Как будто ваш курс это то что мне надо. Надеюсь и пайтон в будущем найду где применить.

***

### Языки
* **python**;
* **SQL**;
* Думаю, основы **HTML** и **CSS** не выветрились полностью из моей головы, но надо вспоминать.

***

### Примеры кода

```Python
def sudoku(puzzle):
    def filter_row(puzzle):
        for y in range(len(puzzle)):
            tmp = []
            for x in range(len(puzzle[y])):
                if isinstance(puzzle[y][x], int):
                    tmp.append(puzzle[y][x])

            for x in range(len(puzzle[y])):
                if isinstance(puzzle[y][x], set):
                    for d in tmp:
                        if d in puzzle[y][x]:
                            puzzle[y][x].remove(d)
                    if len(puzzle[y][x]) == 1:
                        puzzle[y][x] = puzzle[y][x].pop()
        return puzzle

    def filter_col(puzzle):
        for x in range(len(puzzle)):
            tmp = []
            for y in range(len(puzzle[x])):
                if isinstance(puzzle[y][x], int):
                    tmp.append(puzzle[y][x])

            for y in range(len(puzzle[x])):
                if isinstance(puzzle[y][x], set):
                    for d in tmp:
                        if d in puzzle[y][x]:
                            puzzle[y][x].remove(d)
                    if len(puzzle[y][x]) == 1:
                        puzzle[y][x] = puzzle[y][x].pop()
        return puzzle

    def filter_square(puzzle, px, py):
        tmp = []
        for y in range(py*3, py*3 + 3):
            for x in range(px*3, px*3 + 3):
                if isinstance(puzzle[y][x], int):
                    tmp.append(puzzle[y][x])

        for y in range(py*3, py*3 + 3):
            for x in range(px*3, (px+1)*3):
                if isinstance(puzzle[y][x], set):
                    for d in tmp:
                        if d in puzzle[y][x]:
                            puzzle[y][x].remove(d)
                    if len(puzzle[y][x]) == 1:
                        puzzle[y][x] = puzzle[y][x].pop()
        return puzzle



    for y in range(len(puzzle)):
        tmp = set(range(1,10))
        for x in range(len(puzzle[y])):
            if puzzle[y][x] in tmp:
                tmp.remove(puzzle[y][x])

        for x in range(len(puzzle[y])):
            if puzzle[y][x] == 0:
                puzzle[y][x] = tmp.copy()

    puzzle = filter_col(puzzle)

    while not all(map(lambda x: all(map(lambda y: isinstance(y, int), x)), puzzle)):
        puzzle = filter_row(puzzle)
        puzzle = filter_col(puzzle)
        for i in range(3):
            for j in range(3):
                puzzle = filter_square(puzzle, i, j)
    return puzzle
```

***

### Опыт работы
Опыта работы в сфере программирования нет.

***

### Образование и курсы
* **Высшее Инженерное**
* **Курс SQL**
* **Серия из 3х курсов по Python**

***

### Уровень английского языка
Где-то между *Pre-Intermediate* и *Intermediate*.
