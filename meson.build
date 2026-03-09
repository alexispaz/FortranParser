project(
  'fparser',
  ['fortran'],
  version: run_command(meson.current_source_dir()/'version.sh', check: true).stdout().strip(),
  meson_version: '>=1.2'
)

meson.add_dist_script('version.sh')

# Build library
subdir('src/lib')

# Declare a dependency so parent projects can do:                                                                         
#   dependency('fparser', fallback: ['fparser', 'fparser_dep'])
fparser_dep = declare_dependency(
  link_with: fparser_lib
)  

# Build pkgconfig file
pkg = import('pkgconfig')
pkg.generate(
  name : 'fparser',
  description : 'Fortran parser library',
  version : meson.project_version(),
  libraries : fparser_lib
)

# Export the dependency name to the parent project
meson.override_dependency('fparser', fparser_dep)

# Build tests 
subdir('src/tests')
