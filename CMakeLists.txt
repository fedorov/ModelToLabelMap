
#-----------------------------------------------------------------------------
set(MODULE_NAME ModelToLabelMap) # Do not use 'project()'

#-----------------------------------------------------------------------------
SEMMacroBuildCLI(
  NAME ${MODULE_NAME}
  LOGO_HEADER ${Slicer_SOURCE_DIR}/Resources/NAMICLogo.h
  TARGET_LIBRARIES ${ITK_LIBRARIES} vtkIO vtkGraphics
  EXECUTABLE_ONLY
  )

#-----------------------------------------------------------------------------
if(BUILD_TESTING)
  add_subdirectory(Testing)
endif()
