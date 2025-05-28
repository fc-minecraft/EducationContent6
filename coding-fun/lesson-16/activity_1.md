### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Добывай ресурсы!

## Шаг 1
Агент копает **золотую руду** и **железную руду**. Чтобы его отправить в нужную сторону, придумывай простые команды: «**вперед**», «**назад**» или «**вправо**». Попробуй создать несколько команд ``||player:при команде чата||``.

Не пиши в коде, сколько шагов делать: вместо этого используй **переменные**. Тогда в чате можно будет просто написать, например, «**вперед 5**», и агент пройдет пять шагов вперед. Так легко менять, сколько шагов он сделает, не меняя сам код.

### ~ tutorialHint
```block
player.onChat("вправо", function (расстояние) {
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, расстояние)
})
```


```template
player.onChat("вперед", function (расстояние) {
})
```
```ghost
player.onChat("right", function (num1) {
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, num1)
})
player.onChat("back", function (num1) {
    agent.turn(RIGHT_TURN)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, num1)
})
player.onChat("left", function (num1) {
    agent.turn(LEFT_TURN)
    agent.move(FORWARD, num1)
})
player.onChat("collect", function () {
    agent.destroy(DOWN)
    agent.collectAll()
})
```


