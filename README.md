Low-power test and reached 2uA with STM32L476 Disco .

##Activate
MX_GPIO_Init();
MX_DMA_Init();
MX_ADC1_Init();
MX_I2C1_Init();
MX_I2C2_Init();
MX_LPTIM1_Init();
MX_RTC_Init();
MX_SPI1_Init();
MX_SPI2_Init();
MX_TIM1_Init();
MX_TIM2_Init();
MX_TIM3_Init();
MX_TIM4_Init();
MX_TIM5_Init();
MX_LPUART1_UART_Init();
MX_USART1_UART_Init();
MX_USART2_UART_Init();
MX_USART3_UART_Init();

##Deactivate
HAL_I2C_DeInit(&hi2c1);
HAL_I2C_DeInit(&hi2c2);

HAL_TIM_PWM_DeInit(&htim1);
HAL_TIM_PWM_DeInit(&htim2);
HAL_TIM_PWM_DeInit(&htim3);
HAL_TIM_PWM_DeInit(&htim4);
HAL_TIM_PWM_DeInit(&htim5);

HAL_TIM_Base_DeInit(&htim1);
HAL_TIM_Base_DeInit(&htim2);
HAL_TIM_Base_DeInit(&htim3);
HAL_TIM_Base_DeInit(&htim4);
HAL_TIM_Base_DeInit(&htim5);

HAL_SPI_DeInit(&hspi1);
HAL_SPI_DeInit(&hspi2);

HAL_UART_DeInit(&huart1);
HAL_UART_DeInit(&huart2);
HAL_UART_DeInit(&huart3);

HAL_ADC_Stop_DMA(&hadc1); //-0.1uA
HAL_ADC_DeInit(&hadc1);   //-15uA

HAL_SuspendTick();
HAL_PWREx_EnterSTOP2Mode(PWR_STOPENTRY_WFI);  //-13uA, can't use uart2, total : 2.77uA
