# Copyright (C) 2007-2012 LuaDist.
# Created by Peter Kapec, Peter Drahoš
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

project ( gpc C )
cmake_minimum_required ( VERSION 2.6 )
include ( cmake/dist.cmake )

# GPC Library
add_library ( gpc gpc.c libgpc.def )

# Install
install_library ( gpc )
install_header ( gpc.h )
install_doc ( GPC-README.pdf )
