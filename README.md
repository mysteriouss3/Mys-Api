<div align="center">
  <br />
  <p>
    <a href="https://discord.js.org"><img src="https://discord.js.org/static/logo.svg" width="546" alt="discord.js" /></a>
  </p>
</div>

# Mys API

Mys API, kullanıcılara çeşitli bilgilere erişim sağlayan bir API'dir. API, farklı endpointler aracılığıyla veriler sunar ve çeşitli hizmetler sağlar.

## API Hakkında

- Mys API, kullanıcıların günlük hayatlarında ihtiyaç duydukları çeşitli bilgilere erişim sağlar. Hava durumu, burç bilgisi, döviz kuru, namaz vakitleri gibi çeşitli hizmetler sunar.
- Mys API'nin en önemli özelliği ise discord kullanıcılarını stalklamak.

## Kullanım

API'yi kullanmak için çeşitli endpointler bulunmaktadır. İşte bazı örnek endpointler:

- `/user/{id}` - Kullanıcı Bilgisi
- `/burc/{isim}` - Burç Bilgisi
- `/gunlukburc/{isim}` - Günlük Burç Bilgisi
- `/haftalikburc/{isim}` - Haftalık Burç Bilgisi
- `/aylikburc/{isim}` - Aylık Burç Bilgisi
- `/weather/{isim}/` - Hava Durumu Bilgisi
- `/iltifat` - İltifat
- `/doviz` - Döviz Kuru Bilgisi
- `/namaz/{sehir}/{ilce}` - Namaz Vakitleri
- `/nsfw` - NSFW İçerik //

Daha fazla endpoint ve kullanım bilgisi için [API Dökümantasyonu](https://discordpanel.vercel.app/document/) sayfasını ziyaret edebilirsiniz.

## Veri Çekme Örneği

## Npm Paketiyle Veri Çekmek Icin
- https://www.npmjs.com/package/mys-api.js

## Aşağıdaki örnek kod, Axios kullanarak bir API'den veri çekmek için kullanılabilir. API anahtarınızı ve API URL'sini kod içinde belirtmelisiniz.

```javascript
const axios = require('axios');

async function fetchData() {
    const apiKey = 'test'; // API anahtarınızı buraya ekleyin
    const apiUrl = `https://discordpanel.vercel.app/api/user/{id}`; // İstek atılacak API URL'sini belirtin
    
    try {
        const response = await axios.get(apiUrl);
        
        console.log("İstek Başarılı!", response.data);

        const otherNames = response.data["GuildsDisplayNames"].map((x) => x).join("\n");
        console.log(otherNames);
    } catch (error) {
        console.error('Hata:', error);
    }
}

fetchData();
```

## Örnek Ekran Görüntüleri

![Örnek Ekran Görüntüsü 1](https://github.com/mysteriouss3/Mys-Api/assets/142053394/76141f14-6fe8-4b7b-a91a-7103d3cbac30)

![Örnek Ekran Görüntüsü 2](https://github.com/mysteriouss3/Mys-Api/assets/142053394/19ba8a34-515b-41ab-a8e6-26f1c579e90a)

## Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Daha fazla bilgi için [LICENSE](LICENSE) dosyasını inceleyebilirsiniz.
