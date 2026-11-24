# 🧪 LocketGold-DinhTuan — BETA

> Phiên bản thử nghiệm. **Chưa merge vào `main`.**  
> Chỉ dùng để test tính năng mới trước khi đưa vào src chính.

---

## ⚠️ Lưu ý quan trọng

| | Beta (`beta/`) | Src chính (`main/`) |
|---|---|---|
| Mục đích | Thử nghiệm, demo | Production |
| Script path | `/beta/js/...` | `/main/js/...` |
| Conf file | `LocketGold-DinhTuan-Beta.conf` | `LocketGold-DinhTuan.conf` |
| Trạng thái | 🧪 Đang test | ✅ Ổn định |

---

## 🆕 Tính năng đang test trong Beta này

- ✅ **AI Filter** — Bật đầy đủ `ai_filters`, `ai_camera_filters`
- ✅ **PTB (Photo-To-Brush)** — Biến ảnh thành tranh vẽ AI
- ✅ **generateFilteredImage** — Endpoint AI filter không còn bị bypass
- ✅ Toàn bộ flag unlock: `can_use_ai_filter`, `ptb_enabled`, `can_generate_filtered_image`...

---

## 📋 Workflow Beta → Main

```
1. Test kỹ trên beta/
2. Nếu OK → copy file từ beta/js/ sang js/ (src chính)
3. Cập nhật LocketGold-DinhTuan.conf (đổi script-path về /main/)
4. Commit & push lên nhánh main
5. Xóa hoặc giữ beta/ làm staging tiếp theo
```

---

## 📂 Cấu trúc thư mục

```
j/
├── js/                          ← SRC CHÍNH (đừng sửa khi chưa test)
│   ├── locketfix.js
│   ├── locket_filter_resp.js
│   ├── revenuecat.js
│   ├── locket_change_profile.js
│   ├── deleteHeader_RC.js
│   └── deleteHeader_Firebase.js
├── LocketGold-DinhTuan.conf     ← Conf chính (trỏ về /main/)
│
├── beta/                        ← THỬ NGHIỆM (sửa thoải mái ở đây)
│   ├── js/                      ← Bản copy để test
│   ├── worker/
│   ├── LocketGold-DinhTuan-Beta.conf  ← Conf beta (trỏ về /beta/)
│   └── README-BETA.md
│
└── worker/                      ← Cloudflare Worker
```

---

*Maintained by dtuandzxyz*
