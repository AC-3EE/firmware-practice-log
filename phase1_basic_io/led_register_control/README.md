# STM32 HAL LED 閃爍練習

本專案示範如何使用 STM32 HAL 函式庫，透過 `HAL_Delay` 與 `HAL_GPIO_TogglePin` 控制 LED 週期性閃爍。

> 本專案目的是熟悉 STM32CubeIDE 開發環境與 HAL API 的基本使用方法。

---

### 專案目標 (Goal)

* **學習目標 1:** 熟悉 STM32CubeIDE 開發環境與 HAL 函式庫的基本用法。
* **學習目標 2:** 了解如何設定 GPIO 為輸出模式。
* **驗證目標:** 實現一個最基礎的「Hello, World」級別嵌入式程式，確保開發環境與硬體正常運作。

### 開發環境與硬體 (Environment & Hardware)

* **MCU:** STMicroelectronics STM32F446RE
* **開發板 (Board):** Nucleo-F446RE
* **開發工具 (IDE):** STM32CubeIDE v1.18.1
* **硬體連線:**
    * `PA5`: 連接至開發板上的綠色 LED (LD2)。無需額外接線。

### 核心概念與程式邏輯 (Key Concepts & Logic)

1.  **初始化 (Initialization):**
    * 程式首先呼叫 `HAL_Init()` 來初始化 HAL 函式庫、Flash 介面和 Systick 計時器。
    * 接著透過 `SystemClock_Config()` 設定系統時脈。
    * 最後，`MX_GPIO_Init()` 將 `PA5` 腳位設定為推挽輸出模式 (Output Push-Pull)。
2.  **主迴圈 (Main Loop):**
    * 在 `while(1)` 的無窮迴圈中，程式反覆執行兩個主要操作。
    * `HAL_GPIO_TogglePin(GPIOA, GPIO_PIN_5)`: 翻轉 `PA5` 腳位的電位狀態（高電位 -> 低電位，或反之），從而點亮或熄滅 LED。
    * `HAL_Delay(500)`: 執行一個 500 毫秒的阻塞式延遲。這會暫停程式執行，直到延遲時間結束。

### 如何編譯與執行 (How to Build & Run)

1.  使用 STM32CubeIDE 匯入此專案。
2.  點擊 `Build` 按鈕 (槌子圖示) 編譯專案。
3.  將開發板透過 USB 連接至電腦。
4.  點擊 `Run` 按鈕 (綠色播放圖示) 將程式碼燒錄並執行。
5.  觀察開發板上的綠色 LED (LD2) 是否以 1Hz 的頻率閃爍（亮 0.5 秒，滅 0.5 秒）。

### 成果展示 (Showcase)

![LED閃爍](../../doc/phase1_led_register_control.gif)

### 心得與反思 (Learnings & Reflections)

* **阻塞式延遲的缺點:** `HAL_Delay()` 雖然簡單易用，但它是「阻塞式 (Blocking)」的。在 500ms 的延遲期間，CPU 不能做任何其他事情。在更複雜的應用中（例如需要同時監聽按鍵），這種作法會導致系統反應遲鈍。
* **未來改進:** 可以改用 Systick 中斷或 Timer 中斷來實現非阻塞式 (Non-blocking) 的延遲，讓 CPU 在等待期間可以去處理其他任務。