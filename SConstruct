DefaultEnvironment(tools=[])
env=Environment(BIN='mybin',LOCALBIN='localbin')

def install_in_bin_dirs(env, source):
    """Install source in both bin dirs"""
    i1 = env.Install("$BIN", source)
    i2 = env.Install("$LOCALBIN", source)
    print("TEST_VAR=%s"%env['TEST_VAR'])
    return [i1[0], i2[0]] # Return a list, like a normal builder

env.AddMethod(install_in_bin_dirs, "InstallInBinDirs")

env.InstallInBinDirs(env.Program('main.c')) # installs hello in both bin dirs     

oenv=OverrideEnvironment(env,TEST_VAR='abc')
print("Override id:%s"%id(oenv))

