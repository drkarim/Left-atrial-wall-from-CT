cmake_minimum_required(VERSION 2.8)
 
project(la_wall)

find_package(VTK REQUIRED)
include(${VTK_USE_FILE})


 INCLUDE_DIRECTORIES(
	"~/Documents/Code/third_party/irtk/source/image++/include/"
	"~/Documents/Code/third_party/irtk/source/common++/include/"
	"~/Documents/Code/third_party/irtk/source/contrib++/include/"
	"~/Documents/Code/third_party/irtk/source/geometry++/include/"
 )

 LINK_DIRECTORIES(
	"~/Documents/Code/third_party/irtk/binary/lib/"
	"/usr/local/lib/"
	"~/Documents/Code/third_party/zlib/src/"
 )

add_executable(la_wall la_wall.cxx)

target_link_libraries(la_wall ${VTK_LIBRARIES} contrib++ image++ geometry++ common++ znz gsl niftiio z)

