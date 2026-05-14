# DuckMind

**DuckMind** là nền tảng AI agentic giúp chuyển từ việc "nhận câu trả lời" sang **tự động thực thi công việc thực tế**.  
Thay vì chỉ trò chuyện với AI, DuckMind cho phép AI **truy cập dữ liệu, lập kế hoạch và thực hiện các nhiệm vụ nhiều bước**, giúp người dùng giao việc và quay lại khi công việc đã hoàn thành.

DuckMind được thiết kế như một **AI coworker** chạy trên máy của bạn, có thể xử lý các nhiệm vụ phức tạp, tự chia nhỏ công việc và thực hiện tuần tự cho đến khi đạt được kết quả.

---

# Từ câu trả lời đến hành động

DuckMind không chỉ trả lời câu hỏi.  
Nó giúp **thực hiện công việc**.

Bạn chỉ cần mô tả mục tiêu. DuckMind sẽ:

- phân tích nhiệm vụ
- chia thành các bước
- thực thi từng bước
- cập nhật tiến độ
- tạo ra kết quả cuối cùng

Bạn có thể theo dõi quá trình theo thời gian thực hoặc giao việc và quay lại sau.

---

# Cách DuckMind hoạt động

DuckMind sử dụng mô hình **agentic workflow**.

1. Hiểu mục tiêu của người dùng  
2. Phân rã thành các bước nhỏ  
3. Lập kế hoạch thực thi  
4. Truy cập dữ liệu cần thiết  
5. Thực hiện từng bước  
6. Tổng hợp kết quả cuối cùng  

Trong quá trình đó DuckMind có thể:

- đọc file
- phân tích dữ liệu
- viết code
- tạo báo cáo
- tạo slide
- tổng hợp thông tin từ nhiều nguồn

---

# Tự động hóa công việc lặp lại

DuckMind đặc biệt hữu ích với các nhiệm vụ tốn thời gian.

Bạn có thể cấu hình một nhiệm vụ để chạy:

- hàng ngày
- hàng tuần
- hàng tháng

Ví dụ:

- tổng hợp báo cáo mỗi sáng
- phân tích dữ liệu định kỳ
- tổng hợp phản hồi khách hàng
- tạo dashboard hoặc slide tự động

---

# Hướng dẫn cài đặt DuckMind

## 🪟 Windows 11 (WSL + Ubuntu)

DuckMind chạy ổn định nhất trên Linux, vì vậy trên Windows cần cài WSL và Ubuntu trước.

### Bước 1 – Cài WSL và Ubuntu

Mở **PowerShell** hoặc **Windows Terminal** với quyền **Administrator** rồi chạy:

```powershell
wsl --install
```

Lệnh này sẽ tự động:
- Bật Windows Subsystem for Linux
- Bật Virtual Machine Platform
- Cài kernel WSL2
- Cài Ubuntu mới nhất (thường là Ubuntu 24.04 LTS)

Sau khi chạy xong, **khởi động lại máy**.

### Bước 2 - Cài Ubuntu 24.04 từ Microsoft Store
1. Mở **Microsoft Store** (tìm trong Start Menu).
2. Tìm **Ubuntu 24.04**.
3. Chọn **Ubuntu 24.04.1 LTS** rồi bấm **Get** hoặc **Install**.
4. Chờ tải xong (khoảng vài trăm MB).

***

### Bước 3 - Khởi tạo Ubuntu lần đầu

1. Mở **Tabby** (nếu muốn gõ được Tiếng Việt) hoăc mở **Ubuntu 24.04** với quyền **Administrator** từ **Start Menu**.
2. Chờ vài phút để hệ thống giải nén (chỉ xảy ra lần đầu).
3. Nhập **UNIX username**  
   - dùng chữ thường  
   - không dấu  
   - không khoảng trắng
4. Nhập **password**  
   - khi gõ sẽ không hiển thị ký tự, đây là hành vi bình thường.
***

### Bước 4 – Cài toàn bộ môi trường trong Ubuntu

Mở Ubuntu terminal và chạy tuần tự các bước sau:

**Cập nhật hệ thống**
```bash
sudo apt update && sudo apt upgrade -y
```

**Cài các gói hệ thống**
```bash
sudo apt install -y \
  git \
  python3 python3-pip python3-venv \
  build-essential \
  coreutils \
  libreoffice \
  poppler-utils \
  curl
```

**Cài Node.js 22 LTS**
```bash
curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
sudo apt install -y nodejs
```

Kiểm tra:
```bash
node -v
npm -v
```

**Cài các thư viện Python**
```bash
pip3 install --break-system-packages markitdown[all] Pillow openpyxl
```


**Cài đặt Duckmind**
```bash
sudo npm install -g @duckmind/dm docx xlsx pptxgenjs
```

**Kiểm tra cài đặt**
```bash
git --version
python3 --version
node -v && npm -v
dm --version
```

***

## 🐧 Linux Ubuntu

Trên Ubuntu có thể cài trực tiếp mà không cần WSL.

### Bước 1 – Cập nhật hệ thống
```bash
sudo apt update && sudo apt upgrade -y
```

### Bước 2 – Cài các gói hệ thống
```bash
sudo apt install -y \
  git \
  python3 python3-pip python3-venv \
  build-essential \
  coreutils \
  libreoffice \
  poppler-utils \
  curl
```

### Bước 3 – Cài Node.js 22 LTS
```bash
curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
sudo apt install -y nodejs
```

Kiểm tra:
```bash
node -v
npm -v
```

### Bước 4 – Cài Python packages
```bash
pip3 install --break-system-packages markitdown[all] Pillow openpyxl
```

### Bước 5 – Cài DuckMind
```bash
sudo npm install -g @duckmind/dm docx xlsx pptxgenjs
```

### Bước 6 – Kiểm tra hoàn tất
```bash
git --version
python3 --version
node -v && npm -v
duckmind --version
```

***

## 🍎 macOS

### Bước 1 – Cài Homebrew

Nếu chưa có Homebrew:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Nếu dùng **Apple Silicon (M1/M2/M3/M4)**, thêm PATH sau khi cài:
```bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

***

### Bước 2 – Cài Git, Python và Node.js
```bash
brew update
brew install git python node
```

***

### Bước 3 – Cài Xcode Command Line Tools
```bash
xcode-select --install
```

> Một cửa sổ cài đặt sẽ hiện ra, bấm **Install** và chờ hoàn tất.

***

### Bước 4 – Cài các công cụ hệ thống
```bash
brew install poppler coreutils
brew install --cask libreoffice
```

***

### Bước 5 – Cài Python packages
```bash
pip3 install markitdown[all] Pillow openpyxl
```

***

### Bước 6 – Cài đặt DuckMind
```bash
npm install -g @duckmind/dm docx xlsx pptxgenjs
```

***

### Bước 7 – Kiểm tra hoàn tất
```bash
git --version
python3 --version
node -v && npm -v
duckmind --version
```

# Bắt đầu sử dụng DuckMind CLI

Sau khi cài đặt, mở terminal và chạy:
```bash
dm
```
CLI sẽ khởi động vào chế độ tương tác.

---

### Kết nối Model

Trong CLI, gõ:
```bash
/login
```
Chọn **provider** DuckMind từ danh sách hiển thị

### Nhập API Key

Sau khi chọn provider, CLI sẽ yêu cầu:
```bash
Enter API key: sk-xxxx
```
Dán API key của bạn và nhấn Enter.


### Chọn Model

DuckMind có 4 chế độ:
Free
Lite
Smart
Deep

- **Lite**: nhanh,tiết kiệm tokens.
- **Smart**: nhanh, thông minh, phù hợp cho hầu hết tác vụ  
- **Deep**: suy luận sâu, dùng cho nhiệm vụ phức tạp

**Khuyến nghị:**

Ưu tiên chọn Smart. Chỉ dùng Deep khi cần reasoning sâu.
