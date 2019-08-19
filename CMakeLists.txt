cmake_minimum_required (VERSION 2.6)
  
set(APP_NAME Alsa-Radio)
project (${APP_NAME})

add_executable(${APP_NAME} Alsa-Radio.cpp)

find_package(ALSA REQUIRED)                                    
if (ALSA_FOUND)                                                
    include_directories(${ALSA_INCLUDE_DIRS})                  
    target_link_libraries (${APP_NAME} ${ALSA_LIBRARIES})      
endif(ALSA_FOUND)