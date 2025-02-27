# Инструкция по работе с git и удаленными репозиториями

## Создание репозитория
Для того, чтобы добавить версионность к созданной папке, и создать в ней локальный репозиторий, для этого необходимо открыть окно терминала в этой папке и написать команду *git init*. Тогда Ваша папка станет репозиторием, и в ней появится скрытая папка .git

## Добавление файлов в репозиторий
Добавить версионность к файлу, находящемуся в папке-репозитории, можно с помощью команды *git add*. Пишется она следующим образом *git add <название файла>*

## Создание коммитов
Для того, чтобы зафиксировать изменения в текущей версии используется команда *git commit*. Используется она следующим образом: *git commit -m "<Сообщение к коммиту>"*. Сообщение к коммиту писать **ОБЯЗАТЕЛЬНО**

## Просмотр истории коммитов
Для просмотра истории всех сделанных коммитов используется команда *git log*. Чтобы увидеть всю историю коммитов, в папке репозитория в терминале необходимо написать *git log*

## Переключение между коммитами
Для того, чтобы переключаться между коммитами, необходимо использовать команду *git checkout*. Используется она следующим образом: *git checkout <номер коммита>*. Номер коммита можно взять, просмотрев список всех коммитов. 

## Создание ветки
Для того, чтобы создать новую ветку используется команда *git branch*. В папке с репозиторием напишите команду *git branch <название ветки*. Проверить то, что ветка создалась можно с помощью команды *git branch* в папке с репозиторием.

## Переключение между вектками
Для того, чтобы переключиться между ветками используется команда *git checkout*. Применяется она следующим образом: в папке с репозиторием необходимо написать *git checkout <название созданной ветки>*

## Слияние веток
Для слияния веток необходимо использовать команду *branch merge*. Используется она следующим образом: *git merge <имя ветки>*. Имя ветки которую мы хотим объеденить. Ветка которую мы хотим объеденить будет, будет объеденена с той веткой на которой мы находимся.
Так же при слиянии веток возможен конфликт версий. Мы сами должны принять решение, либо из пердложенных *AcceptCurrentChange, AcceptIncoming, AcceptBothChanges, CompareChanges*, либо отредактировать содержимое ветки в ручную. При конгфликте, после изменения в ветке **обязательно** нужно сделать коммит (см. инструкцию выше).

## Удаление веток
Для того что бы удалить ту ветку которая нам больше не нужна, используем команду *git branch -d*. Используется она следующим образом *git branch -d <имя ветки>*. Удаляемая ветка должна быть **ОБЯЗАТЕЛЬНО СЛИТА** с какой-нибудь из существующих веток. Проверить что ветка удалена мы можем при помощи команды *git branch*.

## Создаем удаленный репозиторий
Для работы с удаленным репозиторием в git, нам нужно склонировать внешний репозиторий на наш ПК. Делаем это при помощи команды *git clone <ссылка на репозиторий>*

## Передача изменений в текущий репозиторий
После того как мы внесли нужные изменения, мы должны передать их назад на внешний источник. Делаем это при помощи команды *git push*. Эта команда требует **авторизации** на внешнем источнике

## Получение изменений из текущего репозитория
Для того что бы скачать все из текущего репозитория и автоматически
сделать merge с нашей версией, используем команду *git pull*. 

## Как сделать pull request
1. Делаем fork репозитория
2. Делаем clone СВОЕЙ версии репозитория
3. Создаем новую ветку и в НЕЕ вносим свои изменения
4. Фиксируем изменения (делаем коммиты)
5. Отправляем свою версию в свой GitHub
6. На сайте GitHub нажимаем кнопку pull request 
