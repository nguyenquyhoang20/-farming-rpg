# ⚡ Quick Start - Push Portfolio Lên GitHub

## 🎯 Mục tiêu
Push **CHỈ CODE** lên GitHub cho nhà tuyển dụng xem (loại bỏ hình ảnh, âm thanh)

## 🚀 Cách 1: Tự động (Khuyến nghị)

### Chạy script PowerShell:
```powershell
cd "Farming RPG Course"
.\setup-portfolio.ps1
```

Script sẽ tự động:
- ✅ Tạo branch `portfolio-showcase`
- ✅ Loại bỏ assets lớn khỏi git
- ✅ Thêm documentation
- ✅ Tạo commit

Sau đó làm theo hướng dẫn trên màn hình để push lên GitHub.

---

## 🔧 Cách 2: Thủ công

### Bước 1: Tạo branch mới
```bash
git checkout -b portfolio-showcase
```

### Bước 2: Xóa assets lớn khỏi git (không xóa file thật)
```bash
git rm --cached -r Assets/**/*.png
git rm --cached -r Assets/**/*.jpg
git rm --cached -r Assets/**/*.mp3
git rm --cached -r Assets/**/*.wav
git rm --cached -r Assets/**/*.ttf
```

### Bước 3: Add documentation
```bash
git add .gitignore README.md PORTFOLIO.md
```

### Bước 4: Commit
```bash
git commit -m "Portfolio: Code showcase - removed large assets"
```

### Bước 5: Push lên GitHub
```bash
# Tạo repo trên GitHub trước: https://github.com/new
git remote add origin https://github.com/YOUR_USERNAME/farming-rpg-portfolio.git
git push -u origin portfolio-showcase
```

### Bước 6: Set default branch
- Vào GitHub repo → **Settings** → **Branches**
- Đổi default branch thành `portfolio-showcase`

---

## 📋 Checklist

- [ ] Đã chạy script hoặc làm thủ công
- [ ] Đã tạo repo trên GitHub
- [ ] Đã push branch `portfolio-showcase`
- [ ] Đã set làm default branch
- [ ] Đã kiểm tra README.md hiển thị đẹp
- [ ] Đã update CV/LinkedIn với link GitHub

---

## 💼 Link để share với nhà tuyển dụng

```
GitHub: https://github.com/YOUR_USERNAME/farming-rpg-portfolio
Branch: portfolio-showcase (default)

📝 Note: Repository contains code and architecture only.
Full playable build available upon request.
```

---

## ❓ FAQ

**Q: Tại sao không push hết?**
A: Để giảm size từ 800MB → 5MB, nhà tuyển dụng chỉ cần xem code.

**Q: Họ có chạy được game không?**
A: Không (thiếu assets), nhưng họ có thể đọc code. Nếu họ muốn chạy, bạn gửi build file riêng.

**Q: Branch master có bị ảnh hưởng không?**
A: Không, branch master vẫn giữ nguyên đầy đủ assets.

**Q: Có thể update code sau không?**
A: Có, chỉ cần checkout branch `portfolio-showcase` và commit như bình thường.

---

## 🎉 Done!

Sau khi setup xong, bạn có một portfolio GitHub chuyên nghiệp:
- ✅ Nhẹ (5 MB)
- ✅ Dễ review
- ✅ Tập trung vào code
- ✅ Professional presentation

Good luck với việc tìm việc! 🚀
