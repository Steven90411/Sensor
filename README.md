
# WearableDataMock

### 模擬智慧手環健康數據的生成器

**WearableDataMock** 是一個用於生成智慧手環模擬健康數據的 Spring Boot 應用程式。它生成的數據模擬智慧手環可能會收集的健康指標，包括心率、血壓、血糖、血氧等資訊。這些模擬數據可以用於開發和測試需要穿戴設備數據的應用程式。

## 功能

- **心率 (heartRate)**：模擬每分鐘心跳次數，範圍為 60–100。
- **血壓 (bloodPressure)**：提供收縮壓和舒張壓數據，範圍分別為 110–130 和 70–80。
- **血糖 (bloodSugar)**：模擬血糖水平，範圍為 80–120。
- **血氧 (bloodOxygen)**：模擬血氧濃度，範圍為 95–100。
- **時間戳記 (timestamp)**：自動生成數據的時間戳，記錄數據生成的時間。

## 安裝與運行

1. 克隆此 repository 到本地：

   ```bash
   git clone https://github.com/Steven90411/WearableDataMock.git
   cd WearableDataMock
   ```

2. 使用 Maven 進行打包和運行：

   ```bash
   mvn spring-boot:run
   ```

3. 確認應用程式正在本地伺服器上運行（通常為 `http://localhost:8080`）。

## API

- **GET /api/healthData**：獲取隨機生成的模擬健康數據。

   **範例響應**：
   ```json
   {
       "heartRate": 78,
       "bloodPressure": {
           "systolic": 118,
           "diastolic": 75
       },
       "bloodSugar": 95,
       "bloodOxygen": 97,
       "timestamp": "2024-10-29T14:32:17"
   }
   ```

## 使用案例

WearableDataMock 適合用於需要模擬智慧手環數據的開發場景，例如：

- 測試健康管理應用程式的數據接收功能。
- 在不具備實際穿戴設備的情況下模擬數據來源。
- 提供初步的健康數據供機器學習模型進行測試。

## 貢獻

歡迎提交問題或提出改進建議。如有任何疑問或功能需求，請在 GitHub Issue 中與我們聯繫。
