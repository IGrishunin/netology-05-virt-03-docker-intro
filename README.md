# netology-05-virt-03-docker-intro
Задача 1.
Собрал image с помощью такого Dockerfile

FROM nginx:1.29.0
COPY index.html /usr/share/nginx/html/index.html

командой docker build -t nginx-netology:1.0.0 .
Предварительно создав в каталоге с Dockerfile указанный index.html

В dockerhub не отправлял из-за отсутствия доступа. В качестве аналога сохранил image через docker save nginx-netology:1.0.0 -o nginx-netology:1.0.0.tar


Задача 2.
<img width="1918" height="482" alt="Задача2-term" src="https://github.com/user-attachments/assets/d3477510-eade-450e-a6d8-374e58f864f3" />


Задача 3.
Через docker attach мы подключаемся к стандартному потоку ввода/вывода основного процесса в контейнера. При выполнении CTRL+C в процессе мы отправляем ему SIGINT, что приводит к его завершению
Проблема при обращении на http://127.0.0.1:8080 после смены порта, который слушает nginx возникает из-за того, что при запуске контейнера мы пробросили порт 8080 хоста на порт 80 контейнера, но при изменении default.conf и перезагрузке конфигурации nginx он перестал слушать внутри контейнера этот порт

<img width="865" height="65" alt="Задача3-term3" src="https://github.com/user-attachments/assets/207eb3d2-ba82-486a-b200-faaea54c2d15" />
<img width="867" height="760" alt="Задача3-term2" src="https://github.com/user-attachments/assets/a0d14f52-f2e6-493c-9cc9-24f92adaf2ef" />
<img width="1057" height="825" alt="Задача3-term1" src="https://github.com/user-attachments/assets/71ed884c-9034-4996-9ffb-5d8b445529ba" />


Задача 4.
<img width="1876" height="234" alt="Задача4-term" src="https://github.com/user-attachments/assets/48f80d53-cf31-429f-89f7-f10964958ccc" />


Задача 5.
Был запущен именно compose.yaml, так как он является дефолтным манифестом на который смотрит compose, если его не существует, то compose ищет docker-compose.yaml, иначе путь к манифесту нужно указывать руками через флаг -f

<img width="1405" height="215" alt="Задача5-term2" src="https://github.com/user-attachments/assets/cd0e8bff-134e-45ef-8e31-5bc09ef8bcda" />
<img width="1303" height="899" alt="Задача5-term1" src="https://github.com/user-attachments/assets/7b563898-3402-4355-8fb5-33e4a8898c58" />
<img width="1675" height="721" alt="Задача5-portainer compose" src="https://github.com/user-attachments/assets/e16bec7b-aefa-4b79-9f43-843d1a278d0d" />
<img width="1072" height="889" alt="Задача5-inspect" src="https://github.com/user-attachments/assets/bb3b3e57-4e66-40ce-a532-1ae48baaec16" />
<img width="608" height="295" alt="Задача5-compose yaml" src="https://github.com/user-attachments/assets/cdd63ad2-920e-4f5e-8468-27935c0a83be" />





