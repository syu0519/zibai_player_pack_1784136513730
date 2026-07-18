# 茲白 · 試玩

茲白 Time Machine 世界探索 Demo——用 LingBot-World 生成的 42 段場景影片串接而成的可互動小遊戲，用鍵盤或按鈕在神社場景中自由移動、轉身、待機。

<img width="506" height="902" alt="zibai  2026-07-18 145538" src="https://github.com/user-attachments/assets/35c3dd4b-4a4a-4caf-8600-783facb8f42e" />

## 怎麼玩

打開 `index.html`，用以下按鍵探索：

| 鍵位 | 動作 |
|---|---|
| `W` | 前進 |
| `A` | 左移 |
| `S` | 待機 |
| `D` | 右移 |
| `B` | 後退 |
| `T` | 轉身 |

左上角 🔇/🔊 可切換背景音樂，第一次按方向鍵時會自動嘗試播放（瀏覽器限制，需使用者先互動才能出聲）。

灰掉的按鈕代表目前站的位置還沒有那個方向的記憶。

## 資料夾結構

```
.
├── index.html
├── videos/        42 支場景影片 (seg_001.mp4 ~ seg_042.mp4)
└── music/
    └── bgm.mp3    背景音樂
```

## 技術說明

- 影片由 [LingBot-World](https://github.com/Robbyant/lingbot-world) 生成，透過 ComfyUI (`ComfyUI_Rebels_LingBotWorld` 節點包) 產出
- 場景以節點圖 (graph) 串接，每個節點對應一個場景位置，邊 (edge) 對應一段動作影片
- 純前端實作，無後端依賴，可直接用瀏覽器開啟或部署在任何靜態網頁託管服務

## 建議瀏覽器

Chrome 或 Edge。若要錄影功能穩定運作，建議搭配「匯出可攜包 (ZIP)」版本使用，避免影片跨網域來源導致瀏覽器擋下畫面擷取。

---

vplab · 虛擬製作研習社
