message(STATUS "")
message(STATUS "Libraries")
message(STATUS "=========")

message(STATUS "")
message(STATUS "Shared")
if(BUILD_DLL)
	add_subdirectory(dll)
	if(BUILD_UNICODE)
		add_subdirectory(dllunicode)
	endif(BUILD_UNICODE)
endif(BUILD_DLL)

message(STATUS "")
message(STATUS "Static")
add_subdirectory(static)

if(BUILD_UNICODE)
	add_subdirectory(staticunicode)
endif(BUILD_UNICODE)