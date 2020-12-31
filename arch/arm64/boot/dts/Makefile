# I am only compiling for one chip, so no need to add support for others
dtb-y += exynos7870-j7xelte_eur_open_00.dtb
dtb-y += exynos7870-j7xelte_eur_open_01.dtb
dtb-y += exynos7870-j7xelte_eur_open_02.dtb
dtb-y += exynos7870-j7xelte_eur_open_03.dtb
dtb-y += exynos7870-j7xelte_eur_open_04.dtb

targets += dtbs

DTB_NAMES := $(subst $\",,$(CONFIG_BUILD_ARM64_APPENDED_DTB_IMAGE_NAMES))
ifneq ($(DTB_NAMES),)
DTB_LIST := $(addsuffix .dtb,$(DTB_NAMES))
else
DTB_LIST := $(dtb-y)
endif
targets += $(DTB_LIST)


dtbs: $(addprefix $(obj)/, $(DTB_LIST))

clean-files := dts/*.dtb *.dtb
