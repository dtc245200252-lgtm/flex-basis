# CSS `flex-basis` Property - Hướng Dẫn & Thực Hành

Dự án thực hành chuyên sâu về thuộc tính **`flex-basis`** trong CSS Flexbox, bao gồm lý thuyết cú pháp, các giá trị thường dùng, và 4 ví dụ trực quan sinh động.

---

## 1. Khái Niệm `flex-basis`

- **`flex-basis`** xác định kích thước cơ sở ban đầu của một **Flex Item** dọc theo **trục chính (Main Axis)** trước khi không gian còn trống được phân chia (`flex-grow`) hoặc co lại (`flex-shrink`).
- Thuộc tính này chỉ áp dụng trực tiếp lên **Flex Item** (con trực tiếp của Flex Container).

### Cú pháp
```css
flex-basis: <length> | auto | initial | inherit;
```

---

## 2. Các Giá Trị Thường Dùng

| Giá trị | Ý nghĩa & Mô tả |
| :--- | :--- |
| **`px, %, em, rem...`** | Kích thước cơ sở cố định hoặc tương đối theo trục chính. |
| **`auto`** *(mặc định)* | Lấy theo `width`/`height` của Item hoặc tính theo nội dung bên trong. |
| **`initial`** | Khôi phục về giá trị mặc định (`auto`). |
| **`inherit`** | Kế thừa giá trị từ phần tử cha. |

---

## 3. Các Ví Dụ Thực Hành

### 🔹 Ví Dụ 1: `flex-basis` với đơn vị px (Trục ngang - Row)
- Container mặc định `flex-direction: row`.
- `flex-basis` thiết lập chiều rộng khởi điểm cho từng phần tử:
  - Item 1: `flex-basis: 200px;`
  - Item 2: `flex-basis: 100px;`
  - Item 3: `flex-basis: 150px;`

### 🔹 Ví Dụ 2: `flex-basis` thay đổi theo `flex-direction: column` (Trục dọc)
- Khi `flex-direction: column`, **Main Axis chuyển thành chiều dọc**.
- Do đó, `flex-basis: 100px` sẽ thiết lập **chiều cao (height)** ban đầu của mỗi Item trong Container có `height: 500px`.

### 🔹 Ví Dụ 3: `flex-basis` với phần trăm (%)
- Đặt `flex-basis: 50%` cho 2 Items giúp chia đôi không gian Flex Container thành 2 cột đều nhau.

### 🔹 Ví Dụ 4: Kết hợp `flex-basis` với `flex-grow`
- Cả 3 Items xuất phát với kích thước cơ sở `flex-basis: 100px`.
- Phần không gian thừa trong Container rộng `600px` được chia theo tỷ lệ `flex-grow`:
  - Item 1: `flex-grow: 1`
  - Item 2: `flex-grow: 2` (Nhận phần không gian dư gấp đôi Item 1 & 3)
  - Item 3: `flex-grow: 1`

---

## 4. Ghi Nhớ Quan Trọng

> 💡 **Quy tắc 1:** `flex-basis` phụ thuộc trực tiếp vào `flex-direction`:
> - `flex-direction: row` ➜ Main axis = Chiều ngang ➜ `flex-basis` = Width
> - `flex-direction: column` ➜ Main axis = Chiều dọc ➜ `flex-basis` = Height

> 💡 **Quy tắc 2:** `flex-basis` là kích thước xuất phát điểm ban đầu trước khi tính toán `flex-grow` (nở ra) và `flex-shrink` (co lại).

---

## 5. Cấu Trúc Thư Mục
```
flex-basis Property/
├── index.html        # Giao diện demo trực quan sinh động
├── style.css         # Styling hiện đại, bố cục chuẩn Flexbox
└── README.md         # Tài liệu hướng dẫn và lý thuyết
```
