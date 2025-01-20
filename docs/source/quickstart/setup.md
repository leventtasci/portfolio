# Ayarlar

Projelerimiz aşağıdaki 3 ana konunun birleşimi ile yönetilecek:
Çalışma Alanı Ayarları + Standart Ayarları + Projeler



| No |          Birim             | 				     Dosya 				       |
|----|------------------------    |----------------------------------------------------------------------------|
| 1  | Çalışma alanları ayarı     | ...\Configuration\WorkSpaceSetup.cfg 				       |
| 2  | Standartlara ait ayar      | ...\Configuration\Organization-Civil\_Civil Default Standards - Metric.cfg |
| 3  | Projeler üst başlığı ayarı | ...\Configuration\WorkSpaces\Metric Standards.cfg                          |



## Katmanlar

### Program Yönlendirme

Programı, açılışta çalışacağımız klasöre yönlendirmemiz gerekiyor. Bu klasör Openroads arayüzünde bize pek görünmeyecek.
Klasör çalıştığınız firmanın adı gibi en üst katmanda yer alıyor ve firmanıza ait temel tasarım esasları burada bulunacak.

#### Openroads Designer Versiyon 2021 - Update 2 ve sonrası veriyonu kullananlar için:

Bu update sonrasında açılışa eklenen Manage Configuration bölümüne, en üst katmanı girelim:

-gif is here

Klasörde WorkSpaceSetup.cfg dosyasından okuyacak, aşağıya birşey girmemiz gerekmiyor.


#### Openroads Designer Versiyon 2021 - Update 2 öncesi versiyonları kullananlar için:

_C:\ProgramData\Bentley\OpenRoads Designer CE ....\Configuration klasöründeki WorkSpaceSetup.cfg dosyasını açalım ve aşağıdaki değişiklikleri yapalım:

Yeni versiyonu kullananlar bu katmanı da açılışta görebilirken, siz bu yönlendirmeyi burada yapmalısınız.


### Mühendislik Ayarları Katmanı

Mühendislik ayarları katmanını, **Genel** ve **Tasarim** olarak iki klasörde gruplandı.
Konumuz Openroads Designer ile proje üretmeye başlamak olduğundan **Genel** klasörünün üzerinde ilk aşamada fazla durmayacağız.
Tasarımda ilerledikçe, kişiselleştirme amaçlı bu klasörü kısa süre ziyaret edip ayrılacağız. İşimiz şu aşamada **Temel** klasörü ile.

**Genel** klasörünün içeriği aşağıdaki gibi:

```html
📁 Genel
├── 📁 Araclar
│   ├── 📁 nesne turleri ............. item type'lar ile ilgili arama dosyaları ve şablonlar
│   ├── 📁 programlama ............... vba macro'ları
│   ├── 📖 baglantilar.dgnlib ........ link ayarları
│   └── 📖 grafik filtreler.dgnlib ... grafik filtreleri barındıran dosya
│
├── 📁 Ayarlar
│   ├── 📁 gosterim .................. view attributes ile ilgili ayarlar 
│   ├── 📁 kullanici arayuzu ......... menü şeridini (ribbon) kişiselleştirme
│   ├── 📁 olcekler .................. programın kullandığı ölçekler
│   └── 📁 tercihler ................. genel ayarlar
│
├── 📁 Cizim Unsurlari
│   ├── 📁 cell ...................... tüm cell kütüphaneleri
│   ├── 📁 cizgi tipleri ............. 2D ve 3D çizgi tipleri
│   ├── 📁 font ...................... çizimlerde kullanılabilecek fontlar
│   ├── 📁 kalem ayarlari ............ var ise kalem ayarı dosyaları
│   ├── 📁 materyaller ............... 3D bileşen görselleri için materyaller (asfalt vb.)
│   └── 📁 renk kitapliklari ......... gerekli renk kitaplıkları
│
├── 📁 Paftalama Ayarlari ............ tüm pafta ayarlarını içeren dgnlib dosyaları
│
├── 📁 Raporlar ...................... xml raporları
│
└── 📁 Yeni Dosya Kaynagi
    ├── 📰 kaynak 2d-design.dgn ...... design türünde açacağınız yeni dosyalara ait seed 
    ├── 📰 kaynak 2d-drawing.dgn ..... drawing türünde açacağınız yeni dosyalara ait seed
    └── 📰 kaynak 2d-sheet.dgn ....... sheet türünde açacağınız yeni dosyalara ait seed
```


**Tasarim** klasörünün içeriği ise aşağıdaki gibi:

```html
📁 Tasarim
├── 📁 hesaplar
│   ├── 🗒️ dever_aashto2011.xml ............ dever hesapları bu dosya ile yapılacak
│   ├── 🗒️ gorus mesafesi.xml .............. görüş mesafesi kontrolleri bu dosya ile yapılacak
│   ├── 🗒️ tasarim kontrol.xml ............. tasarım kontrolleri bu dosya ile yapılacak
│   └── 🗒️ yol turleri hiz tablolari.xml ... yol türü ve hız girişleri ile tasarım kontrolleri
│
├── 📖 temel.dgnlib ........................ f. definition, text style, t. favorites, vb.
│
├── 📖 civilcell.dnglib .................... tüm civil cell'ler bu dosyada tutulacak
│
└── 🛤️ kesit kutuphanesi.itl ............... template kütüphanesi
```

Tasarim klasöründeki **<ins>tasarim kaynagi.dgnlib</ins>** dosyasını açalım ve işe başlayalım.

