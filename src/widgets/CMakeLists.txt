project(SVSCraftWidgets
    VERSION ${SVSCRAFT_VERSION}
    LANGUAGES CXX
)

file(GLOB_RECURSE _src *.h *.cpp)

svs_add_library(${PROJECT_NAME} AUTOGEN
    SOURCES ${_src}
    LINKS SVSCraftCore
    QT_LINKS Core Gui Widgets
    QT_INCLUDE_PRIVATE Core Gui Widgets
    INCLUDE_PRIVATE # contexts
    PREFIX SVSCRAFT_WIDGETS
)

set_target_properties(${PROJECT_NAME} PROPERTIES
    CXX_STANDARD 17
    CXX_STANDARD_REQUIRED TRUE
)