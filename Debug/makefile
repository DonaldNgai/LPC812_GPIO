################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include example/src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: periph_gpio.axf

# Tool invocations
periph_gpio.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -L"/home/donald/Documents/MCUXpresso_10.0.0_344/workspace/lpc_chip_8xx/Debug" -L"/home/donald/Documents/MCUXpresso_10.0.0_344/workspace/lpc_board_nxp_lpcxpresso_812/Debug" -Xlinker -Map="periph_gpio.map" -Xlinker --gc-sections -mcpu=cortex-m0 -mthumb -T "periph_gpio_Debug.ld" -o "periph_gpio.axf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) periph_gpio.axf
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "periph_gpio.axf"; # arm-none-eabi-objcopy -v -O binary "periph_gpio.axf" "periph_gpio.bin" ; # checksum -p LPC812 -d "periph_gpio.bin";
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY: post-build

-include ../makefile.targets
