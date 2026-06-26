from building import *

Import('rtconfig')

objs = []
cwd = GetCurrentDir()

if getattr(rtconfig, '_NXP_IMXRT_SDK_LATEST_INCLUDED', False):
    Return('objs')

rtconfig._NXP_IMXRT_SDK_LATEST_INCLUDED = True

if GetDepend(['SOC_IMXRT1020_SERIES']):
    objs = objs + SConscript('MIMXRT1020/SConscript')

if GetDepend(['SOC_IMXRT1050_SERIES']):
    objs = objs + SConscript('MIMXRT1050/SConscript')

if GetDepend(['SOC_IMXRT1064_SERIES']) or GetDepend(['SOC_MIMXRT1064DVL6A']):
    objs = objs + SConscript('MIMXRT1064/SConscript')
elif GetDepend(['SOC_IMXRT1061CVL5A']):
    objs = objs + SConscript('MIMXRT1061/SConscript')
elif GetDepend(['SOC_IMXRT1060_SERIES']):
    objs = objs + SConscript('MIMXRT1060/SConscript')

if GetDepend(['SOC_IMXRT1170_SERIES']):
    objs = objs + SConscript('MIMXRT1170/SConscript')

if GetDepend(['SOC_IMXRT1180_SERIES']):
    objs = objs + SConscript('MIMXRT1180/SConscript')

Return('objs')
