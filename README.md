Low-power test and reached 2uA with STM32L476 Disco .

## Activate ##
MX_GPIO_Init();<br>
MX_DMA_Init();<br>
MX_ADC1_Init();<br>
MX_I2C1_Init();<br>
MX_I2C2_Init();<br>
MX_LPTIM1_Init();<br>
MX_RTC_Init();<br>
MX_SPI1_Init();<br>
MX_SPI2_Init();<br>
MX_TIM1_Init();<br>
MX_TIM2_Init();<br>
MX_TIM3_Init();<br>
MX_TIM4_Init();<br>
MX_TIM5_Init();<br>
MX_LPUART1_UART_Init();<br>
MX_USART1_UART_Init();<br>
MX_USART2_UART_Init();<br>
MX_USART3_UART_Init();<br>

## Deactivate ##
HAL_I2C_DeInit(&hi2c1);<br>
HAL_I2C_DeInit(&hi2c2);<br>

HAL_TIM_PWM_DeInit(&htim1);<br>
HAL_TIM_PWM_DeInit(&htim2);<br>
HAL_TIM_PWM_DeInit(&htim3);<br>
HAL_TIM_PWM_DeInit(&htim4);<br>
HAL_TIM_PWM_DeInit(&htim5);<br>

HAL_TIM_Base_DeInit(&htim1);<br>
HAL_TIM_Base_DeInit(&htim2);<br>
HAL_TIM_Base_DeInit(&htim3);<br>
HAL_TIM_Base_DeInit(&htim4);<br>
HAL_TIM_Base_DeInit(&htim5);<br>

HAL_SPI_DeInit(&hspi1);<br>
HAL_SPI_DeInit(&hspi2);<br>

HAL_UART_DeInit(&huart1);<br>
HAL_UART_DeInit(&huart2);<br>
HAL_UART_DeInit(&huart3);<br>

HAL_ADC_Stop_DMA(&hadc1); //-0.1uA<br>
HAL_ADC_DeInit(&hadc1);   //-15uA<br>

HAL_SuspendTick();<br>
HAL_PWREx_EnterSTOP2Mode(PWR_STOPENTRY_WFI);<br>
