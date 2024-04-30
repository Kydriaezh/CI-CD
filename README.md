Задача
Сделать локальный шаблон CI и отдельный репозиторий с шаблонами, подключить их к своему основному репозиторию через include

Решение
Создан локальный файл local-smoke-tests.gitlab-ci.yml

smoke-test-job:
  script: echo "SMOKE"
Создан основной файл .gitlab-ci.yml

include:
  - local: local-smoke-tests.gitlab-ci.yml
#  - remote: https://github.com/Valinetsky/-CI-CD_Seminar04/blob/main/remote-included-file.yml
# К сожалению, ни собственные файлы в моих репозиториях, ни ссылка на гитхаб не сработали


