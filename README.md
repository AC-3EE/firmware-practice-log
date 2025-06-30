# Firmware Practice Log

此專案紀錄我在 **STM32 Nucleo-F446RE** 開發板 上進行韌體開發的學習過程。

## 專案目標

透過分階段練習 MCU 各項周邊、通訊介面與 RTOS 整合，累積可重用的模組化程式碼庫，並逐步建立一個可在 STM32 上運作的完整系統。

## 硬體需求

本專案所需的所有硬體元件、模組與注意事項，請參考 [物料清單 (Bill of Materials)](./BOM.md)。

## 學習路徑 (Learning Roadmap)

### 第一部分：核心硬體周邊操作 (Core Peripheral Mastery)
- [phase1_basic_io](./phase1_basic_io/README.md)：GPIO 操作、按鍵偵測、LED 控制
- [phase2_uart_ringbuffer](./phase2_uart_ringbuffer/README.md)：UART 雙向通訊 + Ring Buffer
- [phase3_pwm_servo_control](./phase3_pwm_servo_control/README.md)：Timer PWM 輸出、伺服馬達控制
- [phase4_i2c_oled_sensor](./phase4_i2c_oled_sensor/README.md)：I2C 感測器讀取、OLED 顯示
- [phase5_spi_flash_storage](./phase5_spi_flash_storage/README.md)：SPI Nor Flash 底層讀寫

### 第二部分：系統與軟體層整合 (System & Software Integration)
- [phase6_spi_sdcard_fatfs](./phase6_spi_sdcard_fatfs/README.md)：SPI MicroSD 讀寫、FATFS 檔案系統移植
- [phase7_freertos_integration](./phase7_freertos_integration/README.md)：導入 FreeRTOS、多任務設計

### 第三部分：進階應用與總結 (Advanced Application)
- [phase8_canbus_communication](./phase8_canbus_communication/README.md)：CAN Bus 網路建構、雙節點資料交換

>📚 詳細說明
>每個階段資料夾內含程式碼、測試結果、以及對應的 `README.md` 紀錄具體功能與開發筆記。

## 版本控制

我使用 Git 來管理各階段程式碼版本，並將所有測試結果截圖、以及使用邏輯分析儀取得的數位訊號時序圖，附在 `doc/` 資料夾。

## 授權

MIT License。