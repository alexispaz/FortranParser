lib_sources = files(
    'FortranParser_parameters.f90',
    'FortranParser.f90'
)

# Static lib
fparser_lib = static_library(
    'FortranParser',
    lib_sources,
    install: true,
    fortran_args: [
        '-Wall',
    ]
)

