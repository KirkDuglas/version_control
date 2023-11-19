# Инструкция по Git

## Задать имя пользователя и электронную почту
```sh
git config --global user.name "имя пользователя"
git config --global user.email "адрес электронной почты"
```
> Имя пользователя и электронная почта нужны, чтобы привязывать коммиты к вашему имени. Имя и электронная почта будут автоматически отображаться в последующих коммитах.

## Инициалиизация каталога 
```sh 
git init
``` 
> Создает репозиторий Git или вновь инициализирует существующий. При инициализации создается скрытая папка. В ней содержатся все объекты и ссылки, которые Git использует и создаёт в истории работы над проектом.

## Индексирование файла
```sh
git add <Имя файла>
```
>Добавляет файл в область подготовленных файлов, (сохраняет измения в отслеживаемые файлы).

## Проверка статуса репозитория
```sh
git status
```
> Отображает статус нужного репозитория, отслеживает изменения во всех файлах каталога.

## Фиксация изменений и внесение коментариев
```sh  
git commit -m "Коментарий"
```
>Фиксирует изменения в отслеживаемых файлах. При создании коммита можно добавить  сообщение с помощью флага -m. Сообщение вводится непосредственно после флага, в кавычках.

## Просмотр истории изменений
```sh
git log
```
>Отображает список последних коммитов в порядке выполнения. при наличии большого количества коммитов в конце выскакивает фраза [END], чтобы выйти из данного режима нужно нажать клавишу Q.

```sh
git log --oneline
```
>Отображает каждое событие в одну строку.
```sh
git log --graph
```
>Отображает дерево слияния веток
![Отображение дерева](images\branchs.png)

```sh
git log --decorate
```
> Упрощает понимание того, к какой ветке относится каждый коммит.

## Просмотр изменений до коммита
```sh
git diff
```
> отображаются изменения, непроиндексированных файлов.
# Работа с коммитами и ветками 

## Переключение между коммитами
```sh
git checkout <коммит>
```
> Отображает версию файла зафиксированную выбранным коммитом.
```sh
git checkout master
```
>отображает последнюю зафиксированну версию файла.

## слияние веток
```sh
git merge <имя_ветки>
```

## создание веток
```sh
git branch <имя_ветки>
```
> Создает новую ветку 
## Переключение между ветками
```sh
git checkout <имя_ветки>
```
> Отображает версию файла выбранной ветки
## просмотр своего положения в дереве
```sh
git branch
```
> Отображает текущую ветку
=======
## Удаление веток
```sh
git branch -d <имя_ветки>
```
> Удаляет выбранную ветку. если выполнить команду удаления до слияния —  появится сообщение об ошибке. Этот защитный механизм предотвращает потерю доступа к файлам.
```sh
git branch -D <имя_ветки>
```
> Принудительно удаляет ветку, даже если не произведено сляние.

# *Вдохновлялся:*
* статьей [30 команд Git, необходимых для освоения интерфейса командной строки Git](https://habr.com/ru/companies/ruvds/articles/599929/)
* картинкой ![git шпаргалка](images\shpargalka.png)