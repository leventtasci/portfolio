# Menfez Sihirbazı
<div style="overflow: auto;">

<div style="position: relative; width: 100%; max-width: 800px; height: 450px; margin: 0 auto; min-height: 300px;">
  <iframe
    src="https://www.youtube.com/embed/ezX-FJ881jk"
    frameborder="0"
    allowfullscreen
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
  ></iframe>
</div>

  <img src="../_static/culvert_wizard_ui.png" alt="Culvert Wizard UI" style="float: left; margin-right: 20px; margin-top: 5px; padding-right: 10px; max-width: 40%; height: auto;">
  
  
<div style="text-align: justify;">

<h2 style="margin-top: 0;">Tespitler</h2>

Yaygın olarak kullanılan, menfez kesit ve plan yerleşimlerini yapan iki farklı program mevcuttur. Birisi “küçük”tipteki sanat yapılarını 2D yerleştiren, diğeri büyük tipteki menfezleri 3D yerleştiren, başka yetekleri bulunmayan, her ikisi de yaygın bir mühendislik programı olmayan MSAccess programını veri tabanı olarak kullanan kodlardır. Bu kodlar, Inroads ile bağlantılı çalışmazlar, girdileri Inroads’tan alınan text ve/veya xml formatlı raporlardır. 

  ## Başardıkları
  - Kutu menfezler ile ilgili başka bir yardımcı araca ihtiyaç duymaksızın tam bir çözüm sunar. Metraj için başka, paftalama hizmetleri için başka yazılımlar gerekmez. Proje menfezlerini, bir bütün olarak son ürün haline getirir.
  - Menfez Sihirbazı, her iki tipteki (küçük ve büyük) menfezler için 3D olarak çalışır ve hiçbir rapora gerek duymaksızın doğrudan Inroads’a bağlanarak kesit ve güzergah bilgisini okur. Bu durum çalışmalardaki hatayı azaltır ve hızı arttırır.
  - Veri tabanı, KGM kaynakları analiz edilerek detaylı bir formatta excel’de oluşturulmuştur, kabulleri bellidir (kuyu vb.) ve kapsamı mühendisler tarafından genişletilebilir.

  ## Öne Çıkan Özellikleri

  - Menfezin plana ve kesite yerleşimi için iki seçenek sunar:
     1. Inroads’tan okur
     2. Enkesit çiziminden seçimleri okur
  - Veritabanı excel formatlıdır, gerekli okumalar excel’den yapılır, menfez bilgileri excel’e yazılır. 
  - Menfezi plana 3D olarak çizer.
  - Karayollarının farklı tipteki (büyük ve küçük) menfezler için yayınladığı iki dökümandaki menfez tiplerini de içerir. İsteğe bağlı herhangi bir menfez tipine ait karakteristikler veri tabanına girilir ise standart dışı menfezlerin yerleşimini de yapabilir.
  - Yerleşim sırasında detaylı metrajı yapar ve veritabanına saklar. Daha sonra metraj, veri tabanı içerisindeki araçlar ile çıktı formatına yalnızca bir seçimde ulaşır.
  - Projenin tüm menfezlerini, dgn dosyası içerisindeki tüm profil setlerine bir seçimde işler. İşlerken cell kullanmaz, menfezi parametrelerinden okuduğu verilere göre profile çizer (tabliye, taban, kenar duvarı kalınlıkları olması gerektiği gibidir) ve bilgilerini yazar.
  - Menfez sunum paftasını farklı ölçeklerde hazırlayabilir (genel yerleşim).
  - Kuyu tarfilerini içerir, var ise kuyular da 3D olarak çizilir, metraja eklenir.
  - Kesitte istenilen noktaya kot-mesafe  yazmak gibi basit araçlar içerisinde mevcuttur.




</div>


</div>





