cmake_minimum_required(VERSION 3.16.3...3.19.7 FATAL_ERROR)

project(SlicerMauritanieUN_FST)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://www.slicer.org/wiki/Documentation/Nightly/Extensions/SlicerMauritanieUN_FST")
set(EXTENSION_CATEGORY "Examples")
set(EXTENSION_CONTRIBUTORS "Mohamed Abdellahi Sidi Mohamed Blal (UN-FST), El Hacen Mohamed Souilem (UN-FST), Mouhamed Ahmed Mahmoud  (UN-FST)")
set(EXTENSION_DESCRIPTION "The SlicerMauritanieUN_FST extension is an extension designed for 3D Slicer, offering segmentations on medical images by applying advanced medical imaging filters. This extension has been specifically developed to facilitate the image segmentation process, a crucial step for the accurate analysis and interpretation of medical imaging data.")
set(EXTENSION_ICONURL "https://www.example.com/Slicer/Extensions/SlicerMauritanieUN_FST.png")
set(EXTENSION_SCREENSHOTURLS "https://www.example.com/Slicer/Extensions/SlicerMauritanieUN_FST/Screenshots/1.png")
set(EXTENSION_DEPENDS "NA") # Specified as a list or "NA" if no dependencies

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(MauritanieGaussianFilter)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
