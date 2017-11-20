## Laboratory work XII

Сборка проекта программы

```ShellSession
$ cmake -H. -B_build -DCMAKE_INSTALL_PREFIX=_install
$ cmake --build _build --target install
```

Пример работы программы
```ShellSession
$ ./cget https://yandex.ru
Response answer: 200
```

