# Distributed under the MIT License.
# See LICENSE.txt for details.

set(LIBRARY "Test_XctsSolutions")

set(LIBRARY_SOURCES
  Test_ConstantDensityStar.cpp
  Test_Flatness.cpp
  Test_Kerr.cpp
  Test_Schwarzschild.cpp
  )

add_test_library(
  ${LIBRARY}
  "PointwiseFunctions/AnalyticSolutions/Xcts/"
  "${LIBRARY_SOURCES}"
  ""
  )

target_link_libraries(
  ${LIBRARY}
  PRIVATE
  CoordinateMaps
  DataStructures
  Domain
  Spectral
  Utilities
  Xcts
  XctsSolutions
  XctsSolutionsTestHelpers
  )
