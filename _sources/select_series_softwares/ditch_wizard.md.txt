# Hendek Sihirbazı

<div style="overflow: auto;">

<div style="position: relative; width: 100%; max-width: 800px; height: 450px; margin: 0 auto; min-height: 300px;">
  <iframe
    src="https://www.youtube.com/embed/FiD_0VXeGL0"
    frameborder="0"
    allowfullscreen
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
  ></iframe>
</div>

  <img src="../_static/ditch_wizard_ui.png" alt="Ditch Wizard UI" style="float: left; margin-right: 20px; margin-top: 5px; padding-right: 10px; max-width: 45%; height: auto;">
  
  
<div style="text-align: justify;">

<h2 style="margin-top: 0;">Tespitler</h2>

Kafa, topuk, yarma, palye hendeklerinin hesap ve çizimleri, oldukça vakit alan ve yoğun iş gücü gerektiren “Drenaj” başlığının en önemli pozlarından birisidir.
Bu konuda, uluslararası standartta yaygın bir proje üretim aracı bulunmamaktadır. Storm & Sanitary dahilindeki araçlar imalat projeleri için yeterli detayları üretememektedir.
 

  ## Başardıkları

  - Hendek Sihirbazı, boyuna drenajdaki tüm hendeklerinin hesap, metraj ve çizimlerinin tamamını yapar. 
  - Hesaplar, uluslararası standartları da içerir (Spesifik enerji, shear stress, düşü vb.)
  - Çizimler projeye göre özelleştirilebilir.
  - Inroads ile bağlantılı çalışır, ilave raporların alınması gerekmez.

## Öne Çıkan Özellikleri

  - Hendekler tek bir seçimle hesap sayfasına aktarılırken Inroads bağlantısı ile, ilgili güzergah ve dtm ile bağlantı kurularak kot ve kilometraj bilgileri de hendeğe yazılır.
  - Hendek hesap sayfası, KGM ve Global olarak iki farklı mod içerir. 
  	- KGM modu Türkiye’de kullanılan detayları içeren hendek hesap yöntemlerini içerir. 
  	- Global Mode, spesifik enerji kontrolleri, kesme gücü ve froud kontrollerini de içerir. Düşü seçeneği bu değerlerin kontrol edilebilmesi için hesaplarda mevcuttur. Düşü sayısı maliyeti etkileyen bir kalemdir ve Hendek Sihirbazı hendek boyunca yapılan bu düşülerin sayısını da plana işleme yeteneğine sahiptir.
  - Hesap sayfası ile senkronize olarak, hendeğe ait verteks ve boyut bilgilerini özelleştirilebilir formatlarda plana yazar, hazır formatları da içerir. Hendek Sihirbazı, hesapların ardından hendek tahliye  debilerini, diğer drenaj elemanları ile etkileşiminin görülebilmesi için plan üzerine çizebilir.
  - Hesap ve çizimlerin ardından, baskı formatına uygun  ürettiği metrajı ve sahada hendek aplikasyonlarında kullanılabilecek hendek verteks koordinat bilgilerini Generate Reports bölümünden tek bir seçimle hazırlar. 
  - Hendek Sihirbazı, hendeğin 3D modelinin üretilmesinde de önemli işler yapar. Hendek, hesap sayfasına aktarılırken Create alg seçili ise otomatik olarak bir alg yaratılır. Hendek sihirbazı ilk profili belirli kabullerle kendisi üretir. Update Ditch ve Get Vertical alignment opsiyonları, hesap sayfası ile inroads arasında iteratif çalışmalara imkan verir. (Örneğin hesap sayfasında boyut artışları veya düşü eklenmesi hendek profilini değiştirebilir, bu koşulda hendek düşeyi  tekrar bir tuşla hesap sayfasından inroads’a alınır, bunun tersi de mümkündür: hendek için inroads’ta çalışılan düşey hat yine tek bir seçim ile hesap sayfasına gönderilebilir)
  - Hendek Sihirbazı, hendeğe ait tüm verteksleri Inroads’a Cogo Point olarak hesap sayfasından alabilir. Bu noktalar, semboloji ayarları yapılarak istenilen her kesit veya profilde kolayca gösterilebilir. (Örneğin menfez girişini göstermek için hazırlanmış bir izdüşüm profilinde, bu menfeze tahliye olan hendekler de CogoPoint’ler ile detaylandırılabilir.)




<div style="position: relative; width: 100%; max-width: 800px; height: 450px; margin: 0 auto; min-height: 300px;">
  <iframe
    src="https://www.youtube.com/embed/QL9Bv0dOc7Y"
    frameborder="0"
    allowfullscreen
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
  ></iframe>
</div>

  ## Geliştirici Notları

Yapı Merkezi’nin Etiyopya’da imalatını yaptığı bir demiryolu boyuna drenaj projesinde kullanılmak üzere ilk versiyonu geliştirilmiştir. Müşaviri Fransız Systra firması olan, 52km’lik bu işte müşavirin istediği proje formatı ve detayında üretim yapabilme yeteneğine sahip bir yazılım ihtiyacı doğmuştur. Hendeklerin bu proje kapsamında 3D olarak modellenmesi talep edilmiştir, bu yüzden Hendek Sihirbazı 3D modelleme çalışmalarına yönelik araçlar da içerir. Systra’dan, Hendek Sihirbazının ilk versiyonu  ile hazırlanmış projelerin sunumunun ardından revizyon alınmamıştır.
Bu işin ardından, ilk versiyon KGM işleri için de güncellenmiştir;  şu anda hem KGM projelerinde hem de uluslararası projelerde yaklaşık altı yılı aşkın süredir kullanılmaktadır. 


</div>


</div>




