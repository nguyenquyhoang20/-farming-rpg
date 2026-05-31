# 🌿 Repository Branches Guide

Repo này có **2 branches chính** với mục đích khác nhau:

---

## 📋 **Branch Overview**

| Branch | Mục đích | Size | Nội dung |
|--------|----------|------|----------|
| **main** | Full project | ~800 MB | Code + Assets đầy đủ |
| **portfolio-showcase** | Portfolio cho nhà tuyển dụng | ~5 MB | Chỉ code |

---

## 🎮 **Branch: `main`** (Full Project)

### Mục đích:
- Lưu trữ **toàn bộ project** với đầy đủ assets
- Dùng để phát triển và chạy game
- Backup đầy đủ

### Nội dung:
✅ Tất cả C# scripts  
✅ Tất cả sprites/images  
✅ Tất cả audio files  
✅ Tất cả fonts  
✅ Prefabs, Scenes, Animations  
✅ ProjectSettings  

### Khi nào dùng:
- Clone về để chạy game trong Unity
- Tiếp tục phát triển project
- Backup đầy đủ

### Clone:
```bash
git clone -b main https://github.com/nguyenquyhoang20/-farming-rpg.git
```

---

## 💼 **Branch: `portfolio-showcase`** (Code Only)

### Mục đích:
- **Showcase code** cho nhà tuyển dụng
- Tập trung vào **kỹ năng lập trình**
- Repository nhẹ, dễ review

### Nội dung:
✅ Tất cả C# scripts (~80 files, ~15,000 lines)  
✅ Prefabs (structure only)  
✅ Scenes (structure only)  
✅ ScriptableObjects  
✅ Professional documentation  
❌ **KHÔNG có** sprites/images  
❌ **KHÔNG có** audio files  
❌ **KHÔNG có** fonts  

### Khi nào dùng:
- Share với nhà tuyển dụng
- Code review
- Portfolio showcase
- **KHÔNG thể chạy game** (thiếu assets)

### Clone:
```bash
git clone https://github.com/nguyenquyhoang20/-farming-rpg.git
# Default branch là portfolio-showcase
```

---

## 🎯 **Khuyến Nghị Sử Dụng**

### Cho Nhà Tuyển Dụng:
👉 **Dùng branch `portfolio-showcase`**
- Nhẹ, clone nhanh
- Tập trung vào code
- Có documentation đầy đủ

### Cho Bản Thân/Team:
👉 **Dùng branch `main`**
- Đầy đủ assets
- Có thể chạy game
- Tiếp tục phát triển

---

## 📊 **So Sánh Chi Tiết**

### Size:
```
main:               ~800 MB (full)
portfolio-showcase: ~5 MB (99% nhẹ hơn!)
```

### Clone Time (ước tính):
```
main:               ~5-10 phút (tùy mạng)
portfolio-showcase: ~30 giây
```

### Use Cases:
```
main:               Development, Testing, Playing
portfolio-showcase: Code Review, Portfolio, Showcase
```

---

## 🔄 **Switching Between Branches**

### Chuyển sang main (full project):
```bash
git checkout main
```

### Chuyển sang portfolio-showcase (code only):
```bash
git checkout portfolio-showcase
```

---

## 💡 **Tips**

### Khi share với nhà tuyển dụng:
```
GitHub: https://github.com/nguyenquyhoang20/-farming-rpg
Branch: portfolio-showcase (default)

📝 Note: Repository contains code and architecture only.
Full playable build available upon request.
```

### Khi làm việc:
- Develop trên branch `main`
- Merge code changes sang `portfolio-showcase` khi cần update portfolio
- **KHÔNG** merge assets sang `portfolio-showcase`

---

## ⚠️ **Lưu Ý**

1. **Branch `portfolio-showcase` KHÔNG thể chạy game** vì thiếu assets
2. Nếu nhà tuyển dụng muốn chạy game, gửi:
   - Build file (.exe)
   - Hoặc hướng dẫn clone branch `main`
3. Luôn giữ branch `portfolio-showcase` clean và professional

---

## 🚀 **Current Status**

✅ Branch `main` - Pushed (full project)  
✅ Branch `portfolio-showcase` - Pushed (code only)  
✅ Default branch on GitHub: `portfolio-showcase`  
✅ Ready for recruiter review!

---

**Last Updated**: 2026-05-31
