# Linux_Lesson_08
## System boot
### Описание репозитория
Лабораторная работа по загрузке ОС без пароля, изменению имени Volume Group и добавлению собственного модуля в загрузку ОС.

- **hw8_1.txt** - процесс изменения имени Volume Group, записанный с помощью утилиты *script*.
- **hw8_2.txt** - процесс добавления модуля в загрузку ОС (initrd), записанный с помощью утилиты *script*.

---
### Выполнение лабораторной работы
Устанавливаем виртуальную машину на основе CentOS 7.  

Загрузка ОС без ввода пароля:  
*Способ №1*  
В процессе загрузки виртуальной машины, входим в строку редактирования параметров загрузки и вводим строку "rw init=/bin/bash". Продолжаем загрузки с измененными параметрами.  
![1_way](https://github.com/darknetworm/Linux_Lesson_08/assets/82410807/3197e34a-6d3f-4d53-9abb-94cc6fd20843)  
После загрузки системы вводим команду для изменения пароля пользователя root и после последующей перезагрузки будем использовать новый пароль.  
![1_way_login](https://github.com/darknetworm/Linux_Lesson_08/assets/82410807/25ee30d6-8508-4d49-8600-4677a050e861)  
*Способ №2*   
В процессе загрузки виртуальной машины, входим в строку редактирования параметров загрузки и вводим строку "rd.break". Продолжаем загрузки с измененными параметрами.  
![2_way](https://github.com/darknetworm/Linux_Lesson_08/assets/82410807/29eb249a-5233-4502-ba15-a8454e36bd08)  
После загрузки системы вводим команды по монтированию системы, изменению корневого каталога и изменению пароля пользователя root. После перезагрузки будем использовать новый пароль пользователя root.  
![2_way_login](https://github.com/darknetworm/Linux_Lesson_08/assets/82410807/46053364-6426-473e-83ba-b71f821b4d94)  

Добавление собственного модуля в загрузку ОС:  
Во время загрузки ОС с внедренным модулем в *initrd* наступает 10-ти секундная пауза и появляется изображение пингвина.  
![pinguin](https://github.com/darknetworm/Linux_Lesson_08/assets/82410807/615a410d-710d-4392-91b9-03532a231b59)
