![image](https://github.com/user-attachments/assets/ac80e049-54ae-4522-af0d-65193f98d319)
Tested with Greymotion

# 📱 Luyện Thi Trắc Nghiệm CNTT - Mobile App

Ứng dụng giúp người dùng luyện tập trắc nghiệm chuyên ngành Công nghệ Thông tin. Giao diện đơn giản, dễ sử dụng, kết nối trực tiếp với hệ thống website Node.js.

---

## 🔧 Yêu cầu hệ thống

- Node.js >= 16
- Java JDK 17
- Android SDK (nên cài qua Android Studio hoặc Command Line Tools)
- Capacitor CLI (`npm install --global @capacitor/cli`)
- Một thiết bị Android thật **hoặc** trình giả lập như Android Studio AVD, Genymotion

---

## 🚀 Cách cài đặt và build mobile app

# 1. Clone project về
git clone https://github.com/tuandatne4102/mobileapp.git
cd mobileapp

# 2. Cài đặt dependencies
npm install

# 3. Build web (cần có folder dist nếu dùng framework)
npm run build

# 4. Đồng bộ với Capacitor
npx cap sync

# 5. Mở Android Studio để build hoặc debug
npx cap open android

# (Tuỳ chọn) Cài trực tiếp lên thiết bị đã kết nối
npx cap run android --target [device-id]


## Cài APK thủ công

cd android
./gradlew assembleDebug

File APK nằm ở đường dẫn
android/app/build/outputs/apk/debug/app-debug.apk


| Vấn đề                         | Giải pháp                                               |
| ------------------------------ | ------------------------------------------------------- |
| `invalid source release: 21`   | Ép Gradle dùng Java 17                                  |
| `Could not determine SDK root` | Sửa `local.properties` hoặc đặt `ANDROID_HOME`          |
| `licenses not accepted`        | Chạy `sdkmanager --licenses` trong CMD                  |
| VS Code không thấy thiết bị    | Mở emulator hoặc bật USB Debugging trên điện thoại thật |


