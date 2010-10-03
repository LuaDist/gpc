# Copyright (C) 2007-2009 LuaDist.
# Created by Peter Kapec
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

PROJECT(gpc C)
CMAKE_MINIMUM_REQUIRED(VERSION 2.6)
INCLUDE(dist.cmake)

# GPC Library
ADD_LIBRARY(gpc SHARED gpc.c libgpc.def)
INSTALL(TARGETS gpc DESTINATION ${INSTALL_LIB})

IF(MSVC)
	SET_TARGET_PROPERTIES(gpc PROPERTIES OUTPUT_NAME libgpc CLEAN_DIRECT_OUTPUT 1 )
ENDIF()
#~2DO: above necessary? --djm

INSTALL(FILES gpc.h DESTINATION ${INSTALL_INC})
INSTALL(FILES GPC-README.pdf VERSIONS.TXT DESTINATION ${INSTALL_DOC})
