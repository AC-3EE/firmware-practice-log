# Phase 1 - Basic IO

此階段包含基礎 GPIO 操作、HAL 對比、按鍵控制與防抖動實驗，目標是熟悉 STM32 GPIO 操作與開發環境，建立後續開發的基礎。子專案包含：

- led_register_control：直接操作暫存器點亮 LED

- led_hal_comparison：HAL 實作對比

- button_led_control：按鍵控制 LED

- button_debounce_logic：防抖動邏輯與邏輯分析儀驗證