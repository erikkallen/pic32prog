project('pic32prog', 'c')

hidapi = 'hidapi'
if host_machine.system() == 'linux'
	hidapi = 'hidapi-libusb'
endif


sources = [
  'pic32prog.c',
  'target.c',
  'executive.c',
  'serial.c',
  'adapter-pickit2.c',
  'adapter-hidboot.c',
  'adapter-an1388.c',
  'adapter-bitbang.c',
  'adapter-stk500v2.c',
  'adapter-uhb.c',
  'adapter-an1388-uart.c',
  'configure.c',
  'family-mx1.c',
  'family-mx3.c',
  'family-mz.c'
]


dep_libusb =  dependency('libusb-1.0')
dep_hidapi =  dependency(hidapi)

executable('pic32prog', sources, dependencies : [dep_libusb, dep_hidapi])
