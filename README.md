# Mys API - API Belgesi

Mys API, kullanıcılara farklı bilgilere erişim sağlayan bir API'dir. API, çeşitli endpunktler aracılığıyla veriler sunar. Bu belge, Mys API'nin kullanımı ve özellikleri hakkında bilgi içermektedir.

## API Sürümü

- **Sürüm**: 1.0.0
- **OpenAPI Standartı**: 3.0

## Yetkilendirme

API'ye erişim için yetkilendirme gerekmemektedir (Api-Key).

## Endpointler

- `GET /` - Ana Sayfa
- `GET /user/{id}` - Kullanıcı Bilgisi
- `GET /burc/{isim}` - Burç Bilgisi
- `GET /gunlukburc/{isim}` - Günlük Burç Bilgisi
- `GET /haftalikburc/{isim}` - Haftalık Burç Bilgisi
- `GET /aylikburc/{isim}` - Aylık Burç Bilgisi
- `GET /weather/{isim}/` - Hava Durumu Bilgisi
- `GET /iltifat` - İltifat
- `GET /doviz` - Döviz Kuru Bilgisi
- `GET /namaz/{sehir}/{ilce}` - Namaz Vakitleri
- `GET /nsfw` - NSFW İçerik

## Dökümantasyon

- `http://77.90.131.131:10000/api-docs/` - Api Dökümantasyonu


##Api Key ( Anahtar )

- `test` - Api Anahtarınızdır

## Kullanım

API'yi kullanmak için ilgili endpoint'e HTTP GET isteği göndermelisiniz. Örnekler:

### Node.js için api örnek kullanım

```bash
const axios = require('axios'); // axios kurmak için cmd penceresine npm install axios yazmanız yeterlidir 

const apiKey = 'test'; // API anahtarınızı buraya ekleyin
const apiUrl = `http://77.90.131.131:10000/user/${interaction.user.id}`; // İstek atılacak API URL'sini belirtin
// Axios ile GET isteği gönderme
const getData = await axios.get(apiUrl, {
    headers: {
        'x-api-key': apiKey,
    },
}).catch((error) => { console.error('Hata:', error)});


console.log("Istek Başarılı!",getData.data)

const OtherName = getData.data["User"]["Isimler"].map((x) => x).join("\n");

console.log(OtherName)
```

## Discord Kullanıcısının Api Ile Çekilen Bilgileri ( Örnek )

- 1. Resim

![Screenshot_1](https://github.com/mysteriouss3/Mys-Api/assets/142053394/76141f14-6fe8-4b7b-a91a-7103d3cbac30)

- 2. Resim

![Screenshot_2](https://github.com/mysteriouss3/Mys-Api/assets/142053394/19ba8a34-515b-41ab-a8e6-26f1c579e90a)

