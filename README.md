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

## Api Key ( Anahtar )

- `test` - Api Anahtarınızdır

## Dökümantasyon

API'yi daha fazla anlamak ve kullanmak için API dökümantasyonuna başvurabilirsiniz. İşte API'nin dökümantasyonunu incelemek için bir bağlantı:

- [API Dökümantasyonu](http://77.90.131.131:10000/api-docs/)

Bu dökümantasyon, API'nin kullanılabilir end point'lerini, istek yapma yöntemlerini, dönen verileri ve diğer önemli bilgileri içerir. API dökümantasyonunu inceleyerek API'nin işlevselliği hakkında daha fazla bilgi edinebilirsiniz. Başlamadan önce API sağlayıcısının belirttiği kılavuzları ve gereksinimleri dikkatlice okumanız önemlidir.

## Veri Çekme Örneği

Bu örnek kod, Axios kullanarak bir API'den veri çekmek için kullanılabilir. API anahtarınızı ve API URL'sini kod içinde belirtmelisiniz.

Kodunuzu çalıştırmak için aşağıdaki adımları takip edebilirsiniz:

1. API anahtarınızı `apiKey` değişkenine ekleyin.
2. İstek atılacak API URL'sini `apiUrl` değişkenine belirtin.
3. Kodu çalıştırın ve API'den verileri çekin.

Kod, başarılı bir şekilde verileri alıp konsola yazdıracaktır.

```javascript
const axios = require('axios');

async function fetchData() {
    const apiKey = 'test'; // API anahtarınızı buraya ekleyin
    const apiUrl = `http://77.90.131.131:10000/user/${interaction.user.id}`; // İstek atılacak API URL'sini belirtin
    
    try {
        const response = await axios.get(apiUrl, {
            headers: {
                'x-api-key': apiKey,
            },
        });
        
        console.log("İstek Başarılı!", response.data);

        const otherNames = response.data["User"]["Isimler"].map((x) => x).join("\n");
        console.log(otherNames);
    } catch (error) {
        console.error('Hata:', error);
    }
}

fetchData();
```

## Discord Kullanıcısının API Ile Çekilen Bilgileri ( Örnek )

-  1 . Resim

![Screenshot_1](https://github.com/mysteriouss3/Mys-Api/assets/142053394/76141f14-6fe8-4b7b-a91a-7103d3cbac30)

-  2 . Resim

![Screenshot_2](https://github.com/mysteriouss3/Mys-Api/assets/142053394/19ba8a34-515b-41ab-a8e6-26f1c579e90a)

