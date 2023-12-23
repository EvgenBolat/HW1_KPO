# Хавронич Евгений Алексеевич, БПИ226
---
## Данное консольное приложение разработано для работников кинотеатра.
### Как пользоваться приложением
Необходимо запустить Main.kt
#### Регистрация и авторизация
Прежде всего, пользователю выдаётся на выбор три действия, для выбора которого он должен ввести номер соответствующей команды и нажать enter:
1. Войти
Пользователь вводит свой логин и пароль, которые он ранее вводил при авторизации. Если пользователь с приведёнными данными имеется, то производится корректный вход в систему и предоставляется доступ ко всем функциям приложения. Если такого пользователя нет, то пользователь возвращается к изначальному выбору действий.
2. Зарегистрироваться в системе
Пользователь вводит логин и пароль для своего будущего аккаунта и после удачной регистрации входит в систему.
0. Выйти из приложения
Происходит выход из приложения, после чего пользователю будет необходимо заново входить

#### Пользование самим приложением
Пользователю предоставляется список команд, которые он может выполнить, введя соответствующий номер и нажав enter.
1) Продать билет

Система попросит ввести дату сеанса, на который покупается билет зрителем, а также место, на которое покупается билет. Стоит отметить, что всего в кинотеатре 100 мест.
3) Возврат билета 

Система просит ввести id билета, который хотят вернуть.
4) Отметить посещение

Система просит ввести id билета, который хотят отметить.
5) Добавить фильм

Система просит ввести название фильма и его длительность в минутах
6) Редактировать название фильма

Система просит ввести старое название фильма и новое
7) Редактировать длительность фильма

Система просит ввести название фильма и его новую длительность. При этом все сеансы по нему удалятся во избежание возникновения пересечений между сеансами, и произойдёт возврат билетов, если они были куплены на удаляемы сеансы. 
8) Удалить фильм 

Система просит ввести название фильма, который нужно удалить. Будут удалены все незавершённые сеансы и возвращены билеты, если они были на куплены на этот фильм.
9) Добавить сеанс

Система попросит ввести название фильма, на который будет добавлен сеанс, его дату и стоимость. 
10) Редактировать дату сеанса

Система попросит ввести старую дату сеанса и новую. При этом на всех билетах, купленных на данный сеанс, дата тоже поменяется 
11) Редактировать цену сеанса

Система попросит ввести дату сеанса и новую его стоимость. При этом с уже купленными билетами ничего не будет меняться. 
12) Удалить сеанс

Система попросит ввести дату сеанса. При этом все билеты на этот сеанс будут возвращены
13) Показ мест

Система попросит ввести дату сеанса, на которую необходимо показать места. Будет выведено схематично каждое место с его состоянием: занято или свободно 
14) Показать сеансы (по фильму)

Система попросит ввести название фильма. Будет выведена информация по всем сеансам по данному фильму: Название фильма, дата проведения сеанса, его стоимость. 
15) Показать сеансы (по дате) 

Система попросит ввести дату. Будет выведена информация по всем сеансам, что будут проводиться в это время
16) Показать все фильмы

Система выведет все фильмы, которые есть в базе данных. 
0) Выйти 

Происходит выход из приложения.

При выполнении одной из команд, пользователю снова предлагается выбрать одну из имеющихся. Если он хочет выйти из приложения, то должен ввести команду для выхода. 

Учтены различные случаи некорректных вводов или нарушающих логику приложения/ работы кинотеатра вцелом.

#### Хранение данных
Данные хранятся в json-формате. Это связано прежде всего с тем, что JSON разработан для обмена данными и обеспечивает более простой и лаконичный формат. Это также повышает производительность и скорость связи. JSON обычно лучше подходит для API, мобильных приложений и хранилищ данных, кое и необходимо реализовать в нашем проекте в то время как XML пригоден более для сложных структур документов, требующих обмена данными – это мы не реализуем. Таким образом, JSON – самый оптимальный вариант.

