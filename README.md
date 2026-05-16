# MediCare+ — Ứng dụng Đặt lịch Khám bệnh

MediCare+ là một ứng dụng di động được xây dựng bằng React Native (Expo), mô phỏng hệ thống đặt lịch khám bệnh tại phòng khám. Ứng dụng giúp bệnh nhân dễ dàng tìm kiếm bác sĩ, đặt lịch khám, quản lý lịch hẹn và theo dõi hồ sơ y tế cá nhân một cách tiện lợi và nhanh chóng.

Hệ thống được thiết kế nhằm tối ưu trải nghiệm người dùng với giao diện thân thiện, dễ sử dụng và luồng thao tác rõ ràng. Người dùng có thể đăng ký tài khoản bằng số CCCD, đăng nhập để truy cập hệ thống, lựa chọn bác sĩ theo chuyên khoa, đặt lịch khám theo khung giờ và theo dõi lịch sử khám bệnh.

Ngoài ra, MediCare+ còn hỗ trợ quản lý hồ sơ bệnh án điện tử, thông báo trạng thái lịch hẹn (đặt lịch, hủy lịch, thay đổi lịch) và cung cấp các tính năng bảo mật như mã PIN bảo vệ hồ sơ cá nhân.

Ứng dụng hoạt động hoàn toàn offline bằng AsyncStorage, không cần backend, phù hợp cho mục đích học tập và mô phỏng hệ thống thực tế.

---
## Danh sách thành viên

| Họ tên | MSSV | Phân  |
|--------|------|--------|
| Nguyễn Thị Hồng Nhung | 23810340032 | Auth + Home + Navigation |
| Nguyễn Thị Diễm Quỳnh | 23810310350 | Doctor + Appointment |
| Nguyễn Thị Khánh Linh | 23810310394 | Records + Profile + Notification |

### Phân công nhiệm vụ
#### Nguyễn Thị Hồng Nhung — Auth, Home & Navigation: Chịu trách nhiệm toàn bộ luồng khởi tạo và điều hướng của ứng dụng:

- Xây dựng hệ thống đăng nhập / đăng ký / quên mật khẩu
- Quản lý luồng navigation toàn app
- Phát triển màn hình Home
- Quản lý trạng thái người dùng qua AppContext
- Tối ưu UI, text, button và luồng chuyển màn
#### Nguyễn Thị Diễm Quỳnh — Doctor & Appointment: Phụ trách toàn bộ chức năng liên quan đến bác sĩ và đặt lịch:

- Danh sách 50 bác sĩ theo chuyên khoa
- Màn hình chi tiết bác sĩ
- Chức năng đặt lịch khám
- Quản lý lịch hẹn (sắp tới / đã khám / đã hủy)
- Xử lý logic chống trùng lịch
- Cập nhật dữ liệu bác sĩ và khung giờ khám
#### Nguyễn Thị Khánh Linh — Records, Profile & Notifications: Phụ trách hệ thống hồ sơ và cá nhân người dùng:

- Hồ sơ bệnh án (Medical Records)
- Chi tiết hồ sơ khám bệnh
- Trang cá nhân (Profile)
- Cài đặt tài khoản (đổi mật khẩu, PIN bảo mật)
- Hệ thống thông báo (Notifications)
- Tối ưu UI và theme toàn app

---

## Công nghệ sử dụng

| Thư viện | Mục đích |
|----------|----------|
| React Native + Expo SDK 54 | Framework chính |
| @react-navigation/native-stack | Điều hướng stack |
| @react-navigation/bottom-tabs | Tab bar |
| react-native-safe-area-context | Hỗ trợ notch / Dynamic Island |
| @react-native-async-storage/async-storage | Lưu trữ dữ liệu local |
| @expo/vector-icons (Ionicons) | Bộ icon |

---

## Cài đặt & Chạy

```bash
cd MediCare
npm install
npx expo start --clear
```

Quét mã QR bằng **Expo Go** trên điện thoại (cùng mạng WiFi).

---

## Tài khoản demo

| Số CCCD | Mật khẩu | Tên |
|---------|----------|-----|
| `079190012345` | `123456` | Nguyễn Văn An |

> Hoặc tạo tài khoản mới qua màn hình **Đăng ký**.

---
## Hình ảnh minh họa hệ thống
## 🖼️ Giao diện hệ thống

### 🔐 Trang đăng nhập
<p align="center">
  <img src="./assets/login.png" width="300"/>
</p>

### 🔑 Trang quên mật khẩu
<p align="center">
  <img src="./assets/forgot_password.png" width="300"/>
</p>

### 📝 Trang đăng ký
<p align="center">
  <img src="./assets/register.png" width="300"/>
</p>

### 🏠 Trang chủ
<p align="center">
  <img src="./assets/home.png" width="300"/>
</p>

### 🏥 Trang thông tin phòng khám
<p align="center">
  <img src="./assets/clinic_info.png" width="300"/>
  <img src="./assets/clinic_info(2).png" width="300"/>
</p>

### 🔍 Trang tìm kiếm bác sĩ
<p align="center">
  <img src="./assets/search.png" width="300"/>
</p>

### 🩺 Trang danh sách chuyên khoa
<p align="center">
  <img src="./assets/specialty_list.png" width="300"/>
</p>

### 👨‍⚕️ Trang danh sách bác sĩ
<p align="center">
  <img src="./assets/doctor_list.png" width="300"/>
</p>

### 📄 Trang chi tiết bác sĩ
<p align="center">
  <img src="./assets/doctor_detail.png" width="300"/>
  <img src="./assets/doctor_detail(2).png" width="300"/>
  <img src="./assets/doctor_detail(3).png" width="300"/>
</p>

### 📅 Trang đặt lịch khám
<p align="center">
  <img src="./assets/book_appointment.png" width="300"/>
</p>

### ✅ Trang xác nhận đặt lịch
<p align="center">
  <img src="./assets/appointment_confirm.png" width="300"/>
  <img src="./assets/appointment_confirm(2).png" width="300"/>
  <img src="./assets/appointment_confirm(3).png" width="300"/>
</p>

### 🎉 Trang đặt lịch thành công
<p align="center">
  <img src="./assets/booking_success.png" width="300"/>
</p>

### ⏰ Trang lịch hẹn sắp tới
<p align="center">
  <img src="./assets/upcoming_appointment.png" width="300"/>
</p>

### 🔄 Trang đổi lịch khám
<p align="center">
  <img src="./assets/resvhedule_appointment.png" width="300"/>
</p>

### 📋 Trang chi tiết lịch khám
<p align="center">
  <img src="./assets/appointment_detail.png" width="300"/>
  <img src="./assets/appointment_detail(2).png" width="300"/>
</p>

### ✔️ Trang lịch đã khám
<p align="center">
  <img src="./assets/completed_appointment.png" width="300"/>
</p>

### 🧪 Trang kết quả khám bệnh
<p align="center">
  <img src="./assets/medical_result.png" width="300"/>
  <img src="./assets/medical_result(2).png" width="300"/>
</p>

### ⭐ Trang đánh giá bác sĩ
<p align="center">
  <img src="./assets/review_doctor.png" width="300"/>
</p>

### ❌ Trang lịch hẹn đã hủy
<p align="center">
  <img src="./assets/cancelked_appointment.png" width="300"/>
</p>

### 🔐 Trang nhập mã PIN
<p align="center">
  <img src="./assets/verify_pin.png" width="300"/>
</p>

### 📂 Trang hồ sơ bệnh án
<p align="center">
  <img src="./assets/medical_records.png" width="300"/>
</p>

### 📑 Trang chi tiết hồ sơ khám
<p align="center">
  <img src="./assets/record_detail.png" width="300"/>
  <img src="./assets/record_detail(2).png" width="300"/>
</p>

### 👤 Trang cá nhân
<p align="center">
  <img src="./assets/profile.png" width="300"/>
  <img src="./assets/profile(2).png" width="300"/>
</p>

### ✏️ Trang chỉnh sửa hồ sơ
<p align="center">
  <img src="./assets/edit_profile.png" width="300"/>
</p>

### 🔔 Trang thông báo
<p align="center">
  <img src="./assets/notification.png" width="300"/>
</p>

### ⚙️ Trang cài đặt
<p align="center">
  <img src="./assets/settings.png" width="300"/>
  <img src="./assets/settings(2).png" width="300"/>
</p>

### 🔒 Trang đổi mật khẩu
<p align="center">
  <img src="./assets/change_password.png" width="300"/>
</p>


---

## Link figma
https://www.figma.com/design/IZ7ZaRCq5f2WdoZNEVrZmS/mobile?node-id=0-1&t=fmizL3upS3SXnUy0-1

---

## Video demo
(https://drive.google.com/file/d/1F7HWDjo_FI5qENQaw1tFp-MQV5WBsOhI/view?usp=drive_link)

---

## Dữ liệu mẫu

Lần chạy đầu tiên app tự nạp (chỉ tài khoản demo):

- **2 lịch hẹn sắp tới** — BS. Nguyễn Thị Hương (Tim mạch), BS. Phạm Văn Đức (Nội tổng quát)
- **1 lịch đã khám** — BS. Lê Thị Mai (Da liễu) kèm hồ sơ y tế mẫu
- **1 lịch đã hủy** — BS. Trần Văn Minh (Nhi khoa)
- **Thông báo trống** — chỉ xuất hiện khi người dùng đặt / hủy / đổi lịch

---

## Danh sách bác sĩ (50 bác sĩ)

| Chuyên khoa | Số bác sĩ | Tầng | Phòng | Khung giờ |
|---|:---:|:---:|---|---|
| Tim mạch | 6 | 2 | 201–206 | 08:00 · 09:00 · 10:00 · 11:00 · 14:00 · 15:00 · 16:00 |
| Nhi khoa | 6 | 3 | 301–306 | 08:00 · 08:45 · 09:30 · 10:15 · 11:00 · 14:00 · 14:45 · 15:30 |
| Nội tổng quát | 7 | 1 | 101–107 | 08:00 · 08:30 · 09:00 · 09:30 · 10:00 · 10:30 · 11:00 · 14:00 · 14:30 · 15:00 · 15:30 · 16:00 |
| Da liễu | 6 | 4 | 401–406 | 08:00 · 08:30 · 09:00 · 09:30 · 10:00 · 10:30 · 11:00 · 14:00 · 14:30 · 15:00 · 15:30 · 16:00 |
| Thần kinh | 6 | 5 | 501–506 | 08:00 · 09:00 · 10:00 · 11:00 · 14:00 · 15:00 · 16:00 |
| Xương khớp | 6 | 6 | 601–606 | 08:00 · 08:45 · 09:30 · 10:15 · 11:00 · 14:00 · 14:45 · 15:30 |
| Mắt | 6 | 7 | 701–706 | 08:00 · 08:30 · 09:00 · 09:30 · 10:00 · 10:30 · 11:00 · 14:00 · 14:30 · 15:00 · 15:30 · 16:00 |
| Tai Mũi Họng | 7 | 8 | 801–807 | 08:00 · 08:45 · 09:30 · 10:15 · 11:00 · 14:00 · 14:45 · 15:30 |
| **Tổng** | **50** | | | |

> Chủ nhật: tất cả bác sĩ nghỉ.

---

## Chức năng

### Xác thực
- **Đăng nhập** — số CCCD 12 chữ số + mật khẩu; 1 CCCD = 1 sổ bệnh án cá nhân
- **Đăng ký** — họ tên + CCCD 12 số + mật khẩu ≥ 6 ký tự; kiểm tra trùng CCCD; số điện thoại bổ sung trong hồ sơ
- **Quên mật khẩu** — nhập CCCD đã đăng ký → đặt mật khẩu mới ngay trên app
- **Đổi mật khẩu** — trong Cài đặt → nhập mật khẩu cũ + mới + xác nhận
- **Mã PIN hồ sơ** — đặt PIN 6 số trong Cài đặt → Bảo mật; hiển thị màn hình khóa mỗi lần vào tab Hồ sơ; giới hạn 5 lần sai
- Phiên đăng nhập lưu qua AsyncStorage, không mất khi tắt app
- Thông tin hồ sơ (SĐT, ngày sinh...) giữ nguyên sau khi đăng xuất và đăng nhập lại
- Dữ liệu (lịch hẹn, hồ sơ, thông báo) tách biệt theo từng tài khoản

### Trang chủ
- Lời chào theo buổi (sáng / chiều / tối) kèm tên người dùng
- Thanh tìm kiếm nhanh → màn hình tìm bác sĩ
- **Banner nhắc bổ sung số điện thoại** nếu chưa điền — bấm vào chuyển thẳng sang Chỉnh sửa hồ sơ
- Banner thông tin phòng khám MediCare+ Clinic
- 8 chuyên khoa (cuộn ngang) → lọc bác sĩ theo chuyên khoa
- Tối đa 2 lịch hẹn sắp tới hiển thị nhanh
- Danh sách bác sĩ nổi bật (cuộn ngang) với nút Đặt lịch nhanh
- Badge số thông báo chưa đọc

### Tìm & Xem bác sĩ
- Danh sách 50 bác sĩ với tìm kiếm realtime theo tên hoặc chuyên khoa
- **Lọc/Sắp xếp** qua icon button → modal: Mặc định · Rating cao nhất · Kinh nghiệm nhiều nhất · Phí thấp nhất · Phí cao nhất
- Indicator hiển thị bộ lọc đang áp dụng, bấm X để xóa nhanh
- **Trang chi tiết bác sĩ** bao gồm:
  - Ảnh đại diện, chuyên khoa, số bệnh nhân, rating, số phòng khám
  - Giới thiệu
  - Thông tin chuyên môn: năm sinh, học vị, bằng cấp, chứng chỉ hành nghề
  - Kinh nghiệm làm việc: các bệnh viện đã công tác kèm thời gian
  - Thành tích & Giải thưởng
  - Phí khám
  - Lịch làm việc theo tuần (khung giờ theo chuyên khoa)
  - Đánh giá từ bệnh nhân (pool 20 review thực tế, mỗi bác sĩ hiện bộ khác nhau)

### Đặt lịch khám
1. **Chọn ngày** — 14 ngày tới; Chủ nhật hiển thị "Nghỉ" và không thể chọn
2. **Chọn giờ** — khung giờ theo chuyên khoa (30 phút / 45 phút / 1 tiếng); giờ đã qua bị ẩn; **"Đầy"** nếu bác sĩ đã có người đặt; **"Trùng"** nếu bạn đã có lịch khác cùng giờ đó
3. **Ghi chú triệu chứng** (tùy chọn)
4. **Xác nhận** — xem lại thông tin bác sĩ, ngày giờ, phí khám, thông tin bệnh nhân (CCCD)
5. **Quy trình khám 4 bước** với số phòng và người phụ trách cụ thể
6. **Nhắc mang CCCD bản gốc hoặc VNeID** khi đến phòng khám
7. **Màn hình thành công** — animation, nút "Xem lịch hẹn" chuyển thẳng về tab Lịch hẹn

### Quản lý lịch hẹn
3 tab: **Sắp tới · Đã khám · Đã hủy**

| Thao tác | Áp dụng cho | Kết quả |
|----------|-------------|---------|
| Đổi lịch | Sắp tới | Chọn ngày/giờ mới — chi tiết cập nhật tức thì khi quay lại |
| Hủy lịch | Sắp tới | Chuyển sang Đã hủy, gửi thông báo |
| Xác nhận đã khám | Sắp tới | Chuyển sang Đã khám → tự động mở trang đánh giá |
| Đánh giá bác sĩ | Đã khám | 1–5 sao + nhận xét |
| Xem hồ sơ khám | Đã khám | Mở hồ sơ y tế liên kết |

**Chi tiết lịch hẹn sắp tới** hiển thị thêm:
- Mã lịch hẹn (VD: MC202404190042) và số thứ tự (VD: A012)
- Quy trình khám 4 bước với tầng, phòng, người phụ trách từng bước
- Nhắc mang CCCD bản gốc hoặc VNeID

> Lịch hẹn sắp tới đã qua ngày sẽ tự động bị xóa khi mở app.

### Hồ sơ khám bệnh
- Được bảo vệ bằng mã PIN (nếu đã bật) — hiển thị màn hình khóa, bấm để nhập PIN
- Banner gợi ý đặt PIN nếu chưa bật bảo mật
- Danh sách tất cả lần khám đã hoàn thành
- Chi tiết từng hồ sơ: bác sĩ, chuyên khoa, ngày khám, chẩn đoán, đơn thuốc, ghi chú
- Hồ sơ tự động tạo sau khi xác nhận đã khám

### Thông báo
- Tự động tạo khi đặt lịch (xanh lá), hủy lịch (đỏ), đổi lịch (xanh dương)
- Đánh dấu đã đọc từng thông báo hoặc tất cả cùng lúc
- Badge số chưa đọc trên tab Cá nhân

### Hồ sơ cá nhân & Cài đặt
- Chỉnh sửa: họ tên, SĐT, ngày sinh (DD-MM-YYYY, có validation), giới tính, nhóm máu
- Số CCCD hiển thị read-only (dùng để đăng nhập, không thể đổi)
- Bật/tắt thông báo Push và Email
- **Đổi mật khẩu** — xác minh mật khẩu cũ trước khi đổi
- **Bảo mật** — đặt / tắt mã PIN bảo vệ hồ sơ khám bệnh
- Xem thống kê: số lịch hẹn, hồ sơ bệnh, đánh giá đã gửi

---

## Quy trình khám tại MediCare+ Clinic

| Bước | Địa điểm | Người phụ trách | Nội dung |
|:---:|---|---|---|
| 1 | Tầng 1 — Quầy lễ tân | Nhân viên lễ tân | Xuất trình CCCD bản gốc hoặc VNeID + mã lịch hẹn, nhận số thứ tự |
| 2 | Tầng X — Khu vực chờ | Điều dưỡng | Ngồi chờ, theo dõi bảng điện tử gọi số |
| 3 | Tầng X — Phòng khám | Bác sĩ chuyên khoa | Vào phòng khi được gọi, mang CCCD để bác sĩ đối chiếu |
| 4 | Tầng 1 — Quầy thu ngân | Nhân viên thu ngân | Thanh toán phí khám và nhận toa thuốc |

> Tầng X và số phòng cụ thể hiển thị trong chi tiết lịch hẹn theo từng bác sĩ.

---

## Lưu ý kỹ thuật

- Toàn bộ dữ liệu lưu **local** bằng AsyncStorage — không có backend, không đồng bộ qua mạng
- Đăng nhập bằng **số CCCD 12 chữ số** — 1 người 1 tài khoản 1 sổ bệnh án
- Dữ liệu mỗi tài khoản độc lập — không rò rỉ sang tài khoản khác
- **Chống đặt trùng:** mỗi bác sĩ chỉ khám 1 bệnh nhân / khung giờ (kiểm tra toàn bộ người dùng); 1 bệnh nhân không thể có 2 lịch cùng giờ dù khác bác sĩ
- Mỗi lịch hẹn có **mã lịch hẹn** (VD: MC202404190042) và **số thứ tự** (VD: A012)
- Chủ nhật không có lịch khám
- Hồ sơ y tế mặc định "Chưa cập nhật" vì không có portal bác sĩ
- Đánh giá bác sĩ lưu local, không thay đổi điểm rating hiển thị
- Thông tin bác sĩ (học vị, bệnh viện, giải thưởng) là dữ liệu mẫu minh họa

---

## Cấu trúc thư mục

```
MediCare/
├── App.js
└── src/
    ├── context/AppContext.js       # Toàn bộ state và business logic
    ├── data/mockData.js            # 50 bác sĩ, 8 chuyên khoa, lịch theo chuyên khoa, phòng khám
    ├── navigation/AppNavigator.js  # Điều hướng toàn app
    ├── screens/
    │   ├── auth/                   # Login · Register · ForgotPassword
    │   ├── home/                   # Home · ClinicInfo
    │   ├── doctor/                 # DoctorList · DoctorDetail · Search · Specialty
    │   ├── appointment/            # Book · Confirm · Success · List · Detail · Reschedule · Rate
    │   ├── records/                # MedicalRecords · RecordDetail
    │   ├── profile/                # Profile · EditProfile · Settings · ChangePassword · SetPasscode · PasscodeEntry
    │   └── notifications/          # Notifications
    ├── theme/colors.js
    └── utils/
        ├── dateUtils.js
        └── storage.js
```

---



*Phiên bản 1.1.0*
