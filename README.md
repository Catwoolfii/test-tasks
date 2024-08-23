# Описание выполнения тестового задания

1. Необходимо склонировать репозиторий, перейти в его директорию и выполнить сборку образа:
   ```
   sudo docker build --no-cache -t ubuntu:test .
   ```
   Пример результата выполнения команды:
   ![](/docker_build_result.PNG)
2. Запустить контейнер:
   ```
   sudo docker run --interactive --detach --name container-test ubuntu:test
   ```
3. Проверить дату и часовой пояс в контейнере:
   ```
   sudo docker exec --interactive --tty container-test sh -c 'date'
   ```
   Проверить версию git в контейнере:
   ```
   sudo docker exec --interactive --tty container-test sh -c 'git -v'
   ```
