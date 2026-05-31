# 📦 Danh Sách Files Sẽ Push Lên GitHub (Portfolio)

## ✅ SẼ PUSH (Quan trọng cho nhà tuyển dụng)

### 📄 Documentation (3 files)
```
✅ README.md              - Giới thiệu project, technical skills
✅ PORTFOLIO.md           - Code highlights, best practices
✅ .gitignore             - Professional git workflow
```

### 💻 Scripts - Core Code (~80 files, ~15,000 lines)
```
✅ Assets/Scripts/
   ├── Animation/         - Character customization system ⭐⭐⭐⭐⭐
   │   ├── ApplyCharacterCustomisation.cs (1078 lines)
   │   ├── AnimationOverrides.cs
   │   ├── CharacterAttribute.cs
   │   └── MovementAnimationParameterControl.cs
   │
   ├── AStar/            - Pathfinding algorithm ⭐⭐⭐⭐⭐
   │   ├── AStar.cs
   │   ├── GridNodes.cs
   │   └── Node.cs
   │
   ├── Crop/             - Farming system ⭐⭐⭐⭐
   │   ├── Crop.cs
   │   ├── CropDetails.cs
   │   ├── CropInstantiator.cs
   │   └── SO_CropDetailsList.cs
   │
   ├── Enums/            - Type definitions
   │   └── Enums.cs
   │
   ├── Events/           - Event-driven architecture ⭐⭐⭐⭐
   │   └── EventHandler.cs
   │
   ├── GameManager/      - Core game state
   │   └── GameManager.cs
   │
   ├── Inventory/        - Inventory system ⭐⭐⭐⭐
   │   ├── InventoryManager.cs
   │   └── InventoryItem.cs
   │
   ├── Item/             - Item interaction
   │   ├── Item.cs
   │   ├── ItemDetails.cs
   │   ├── ItemNudge.cs
   │   └── ObscuringItemFader.cs
   │
   ├── Map/              - Grid system ⭐⭐⭐⭐
   │   ├── GridPropertiesManager.cs
   │   ├── GridPropertyDetails.cs
   │   └── TilemapGridProperties.cs
   │
   ├── Misc/             - Utilities
   │   ├── Settings.cs
   │   ├── SingletonMonobehaviour.cs
   │   └── Tags.cs
   │
   ├── NPC/              - AI system ⭐⭐⭐⭐
   │   ├── NPC.cs
   │   ├── NPCManager.cs
   │   ├── NPCMovement.cs
   │   ├── NPCPath.cs
   │   └── NPCSchedule.cs
   │
   ├── Player/           - Player controller ⭐⭐⭐⭐⭐
   │   ├── Player.cs (1071 lines)
   │   ├── ItemPickUp.cs
   │   └── PlayerAnimationTest.cs
   │
   ├── SaveSystem/       - Save/Load ⭐⭐⭐⭐
   │   ├── SaveLoadManager.cs
   │   ├── ISaveable.cs
   │   ├── GameSave.cs
   │   └── GenerateGUID.cs
   │
   ├── Scene/            - Scene management
   │   ├── SceneControllerManager.cs
   │   └── SceneTeleport.cs
   │
   ├── Sounds/           - Audio system
   │   ├── AudioManager.cs
   │   └── Sound.cs
   │
   ├── TimeSystem/       - Time management
   │   ├── TimeManager.cs
   │   └── GameClock.cs
   │
   ├── UI/               - User interface
   │   ├── UIManager.cs
   │   ├── Cursor.cs
   │   └── GridCursor.cs
   │
   ├── Utilities/        - Helper classes
   │   └── HelperMethods.cs
   │
   └── VFX/              - Visual effects
       ├── VFXManager.cs
       └── PoolManager.cs
```

### 🎮 Unity Assets (Structure only)
```
✅ Assets/Prefabs/        - All .prefab files (~50 files)
✅ Assets/Scenes/         - All .unity scene files (4 scenes)
✅ Assets/Animation/      - Animation controllers & clips
✅ All .meta files        - Unity needs these for references
```

### ⚙️ Project Configuration
```
✅ ProjectSettings/       - Unity project settings
✅ Packages/manifest.json - Package dependencies
```

---

## ❌ KHÔNG PUSH (Loại bỏ để giảm size)

### 🖼️ Large Asset Files (~100 MB)
```
❌ Assets/**/*.png        - Sprite images (~80 MB)
❌ Assets/**/*.jpg        - Textures
❌ Assets/**/*.psd        - Photoshop files
```

### 🔊 Audio Files (~15 MB)
```
❌ Assets/**/*.mp3        - Music
❌ Assets/**/*.wav        - Sound effects
❌ Assets/**/*.ogg        - Compressed audio
```

### 🔤 Font Files (~2 MB)
```
❌ Assets/**/*.ttf        - TrueType fonts
❌ Assets/**/*.otf        - OpenType fonts
❌ Assets/TextMesh Pro/   - TextMeshPro assets
```

### 🗂️ Unity Generated (~700 MB)
```
❌ Library/               - Unity cache (700 MB!)
❌ Temp/                  - Temporary files
❌ Obj/                   - Build artifacts
❌ Build/                 - Compiled game
❌ Logs/                  - Log files
❌ UserSettings/          - User preferences
```

### 💻 IDE Files
```
❌ .vs/                   - Visual Studio cache
❌ .idea/                 - Rider cache
❌ *.csproj               - Auto-generated
❌ *.sln                  - Auto-generated
```

---

## 📊 Kích Thước So Sánh

| Category | Before | After | Saved |
|----------|--------|-------|-------|
| **Code & Scripts** | 2 MB | 2 MB | ✅ Keep |
| **Prefabs & Scenes** | 3 MB | 3 MB | ✅ Keep |
| **Images** | 80 MB | 0 MB | ❌ Remove |
| **Audio** | 15 MB | 0 MB | ❌ Remove |
| **Fonts** | 2 MB | 0 MB | ❌ Remove |
| **Library** | 700 MB | 0 MB | ❌ Ignored |
| **TOTAL** | ~800 MB | **~5 MB** | **99% smaller!** |

---

## 🎯 Tại Sao Làm Như Vậy?

### ✅ Lợi ích cho nhà tuyển dụng:
1. **Clone nhanh**: 5 MB vs 800 MB
2. **Focus vào code**: Không bị phân tâm bởi assets
3. **Dễ browse**: Chỉ cần đọc code trên GitHub
4. **Professional**: Hiểu cách tổ chức portfolio

### ✅ Lợi ích cho bạn:
1. **Bandwidth**: Không tốn băng thông upload 800 MB
2. **GitHub limits**: Tránh vượt quá giới hạn file size
3. **Maintenance**: Dễ update code, không cần sync assets
4. **Privacy**: Không share assets có thể có bản quyền

---

## 💼 Nhà Tuyển Dụng Sẽ Thấy Gì?

### Trên GitHub:
```
farming-rpg-portfolio/
├── 📄 README.md          ← Professional introduction
├── 📄 PORTFOLIO.md       ← Code highlights
├── 📁 Assets/
│   ├── 📁 Scripts/       ← YOUR CODE (80+ files)
│   ├── 📁 Prefabs/       ← Game structure
│   └── 📁 Scenes/        ← Level design
├── 📁 ProjectSettings/   ← Unity config
└── 📁 Packages/          ← Dependencies
```

### Họ có thể:
- ✅ Đọc code trực tiếp trên GitHub
- ✅ Clone về để xem structure
- ✅ Review architecture và design patterns
- ✅ Đánh giá coding style và best practices
- ❌ Không chạy được game (thiếu assets)
  - → Nếu họ muốn chạy, bạn gửi build file riêng

---

## 🚀 Ready to Push?

Chạy lệnh này để setup:
```bash
cd "Farming RPG Course"
git checkout -b portfolio-showcase
git add .gitignore README.md PORTFOLIO.md
git commit -m "Add portfolio documentation"
git remote add origin https://github.com/yourusername/farming-rpg-portfolio.git
git push -u origin portfolio-showcase
```

Sau đó vào GitHub Settings → Branches → Set `portfolio-showcase` làm default branch.

---

**Kết quả**: Một portfolio GitHub chuyên nghiệp, nhẹ, dễ review, tập trung vào CODE! 🎯
