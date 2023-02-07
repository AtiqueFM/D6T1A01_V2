################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
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
D6T1A01_V2.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
D6T1A01_V2.list \


# All Target
all: D6T1A01_V2.elf secondary-outputs

# Tool invocations
D6T1A01_V2.elf: $(OBJS) $(USER_OBJS) /home/atiqueshaikh/Forbes\ Marshall\ -\ Projects/STM32_UART/D6T1A01_V2/STM32F407VGTX_FLASH.ld
	arm-none-eabi-gcc -o "D6T1A01_V2.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"/home/atiqueshaikh/Forbes Marshall - Projects/STM32_UART/D6T1A01_V2/STM32F407VGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="D6T1A01_V2.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -u _printf_float -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

D6T1A01_V2.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "D6T1A01_V2.list"
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
