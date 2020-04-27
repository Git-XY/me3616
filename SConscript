from building import *

cwd = GetCurrentDir()
path = [cwd + '/inc']

# ME3616
if GetDepend(['PKG_USING_ME3616']):
    src += Glob('src/at_device_me3616.c')
    if GetDepend(['AT_USING_SOCKET']):
        src += Glob('src/at_socket_me3616.c')
    if GetDepend(['AT_DEVICE_ME3616_SAMPLE']):
        src += Glob('samples/at_sample_me3616.c')
      
group = DefineGroup('me3616', src, depend = ['PKG_USING_ME3616'], CPPPATH = path)

Return('group')
