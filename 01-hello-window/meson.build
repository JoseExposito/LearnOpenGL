project('hello-window', 'c')

cc = meson.get_compiler('c')

cflags = [
    '-Wno-unused-parameter',
    '-fvisibility=hidden',
    '-Wmissing-prototypes',
    '-Wstrict-prototypes'
]

add_project_arguments(cflags, language: 'c')
add_project_arguments(cflags, language: 'cpp')

gl_dep = dependency('gl')
glfw3_dep = dependency('glfw3')
dl_dep = cc.find_library('dl')

include_directories = include_directories('../glad/include')

executable('hello-window',
    'main.c',
    '../glad/src/glad.c',
    include_directories: include_directories,
    dependencies: [gl_dep, glfw3_dep, dl_dep]
)
