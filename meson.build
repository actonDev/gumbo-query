project('gumbo-query', 'cpp')

gumbo_parser_proj = subproject('gumbo-parser')
gumbo_parser_dep = gumbo_parser_proj.get_variable('gumbo_parser_dep')

gumbo_query_lib = library(
  'gumbo-query',
  sources: files(
    'src/Document.cpp',
 'src/Node.cpp',
 'src/Object.cpp',
 'src/Parser.cpp',
 'src/QueryUtil.cpp',
 'src/Selection.cpp',
 'src/Selector.cpp',
  ),
  include_directories: [
    include_directories('src')
  ],
  dependencies: [
    gumbo_parser_dep
    ]
)
gumbo_query_dep = declare_dependency(
  link_with: gumbo_query_lib,
  include_directories: include_directories('src'),
)
