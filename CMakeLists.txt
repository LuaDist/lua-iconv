# Copyright (C) 2007-2012 LuaDist.
# Created by Peter Drahoš
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

project ( lua-iconv C )
cmake_minimum_required ( VERSION 2.8 )
include ( cmake/dist.cmake )
include ( lua )

find_package ( Iconv REQUIRED )
include_directories ( ${ICONV_DIRECTORIES} )
install_lua_module ( iconv luaiconv.c LINK ${ICONV_LIBRARIES} )
add_lua_test ( test_iconv.lua )
