# ImageFX API

Bu uygulama, Google'ın ImageFX servisini kullanarak yapay zeka destekli görsel oluşturmanızı sağlayan bir web uygulamasıdır. Modern bir arayüz ve kullanıcı dostu özelliklerle, görsel oluşturma sürecini kolaylaştırır.

## Özellikler

- 🎨 Yapay zeka destekli görsel oluşturma
- 🌐 Modern ve duyarlı web arayüzü
- ⚙️ Özelleştirilebilir ayarlar
- 🔑 Güvenli token yönetimi
- 📱 Mobil uyumlu tasarım
- 🔄 Gerçek zamanlı görsel önizleme
- 📥 Görsel indirme özelliği
- 🔍 Görsel büyütme ve detay görüntüleme
- 🌍 Harici API erişimi

## Kurulum

1. Gerekli Python paketlerini yükleyin:
```bash
pip install -r requirements.txt
```

2. Google ImageFX token'ınızı alın:
   - [ImageFX](https://labs.google/fx/tools/image-fx) sayfasını ziyaret edin
   - Dev-tools'u açın ve aşağıdaki kodu yapıştırarak token'ınızı alın:
   ```javascript
   let script = document.querySelector("#__NEXT_DATA__");
   let obj = JSON.parse(script.textContent);
   let authToken = obj['props']['pageProps']['session']['access_token'];
   window.prompt("Token'ı kopyalayın: ", authToken);
   ```

3. Uygulamayı başlatın:
```bash
python app.py
```

4. Tarayıcınızda `http://localhost:5000` adresini açın

5. Token'ınızı ayarlayın:
   - Sağ üst köşedeki "Settings" butonuna tıklayın
   - Kopyaladığınız token'ı "Authentication Token" alanına yapıştırın
   - "Save Changes" butonuna tıklayın

## Kullanım

### Web Arayüzü
1. Ana sayfada görsel oluşturmak istediğiniz açıklamayı girin
2. Oluşturmak istediğiniz görsel sayısını seçin (1-8)
3. İsterseniz bir seed değeri girin (tutarlı sonuçlar için)
4. "Generate Magic ✨" butonuna tıklayın
5. Oluşturulan görselleri indirin veya büyütün

### Ayarlar Sayfası
1. Sağ üst köşedeki "Settings" butonuna tıklayın
2. Google ImageFX token'ınızı girin
3. Varsayılan görsel sayısını ayarlayın
4. Değişiklikleri kaydedin

### API Kullanımı
1. `/api` sayfasından API dokümantasyonuna erişin
2. `/api/test` sayfasından API'yi test edin
3. API endpoint'lerini kullanarak harici uygulamalardan görsel oluşturun

## API Endpoint'leri

### Görsel Oluşturma
```
GET /api/generate?prompt=your_prompt&count=4&seed=12345
```

### Ayarlar
```
GET /api/settings
POST /api/settings
```

## Önemli Notlar

- Token'lar yaklaşık 3 gün geçerlidir
- Token'ınızı güvenli bir şekilde saklayın
- Uygulama TailwindCSS kullanmaktadır
- API kullanımı için token gerektirmez

## Geliştirme

- Flask web framework'ü kullanılmaktadır
- TailwindCSS ile modern ve duyarlı tasarım
- JavaScript ile dinamik kullanıcı deneyimi
- Python ile güçlü backend işlemleri

## Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Detaylar için `LICENSE` dosyasına bakın.
