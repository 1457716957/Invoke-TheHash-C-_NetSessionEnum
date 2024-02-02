# CMakeList.txt : Top-level CMake project file, do global configuration
# and include sub-projects here.
#
cmake_minimum_required (VERSION 3.8)

project ("Invoke-TheHash-C++")

# Include sub-projects.
#add_subdirectory ("TeamServer")

add_executable (${PROJECT_NAME} 
	 Invoke-TheHash-C++/lib/hmac.h Invoke-TheHash-C++/lib/hmac.c
	 Invoke-TheHash-C++/lib/md5.h Invoke-TheHash-C++/lib/md5.c
	 Invoke-TheHash-C++/lib/sha256.h Invoke-TheHash-C++/lib/sha256.c
	 
	 Invoke-TheHash-C++/EasyTcpClient.hpp Invoke-TheHash-C++/Log.h
	 Invoke-TheHash-C++/memory.hpp
	 Invoke-TheHash-C++/ntlm.hpp
	 Invoke-TheHash-C++/smb_lib.hpp

	 Invoke-TheHash-C++/main.cpp
	)

add_compile_options(-fshort-wchar)

