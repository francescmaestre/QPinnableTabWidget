file(GLOB SRC_FILES
    include/*.h
    include/QPinnableTabWidget
    src/*.cpp
    src/*.h
)

add_library(QPinnableTabWidget STATIC
    ${SRC_FILES}
)

target_link_libraries(QPinnableTabWidget
    PUBLIC
    Qt::Core
    Qt::Widgets
)

target_include_directories(QPinnableTabWidget SYSTEM PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)
target_include_directories(QPinnableTabWidget SYSTEM PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src)
