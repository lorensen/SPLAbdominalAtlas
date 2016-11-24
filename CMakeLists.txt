cmake_minimum_required(VERSION 2.8)
 
get_filename_component(PROG ${CMAKE_SOURCE_DIR} NAME)
project(${PROG})

set(ATLAS_NAME ${PROJECT_NAME})
set(ATLAS_VOLUME ${CMAKE_SOURCE_DIR}/Atlas/I.nrrd)
set(ATLAS_VOLUME_NAME I)
set(ATLAS_LABELS ${CMAKE_SOURCE_DIR}/Atlas/seg.nrrd)
set(ATLAS_LABELS_NAME seg)
set(ATLAS_COLOR_TABLE_NAME AbdominalAtlasColors)
set(ATLAS_COLOR_TABLE ${CMAKE_SOURCE_DIR}/Atlas/AbdominalAtlasColors.ctbl)
set(MRML_FILENAME ${CMAKE_SOURCE_DIR}/Atlas/${ATLAS_NAME}.mrml.in)

configure_file(${CMAKE_SOURCE_DIR}/${ATLAS_NAME}.config.in  ${CMAKE_BINARY_DIR}/${ATLAS_NAME}.config @ONLY)

configure_file(${CMAKE_SOURCE_DIR}/Atlas/${ATLAS_NAME}.mrml.in  ${CMAKE_BINARY_DIR}/${ATLAS_NAME}.mrml @ONLY)
