cmake_minimum_required(VERSION 2.8)
 
project(la_wall)

find_package(VTK REQUIRED)
include(${VTK_USE_FILE})


 INCLUDE_DIRECTORIES(
	"~/Documents/Code/irtk/src/image++/include/"
	"~/Documents/Code/irtk/src/common++/include/"
	"~/Documents/Code/irtk/src/contrib++/include/"
	"~/Documents/Code/irtk/src/geometry++/include/"
 )

 LINK_DIRECTORIES(
	"~/Documents/Code/irtk/bin/lib/"
	"/usr/local/lib/"
	"~/Documents/Code/third_party/zlib/src/"
 )

add_executable(la_wall la_wall.cxx)

target_link_libraries(la_wall ${VTK_LIBRARIES} contrib++ image++ geometry++ common++ znz gsl niftiio z)

