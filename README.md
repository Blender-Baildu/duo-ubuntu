
<h1 align="center">🚀 GitHub Actions: SSH + Tailscale Auto Setup</h1>

<p align="center">
  <img src="https://img.shields.io/github/license/Blender-Baildu/duo-ubuntu?style=flat-square" alt="License">
  <img src="https://img.shields.io/badge/Tailscale-Enabled-blue?logo=tailscale&style=flat-square">
  <img src="https://img.shields.io/badge/SSH-Server-green?logo=openssh&style=flat-square">
</p>

---

## 🌐 Mô tả

Workflow này giúp bạn:

- 🖥️ Tự động cài đặt **OpenSSH Server** để kết nối từ xa.
- 🔐 Kết nối an toàn bằng **Tailscale VPN** (qua AuthKey).
- 👨‍💻 Tạo user `admin` có quyền `sudo` và mật khẩu tùy chỉnh.
- ♾️ Giữ runner GitHub Actions **luôn hoạt động** để bạn kết nối thủ công khi cần.

> ✅ **Dành cho mục đích học tập, thử nghiệm CI/CD hoặc kết nối an toàn tạm thời.**

---

## 🛠️ Cách sử dụng

### 1. 🌱 Fork hoặc Clone repo này

```bash
git clone https://github.com/Blender-Baildu/duo-ubuntu.git
```

### 2. 🔑 Thêm `Tailscale AuthKey` vào GitHub Secrets

1. Truy cập [https://login.tailscale.com/admin/settings/authkeys](https://login.tailscale.com/admin/settings/authkeys)
2. Tạo một AuthKey (chọn `Reusable`, `Ephemeral`)
3. Vào GitHub repo → **Settings** → **Secrets** → **New repository secret**
4. Đặt tên: `TAILSCALE_AUTHKEY`

### 3. ▶️ Chạy workflow thủ công

- Vào tab **Actions** → Chọn workflow **"Setup VM and SSH"**
- Click **"Run workflow"** → đợi khoảng 1-2 phút

---

## 🧪 Kết nối

Sau khi workflow hoàn tất:

- ✅ Runner đã kết nối vào Tailscale
- 🔍 Vào Tailscale Admin để thấy IP (VD: `100.x.x.x`)
- 🛜 SSH từ terminal:

```bash
ssh admin@100.x.x.x
# Mật khẩu: 123456Hi (mặc định hoặc bạn thay trong YAML)
```

---

## 📄 Cấu trúc file chính

```yaml
.github/workflows/ssh-tailscale.yml   # File GitHub Actions chính
LICENSE                               # MIT License
README.md                             # Tài liệu sử dụng này
```

---

## 📌 Điều khoản & Trách nhiệm

> ❗ **Vui lòng đọc kỹ trước khi sử dụng!**

- 🧠 Repo này chỉ phục vụ mục đích học tập, nghiên cứu hoặc CI/CD cá nhân.
- ❌ Tuyệt đối **KHÔNG** sử dụng để đào coin, tấn công, lưu trữ dữ liệu bất hợp pháp, hay chạy dịch vụ trái phép.
- ☠️ Mọi hành vi vi phạm **Điều khoản dịch vụ của GitHub** sẽ dẫn đến:
  - Bị xóa repository
  - Khoá tài khoản GitHub
  - Truy cứu trách nhiệm nếu gây thiệt hại
- 📜 Bằng việc sử dụng repo này, bạn **đồng ý hoàn toàn với các điều khoản** trên.

---

## ✅ Tôi đồng ý sử dụng hợp pháp

✔️ Tôi đã đọc và hiểu điều khoản.  
✔️ Tôi đồng ý sử dụng repository này cho mục đích học tập/hợp pháp.  
✔️ Tôi chịu hoàn toàn trách nhiệm nếu sử dụng sai mục đích.

---

## 📜 Giấy phép

Phát hành dưới giấy phép [MIT](./LICENSE).

> Feel free to fork, star ⭐ and improve this project!

---

## 💬 Liên hệ & Góp ý

Nếu bạn thấy hữu ích, hãy ⭐ repo này!  
Đóng góp, báo lỗi, hoặc tạo PR nếu bạn có ý tưởng hay 👇

📧 Email: baildu204@gmail.com
🌐 Tác giả: [Blender-Baildu](https://github.com/Blender-Baildu)
