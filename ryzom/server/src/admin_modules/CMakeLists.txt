FILE(GLOB SRC *.cpp *.h)

NL_TARGET_LIB(ryzom_adminmodules ${SRC})

INCLUDE_DIRECTORIES(${LIBXML2_INCLUDE_DIR} ${CMAKE_CURRENT_SOURCE_DIR})

TARGET_LINK_LIBRARIES(ryzom_adminmodules nelmisc nelnet)
NL_DEFAULT_PROPS(ryzom_adminmodules "Ryzom, Library: Service Admin Modules")
NL_ADD_RUNTIME_FLAGS(ryzom_adminmodules)
NL_ADD_LIB_SUFFIX(ryzom_adminmodules)

ADD_DEFINITIONS(${LIBXML2_DEFINITIONS})

INSTALL(TARGETS ryzom_adminmodules LIBRARY DESTINATION ${RYZOM_LIB_PREFIX} ARCHIVE DESTINATION ${RYZOM_LIB_PREFIX} COMPONENT libraries)
