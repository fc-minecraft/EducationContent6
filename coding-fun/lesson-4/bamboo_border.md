### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Бамбуковая граница

## Шаг 1
Есть стартовый код, который мы подготовили для тебя. Попробуй сначала запустить его. Конечная цель — посадить бамбук вдоль 4 сторон участка панды.

```template
player.onChat("bamboo", function () {
    agent.setItem(BAMBOO, 64, 1)
    for (let index = 0; index < 16; index++) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
    agent.turn(LEFT_TURN)
})
```
