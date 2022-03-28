add_executable(hmap2obj hmap2obj.cpp)
target_link_libraries(
	hmap2obj
	PRIVATE
	lodepng
	obj)