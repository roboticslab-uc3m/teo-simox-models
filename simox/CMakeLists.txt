# Copyright: 2014 UC3M
# Author: Juan G Victores
# CopyPolicy: Released under the terms of the GNU GPL v2.0.

set(appname simox)

find_package(YARP REQUIRED)

list(APPEND CMAKE_MODULE_PATH ${YARP_MODULE_PATH})
include(YarpInstallationHelpers)
yarp_configure_external_installation(teo-simox-models)

#yarp_install(FILES ymanager.ini DESTINATION ${TEO_SIMOX_MODELS_DATA_INSTALL_DIR})  # Cleaner than ${TEO_SIMOX_MODELS_ROBOTS_INSTALL_DIR}/../ or similar.

file(GLOB teo ${CMAKE_CURRENT_SOURCE_DIR}/teo/*.xml)
file(GLOB teo/models ${CMAKE_CURRENT_SOURCE_DIR}/teo/models/*.wrl)

yarp_install(FILES ${teo} DESTINATION ${TEO-SIMOX-MODELS_CONTEXTS_INSTALL_DIR}/${appname}/teo)
yarp_install(FILES ${teo/models} DESTINATION ${TEO-SIMOX-MODELS_CONTEXTS_INSTALL_DIR}/${appname}/teo/models)

