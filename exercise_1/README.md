
Задание 1

Создание образа

docker image build . --tag=crud_morozovs

Запуск контейнера

docker run --name=crud_morozovs -d -p 7007:80 crud_morozovs