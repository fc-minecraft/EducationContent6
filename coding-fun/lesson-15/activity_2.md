### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# Колонны!

## Этап 1
Время строить акведуки! Сначала создай переменные ``||variable: длина||`` и ``||variable: сегменты||``. 

Затем в блоке ``||loops: при старте||`` задай переменным значения ``||variable: длина||`` в **5** и ``||variable: сегменты||`` в **6**.

### ~ tutorialHint
```blocks
let сегменты = 0
let длина = 0
длина = 5
сегменты = 6
```


## Этап 2
Теперь внутри ``||loops: при старте||`` тебе нужно добавить все действия, которые Агент должен выполнить, чтобы построить **1** сегмент акведука: ``||agent: выдать блок песчаника||`` в количестве **64**, ``||agent: разместить||`` и ``||agent: двигаться вперёд||``. 

Вода будет течь, если есть уклон, поэтому Агенту нужно **разместить влево, вправо и вниз**. 

Помести все эти действия внутри цикла ``||loops: повторить||``, который **повторяется** ``||variable: длина||`` раз.

### ~ tutorialHint
```blocks
let сегменты = 0
let длина = 0
длина = 5
сегменты = 6
    agent.move(DOWN, 1)
    for (let index = 0; index < длина; index++) {
        ...
    }
    agent.move(DOWN, 1)
```


## Этап 3
Теперь вложи первый цикл ``||loops: повторить||`` в другой цикл ``||loops: повторить||``, который повторяется ``||variables:сегменты||`` раз. 

### ~ tutorialHint
Добавь блок ``||agent: агент двигаться вниз||`` перед внутренним циклом, чтобы код работал!
### ~ tutorialHint
```blocks
    agent.move(DOWN, 1)
    for (let index = 0; index < сегменты; index++) {
        for (let index = 0; index < длина; index++) {
            ...
        }
        agent.move(DOWN, 1)
    }
let сегменты = 0
let длина = 0
длина = 5
сегменты = 6
```

```ghost
    agent.move(DOWN, 1)
    for (let index = 0; index < Segments; index++) {
        for (let index = 0; index < length; index++) {
            agent.setItem(WHITE_CONCRETE, 64, 1)
            agent.place(LEFT)
            agent.place(RIGHT)
            agent.place(DOWN)
            agent.move(FORWARD, 1)
        }
        agent.move(DOWN, 1)
    }
let Segments = 0
let length = 0
length = 5
Segments = 6
```
```template
agent.move(DOWN, 1)
```
