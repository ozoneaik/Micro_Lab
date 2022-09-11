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
lab13_Timer.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
lab13_Timer.list \

OBJCOPY_HEX += \
lab13_Timer.hex \

OBJCOPY_BIN += \
lab13_Timer.bin \

OBJCOPY_SREC += \
lab13_Timer.srec \


# All Target
all: lab13_Timer.elf secondary-outputs

# Tool invocations
lab13_Timer.elf: $(OBJS) $(USER_OBJS) C:\Users\Phuwadech\STM32CubeIDE\workspace_1.3.0\lab13_Timer\STM32F401CCFX_FLASH.ld
	arm-none-eabi-gcc -o "lab13_Timer.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\Phuwadech\STM32CubeIDE\workspace_1.3.0\lab13_Timer\STM32F401CCFX_FLASH.ld" --specs=nosys.specs -Wl,-Map="lab13_Timer.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

lab13_Timer.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "lab13_Timer.list"
	@echo 'Finished building: $@'
	@echo ' '

lab13_Timer.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "lab13_Timer.hex"
	@echo 'Finished building: $@'
	@echo ' '

lab13_Timer.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "lab13_Timer.bin"
	@echo 'Finished building: $@'
	@echo ' '

lab13_Timer.srec: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O srec $(EXECUTABLES) "lab13_Timer.srec"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN) $(OBJCOPY_SREC)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
