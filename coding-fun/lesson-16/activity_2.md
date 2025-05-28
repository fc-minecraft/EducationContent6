### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Построй стартовый дом!

## Шаг 1
Используй предоставленный пример кода, чтобы разместить 1 ряд блоков. Затем Агенту нужно повторить ту же процедуру **4 раза**, затем ``||agent: переместиться вверх||`` и **повторить** ее еще раз. Создай ``||variable: высота||`` и добавь ее в блок ``||loops: повторить||``. Этот код позволит построить **1** дом.

### ~ tutorialHint
Не забудь ввести свои числа в чате при вводе команды, например **домик 2 5**.
Пример кода показан ЧАСТИЧНО.
```block
player.onChat("домик", function (высота, размер) {
    for (let index = 0; index < высота; index++) {
        for (let index = 0; index < 4; index++) {
            for (let index = 0; index < размер; index++) {

            }
        }
    }
})
```

```template    
 player.onChat("домик", function (высота, размер) {
    for (let index = 0; index < размер; index++) {
        agent.setItem(STONE, 1, 1)
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
    agent.turn(RIGHT_TURN)
})
```

```ghost
player.onChat("build-simple", function (size, height) {
    for (let index = 0; index < height; index++) {
        for (let index = 0; index < 4; index++) {
            for (let index = 0; index < size; index++) {
                agent.setItem(STONE, 1, 1)
                agent.place(DOWN)
                agent.move(FORWARD, 1)
            }
            agent.turn(RIGHT_TURN)
        }
        agent.move(UP, 1)
    }
})
```



