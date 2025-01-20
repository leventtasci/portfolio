# Konfigürasyon

Openroads Designer neredeyse tamamı ile özelleştirilebilir bir yapıya sahip. Bu bölüm, Openroads'un esnek kişiselleştirme özelliklerini nasıl ayarlayabileceğini öğrenmek isteyenler için temel kavramları içeriyor.


Programı kurduğunuzda, <span style="color: #FF8C00; font-weight: bold;">`C:\ProgramData\Bentley\OpenRoads Designer CE ...\Configuration`</span> adresine, başlangıcı 
yapabilmeniz Bentley tarafından hazırlanan bir paket eklendi (`...` sizin kullandığınız versiyona göre değişir).


Bu bölümde, Bentley'e ait seti kullanarak, bilgisayarımızda bir çalışma alanı yaratacağız. Amacımız konfigürasyon dosyalarının temel görevlerini kavramak, daha fazlası değil. 
Daha sonraki bölümde detayları daha iyi anlaşılır bir sistem üzerinde ilerleyeceğiz ve o sistem üzerinde çalışacağız. Şu aşamada tüm dosyaların ve klasörlerin içerisinde kaybolmaktansa yalnızca şuna odaklanalım: 
- Konfigürasyon (`.cfg`) dosyaları nasıl kullanıyor?


## Konfigürasyon Dosyaları

Konfigurasyon (`.cfg`) dosyalarının iki temel görevi var:
- **Yönlendirme:** Programı kullanırken size lazım olan tüm dosya ve klasörlerin adreslerini tutmak. Openroads designer `.cfg` dosyalarındaki bu adresleri okuyarak tüm kaynaklara ve projelerinize ulaşacak.
- **Ayarlar:** Kardinal nokta kısaltmaları, profil view'larında düşey abartı seçenekleri vb. gibi detay ayarları tutmak.


## Yönlendirme

2. ve 3. adımlarda,sol taraf eski, sağ taraf son hali belirtir.


Adımlarda kullanılan simgeler: 
- Karşısında `➔` simgesi olan dosya veya klasörler __yeniden__ __adlandırılacak__.
- Karşısında `➾` simgesi olan dosya veya klasörler __değişirilmeyecek__. 
- <del>Üzeri çizili dosya veya klasörler</del> __silinecek__.
### 1. Adım: Bentley Örneğinden Kopya Oluşturma
<span style="color: #FF8C00; font-weight: bold;">`C:\ProgramData\Bentley\OpenRoads Designer CE ...\Configuration`</span> klasörü içerisindeki:
<span style="color: #FF8C00; font-weight: bold;">`Organization-Civil`</span>  ve <span style="color: #FF8C00; font-weight: bold;">`WorkSpaces`</span> klasörlerini ve `WorkSpaceSetup.cfg` dosyasını çalışmak istediğimiz konuma kopyalayalım ve yeniden adlandıralım. 
Örnekte bu klasör ve dosyalar <span style="color: #FF8C00; font-weight: bold;">`C:\AnaKlasor`</span> adresine kopyalandı.


<div style="display: flex;">
  <div style="flex: 1;">
    <!-- Column 1 content -->
    <details open>
      <summary>📁 ...\Configuration</summary>
      <pre>
├─  ...
├──📁Organization-Civil        ➔
├──📁WorkSpaces                ➔
└──🗒️WorkSpaceSetup.cfg        ➔
      </pre>
    </details>
  </div>
  <div style="flex: 1;">
    <!-- Column 2 content -->
    <details open>
      <summary>📁 C:\AnaKlasor</summary>
      <pre>
│
├──📁OrganizasyonIsmi
├──📁Projeler
└──🗒️Yonlendirme.cfg
      </pre>
    </details>
  </div>
</div>

### 2. Adım: OrganizasyonIsmi Klasörü
<span style="color: #00FFFF; font-weight: bold;">`OrganizasyonIsmi`</span> klasöründe aşağıdaki değişiklikleri yapalım. Bu klasörün sonuç içeriğinde iki `klasör` ve bir `.cfg` dosyası yer alacak.

<div style="display: flex;">
  <div style="flex: 1;">
    <!-- Column 1 content -->
    <details open>
      <summary>📁 C:\AnaKlasor\OrganizasyonIsmi</summary>
      <pre>
│
├──📁<del>_Civil Default Standards - Imperial</del>     	  
├──📁_Civil Default Standards - Metric      	➔   
├──📁Preference Seeds                         	➾   
├──🗒️<del>_Civil Default Standards - Imperial.cfg</del>   
├──🗒️_Civil Default Standards - Metric.cfg  	➔   
└──<del>Var ise diğer dosya ve klasörler</del>   
      </pre>
    </details>
  </div>
  <div style="flex: 1;">
    <!-- Column 2 content -->
    <details open>
      <summary>📁 C:\AnaKlasor\OrganizasyonIsmi</summary>
      <pre>
│
│
├──📁Standartlar
├──📁Preference Seeds
│
└──🗒️Standartlar.cfg
      </pre>
    </details>
  </div>
</div>

### 3. Adım: Projeler Klasörü
Projeler klasörünü açalım ve aşağıdaki düzenlemeyi yapalım. Bu klasörün sonuç içeriğinde üç `klasör` ve bir `.cfg` dosyası yer alacak.

<div style="display: flex;">
  <div style="flex: 1;">
    <!-- Column 1 content -->
    <details open>
      <summary>📁 C:\AnaKlasor\Projeler</summary>
      <pre>
├──📁<del>Imperial Standards</del>
├──📁Metric Standards         	  ➔
├──📁NoWorkSpace              	  ➾
├──📁Template                	  ➾
├──🗒️<del>Imperial Standards.cfg</del>
├──🗒️Metric Standards.cfg     	  ➔
├──🗒️<del>Training and Examples.cfg</del> 
└──<del>Var ise diğer dosya ve klasörler</del>
      </pre>
    </details>
  </div>
  <div style="flex: 1;">
    <!-- Column 2 content -->
    <details open>
      <summary>📁 C:\AnaKlasor\Projeler</summary>
      <pre>
│
├──📁OrganizasyonProjeleri
├──📁NoWorkSpace
├──📁Template
│
└──🗒️OrganizasyonProjeleri.cfg 
      </pre>
    </details>
  </div>
</div>

### 4. Adım: Konfigürasyon Dosyalarının Düzenlenmesi
Bu madde altında yaptıklarımızı toparlayalım.

#### Yonlendirme.cfg
Openroads Designer, açılışta ilk olarak bu dosyayı okuyacak ve aşağıdaki sorunların cevaplarına ulaşacak:
1. Proje üreteceğiniz organizasyona ait standartlar hangi klasörde? (`MY_CIVIL_ORGANIZATION_ROOT`)
2. Projeler klasörünüz nerede? (`MY_WORKSPACES_LOCATION`)
3. Klasör oluşturma görevleri neler?
   - Yeni bir Projeler seti oluşturduğunuzda hangi klasör setleri oluşturulsun?
   - Yeni bir Proje oluşturduğunuzda hangi klasör setleri oluşturulsun?
4. Program tercihlerinizi (preferences) nereden okumalıyım? 


 `C:\AnaKlasor` klasöründeki  `Yonlendirme.cfg` dosyasını açıp aşağıdaki değişiklikleri yapalım:
 ```{hint}
Konfigüraston dosyalarında, `hash` sembolü (`#`) ile başlayan satırlar Openroads Designer tarafından dikkate alınmaz.
```
- Openroads Designer, kullandığı değişkenlerin çoğunluğunu `OrganizasyonIsmi` olarak belirlediğimiz klasöründen okuyacak.
Halihazırda zaten Bentley gerekli değişkenleri giriş için hazırlamış fakat önlerinde `hash` (`#`) sembolü var. Bu sembolü kaldırıp
`MY_CIVIL_ORGANIZATION_ROOT` değişkenini aşağıdaki hale getirelim:
   - ```
     MY_CIVIL_ORGANIZATION_ROOT = C:/AnaKlasor/OrganizasyonIsmi/
     ```

- Projelerin tutulacağı klasörü tanıtalım:
   - ```
     MY_WORKSPACES_LOCATION = C:/AnaKlasor/Projeler/
     ```
Şu aşamada başka bir değişiklik yapmamız gerekmiyor, ileride bu `.cfg` dosyasının içeriğini nasıl düzenleyebileceğimiz konusunu başka örnekler ile detaylandıracağız.
Dosyayı kaydedip kapatabiliriz.

```{important}
- `.cfg` dosyalarını düzenlerken klasör ayıraç işaretlerinin (`/`) şeklinden ve adresin sonuna da bu ayıracın konulduğundan emin olunmalıdır. Aşağıdaki örnekleri inceleyiniz.

    - `C:\AnaKlasor\OrganizasyonProjeleri\` hatalı, `C:/AnaKlasor/OrganizasyonProjeleri/` olmalı
    - `C:/AnaKlasor/OrganizasyonProjeleri` hatalı, `C:/AnaKlasor/OrganizasyonProjeleri/` olmalı
```
#### OrganizasyonProjeleri.cfg
Projelere ait konfigürasyon dosyasında, projelerde hangi standardın kullanacağı, `CIVIL_ORGANIZATION_NAME` değişkenini ayarlayarak tarif edilmelidir.
`OrganizasyonProjeleri.cfg` dosyasını açıp aşağıdaki değişikliği yapalım:
   - ```
     CIVIL_ORGANIZATION_NAME = OrganizasyonIsmi
     ```
```{important}
- Burada `CIVIL_ORGANIZATION_NAME` değişkenine verilen değerin, klasör adresi değil klasör ismi olduğuna dikkat edelim.
```

### 5. Adım: Openroads






