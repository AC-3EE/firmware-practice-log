Firmware Practice Log

此專案紀錄我的韌體開發學習過程，分階段完成各種 MCU 周邊、通訊協定、RTOS 等相關練習，並逐步整合為一個完整系統。

階段列表

phase1_basic_io：GPIO 基礎操作、按鍵偵測、LED 控制。

phase2_uart_ringbuffer：UART 雙向通訊 + Ring Buffer 實作。

phase3_i2c_oled_sensor：驅動 I2C 溫度感測器與 OLED 顯示。

phase4_spi_sdcard_fatfs：SPI Flash、MicroSD + FATFS。

phase5_freertos_integration：FreeRTOS 任務管理、資源共享。

版本控制

我使用 Git 來管理各階段程式碼版本，並附上測試結果截圖、波形圖於 doc/ 資料夾。

授權

MIT License。
