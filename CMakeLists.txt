
cmake_minimum_required(VERSION 2.4.3)


# set the project name
project(App_HelloWorld)


FIND_PACKAGE(Bullet COMPONENTS REQUIRED)
INCLUDE_DIRECTORIES(  ${BULLET_INCLUDE_DIRS}
)
LINK_LIBRARIES(
 BulletDynamics BulletCollision LinearMath
)


LINK_LIBRARIES(${BULLET_LIBRARIES})


ADD_EXECUTABLE(App_HelloWorld HelloWorld.cpp)

