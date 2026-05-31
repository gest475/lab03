# Лабораторная работа №3 — CMake

**Студент:** Артеменко Арина ИУ8-22  
**Репозиторий:** https://github.com/gest475/lab03

---

## Цель работы

Освоить систему сборки **CMake**, научиться описывать статические библиотеки и приложения, подключать зависимости между модулями.

---

## Структура проекта
# Лабораторная работа №3 — CMake

## Цель
Освоить систему сборки CMake, научиться описывать библиотеки и приложения.

## Структура


- `formatter_lib/` — статическая библиотека (форматирование текста в рамку)
- `formatter_ex_lib/` — расширение формата, зависит от `formatter_lib`
- `hello_world_application/` — приложение, использует `formatter_ex_lib`
- `solver_lib/` — библиотека для решения квадратных уравнений
- `solver_application/` — приложение, использует `solver_lib` и `formatter_ex_lib`

## Сборка

```bash
cmake -H. -B_build
cmake --build _build
```

## Установка

```bash
cmake -H. -B_build -DCMAKE_INSTALL_PREFIX=_install
cmake --build _build --target install
```

## Запуск

```bash
./_build/hello_world/hello_world
./_build/solver/solver 1 -3 1
```




