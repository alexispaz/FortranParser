

if meson.is_subproject()
  inst=false
else
  inst=true
endif


executable('fp', 'testfp.f90',  dependencies: fparser_dep, install: inst)
executable('fp1','testfp1.f90', dependencies: fparser_dep, install: inst)
executable('fp2','testfp2.f90', dependencies: fparser_dep, install: inst)
executable('fp3','testfp3.f90', dependencies: fparser_dep, install: inst)
executable('fp4','testfp4.f90', dependencies: fparser_dep, install: inst)
executable('fp5','testfp5.f90', dependencies: fparser_dep, install: inst)

