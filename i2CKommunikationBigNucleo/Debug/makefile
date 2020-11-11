################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32L4xx_HAL_Driver/Src/subdir.mk
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
i2CKommunikationBigNucleo.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
i2CKommunikationBigNucleo.list \

OBJCOPY_BIN += \
i2CKommunikationBigNucleo.bin \


# All Target
all: i2CKommunikationBigNucleo.elf secondary-outputs

# Tool invocations
i2CKommunikationBigNucleo.elf: $(OBJS) $(USER_OBJS) E:\OneDrive\arbeit\Elektronik\STM\CubeIDE\i2CKommunikationBigNucleo\STM32L476RGTX_FLASH.ld
	arm-none-eabi-gcc -o "i2CKommunikationBigNucleo.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"E:\OneDrive\arbeit\Elektronik\STM\CubeIDE\i2CKommunikationBigNucleo\STM32L476RGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="i2CKommunikationBigNucleo.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

i2CKommunikationBigNucleo.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "i2CKommunikationBigNucleo.list"
	@echo 'Finished building: $@'
	@echo ' '

i2CKommunikationBigNucleo.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "i2CKommunikationBigNucleo.bin"
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
