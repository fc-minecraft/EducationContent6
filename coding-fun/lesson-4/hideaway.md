### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Бамбуковое укрытие

## Шаг 1
Запрограммируй агента посадить 3 блока бамбука на каждой стороне песчаного участка. Добавь команду поворота агента, чтобы убедиться, что агент может завершить задачу.

#### ~ tutorialhint
Должно быть 2 цикла повторения, один вложенный в другой.

 
```ghost
player.onChat("bamboo", function () {
    for (let index = 0; index < 3; index++) {
        agent.setItem(BAMBOO, 64, 1)
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
    agent.turn(RIGHT_TURN)
})
```


