# Author: Kang Lin (kl222@126.com)

project(turnutils_uclient)

set(SOURCE_FILES
    uclient.c
    startuclient.c
    mainuclient.c
    )

add_executable(${PROJECT_NAME} ${SOURCE_FILES})
target_link_libraries(${PROJECT_NAME} PRIVATE turnclient)
INSTALL(TARGETS ${PROJECT_NAME}
    RUNTIME DESTINATION "${CMAKE_INSTALL_BINDIR}"
        COMPONENT Runtime
    )
