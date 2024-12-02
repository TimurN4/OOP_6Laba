cmake_minimum_required(VERSION 3.10)

# Устанавливаем имя проекта
project(MyGame)

# Указываем стандарт C++
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Добавляем директорию с заголовочными файлами
include_directories(include)

# Добавляем исходные файлы
file(GLOB_RECURSE SOURCES src/*.cpp)

# Добавляем исполняемый файл
add_executable(MyGame ${SOURCES})

# Если у вас есть дополнительные библиотеки, которые нужно линковать, добавьте их здесь
# target_link_libraries(MyGame some_library)