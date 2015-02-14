cmake_minimum_required(VERSION 2.8)
 
project(SPLAbdominalAtlas)

configure_file(${SPLAbdominalAtlas_SOURCE_DIR}/SPLAbdominalAtlas.config.in  ${SPLAbdominalAtlas_BINARY_DIR}/SPLAbdominalAtlas.config @ONLY)

set(ATLAS_NAME SPLAbdominalAtlas)
set(ATLAS_VOLUME_NAME I)
set(ATLAS_VOLUME ${SPLAbdominalAtlas_SOURCE_DIR}/Atlas/I.nrrd)

set(ATLAS_LABELS_NAME seg)
set(ATLAS_LABELS ${SPLAbdominalAtlas_SOURCE_DIR}/Atlas/seg.nrrd)

set(ATLAS_COLOR_TABLE_NAME AbdominalAtlasColors)
set(ATLAS_COLOR_TABLE ${SPLAbdominalAtlas_SOURCE_DIR}/Atlas/AbdominalAtlasColors.ctbl)

set(MRML_FILENAME ${SPLAbdominalAtlas_SOURCE_DIR}/Atlas/${ATLAS_NAME}.mrml.in)

configure_file(${SPLAbdominalAtlas_SOURCE_DIR}/Atlas/SPLAbdominalAtlas.mrml.in  ${SPLAbdominalAtlas_BINARY_DIR}/SPLAbdominalAtlas.mrml @ONLY)
