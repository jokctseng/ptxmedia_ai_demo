# 不上雲 AI 助理 (Local WebLLM Assistant)

這是一個基於 [WebLLM](https://webllm.mlc.ai/) 技術打造的純前端單頁應用程式，可視為Gem與相類預先設置系統提示詞及資料庫的在地版；透過 WebGPU 技術，所有的 AI 模型下載與推論運算皆在**使用者的瀏覽器端**完成，對話資料不上雲，確保隱私安全。


---

## 核心特色

*  **完全離線運算**：無後端伺服器，對話內容 100% 留在您的設備中。
*  **多模型自由切換**：內建支援 Google Gemma-2 (2B/9B) 與 Meta Llama-3 (1B/3B/8B) 系列量化模型，未使用中國模型，可適用於公部門與大專院校。
*  **即時參數調整**：提供介面隨時調整 `Temperature`、`Top P` 與 `Max Tokens`，控制文案的創造力與長度。
*  **參考文件輔助**：支援上傳 `.txt`, `.md`, `.csv` 等純文字檔案作為 AI 寫作的單次參考素材。

## 系統與硬體需求

由於 AI 模型是在GPU上執行，請確保您的設備符合以下條件：
1.  **瀏覽器**：最新版本的 Google Chrome、Microsoft Edge和其他以Chromium為基礎的瀏覽器（需支援 WebGPU）。
2.  **記憶體 (RAM/VRAM)**：
    * 執行 **2B / 3B** 模型：建議至少 4GB 系統可用記憶體。
    * 執行 **8B / 9B** 模型：建議至少 8GB 系統可用記憶體與強大的獨立顯卡 / Apple M 系列晶片。
3.  **網路環境**：初次啟用各模型時，需下載 1GB ~ 5GB 不等的權重檔案（下載後將自動快取於瀏覽器中，後續使用可完全斷網）。

## 開發與測試

若想下載並在電腦上使用，或者自行開發其他版本，使用檔案時，建議**勿直接雙擊 `index.html` 開啟！**
瀏覽器可能會阻擋 `file:///` 路徑載入 WebGPU 與外部模組。

1.  建議使用 [Visual Studio Code](https://code.visualstudio.com/) 編輯器。
2.  安裝 [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) 擴充套件。
3.  在 `index.html` 點擊右鍵，選擇 **"Open with Live Server"**。
4.  瀏覽器將自動開啟 `http://127.0.0.1:5500/index.html`，即可順利載入模型。

或於終端機以python `http.server` 建立local host



## 技術

* [WebLLM](https://webllm.mlc.ai/) 
* [Tailwind CSS](https://tailwindcss.com/) 
* [Marked.js](https://marked.js.org/) 
* [DOMPurify](https://github.com/cure53/DOMPurify) 
* [Phosphor Icons](https://phosphoricons.com/) 
* Google Fonts (Google Sans Flex / Noto Sans TC)

