# Copyright (c) 2025 Alif Semiconductor
# SPDX-License-Identifier: Apache-2.0

zephyr_include_directories(.)
add_subdirectory(common)
add_subdirectory(${SOC_SERIES})

zephyr_sources_ifdef(CONFIG_ARM_AARCH32_MMU common/mmu_regions.c)
zephyr_sources_ifdef(CONFIG_APSS common/vector_table.c)

