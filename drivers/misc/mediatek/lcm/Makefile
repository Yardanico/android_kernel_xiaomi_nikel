#
# Makefile for misc devices that really don't fit anywhere else.
#

obj-y += tps65132.o mt65xx_lcm_list.o

LCM_LISTS := $(subst ",,$(CONFIG_CUSTOM_KERNEL_LCM))
#obj-y += $(foreach LCM,$(LCM_LISTS),$(LCM)/)
obj-y += nt35596_fhd_tianma_phantom/

subdir-ccflags-$(CONFIG_MTK_LCM) += -I$(srctree)/drivers/misc/mediatek/lcm/inc
subdir-ccflags-$(CONFIG_MTK_FB) += -I$(srctree)/drivers/misc/mediatek/video/$(MTK_PLATFORM)/dispsys \
                                       -I$(srctree)/drivers/misc/mediatek/video/$(MTK_PLATFORM)/dispsys/mt6735 \
                                       -I$(srctree)/drivers/misc/mediatek/video/$(MTK_PLATFORM)/videox \
                                       -I$(srctree)/drivers/misc/mediatek/video/include

ccflags-$(CONFIG_MTK_LCM) += $(addprefix -D, $(DEFINES))
ccflags-$(CONFIG_MTK_LCM_DEVICE_TREE_SUPPORT) += -DMTK_LCM_DEVICE_TREE_SUPPORT
