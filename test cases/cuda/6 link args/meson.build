project('simple', 'cuda', version : '1.0.0')

subdir('shared')

link_args = []
if build_machine.system() == 'windows'
   link_args = ['/MAP']
else
   link_args = ['-Map']
endif

exe = executable('prog', 'main.cu', dependencies: libkernels, link_args: link_args)
test('cudatest', exe)
