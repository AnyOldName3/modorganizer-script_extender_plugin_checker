# Version chosen arbitrarily
CMAKE_MINIMUM_REQUIRED(VERSION 3.0)

PROJECT(ScriptExtenderPluginChecker LANGUAGES NONE)

# Value passed from modorganizer-umbrella
SET(DEPENDENCIES_DIR CACHE PATH "")

LIST(APPEND CMAKE_PREFIX_PATH ${QT_ROOT}/lib/cmake)

# Find Python
FILE(GLOB_RECURSE PYTHON_ROOT ${DEPENDENCIES_DIR}/pyconfig.h.in)
GET_FILENAME_COMPONENT(PYTHON_ROOT ${PYTHON_ROOT} DIRECTORY)

ADD_SUBDIRECTORY(src)
