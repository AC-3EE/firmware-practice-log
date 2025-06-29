# Firmware Practice Log

此專案紀錄我在 **STM32 Nucleo-F446RE** 開發板 上進行韌體開發的學習過程。

## 專案目標

透過分階段練習 MCU 各項周邊、通訊介面與 RTOS 整合，累積可重用的模組化程式碼庫，並逐步建立一個可在 STM32 上運作的完整系統。

## 階段列表

- `phase1_basic_io`：GPIO 操作、按鍵偵測、LED 控制

- `phase2_uart_ringbuffer`：UART 雙向通訊 + Ring Buffer

- `phase3_i2c_oled_sensor`：I2C 溫度感測器讀取、OLED 顯示

- `phase4_spi_sdcard_fatfs`：SPI MicroSD 讀寫、FATFS 檔案系統

- `phase5_freertos_integration`：導入 FreeRTOS、多任務整合

>📚 詳細說明
>每個階段資料夾內含程式碼、測試結果、以及對應的 `README.md` 紀錄具體功能與開發筆記。

## 版本控制

我使用 Git 來管理各階段程式碼版本，並附上測試結果截圖、波形圖於 `doc/` 資料夾。

## 授權

MIT License。
