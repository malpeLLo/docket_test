Чтобы собрать контейнер нужно. 
1) Скачать и запустить "docker"
2) В командной строке перейти в директорию, где лежит Dockerfile
3) Выполнить команду 

  `docker build -t test_docker`

5) По завершению сборки можно запустить контейнер командой 

  `docker run -p 5000:5000 tesk_docker`

6) Чтобы протестировать работу API можно зайти в powershell и ввести команду:

  `Invoke-WebRequest -Uri http://127.0.0.1:5000/reverse -Method POST -Headers @{"Content-Type"="application/json"} -Body '{"text": "Hello, World!"}'`

Должен прийти ответ с перевёрнутым сообщением: "Hello World!"

Столкнулся с проблемой нехватки памяти на первом диске, а при установке через установщик не даётся выбора куда устанавливать.
Решил проблему, перейдя в директорию с установщиком и произведя установку командой через консоль:

  `start /w "" "Docker Desktop Installer.exe" install -accept-license  --installation-dir=E:\path\to\folder`
