project(Examples)

file(GLOB SOURCES "*.h" "*.cpp")

add_executable(Examples
    ${SOURCES}
)

target_link_libraries(Examples
  PUBLIC
    raw_pdb
)

target_precompile_headers(Examples
  PUBLIC
    Examples_PCH.h
)