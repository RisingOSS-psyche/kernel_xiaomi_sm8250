# SPDX-License-Identifier: GPL-2.0-only

# auto-detect subdirs
ifeq ($(CONFIG_ARCH_KONA), y)
include $(srctree)/techpack/camera-xiaomi-psyche/config/konacamera.conf
endif

ifeq ($(CONFIG_ARCH_LITO), y)
include $(srctree)/techpack/camera-xiaomi-psyche/config/litocamera.conf
endif

ifeq ($(CONFIG_ARCH_BENGAL), y)
include $(srctree)/techpack/camera-xiaomi-psyche/config/bengalcamera.conf
endif

ifeq ($(CONFIG_ARCH_KONA), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera-xiaomi-psyche/config/konacameraconf.h
endif

ifeq ($(CONFIG_ARCH_LITO), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera-xiaomi-psyche/config/litocameraconf.h
endif

ifeq ($(CONFIG_ARCH_BENGAL), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera-xiaomi-psyche/config/bengalcameraconf.h
endif

ifdef CONFIG_SPECTRA_CAMERA
# Use USERINCLUDE when you must reference the UAPI directories only.
USERINCLUDE     += \
                -I$(srctree)/techpack/camera-xiaomi-psyche/include/uapi

# Use LINUXINCLUDE when you must reference the include/ directory.
# Needed to be compatible with the O= option
LINUXINCLUDE    += \
                -I$(srctree)/techpack/camera-xiaomi-psyche/include/uapi \
                -I$(srctree)/techpack/camera-xiaomi-psyche/include
obj-y += drivers/
else
$(info Target not found)
endif
