# Konfigurasyon

## Giriş
Konfigürasyon konusunun detaylarına girmeden önce, Bentley'nin program kurulduğunda gelen hazır setini bilgisayarınızda bir başka klasöre nasıl taşınabileceğinize kısaca değinelim ve konfigürasyon dosyalarının genel parametrelerini anlayalım.


## Gerçek Hayat
Bentley'nin programı kurduğunuzda gelen örnekleri, başlangıç pratiklerini uygulayabilmeniz için pakette yer alıyor, örneklerdeki dosyalama veya çalışma sistemini uygulamanız elbette gerekmiyor.
Gerçek hayatta, her bir ticari oluşum kendine özgü bir proje üretme yapısına sahip: İşi aldığı idare ve çalışma gruplarının yapısı aynı olan iki firma bulmak oldukça zor. Konfigürasyon dosyaları kendi sisteminizi veya firmanızın sistemini oluştururken en önemli anahtarlarınız. 

Aşağıdaki kurguları en tepeden bakarak, işi yürüten firma veya kurum gözü ile incelemekte fayda var.
Konfigürasyon (`Configuration`) ve Çalışma Alanı (`Workspace`) başlıklarını tam fonksiyonları ile kullanabilmeniz, tek bir çalışma sistemine bağlı kalmamanızı sağlayacak. Programın neredeyse tamamen özelleştirilebilen çalışma şekli, sizin kurgunuza bağlı sınırsız seçenekler sunuyor.

### Konfigürasyon Kurguları

> **Global** piyasada <u>**karayolu ve demiryolu**</u> projesi üreten bir proje firması:
```
💼 Firma-Uluslararası Connect .................... COMPANY
│
├── ⚙️ Ulusal-Demiryolu .......................... Configuration
│   ├── 🚆 Konvansiyonel Projeler ................ Workspace
│   ├── 🚄 Hızlı Tren Projeleri .................. Workspace
│   └── 🚈 Hafif Rayli Sistem Projeleri .......... Workspace
│
├── ⚙️ Ulusal-Karayolu  .......................... Configuration
│   ├── 🏢 KGM Projeleri ......................... Workspace
│   ├── 🏬 KGM Bölge Projeleri ................... Workspace
│   └── 🏛️ Belediye Projeleri .................... Workspace
│
├── ⚙️ Global-Demiryolu .......................... Configuration
│   ├── 📚 Projeler (Tür-1) ...................... Workspace
│   └── 📚 Projeler (Tür-2) ...................... Workspace
│
└── ⚙️ Global-Karayolu ........................... Configuration
    ├── 📚 Projeler (Tür-1) ...................... Workspace
    └── 📚 Projeler (Tür-2) ...................... Workspace
```
<small>Gerekli programlar: _Openrail Designer_</small>

___

> **Türkiye**'de <u>**karayolu ve demiryolu**</u> projesi üreten bir proje firması:
```
💼 Firma-TR-KD Connect ........................... COMPANY
│
├── ⚙️ Karayolu .................................. Configuration
│   ├── 🏢 KGM Projeleri ......................... Workspace
│   ├── 🏬 KGM Bölge Projeleri ................... Workspace
│   └── 🏛️ Belediye Projeleri .................... Workspace
│
└── ⚙️ Demiryolu  ................................ Configuration
    ├── 🚆 Konvansiyonel Projeler ................ Workspace
    ├── 🚄 Hızlı Tren Projeleri .................. Workspace
    └── 🚈 Hafif Rayli Sistem Projeleri .......... Workspace
```
<small>Gerekli programlar: _Openrail Designer_</small>

___

> **Türkiye**'de <u>**yalnızca karayolu**</u> projesi üreten bir proje firması:
```
💼 Firma-TR-K Connect ............................ COMPANY
│
├── ⚙️ KGM ....................................... Configuration
│   └── 🏢 Danışmanlık Projeleri ................. Workspace
│
├── ⚙️ KGM Bölgeler............................... Configuration
│   ├── 🏬 01- İstanbul Bölge Projeleri .......... Workspace
│   ├── 🏬 02- İzmir Bölge Projeleri ............. Workspace
│   ├── 🏬 03- Konya Bölge Projeleri ............. Workspace
│   ├── 🏬 04- Ankara Bölge Projeleri ............ Workspace
│   ├── 🏬 05- Mersin Bölge Projeleri ............ Workspace
│   ├── 🏬 06- Kayseri Bölge Projeleri ........... Workspace
│   ├── 🏬 07- Samsun Bölge Projeleri ............ Workspace
│   ├── 🏬 08- Elazığ Bölge Projeleri ............ Workspace
│   ├── 🏬 09- Diyarbakır Bölge Projeleri ........ Workspace
│   ├── 🏬 10- Trabzon Bölge Projeleri ........... Workspace
│   ├── 🏬 11- Van Bölge Projeleri ............... Workspace
│   ├── 🏬 12- Erzurum Bölge Projeleri ........... Workspace
│   ├── 🏬 13- Antalya Bölge Projeleri ........... Workspace
│   ├── 🏬 14- Bursa Bölge Projeleri ............. Workspace
│   ├── 🏬 15- Kastamonu Bölge Projeleri ......... Workspace
│   ├── 🏬 16- Sivas Bölge Projeleri ............. Workspace
│   └── 🏬 18- Kars Bölge Projeleri .............. Workspace
│
└── ⚙️ Belediyeler................................ Configuration
    ├── 🏛️ Ankara BBB ............................ Workspace
    ├── 🏛️ İzmir BBB ............................. Workspace
    └── 🏛️ İstanbul BBB .......................... Workspace
```
<small>Gerekli programlar: _Openroads Designer_</small>

___

> **Türkiye**'de bir yol yapım şantiyesinin <u>**teknik ofisi**</u>:
```
💼 Firma-TR-Yapim Connect ........................ COMPANY
│
└── ⚙️ Şantiye ................................... Configuration
    ├── 🏢 İhale Edilen Proje .................... Workspace
    ├── 📐 As-Build-Km=0+000-1+200. .............. Workspace
    ├── 📐 As-Build-Km=14+000-16+000 ............. Workspace
    └── 🌉 Köprü Projeleri ....................... Workspace
```
<small>Gerekli programlar: _Openroads Designer_, _OpenBridge Designer_</small>

___

> **Türkiye**'de karayolu projelerinde uzman bir <u>**serbest mühendis**</u> :
```
💼 Firma-TR-Yapim Connect ........................ COMPANY
│
└── ⚙️ Projeler .................................. Configuration
    ├── 🏢 Karayolu Projeleri .................... Workspace
    ├── 📐 Kavşak Projeleri ...................... Workspace
    ├── 📐 Yapım Projeleri ....................... Workspace
    └── 🌉 Tünel Geometri Projeleri .............. Workspace
```
<small>Gerekli programlar: _Openroads Designer_</small>

___

> **Türkiye**'de genel kontrol makamı <u>**KGM (Kurum)**</u>:
```
💼 KGM Connect ................................... ORGANIZATION
│
├── ⚙️ Etüt, Proje ve Çevre Dairesi Başkanlığı ... Configuration
│   ├── 🏢 Danışmanlık Projeleri ................. Workspace
│   ├── 🏢 Hizmet Alımı Projeleri ................ Workspace
│   ├── 🏢 Diğer Projeler ........................ Workspace
│   └── 🏢 Planlama Projeleri..................... Workspace
│
└── ⚙️ Bölgeler................................... Configuration
    ├── 🏬 01- İstanbul Bölge Projeleri .......... Workspace
    ├── 🏬 02- İzmir Bölge Projeleri ............. Workspace
    ├── 🏬 03- Konya Bölge Projeleri ............. Workspace
    ├── 🏬 04- Ankara Bölge Projeleri ............ Workspace
    ├── 🏬 05- Mersin Bölge Projeleri ............ Workspace
    ├── 🏬 06- Kayseri Bölge Projeleri ........... Workspace
    ├── 🏬 07- Samsun Bölge Projeleri ............ Workspace
    ├── 🏬 08- Elazığ Bölge Projeleri ............ Workspace
    ├── 🏬 09- Diyarbakır Bölge Projeleri ........ Workspace
    ├── 🏬 10- Trabzon Bölge Projeleri ........... Workspace
    ├── 🏬 11- Van Bölge Projeleri ............... Workspace
    ├── 🏬 12- Erzurum Bölge Projeleri ........... Workspace
    ├── 🏬 13- Antalya Bölge Projeleri ........... Workspace
    ├── 🏬 14- Bursa Bölge Projeleri ............. Workspace
    ├── 🏬 15- Kastamonu Bölge Projeleri ......... Workspace
    ├── 🏬 16- Sivas Bölge Projeleri ............. Workspace
    └── 🏬 18- Kars Bölge Projeleri .............. Workspace
```
<small>Gerekli programlar: _Openroads Designer_, _Concept Station_, _Openbridge Designer_</small>
___

```{important}
Yukarıdakiler, **Konfigürasyon** (`Configuration`) ve **Çalışma Alanı** (`Workspace`) unsurlarının, farklı firmalar veya kurumlar için farklı şekillerde ayarlanabileceğini göstermek amacı ile derlendi.
Elbette ki firma veya kurum, oluşturacağı sistemde çalışacak herkesin rahatlıkla anlayabileceği şekilde, alanında uzman mühendisleri ile birlikte çalışarak sistem şemasını oluşturmalıdır.


Yukarıdaki örnekler incelendiğinde bir firma veya kurumun yalnızca bir sistemi olmalı kanısı oluşmamalı.
Bir firma veya kurum içerisinde farklı sistemler olabilir, konfigürasyon ayarlarını kullanarak bu farklı sistemler ortak dosyaları rahatlıkla paylaşabilir.


Firmanın veya kurumun tüm projeleri, her persolene açık olmak zorunda da değil. Yukarıda gördüğünüz her bir birim, düzenlemenizin sonunda bilgisayarınızda veya server'da bir klasör olacak.
Server ayarlarınız ile farklı ekipleri farklı çalışma alanı (`Workspace`) klasörleri için yetkilendirerek, aslında tek kaynaktan beslenen, herkesin kendi iş kapsamına ulaşabildiği bir şema oluşturmak da mümkün olacak.
```

## Neden Yeni Bentley Tasarım Serisinin Adı Connect?





