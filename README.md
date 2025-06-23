# Proteus Flip-Flop Devresi (Proteus #3)


🔗 [Web Siteme Bakmak İçin Tıkla](https://www.hakkiharmankaya.com/)

Proteus üzerinden Flip-Flop devresi yapmak oldukça öğretici ve dijital devre mantığını kavramak açısından önemlidir. Bu rehberde SR Flip-Flop devresi örneği üzerinden adım adım bir kurulum anlatılmıştır. GitHub üzerinden yaklaşık yapıya sahip devre dosyalarına ulaşabilirsiniz.

---

## 🔧 Gerekli Malzemeler

- 2 adet NAND kapısı (74LS00 veya 4011)  
- 2 adet buton (düğme)  
- 2 adet LED  
- Dirençler (220Ω önerilir)  
- 5V DC Güç Kaynağı  
- Breadboard (simülasyon görünümü için)

---

## ⚙️ Adım Adım Kurulum

### 1️⃣ SR Flip-Flop Devresi Tasarımı

#### A. Devre Elemanlarını Seç
- Proteus arayüzünde “P” butonuna tıklayın.
- NAND kapısı için “4011” veya “74LS00” yazın.
- Buton, LED ve dirençleri ekleyin.

#### B. NAND Kapılarıyla Flip-Flop Oluştur
- İki NAND kapısını birbirine geri beslemeli bağlayarak SR Flip-Flop yapısı kurun.
- Birinci NAND’ın çıkışını, ikinci NAND’ın girişine; ikinci NAND’ın çıkışını, birinci NAND’ın girişine bağlayın.

#### C. Giriş Butonlarını Bağla
- İlk NAND’ın boş girişine bir buton bağlayın (Set - S).
- İkinci NAND’ın boş girişine bir buton daha bağlayın (Reset - R).
- Buton uçlarını GND’ye bağlayın ve pull-up dirençlerle stabilizasyon sağlayın.

#### D. LED ve Çıkışları Bağla
- Birinci NAND çıkışına LED bağlayın → Q çıkışı.
- İkinci NAND çıkışına LED bağlayın → Q̅ (ters Q) çıkışı.
- LED’leri 220Ω dirençler aracılığıyla GND’ye bağlayarak tamamlayın.

---

### 2️⃣ Simülasyonu Başlat

- Proteus'ta tüm bağlantıları yaptıktan sonra **"Run"** butonuna basarak simülasyonu çalıştırın.
- `S` butonuna bastığınızda: **Q = 1**, **Q̅ = 0** → LED1 yanar.
- `R` butonuna bastığınızda: **Q = 0**, **Q̅ = 1** → LED2 yanar.
- Her iki giriş aktif olduğunda tanımsız durum oluşur (kaçınılmalıdır).

---

## 🔁 Alternatif Flip-Flop Entegreleri

Proteus içinde daha gelişmiş Flip-Flop devreleri yapmak için aşağıdaki entegreler kullanılabilir:

- **JK Flip-Flop:** `74LS76`, `74LS112`  
- **D Flip-Flop:** `74LS74`

Bu entegreler sayesinde daha kompakt devreler kurabilir, sayıcı ve saklayıcı sistemleri kolayca tasarlayabilirsiniz.

---

## 🔍 Flip-Flop’un Çalışma Mantığı

- **Set (S)** girişine 1 → Q çıkışı HIGH olur (LED yanar).  
- **Reset (R)** girişine 1 → Q çıkışı LOW olur (LED söner).  
- **S = 1, R = 1** → **Tanımsız durum** (kaçınılmalıdır).

---

Bu temel devre sayesinde dijital mantığın yapı taşlarından biri olan Flip-Flop kavramını deneyimleyebilir, mantık devrelerini Proteus ortamında simüle ederek öğrenebilirsin.
