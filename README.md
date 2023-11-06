# EXPERIMENT--02-INTEFACING-A-DIGITAL-INPUT-TO-ARM-DEVELOPMENT-BOARD
## Aim: To Interface a Digital Input  (userpush button  ) to ARM   development board and write a  program to obtain  the data and flash the led  
## Components required: STM32 CUBE IDE, ARM IOT development board,  STM programmer tool.
## Theory 
The full form of an ARM is an advanced reduced instruction set computer (RISC) machine, and it is a 32-bit processor architecture expanded by ARM holdings. The applications of an ARM processor include several microcontrollers as well as processors. The architecture of an ARM processor was licensed by many corporations for designing ARM processor-based SoC products and CPUs. This allows the corporations to manufacture their products using ARM architecture. Likewise, all main semiconductor companies will make ARM-based SOCs such as Samsung, Atmel, TI etc.

## STM 32 CUBE PROGRAM :
```
DEVELOPED BY:Tejusve Kabeer.F REG.NO: 212222100054

#include "main.h"
#include "stdbool.h"
bool button_status;
void push_button();
void SystemClock_Config(void);
static void MX_GPIO_Init(void);
int main(void){
while (1){
push_button();
}
}
void push_button(){
button_status =HAL_GPIO_ReadPin(GPIOC, GPIO_PIN_13);
if(button_status == 0){
HAL_GPIO_WritePin(GPIOA, GPIO_PIN_5, GPIO_PIN_SET);
HAL_Delay(1000);
HAL_GPIO_WritePin(GPIOA, GPIO_PIN_5, GPIO_PIN_RESET);
HAL_Delay(1000);
}
else
{
HAL_GPIO_WritePin(GPIOA, GPIO_PIN_5, GPIO_PIN_RESET);
}
}
```
## Output  :
![image](https://github.com/Reebak04/EXPERIMENT--02-INTEFACING-A-DIGITAL-INPUT-TO-ARM-DEVELOPMENT-BOARD/assets/118364993/b0e7c63a-137f-4caf-b834-e6525a9e1d33)


![image](https://github.com/Reebak04/EXPERIMENT--02-INTEFACING-A-DIGITAL-INPUT-TO-ARM-DEVELOPMENT-BOARD/assets/118364993/4e123df3-86b9-4266-8c56-81bfe8a62011)

## Result :
Interfacing a digital Input (Pushbutton ) with ARM microcontroller based IOT development is executed and the results are verified.
