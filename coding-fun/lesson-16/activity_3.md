### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Построй ратушу!

## Шаг 1
Используй **камень** в качестве строительного материала, создайте **3** ``||variable: переменные||`` и назови их **ширина**, **длина** и **высота**; установи ``||variable: переменным||`` правильные значения. Не забудь добавить свои переменные в команду ``||player: при команде чата||``.
### ~ tutorialHint
```block
player.onChat("ратуша", function (длина, ширина, высота) {
    for (let index = 0; index < высота; index++) {
        for (let index = 0; index < КОЛИЧЕСТВО; index++) {
            for (let index = 0; index < длина; index++) {
            СТРОИТЕЛЬСТВО
            }
            ПОВОРОТ
            for (let index = 0; index < ширина; index++) {
            СТРОИТЕЛЬСТВО
            }
            ПОВОРОТ
        }
        ДВИЖЕНИЕ
    }
})
```

```template
player.onChat("ратуша", function (длина, ширина, высота) {

})
```


```ghost
player.onChat("town_hall", function (length, width, height) {
    for (let index = 0; index < height; index++) {
        for (let index = 0; index < 2; index++) {
            for (let index = 0; index < length; index++) {
                agent.setItem(STONE, 1, 1)
                agent.place(DOWN)
                agent.move(FORWARD, 1)
            }
            agent.turn(RIGHT_TURN)
            for (let index = 0; index < width; index++) {
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
