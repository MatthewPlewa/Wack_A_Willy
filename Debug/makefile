################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include Drivers/STM32F3xx_HAL_Driver/Src/subdir.mk
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
Wack_A_Willy.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Wack_A_Willy.list \

OBJCOPY_BIN += \
Wack_A_Willy.bin \


# All Target
all: Wack_A_Willy.elf secondary-outputs

# Tool invocations
Wack_A_Willy.elf: $(OBJS) $(USER_OBJS) D:\Embeded_Work\Wack_A_Willy\STM32F303RETX_FLASH.ld
	arm-none-eabi-gcc -o "Wack_A_Willy.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"D:\Embeded_Work\Wack_A_Willy\STM32F303RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Wack_A_Willy.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Wack_A_Willy.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Wack_A_Willy.list"
	@echo 'Finished building: $@'
	@echo ' '

Wack_A_Willy.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "Wack_A_Willy.bin"
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
