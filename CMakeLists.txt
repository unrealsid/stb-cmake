cmake_minimum_required(
	VERSION 4.0.0 
	FATAL_ERROR
)

project(
	lib-stbimage
	LANGUAGES C
)

include(GNUInstallDirs)

set(
    Header_Files
    stb_connected_components.h
    stb_c_lexer.h
    stb_divide.h
    stb_ds.h
    stb_dxt.h
    stb_easy_font.h
    stb_herringbone_wang_tile.h
    stb_hexwave.h
    stb_image.h
    stb_image_resize2.h
    stb_image_write.h
    stb_include.h
    stb_leakcheck.h
    stb_perlin.h
    stb_rect_pack.h
    stb_sprintf.h
    stb_textedit.h
    stb_tilemap_editor.h
    stb_truetype.h
    stb_voxel_render.h
)

set(
    Source_Files
    stb_vorbis.c
)

source_group(
	TREE "${CMAKE_CURRENT_SOURCE_DIR}" 
	PREFIX "Header Files" 
	FILES ${Header_Files}
)

set(
    ALL_FILES
    ${Header_Files}
    ${Source_Files}
)

add_library(
    ${PROJECT_NAME} 
    STATIC
	${ALL_FILES}
)

message(STATUS "Current source files in source: ${ALL_FILES}")