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
git log --all --decorate --oneline --graph 
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

&nbsp;&nbsp;&nbsp;&nbsp; Выше было продемонстрировано два разных способа отката коммита: первый подразумевает его полное удаление, а второй - создание диаметрально противоположного коммита. Поскольку стертый коммит остался существовать в удаленном репозитории, мы переписали ветку через команду

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
git config --global user.name "В3441 Bizin R S"  
git config --global user.email romanic523@gmail.com   
git clone https://github.com/roman-developer-git/LR6.git  
git pull origin master  
git log master  
git checkout -b branch1 origin/branch1  
git log branch1  
git log --all --decorate --oneline --graph  
git checkout master  
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

# История операций
```
commit 6407be0deb1e184048958f4987dcc36379826bbf (HEAD -> master, origin/master, origin/HEAD)
Author: B3441 Bizin R S <romanic523@gmail.com>
Date:   Sun Oct 20 23:23:50 2024 +0300

    Revert "doc: add file_test1"
    
    This reverts commit d60549092a841c56591e61c46914c8845e3a3c00.

commit d60549092a841c56591e61c46914c8845e3a3c00
Author: B3441 Bizin R S <romanic523@gmail.com>
Date:   Sun Oct 20 23:05:52 2024 +0300

    doc: add file_test1

commit f1a0ab50c00988ab481c58fa401fb05b93647da0
Merge: 29efb28 0f9f50d
Author: B3441 Bizin R S <romanic523@gmail.com>
Date:   Sun Oct 20 22:32:53 2024 +0300

    resolved conflict

commit 29efb283972918b621d65642eed9cb7092f56d5f
Author: roman-developer-git <romanic523@gmail.com>
Date:   Sun Oct 20 21:29:36 2024 +0300

    doc: add new file

commit 921f53b8d0cebf542c791cf31f04e9b792f385a4
Author: Kurtyanik <45309985+Kurtyanik@users.noreply.github.com>
Author: Kurtyanik <45309985+Kurtyanik@users.noreply.github.com>
Date:   Sat Nov 21 20:09:49 2020 +0300

    Обновление информации

commit 0f9f50db68a6983b47398017545532cd0f992846
Author: Kurtyanik <45309985+Kurtyanik@users.noreply.github.com>
Date:   Sat Nov 21 20:08:33 2020 +0300

    Заполнил файл

commit c08a654a63cfc3a7146b2b7015884d9020f5cbf5
Author: Kurtyanik <45309985+Kurtyanik@users.noreply.github.com>
Date:   Sat Nov 21 20:02:16 2020 +0300

    Файл создан пустым

commit 3c6e9131bb47ed6009c28226afb0535c7f6d5964
Author: Kurtyanik <45309985+Kurtyanik@users.noreply.github.com>
Date:   Sat Nov 21 19:58:20 2020 +0300

    Initial commit
```
