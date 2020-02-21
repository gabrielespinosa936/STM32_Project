################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F7xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
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
Data_Grabber_V0.01.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Data_Grabber_V0.01.list \

OBJCOPY_BIN += \
Data_Grabber_V0.01.bin \


# All Target
all: Data_Grabber_V0.01.elf secondary-outputs

# Tool invocations
Data_Grabber_V0.01.elf: $(OBJS) $(USER_OBJS) /Users/gabrielespinosa/STM32CubeIDE/workspace_1.0.1/Data_Grabber_V0.01/STM32F746ZGTX_FLASH.ld
	arm-none-eabi-gcc -o "Data_Grabber_V0.01.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m7 -T"/Users/gabrielespinosa/STM32CubeIDE/workspace_1.0.1/Data_Grabber_V0.01/STM32F746ZGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Data_Grabber_V0.01.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv5-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Data_Grabber_V0.01.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Data_Grabber_V0.01.list"
	@echo 'Finished building: $@'
	@echo ' '

Data_Grabber_V0.01.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "Data_Grabber_V0.01.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
