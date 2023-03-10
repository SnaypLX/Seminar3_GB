# Инструкция по работе с Git и удаленными репозиториями

## Что такое Git?
**Git это наиболее популярная реализация распределенной системы контроля версий. Самая популярная реализация **Git** - это [GitHub](https://github.com/) **

## Подгатовка репозитория
Для создания репозитория используется команда "git init". Для создания репозитория необходимо в терминале перейти в пустую папку, где в будущем будет репозиорий. Затем в терминале с папкой написать команду "git init".

### Добавление файла к коммиту
Для добавления файла к будущему коммиту используется команда "git add". Для этого в терминале с папкой-репозиторием необходимо написать *git add <название файла>*.

## Создание коммита
Для создания коммита используетсвя команда *git commit*. Для этого в терминале с папкой репозиторием необходимо написать *git commit -m <сообщение к коммиту>*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО!!!***.

## Журнал изменений
Для просмотра журнала изменений используется команда *git log*. Для этого в терминале с папкой-репозиторием необходимо написать *git log*.

## Перемещение между коммитами
Для перемещения на предыдущие коммиты используется комманда *git checkout*. Для этого необходимо в журнале изменений, как показано в предыдущей части, найти необходимый коммит и его номер. После чего в терминале с папкой-репозиторием написать команду *git checkout <номер коммита>*. После применения этой команды вы попадёте в состояние *Detached head*, в котором никакие изменения фиксироваться не будут. Для возврата в обычное состояние необходимо написать команду *gbr checkout master*.

## Отображение состояния
Команда выводит только информацию, она не будет изменять коммиты или изменения в вашем локальном репозитории. Полезной особенностью комманды *git status является то, что он будет предоставлять полезную информацию в зависимости от вашей текущей ситуации. В общем, вы можете рассчитывать на то, что он вам подскажет.
*git status: Чаще всего используется в форме по умолчанию, это показывает хорошую базу информации.

## Сравнение изменений в Git
Для вывода изменений в файлах по сравнению с последним коммитом, используется git diff без параметров:
*git diff
Команда выводит изменения в файлах, которые еще не были добавлены в индекс. Сравнение происходит с последним коммитом.

## Слияние веток и разрешение конфликтов
Для слияния веток необходимо переместиться на главную ветку - master, для этого вводим *git checkout master. Для слияния веток вводим *git merge <name>.
конфликты регулярно возникают при слиянии ветвей или при отправке чужого кода. Иногда конфликты исправляются автоматически, но обычно с этим приходится разбираться вручную — решать, какой код остается, а какой нужно удалить.
Если система не смогла разрешить конфликт автоматически, значит, это придется сделать разработчикам. Приложение отметит строки, содержащие конфликт. 
Над разделителем ======= мы увидим последний (HEAD) коммит, а под ним - конфликтующий. Таким образом, можно увидеть, чем они отличаются и решать, какая версия лучше. Или вовсе написать новую. В этой ситуации мы так и поступим, перепишем все, удалив разделители.

## Ветки в Git
Для создания новой ветки используется команда *git branch* для этого в терминале с папкой-репозиторием необходимо написать *git branch <название ветки>*
Основная ветка в каждом репозитории называется master. Чтобы создать еще одну ветку, используем команду *git branch <name>. Это создаст новую ветку, пока что точную копию ветки master.
В Git ветка — это отдельная линия разработки. *git checkout <name> позволяет нам переключаться как между удаленными, так и меду локальными ветками. 

 ### Переключение между ветками
  Для переключения между ветками используется команда *git checkout*. Для этого в терминале с папкой-репозиторием пишем команду *git checkout <название ветки>*. Для перехода на ветку ветка должна быть ***создана***!!!
  
## Удаление веток
Для удаления ветки(После объединения или удаление ненужной) вводим следующее
*git branch -d <name>. Но удалять ветку нужно находясь в другой.
