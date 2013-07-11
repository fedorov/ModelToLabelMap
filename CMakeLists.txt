
#-----------------------------------------------------------------------------
set(MODULE_NAME ModelToLabelMap) # Do not use 'project()'

find_package(VTK REQUIRED)
include_directories(${VTK_SOURCE_DIR})
link_directories(${VTK_LIBRARY_DIRS})

#-----------------------------------------------------------------------------
SEMMacroBuildCLI(
  NAME ${MODULE_NAME}
  LOGO_HEADER ${Slicer_SOURCE_DIR}/Resources/NAMICLogo.h
  TARGET_LIBRARIES ${ITK_LIBRARIES} vtkIO vtkGraphics ${VTK_LIBRARIES}
  )

#-----------------------------------------------------------------------------
if(BUILD_TESTING)
  add_subdirectory(Testing)
endif()
