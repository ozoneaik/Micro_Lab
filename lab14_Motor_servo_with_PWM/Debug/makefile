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
lab14_Motor_servo_with_PWM.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
lab14_Motor_servo_with_PWM.list \

OBJCOPY_HEX += \
lab14_Motor_servo_with_PWM.hex \

OBJCOPY_BIN += \
lab14_Motor_servo_with_PWM.bin \


# All Target
all: lab14_Motor_servo_with_PWM.elf secondary-outputs

# Tool invocations
lab14_Motor_servo_with_PWM.elf: $(OBJS) $(USER_OBJS) C:\Users\Phuwadech\STM32CubeIDE\workspace_1.3.0\lab14_Motor_servo_with_PWM\STM32F401CCFX_FLASH.ld
	arm-none-eabi-gcc -o "lab14_Motor_servo_with_PWM.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\Phuwadech\STM32CubeIDE\workspace_1.3.0\lab14_Motor_servo_with_PWM\STM32F401CCFX_FLASH.ld" --specs=nosys.specs -Wl,-Map="lab14_Motor_servo_with_PWM.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

lab14_Motor_servo_with_PWM.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "lab14_Motor_servo_with_PWM.list"
	@echo 'Finished building: $@'
	@echo ' '

lab14_Motor_servo_with_PWM.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "lab14_Motor_servo_with_PWM.hex"
	@echo 'Finished building: $@'
	@echo ' '

lab14_Motor_servo_with_PWM.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "lab14_Motor_servo_with_PWM.bin"
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
