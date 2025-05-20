### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Обеспечь безопасность территории

## Шаг 1
Запрограммируй агента построить дубовый забор. Агенту нужно разместить блоки дубового забора справа, разрушить препятствия и двигаться вперёд. Забор должен быть длиной 17 блоков.

#### ~ tutorialhint
Убедись, что агент размещает блоки справа и разрушает блоки слева.


```blocks
player.onChat("fence", function () {
    agent.setItem(OAK_FENCE, 64, 1)
    for (let index = 0; index < 17; index++) {
            }
})
```
```ghost
player.onChat("fence", function () {
    agent.setItem(OAK_FENCE, 64, 1)
    for (let index = 0; index < 17; index++) {
        agent.place(RIGHT)
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
})
``` 

