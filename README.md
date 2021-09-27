# ATI.Services.Common
## Деплой
Выкладка в nuget происходит на основе триггера на тег определённого формата 
- `v1.0.0` - формат релизная версия на ветке master 
- `v1.0.0-rc1` - формат тестовой/альфа/бета версии на любой ветке  

Тег можно создать через git(нужно запушить его в origin) [создание тега и пуш в remote](https://git-scm.com/book/en/v2/Git-Basics-Tagging)  
или через раздел [releses](https://github.com/atidev/ATI.Services.Common/releases)(альфа версии нужно помечать соответсвующей галкой).

#### Разработка теперь выглядит вот так:
1. Создаем ветку, пушим изменения, создаем pull request.
2. Вешаем на ветку тег например `v1.0.2-new-auth-12`
3. Срабатывает workflow билдит и пушит версию(берёт из названия тега) в nuget.
4. По готовности мерджим ветку в master.
5. Вешаем релизный тег на нужный коммит мастера.
Нужно обязательно описать изменения внесённые этим релизом в release notes
Здесь лучше воспользоваться интерфейсом гитхаба, там удобнее редакитровать текст.
6. Срабатывает релизный workflow билдит и пушит в нугет релизную версию.
7. В разделе [Releses](https://github.com/atidev/ATI.Services.Common/releases) появляется информация о нашем релиз и release notes.
