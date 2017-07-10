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
    '-DDLIB_ISO_CPP_ONLY=1',
  ],
  visibility = [
    'PUBLIC',
  ],
)
