# SpaceXCleanArch

這是一個基於 SpaceX API 的 Android 專案，旨在實踐 **Clean Architecture (乾淨架構)**、**Jetpack Compose** 以及現代 Android 開發的最佳實踐。

## 🏗️ 專案架構 (Architecture)

本專案採用多模組 (Multi-module) 結構，並嚴格遵循 Clean Architecture 原則：

- **`:domain`**: (Pure Kotlin/Java) 包含業務邏輯、實體 (Entities) 與 Use Cases。它不依賴於任何架構層級。
- **`:data`**: 負責資料來源的管理，包括網路請求 (Retrofit) 與本地資料庫。實作 `:domain` 層定義的 Repository 介面。
- **`:app`**: (Android/UI) 包含 UI 元件 (Jetpack Compose)、ViewModel 與相應的架構組件。

## 🛠️ 技術棧 (Tech Stack)

- **Language**: [Kotlin](https://kotlinlang.org/)
- **UI**: [Jetpack Compose](https://developer.android.com/jetpack/compose) (Material 3)
- **Dependency Injection**: [Hilt](https://developer.android.com/training/dependency-injection/hilt-android)
- **Networking**: [Retrofit](https://square.github.io/retrofit/) & [Kotlinx Serialization](https://github.com/Kotlin/kotlinx.serialization)
- **Asynchronous**: [Kotlin Coroutines](https://kotlinlang.org/docs/coroutines-overview.html) & [Flow](https://kotlinlang.org/docs/flow.html)
- **Build System**: Gradle Kotlin DSL & Version Catalog

## 🚀 模組介紹

### `:domain`
- 包含純 Kotlin 代碼。
- 定義專案的核心業務邏輯。
- 使用 `Repository` 介面定義資料需求。

### `:data`
- 實作資料存取邏輯。
- 包含 API 服務與資料映射器 (Mappers)。

### `:app`
- 負責顯示 UI 與處理使用者互動。
- 使用 Hilt 進行依賴注入。
- 使用 ViewModel 管理狀態。

## 📦 如何開始

1. 複製此專案：
   ```bash
   git clone https://github.com/your-username/SpaceXCleanArch.git
   ```
2. 使用 Android Studio 打開專案。
3. 等待 Gradle 同步完成。
4. 點擊 **Run** 即可在模擬器或實體裝置上運行。

## 📜 授權

此專案基於 MIT 授權。
