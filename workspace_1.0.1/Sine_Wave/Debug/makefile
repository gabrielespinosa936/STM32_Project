################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include Drivers/STM32F7xx_HAL_Driver/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
Sine_Wave.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Sine_Wave.list \


# All Target
all: Sine_Wave.elf secondary-outputs

# Tool invocations
Sine_Wave.elf: $(OBJS) $(USER_OBJS) /Users/gabrielespinosa/STM32CubeIDE/workspace_1.0.1/Sine_Wave/STM32F746ZGTX_FLASH.ld
	arm-none-eabi-gcc -o "Sine_Wave.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m7 -T"/Users/gabrielespinosa/STM32CubeIDE/workspace_1.0.1/Sine_Wave/STM32F746ZGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Sine_Wave.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv5-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Sine_Wave.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Sine_Wave.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
