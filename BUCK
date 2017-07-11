macos_preprocessor_flags = [
  '-I/opt/X11/include',
]

cxx_library(
  name = 'dlib',
  header_namespace = '',
  exported_headers = subdir_glob([
    ('', 'dlib/**/*.h'),
  ]),
  headers = subdir_glob([
    ('dlib', '**/*.cpp'), # This is because source.cpp includes other translation-units
  ]),
  srcs = [
    'dlib/all/source.cpp',
  ],
  compiler_flags = [
    '-std=c++11',
  ],
  platform_preprocessor_flags = [
    ('default', macos_preprocessor_flags),
    ('^macos.*', macos_preprocessor_flags),
  ],
  visibility = [
    'PUBLIC',
  ],
)
