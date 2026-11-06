cmake_minimum_required(VERSION 3.20)
project(uin_campus_core)

# Activer le standard c++23 
set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(uincampus_core
   src/version.cpp
   src/regles.cpp
   src/saisie.cpp)

target_include_directories(uincampus_core PUBLIC include)

#Ajouter l excutable principal du fil rouge
add_executable(uin-campus app/main.cpp)
target_link_libraries(uin-campus PRIVATE uincampus_core)
