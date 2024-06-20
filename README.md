# WisecraneFA Base API

Merupakan base API dari aplikasi WisecraneFA.\
Machine Learning deploy API bisa diakses pada [Link ini](https://storage.googleapis.com/capstone-ml123/financial_recommendation_model.json).

## Daftar Isi

- [Fitur](#fitur)
- [Prasyarat](#prasyarat)
- [Instalasi](#instalasi)
- [Konfigurasi Firebase](#konfigurasi-firebase)
- [Penggunaan](#penggunaan)
- [Lisensi](#lisensi)

## Fitur

- Registrasi pengguna dengan email dan password
- Login pengguna dengan email dan password
- Reset password pengguna
- Login pengguna dengan akun Google
- Verifikasi email pengguna

## Prasyarat

Sebelum memulai, pastikan Anda telah menginstal perangkat lunak berikut:

- [Android Studio](https://developer.android.com/studio)
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)

## Instalasi

1. Clone repositori ini ke mesin lokal Anda:

    ```sh
    git clone [https://github.com/username/repo-name.git](https://github.com/wisecrane-fa/WisecraneFA-Base-API.git)
    cd WisecraneFA-Base-API
    ```

2. Buka proyek ini di Android Studio.

3. Tambahkan dependensi Firebase ke proyek Anda dengan menambahkan baris berikut ke berkas `build.gradle` di tingkat aplikasi:

    ```groovy
    dependencies {
        implementation 'com.google.firebase:firebase-auth'
        implementation 'com.google.android.gms:play-services-auth'
    }
    ```

4. Sinkronkan proyek Anda dengan Gradle.

## Konfigurasi Firebase

1. Pergi ke [Firebase Console](https://console.firebase.google.com/).
2. Buat proyek baru atau pilih proyek yang sudah ada.
3. Tambahkan aplikasi Android ke proyek Firebase:
    - Masukkan package name aplikasi.
    - Unduh `google-services.json` dan letakkan di direktori `app/` pada proyek Anda.
4. Di Firebase Console, navigasikan ke **Authentication** > **Sign-in method**.
    - Aktifkan **Email/Password**.
    - Aktifkan **Google**.

5. Tambahkan ID Klien Web Default ke berkas `res/values/strings.xml`:

    ```xml
    <resources>
        <string name="app_name">YourAppName</string>
        <string name="default_web_client_id">YOUR_WEB_CLIENT_ID</string> // Anda bisa menemukannya pada opsi sign-in Google
    </resources>
    ```

## Penggunaan

### Registrasi Pengguna

1. Pengguna memasukkan email dan password mereka di layar registrasi.
2. Aplikasi akan mengirim email verifikasi ke alamat email pengguna.
3. Setelah verifikasi, pengguna bisa login ke aplikasi.

### Login dengan Email/Password

1. Pengguna memasukkan email dan password mereka di layar login.
2. Jika email terverifikasi, pengguna akan berhasil login.

### Login dengan Akun Google

1. Pengguna mengklik tombol "Sign in with Google".
2. Pengguna akan diarahkan ke layar Google Sign-In.
3. Setelah berhasil login, pengguna akan diarahkan kembali ke aplikasi.

## Lisensi

Proyek ini dilisensikan di bawah lisensi MIT. Lihat berkas [LICENSE](LICENSE) untuk informasi lebih lanjut.
