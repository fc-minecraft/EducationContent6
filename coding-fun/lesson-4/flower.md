### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1


# Сделай территорию красивой!

## Шаг 1
Тебе нужно посадить 14 одуванчиков вдоль 4 сторон укрытия. Агент может посадить 14 одуванчиков на одной стороне.

#### ~ tutorialhint
Не забудь выбрать количество для команды установить блок агента.

```template
player.onChat("flower", function () {

})
```

```ghost
player.onChat("flower", function () {
    for (let index = 0; index < 4; index++) {
        for (let index = 0; index < 14; index++) {
            agent.setItem(YELLOW_FLOWER, 64, 1)
            agent.place(DOWN)
            agent.move(FORWARD, 1)
        }
        agent.turn(RIGHT_TURN)
    }
})

``` 
