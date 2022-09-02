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
lab11.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
lab11.list \

OBJCOPY_HEX += \
lab11.hex \

OBJCOPY_BIN += \
lab11.bin \


# All Target
all: lab11.elf secondary-outputs

# Tool invocations
lab11.elf: $(OBJS) $(USER_OBJS) C:\Users\Phuwadech\STM32CubeIDE\workspace_1.3.0\lab11\STM32F401CCFX_FLASH.ld
	arm-none-eabi-gcc -o "lab11.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\Phuwadech\STM32CubeIDE\workspace_1.3.0\lab11\STM32F401CCFX_FLASH.ld" --specs=nosys.specs -Wl,-Map="lab11.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

lab11.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "lab11.list"
	@echo 'Finished building: $@'
	@echo ' '

lab11.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "lab11.hex"
	@echo 'Finished building: $@'
	@echo ' '

lab11.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "lab11.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
