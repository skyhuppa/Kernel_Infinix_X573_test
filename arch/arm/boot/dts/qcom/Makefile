# SPDX-License-Identifier: GPL-2.0
dtb-$(CONFIG_ARCH_MSMCOBALT) += msmcobalt-sim.dtb \
	msmcobalt-rumi.dtb \
	msmcobalt-cdp.dtb \
	msmcobalt-mtp.dtb \
	msmcobalt-v2-sim.dtb \
	msmcobalt-v2-rumi.dtb \
	msmcobalt-v2-mtp.dtb \
	msmcobalt-v2-cdp.dtb

# dtb-$(CONFIG_ARCH_MSM8937) += msm8937-rumi.dtb 

dtb-$(CONFIG_MSM8937_MSM8917_TECNO_DTB) += msm8937-rumi.dtb \
msm8917-rumi.dtb

# dtb-$(CONFIG_ARCH_MSM8917) += msm8917-rumi.dtb

ifeq ($(CONFIG_ARM64),y)
always          := $(dtb-y)
subdir-y        := $(dts-dirs)
else
targets += dtbs
targets += $(addprefix ../, $(dtb-y))

$(obj)/../%.dtb: $(src)/%.dts FORCE
        $(call if_changed_dep,dtc)

dtbs: $(addprefix $(obj)/,$(dtb-y))
endif
clean-files := *.dtb
endif
