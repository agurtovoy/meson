libkernels = shared_library('kernels', 'kernels.cu',
                            cuda_args: ['-DTAG_IS_SHARED=1', '-DTAG_IS_BUILDING=1'],
                            gnu_symbol_visibility: 'hidden')
link_args = []
if build_machine.system() == 'windows'
   link_args = ['/LIBPATH:shared']
else
   link_args = ['-L shared']
endif

libkernels = declare_dependency(compile_args: ['-DTAG_IS_SHARED=1'],
                                link_with:    libkernels,
                                link_args:    link_args)
