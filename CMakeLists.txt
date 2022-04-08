cmake_minimum_required(VERSION 3.18)
project(qt_test)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

SET(CMAKE_PREFIX_PATH /Users/victor/Qt/5.15.2/clang_64/lib/cmake/)
find_package(Qt5 COMPONENTS
        Core
        REQUIRED)

add_executable(bluezapi2qt
        src/BluezApiParser.cpp
        src/Comment.cpp
        src/CppGenerator.cpp
        src/Interface.cpp
        src/Method.cpp
        src/Methods.cpp
        src/Parameter.cpp
        src/Properties.cpp
        src/Property.cpp
        src/TypeAnnotation.cpp
        src/XmlGenerator.cpp
        src/main.cpp
        )

target_link_libraries(bluezapi2qt
        Qt${QT_MAJOR_VERSION}::Core
        )
