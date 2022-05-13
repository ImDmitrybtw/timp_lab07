# timp_lab07

# Ход работы
[Документация](https://hunter.readthedocs.io/en/latest/creating-new/create/cmake.html)

1) Дополнительно создаем [репозиторий с функцией](https://github.com/ImDmitrybtw/hello_foo) которую хотим запакетизировать в hunter'е и [форк от хантера](https://github.com/ImDmitrybtw/hunter/tree/hello_foo).
2) В репозитории функции прописываем в CMakeLists.txt параметры установки и файла конфигурации.
   ![image](https://user-images.githubusercontent.com/92674699/168253350-b1371d73-26df-43de-b848-0673bcf92492.png)
 
3) Прописываем файл Config.cmake.in

   ![image](https://user-images.githubusercontent.com/92674699/168253252-4d6cda9c-3e4d-4f44-865a-08ed13d2b52c.png)

4) Переходим в форк hunter'а и добавляем [сюда](https://github.com/ImDmitrybtw/hunter/tree/hello_foo/cmake/projects) папку с CMakeLists.txt для нашей функции.

![image](https://user-images.githubusercontent.com/92674699/168254417-e5d534c5-75e7-4a7e-bedd-dd1a406da89d.png)

Чтобы заполнить поля URL и SHA1 необходимо создать tag с версией для репозитория функции, скачать архив и через командную консоль прописать команду <openssl sha1>
