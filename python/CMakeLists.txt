#
# This file is part of KDDockWidgets.
#
# SPDX-FileCopyrightText: 2020 Klarälvdalens Datakonsult AB, a KDAB Group company <info@kdab.com>
# Author: Renato Araujo Oliveira Filho <renato.araujo@kdab.com>
#
# SPDX-License-Identifier: GPL-2.0-only OR GPL-3.0-only
#
# Contact KDAB at <info@kdab.com> for commercial licensing options.
#

set(PYTHON_VERSION "3.7" CACHE STRING  "Use specific python version to build the project.")
find_package(Python3 ${PYTHON_VERSION} REQUIRED COMPONENTS Interpreter Development)
find_package(Shiboken2 REQUIRED)
find_package(PySide2 ${Qt5Widgets_VERSION} EXACT REQUIRED)
include(PySide2ModuleBuild)

add_subdirectory(PyKDDockWidgets)
