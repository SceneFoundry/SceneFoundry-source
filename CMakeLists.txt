cmake_minimum_required(VERSION 3.16)
project(SceneFoundry-source)



add_subdirectory(app/gpu)
add_subdirectory(app/gpu_opengl)
add_subdirectory(app-graphics3d/draw2d_opengl)
add_subdirectory(app-graphics3d/draw2d_nanovg)
add_subdirectory(app-graphics3d/gpu_vulkan)
add_subdirectory(app-graphics3d/draw2d_vulkan)
add_subdirectory(app-graphics3d/draw2d_vkvg)
add_subdirectory(app-graphics3d/draw2d_directx12)
add_subdirectory(app-graphics3d/write_text_directx12)
add_subdirectory(app-graphics3d/gpu_directx12)
add_subdirectory(app-graphics3d/graphics3d)
add_subdirectory(app-graphics3d/graphics3d_directx11)
add_subdirectory(app-graphics3d/graphics3d_directx12)
add_subdirectory(app-graphics3d/graphics3d_khronos)
add_subdirectory(app-graphics3d/graphics3d_opengl)
add_subdirectory(app-graphics3d/graphics3d_vulkan)
add_subdirectory(app-graphics3d/continuum)
add_subdirectory(SceneFoundry/pbr-renderer)
add_subdirectory(SceneFoundry/SceneFoundry)



add_custom_target(release_all)
add_dependencies(release_all _app_graphics3d_continuum)


