CMAKE_MINIMUM_REQUIRED(VERSION 2.8)
PROJECT(TDengine)

INCLUDE_DIRECTORIES(${TD_COMMUNITY_DIR}/src/client/inc)
INCLUDE_DIRECTORIES(inc)

IF (TD_LINUX)
  AUX_SOURCE_DIRECTORY(. SRC)
  ADD_EXECUTABLE(taosdemo ${SRC})
  
#  IF (TD_PAGMODE_LITE)
    TARGET_LINK_LIBRARIES(taosdemo taos)
#  ELSE ()
#    TARGET_LINK_LIBRARIES(taosdemo taos_static)
#  ENDIF ()

ENDIF ()
