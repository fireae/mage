FILE(GLOB SRC ${SRC} *.cpp)

SET(APP_NAME memorytest)

INCLUDE_DIRECTORIES(${MAGE_SRC_PATH})
INCLUDE_DIRECTORIES(${MAGE_HTS_ENGINE_PATH})
INCLUDE_DIRECTORIES(${MAGE_PORTAUDIO_PATH})
INCLUDE_DIRECTORIES(${MAGE_SPTK_PATH})

ADD_EXECUTABLE(${APP_NAME} ${SRC} ${HDR})
TARGET_LINK_LIBRARIES(${APP_NAME} pthread m)
TARGET_LINK_LIBRARIES(${APP_NAME} ${MAGE_LIB_NAME})

