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

### Ana Sayfa

```http
GET /
