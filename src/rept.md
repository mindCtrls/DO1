## Part 1. Установка ОС
<div align="center">
  ![screen_task_1](/misc/images/rept/task_1.png)
  <figcaption>Вывод версии ОС</figcaption>
</div>




## Part 2. Создание пользователя
<div align="center">
  ![screen_task_2.1](/misc/images/rept/task_2.1.png)
  <figcaption>Команда для создания пользователя</figcaption>
</div>
<br>  
<div align="center">
  ![screen_task_2.2](/misc/images/rept/task_2.2.png)
  <figcaption>Вывод команды cat /etc/passwd</figcaption>
</div>

## Part 3. Настройка сети ОС

##### Задай название машины вида user-1.
- sudo vim /etc/hostname - редактирование файла, в котором указано имя ВМ. Использовал ее, что изменить имя ВМ.

##### Установи временную зону, соответствующую твоему текущему местоположению. 

- sudo timedatectl list-timezone - список временных зон
- sudo timedatectl set-timezone Asia/Novosibirsk - установка временной зоны

<div align="center">
  ![screen_task_2.2](/misc/images/rept/task_3.2.png)
  <figcaption>Установка временной зоны и текущее время</figcaption>
</div>

##### Выведи названия сетевых интерфейсов с помощью консольной команды.
<div align="center">
  ![screen_task_2.2](/misc/images/rept/task_3.4.png)
  <figcaption>Вывод сетевых интерфейсов</figcaption>
</div>


lo - локахост (127.0.0.1) интерфейс, указывающий на саму машину. Все запросы на него идут с указанием порта (не уверен, что прям все). Нужен, чтобы приложения на самом компьютере обменивались данными между собой, не выходя в локальную сеть.

##### Используя консольную команду, получи ip адрес устройства, на котором ты работаешь, от DHCP-сервера. 
<div align="center">
  ![screen_task_2.2](/misc/images/rept/task_3.4_new.png)
  <figcaption>Вывод ip от DHCP и вывод сетевых интерфейсов</figcaption>
</div>

##### Определи и выведи на экран внешний ip-адрес шлюза (ip) и внутренний IP-адрес шлюза, он же ip-адрес по умолчанию (gw). 

  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_3.5.1.png)
    <figcaption>Внещний ip адрес</figcaption>
  </div>
  <br>  
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_3.5.2.png)
    <figcaption>Внутренний ip адрес</figcaption>
  </div>

##### Задай статичные (заданные вручную, а не полученные от DHCP-сервера) настройки ip, gw, dns (используй публичный DNS-серверы, например 1.1.1.1 или 8.8.8.8).  

  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_3.6.png)
    <figcaption>Вывод настроек для сетевого интерфейса enp0s3</figcaption>
  </div>

##### Перезагрузи виртуальную машину. Убедись, что статичные сетевые настройки (ip, gw, dns) соответствуют заданным в предыдущем пункте.  

  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_3.7.png)
    <figcaption>ping хостов ya.ru и 1.1.1.1</figcaption>
  </div>


## Part 4. Обновление ОС

  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_4.png)
    <figcaption>Вывод команды sudo apt update</figcaption>
  </div>

## Part 5. Использование команды **sudo**

sudo (SuperUser DO) позволяет использовать команды от имени root пользователя.
root пользователь - это пользователь у которого нет ограничений на выполнение команд. 

  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_5.1.png)
    <figcaption>Вывод содержимого /etc/sudoers</figcaption>
  </div>
  <br>
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_5.2.png)
    <figcaption>Вход под пользователем fuse и смена hostname под ним</figcaption>
  </div>

## Part 6. Установка и настройка службы времени

  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_6.png)
    <figcaption>Вывод часового пояса и времени</figcaption>
  </div>

## Part 7. Установка и использование текстовых редакторов 

##### Используя каждый из трех выбранных редакторов, создай файл *test_X.txt*, где X — название редактора, в котором создан файл. Напиши в нём свой никнейм, закрой файл с сохранением изменений.

  ctrl + x - выход из nano. Выдает контекстное меню в котором выбираем сохранение.
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_7.1.1.png)
    <figcaption>Окно nano</figcaption>
  </div>

  shift + : - вызов командной строки
  команда wq - сохранение и выход из программы
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_7.1.2.png)
    <figcaption>Окно vim</figcaption>
  </div>


  ctrl + x, ctrl + c - выход из emacs. Выдает контекстное меню в котором выбираем сохранение.
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_7.1.3.png)
    <figcaption>Окно emacs</figcaption>
  </div>

##### Используя каждый из трех выбранных редакторов, открой файл на редактирование, отредактируй файл, заменив никнейм на строку «21 School 21», закрой файл без сохранения изменений.

  ctrl + x - выход из nano. Выдает контекстное меню в котором не выбираем сохранение.
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_7.2.1.png)
    <figcaption>Окно nano с измененным текстом</figcaption>
  </div>

  shift + : - вызов командной строки
  <br>
  команда qa! - выход из программы без сохранения
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_7.2.2.png)
    <figcaption>Окно vim с измененным текстом</figcaption>
  </div>


  ctrl + x, ctrl + c - выход из emacs. Выдает контекстное меню в котором не выбираем сохранение.
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_7.2.3.png)
    <figcaption>Окно emacs с измененным текстом</figcaption>
  </div>

##### Используя каждый из трех выбранных редакторов, отредактируй файл ещё раз (по аналогии с предыдущим пунктом), а затем освой функции поиска по содержимому файла (слово) и замены слова на любое другое.

  ctrl + w,  - поиск
  <br>
  ctrl + w , ctrl + r или ctrl + \ - замена
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_7.3.1.1.png)
    <figcaption>Поиск в редакторе nano</figcaption>
  </div>
  <br>
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_7.3.1.2.png)
    <figcaption>Замена в редакторе nano</figcaption>
  </div>

  / + слово - поиск
  <br>
  :%s/a/u/g - замена во всем файле 'a' на 'u', без учета регистра
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_7.3.2.1.png)
    <figcaption>Поиск в редакторе vim</figcaption>
  </div>
  <br>
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_7.3.2.2.png)
    <figcaption>Замена в редакторе vim</figcaption>
  </div>


  ctrl+s- поиск и переход по вхождениям
  <br>
  alt+shift+5 - замена. n- пропуск, y-текущее, ! - все без подтверждения, q - отмена
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_7.3.3.1.png)
    <figcaption>Поиск в редакторе emacs</figcaption>
  </div>
  <br>
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_7.3.3.2.png)
    <figcaption>Замена в редакторе emacs</figcaption>
  </div>

## Part 8. Установка и базовая настройка сервиса **SSHD**
- sudo apt install ssh - установка
- sudo systemctl enable ssh - включение автозапуска
- sudo vim /etc/ssh/sshd_config - изменение конфига
- systemctl restart ssh - перазапуск службы, чтобы применился конфиг
  
ps aux | grep ssh
- a - показывать процессы всех пользователей
- u - показывает доп инфу, юзер, сколько cpu, mem, время запуска…
- x - показывает фоновые службы



netstat -tan
- t - все активные tcp соединения 
- a -  покажет какие порты прослушиваются
- n - отключает преобразование адрес в доменные имена

  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_8.png)
    <figcaption>Вывод команды netstat -tan</figcaption>
  </div>

- proto - протокол подключения
- recv-Q - очередь полученных и необработанных запросов
- send-Q - очередь отправленных и необработанных запросов
- local address - локальный адрес соединения
- foreign address - удаленный адрес соединения
- state - состояние подключение

0.0.0.0 - это адрес, который относится ко всем сетевым интерфейсам. Например, сделав 192.168.0.169:2022. Я бы мог подключиться только по этому ip к машине. Но у нее же могут быть и другие сетевые интерфейсы по которым я хочу подключиться к серверу.

## Part 9. Установка и использование утилит **top**, **htop**

  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_9.1.png)
    <figcaption>Окно top</figcaption>
  </div>

- uptime (сколько сервер включен/активен) - 10:02
- user (кол-во авторизованных юзеров) - 1
- средняя нагрузка системы (LA) - 0.04, 0.05, 0.01
- кол-во процессов - 100
- загрузка cpu - 0.9
- загрузка памяти – 209.8 MiB
- pid по памяти - 1415
- pid по процу - 1474

  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_9.2.png)
    <figcaption>Сортировка по PID</figcaption>
  </div>
  <br>
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_9.3.png)
    <figcaption>Сортировка по Percent CPU</figcaption>
  </div>
  <br>
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_9.4.png)
    <figcaption>Сортировка по Percent_mem</figcaption>
  </div>
  <br>
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_9.5.png)
    <figcaption>Сортировка по TIME</figcaption>
  </div>
  <br>
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_9.6.png)
    <figcaption>Фильтр sshd</figcaption>
  </div>
  <br>
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_9.7.png)
    <figcaption>Поиск syslog</figcaption>
  </div>
  <br>
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_9.8.png)
    <figcaption>Добавление информации о uptime, hostname, clock</figcaption>
  </div>

## Part 10. Использование утилиты **fdisk**

- название - /dev/sda
- размер 50 GiB
- кол-во секторов 104857600
- Размер swap - 4 GiB

  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_10.png)
    <figcaption>Вывод fdisk -l</figcaption>
  </div>
  <br>
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_10.2.png)
    <figcaption>Вывод размера swap</figcaption>
  </div>

## Part 11. Использование утилиты **df** 


##### Запусти команду df. 

- размер раздела 24590672
- размер занятого пространства 7367960
- размер свободного пространства 15948244
- процент использования - 32

  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_11.1.png)
    <figcaption>Вывод df</figcaption>
  </div>

##### Запусти команду df -Th.

- размер раздела 24 GiB
- размер занятого пространства 7.1 GiB
- размер свободного пространства 16 GiB
- процент использования 32

  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_11.2.png)
    <figcaption>Вывод df -Th</figcaption>
  </div>

Тип файловой системы - ext4

## Part 12. Использование утилиты **du**

##### Запусти команду du.
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_12.3.png)
    <figcaption>Вывод du</figcaption>
  </div>

##### Выведи размер папок /home, /var, /var/log (в байтах, в человекочитаемом виде).
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_12.1.png)
    <figcaption>Вывод размера папок /home, /var, /var/log</figcaption>
  </div>

##### Выведи размер всего содержимого в /var/log (не общее, а каждого вложенного элемента, используя *).

  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_12.2.png)
    <figcaption>Вывод размера всего содержимого в /var/log</figcaption>
  </div>

## Part 13. Установка и использование утилиты **ncdu**

##### Выведи размер папок /home, /var, /var/log.

<div align="center">
    ![screen_task_2.2](/misc/images/rept/task_13.1.png)
    <figcaption>Вывод размера папок /home, /var</figcaption>
</div>
<br>
<div align="center">
    ![screen_task_2.2](/misc/images/rept/task_13.2.png)
    <figcaption>Вывод размера папки /var/log</figcaption>
</div>
<br>
<div align="center">
    ![screen_task_2.2](/misc/images/rept/task_13.3.png)
    <figcaption>Вывод размера содержимого папки /var/log</figcaption>
</div>


## Part 14. Работа с системными журналами

- Метод входа - sshd
- Время входа Apr 26 18:07:47
- Имя пользователя flox

  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_14.1.png)
    <figcaption>Последняя авторизация пользователя</figcaption>
  </div>

Перезапуск sshd

  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_14.2.png)
    <figcaption>Сообщение о рестарте службы</figcaption>
  </div>

## Part 15. Использование планировщика заданий **CRON**

  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_15.1.png)
    <figcaption>Вывод команды crontab -l</figcaption>
  </div>
  <br>
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_15.2.png)
    <figcaption>Строки в логе о выполнеии задачи в cron</figcaption>
  </div>
  <br>
  После удаления всех задач
  <div align="center">
    ![screen_task_2.2](/misc/images/rept/task_15.3.1.png)
    <figcaption>Вывод команды crontab -l</figcaption>
  </div>