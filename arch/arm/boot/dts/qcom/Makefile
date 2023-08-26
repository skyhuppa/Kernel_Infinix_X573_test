# SPDX-License-Identifier: GPL-2.0
dtb-$(CONFIG_ARCH_MSM8937) += msm8937-X573.dtb \
                              msm8917-X573.dtb

dtb-$(CONFIG_MSM_GVM_QUIN) += vplatform-lfv-msm8996.dtb

dtb-$(CONFIG_ARCH_MSMCOBALT) += msmcobalt-sim.dtb \
	msmcobalt-rumi.dtb \
	msmcobalt-cdp.dtb \
	msmcobalt-mtp.dtb \
	msmcobalt-v2-sim.dtb \
	msmcobalt-v2-rumi.dtb \
	msmcobalt-v2-mtp.dtb \
	msmcobalt-v2-cdp.dtb

# ifeq ($(strip $(CONFIG_BUILD_ARM64_APPENDED_DTB_IMAGE)), y)
# dtb-y += $(addsuffix .dtb, $(notdir $(subst $\",,$(CONFIG_BUILD_ARM64_APPENDED_DTB_IMAGE_NAMES))))
# endif

# ifeq ($(strip $(CONFIG_MSM8937_MSM8917_TECNO_DTB)), y)
# dtb-y += $(addsuffix .dtb, $(notdir $(subst $\",,$(CONFIG_MSM8937_MSM8917_TECNO_DTB))))
# endif

targets  += $(dtb-y)
always   := $(dtb-y)
subdir-y := $(dts-dirs)

clean-files := *.dtb
