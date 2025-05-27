### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# Красивые вещи!

## Этап 1
Твоя миссия — построить чередующийся узор из **кварцевых колонн** и **лазуритовых блоков** вдоль границы дна бассейна. 

Начни с создания переменных ``||variable:блокА||`` и ``||variable:блокБ||``. 

Установи переменную ``||variable:блокА||`` в **кварцевый блок** и переменную ``||variable:блокБ||`` в **лазуритовый блок**. 

Добавь команды в блок ``||loops: при старте||``.

### ~ tutorialHint
```blocks
let счетчик = 0
let блокB = 0
let блокA = 0
блокA = BLOCK_OF_QUARTZ
блокB = LAPIS_LAZULI_BLOCK
```



## Этап 2
``||logic: Если||`` ``||счётчик||`` = **0**, то Агенту нужно установить ``||variable:блокА||``, ``||agent:разрушить вниз||``, ``||agent:разместить вниз||`` и ``||variable:изменить счётчик на 1||``. 

``||logic: Иначе||`` Агенту нужно установить ``||блокБ||``, разместить блоки и ``||изменить счётчик на -1||``.

## Этап 3
Агенту нужно размещать блоки в ряд ``||loops: пока||`` он ``||logic:не||`` ``||обнаруживает||`` блок **впереди**.

## Этап 4
Есть **4** стороны резервуара, которые Агенту нужно завершить, поэтому добавь блок ``||loops: повторить||``. 

Установи ``||счётчик||`` в **0** перед тем, как отправить Агента размещать блоки.
### ~ tutorialHint
Эта подсказка НЕ содержит код полностью.
```blocks
счетчик = 0
let счетчик = 0
let блокB = 0
let блокA = 0
блокA = BLOCK_OF_QUARTZ
блокB = LAPIS_LAZULI_BLOCK
for (let index = 0; index < 4; index++) {
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        if (счетчик == 0) {
            счетчик += 1
            ...
        } else {
            счетчик += -1
            ...
        }
    }
}
```

```template
count = 0
for (let index = 0; index < 4; index++) {
    while (!(true)) {
        if (true) {
        } else {
        }
    }
}
let count = 0
let blockB = 0
let blockA = 0
blockA = BLOCK_OF_QUARTZ
blockB = LAPIS_LAZULI_BLOCK
```


```ghost
count = 0
for (let index = 0; index < 4; index++) {
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        if (count == 0) {
            agent.setItem(blockA, 1, 1)
            agent.destroy(DOWN)
            agent.place(DOWN)
            count += 1
        } else {
            agent.setItem(blockB, 1, 1)
            agent.destroy(DOWN)
            agent.place(DOWN)
            count += -1
        }
        agent.move(FORWARD, 1)
    }
    agent.turn(RIGHT_TURN)
}
let count = 0
let blockB = 0
let blockA = 0
blockA = BLOCK_OF_QUARTZ
blockB = LAPIS_LAZULI_BLOCK
```
