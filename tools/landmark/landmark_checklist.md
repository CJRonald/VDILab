# Landmark 標註清單（17 點，schema v1.1）

工具載入照片後右側面板會列出這 17 點；本卡供離線對照。完整定義見 [SimAI landmark_schema_v1.md](../../Rhino_Hsiao_SimAI_Landmark/01_Annotation/landmark_schema_v1.md)。

> **戒律**：標完一張一定 17 點都動過，看不到的點也要 placeholder + vis=0。

## 標註順序（建議）

### 鼻部主軸（先標當骨架）
| # | 點 | 中 | 解剖定義 | AP | Lateral |
|---|----|----|---------|:--:|:------:|
| 1 | **Nasion** | 鼻根 | 鼻額縫最深點軟組織投影 | ✅ | ✅ |
| 2 | **Pronasale** | 鼻尖 | 鼻尖最突點 | ✅ | ✅ |
| 3 | **Subnasale** | 鼻下點 | 鼻小柱與上唇接點正中 | ✅ | ✅ |

### 左右配對（一起標避免錯邊；R=病人自己的右=AP 照觀察者的左）
| # | 點 | 中 | 解剖定義 | AP | Lateral |
|---|----|----|---------|:--:|:------:|
| 4 | **Alare R** | 右鼻翼緣 | 右鼻翼緣最外側點 | ✅ | (近側可見) |
| 5 | **Alare L** | 左鼻翼緣 | 左鼻翼緣最外側點 | ✅ | (近側可見) |
| 6 | **Alar base R** | 右鼻翼基底 | 右鼻翼與面頰交界最下點 | ✅ | — |
| 7 | **Alar base L** | 左鼻翼基底 | 左鼻翼與面頰交界最下點 | ✅ | — |

### 鼻下/輔助
| # | 點 | 中 | 解剖定義 | AP | Lateral |
|---|----|----|---------|:--:|:------:|
| 8 | **Columella-lip** | 鼻小柱底 | 鼻小柱底與人中接點 | ✅ | ✅ |
| 9 | **Labiale sup.** | 上唇紅唇緣 | 上唇紅唇邊緣正中點 | ✅ | ✅ |
| 10 | **Glabella** | 眉間 | 兩眉之間額骨最前突軟組織 | (退化) | ✅ |
| 11 | **Rhinion** ⭐ | 鼻背中點 | 鼻骨與軟骨交界軟組織投影 | — | ✅ |

### 眼部 6 點（normalize 用，最後標）
| # | 點 | 中 | AP | Lateral |
|---|----|----|:--:|:------:|
| 12 | **Med canthus R** | 右內眼角 | ✅ | 近側 |
| 13 | **Med canthus L** | 左內眼角 | ✅ | 近側 |
| 14 | **Lat canthus R** | 右外眼角 | ✅ | 近側 |
| 15 | **Lat canthus L** | 左外眼角 | ✅ | 近側 |
| 16 | **Pupil R** | 右瞳孔 | ✅ | (退化) |
| 17 | **Pupil L** | 左瞳孔 | ✅ | (退化) |

## Slope spreader 量測關鍵點（⭐ 必精準）

側面角度全靠這幾點，標 lateral 時優先確保：
- **Glabella(10) + Nasion(1) + Pronasale(2)** → NFA + dorsal slope
- **Nasion(1) + Rhinion(11) + Pronasale(2)** → ⭐ dorsal curvature（slope spreader 直接療效）
- **Pronasale(2) + Subnasale(3) + Labiale sup.(9)** → NLA

## Visibility 速查

| 值 | 意義 |
|---|---|
| 1.0 | 清晰，一秒鎖定 |
| 0.7 | 可見但輕度遮/陰影 |
| 0.3 | 推測位置（厚妝/中度遮）|
| 0.0 | 完全不可見 / 該 view 不存在（仍 placeholder）|

## 邊緣 case

| 情況 | 處理 |
|------|------|
| 口罩遮下臉 | 整張 exclude |
| 眼鏡遮 glabella | glabella vis=0.3 |
| Saddle nose 無 rhinion bump | 標 dorsum 中點 vis=0.7 |
| Scar 遮鼻部（如 SS04）| 受影響點 vis=0.3-0.5 |
| Lateral 對側 alare 看不到 | placeholder + vis=0.0 |

---

*對齊 Rhino_Hsiao_SimAI_Landmark schema v1.1 | 2026-06-14*
