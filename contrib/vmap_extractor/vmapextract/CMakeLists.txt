# This file is part of the UeCore Project. See AUTHORS file for Copyright information
#
# This program is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; either version 2 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA  02111-1307  USA

cmake_minimum_required (VERSION 2.6)
set(EXECUTABLE_NAME "vmap_extractor")
project (${EXECUTABLE_NAME})

add_executable(${EXECUTABLE_NAME} adtfile.cpp  dbcfile.cpp gameobject_extract.cpp model.cpp  mpq_libmpq.cpp  vmapexport.cpp  wdtfile.cpp  wmo.cpp)

target_link_libraries(${EXECUTABLE_NAME} mpq bz2 z)
install(TARGETS ${EXECUTABLE_NAME} DESTINATION ${BIN_DIR}/tools)
