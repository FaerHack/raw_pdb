file(GLOB SOURCES "Foundation" "*.h")
file(GLOB SOURCES "*.h" "*.cpp")

add_library(raw_pdb
	STATIC
	${SOURCES}
)

target_include_directories(raw_pdb
  PUBLIC
    .
)

target_precompile_headers(raw_pdb
  PRIVATE
    PDB_PCH.h
)

if(RAWPDB_BUILD_EXAMPLES)
	add_subdirectory(Examples)
endif()