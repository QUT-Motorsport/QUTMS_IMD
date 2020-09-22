################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F0xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
QUTMS_SHDN_IMD.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
QUTMS_SHDN_IMD.list \

OBJCOPY_BIN += \
QUTMS_SHDN_IMD.bin \


# All Target
all: QUTMS_SHDN_IMD.elf secondary-outputs

# Tool invocations
QUTMS_SHDN_IMD.elf: $(OBJS) $(USER_OBJS) C:\Users\Motorsports\Desktop\git\QUTMS_IMD\Software\STM32F042C6TX_FLASH.ld
	arm-none-eabi-gcc -o "QUTMS_SHDN_IMD.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0 -T"C:\Users\Motorsports\Desktop\git\QUTMS_IMD\Software\STM32F042C6TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="QUTMS_SHDN_IMD.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

QUTMS_SHDN_IMD.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "QUTMS_SHDN_IMD.list"
	@echo 'Finished building: $@'
	@echo ' '

QUTMS_SHDN_IMD.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "QUTMS_SHDN_IMD.bin"
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
