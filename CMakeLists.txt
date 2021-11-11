set(SRC_FILES
    "imconfig.h"
    "imgui.h"
    "imgui.cpp"
    "imgui_draw.cpp"
    "imgui_internal.h"
    "imgui_widgets.cpp"
    "imstb_rectpack.h"
    "imstb_textedit.h"
    "imstb_truetype.h"
    "imgui_demo.cpp"
    "imgui_tables.cpp"
)

if(WIN32)
    set(SRC_FILES ${SRC_FILES}
        "backends/imgui_impl_dx12.cpp"
        "backends/imgui_impl_win32.cpp"
    )
endif()

add_library(ImGui
    ${SRC_FILES}
)

target_include_directories(ImGui
    PUBLIC "" # ImGui does not have a incldue folder
)