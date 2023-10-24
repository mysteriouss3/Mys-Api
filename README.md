# Mys API - API Belgesi

Mys API, kullanıcılara farklı bilgilere erişim sağlayan bir API'dir. API, çeşitli endpunktler aracılığıyla veriler sunar. Bu belge, Mys API'nin kullanımı ve özellikleri hakkında bilgi içermektedir.

## API Sürümü

- **Sürüm**: 1.0.0
- **OpenAPI Standartı**: 3.0

## Yetkilendirme

API'ye erişim için yetkilendirme gerekmemektedir (default).

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

## Kullanım

API'yi kullanmak için ilgili endpoint'e HTTP GET isteği göndermelisiniz. Örnekler:

###Node.js İçin Bazı Örnekler

```bash

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

        console.log(OtherName)```

### Ana Sayfa
