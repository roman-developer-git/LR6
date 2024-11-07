# LR6
Лабораторная работа №6

***Порядок выполнения работы***
1. Создать аккаунт на сайте GitHub.
2. Сделать копию в личное хранилище из 
https://github.com/Kurtyanik/LR6/ (Fork).

![Рисунок 1](screenshots/1.png)

![Рисунок 2](screenshots/2.png)

![Рисунок 3](screenshots/3.png)

3. Установить Git (https://git-scm.com/).

![Рисунок 4](screenshots/4.png)

4. После установки настроить клиент git, введя имя пользователя (Группа 
Фамилия И.О.) и email.

![Рисунок 5](screenshots/5.png)

5. Клонировать свой личный удалённый репозиторий на компьютер.

![Рисунок 6](screenshots/6.png)

![Рисунок 7](screenshots/7.png)

6. Добавить файл через интерфейс GitHub. Подтянуть изменения в 
локальный репозиторий.

![Рисунок 8](screenshots/8.png)

![Рисунок 9](screenshots/9.png)

![Рисунок 10](screenshots/10.png)

![Рисунок 11](screenshots/11.png)

![Рисунок 12](screenshots/12.png)

7. Получить историю операций для каждой из веток.

![Рисунок 13](screenshots/13.png)

![Рисунок 14](screenshots/14.png)

![Рисунок 15](screenshots/15.png)

&nbsp;&nbsp;&nbsp;&nbsp; Для визуального представления истории изменений можно использовать 
```
git log --graph --oneline --decorate
```
&nbsp;&nbsp;&nbsp;&nbsp; Данная команда выведет в графическом интерфейсе историю коммитов для лучшего понимания их структуры.

![Рисунок 16](screenshots/16.png)

8. Просмотреть последние изменения. 

![Рисунок 17](screenshots/17.png)

9. Выполнить слияние в ветку master, разрешив конфликт (можно 
использовать специальные редакторы или графический интерфейс git).

![Рисунок 18](screenshots/18.png)

![Рисунок 19](screenshots/19.png)

![Рисунок 20](screenshots/20.png)

![Рисунок 21](screenshots/21.png)

&nbsp;&nbsp;&nbsp;&nbsp; Заливаем изменения на удаленный репозиторий.

![Рисунок 22](screenshots/22.png)

![Рисунок 23](screenshots/23.png)

10. Удалить побочную ветку после успешного слияния.

&nbsp;&nbsp;&nbsp;&nbsp; Удалили в локальном репозитории.

![Рисунок 24](screenshots/24.png)

&nbsp;&nbsp;&nbsp;&nbsp; Удалили в удаленном репозитории.

![Рисунок 25](screenshots/25.png)

&nbsp;&nbsp;&nbsp;&nbsp; Теперь в удаленном репозитории только одна ветка.

![Рисунок 26](screenshots/26.png)

11. Сделать изменения и зафиксировать их, оставляя комментарии, 
несколько раз.

![Рисунок 27](screenshots/27.png)

![Рисунок 28](screenshots/28.png)

![Рисунок 29](screenshots/29.png)

![Рисунок 30](screenshots/30.png)

12. Сделать откат коммита.

![Рисунок 31](screenshots/31.png)

![Рисунок 32](screenshots/32.png)

&nbsp;&nbsp;&nbsp;&nbsp; Выше было продемонстрировано два разных способа отката коммита: первый подразумевает его полное удаление, а второй - создание диаметрально противоположного коммита. Поскльку стертый коммит остался существовать в удаленном репозитории, мы переписали ветку через команду

```
git push --force
```

![Рисунок 33](screenshots/33.png)

![Рисунок 34](screenshots/34.png)

13. Создать ветку для отчёта.

![Рисунок 35](screenshots/35.png)

&nbsp;&nbsp;&nbsp;&nbsp; Заливаем ветку на удаленный репозиторий.

![Рисунок 36](screenshots/36.png)

# Лог команд
```
git config --global user.name  
git config --global user.email  
git clone  
git pull origin master  
git log master  
git checkout -b branch1 origin/branch1  
git log branch1  
git log --graph --oneline --decorate  
git log -p  
git merge branch1  
git commit -m "resolved conflict"  
git push  
git branch -d branch1  
git push -d origin branch1  
echo "hello world" > file_test1.txt  
git add file_test1.txt  
git commit -m "doc: add file_test1"  
git push  
echo "2hello world" > file_test2.txt  
git add file_test2.txt  
git commit -m "doc: add file_test2"  
git push  
git reset --hard HEAD~1  
git revert HEAD  
git push --force  
git checkout -b report  
git push --set-upstream origin report
```


