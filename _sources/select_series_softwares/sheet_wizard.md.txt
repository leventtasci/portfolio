# Pafta Sihirbazı

<div style="overflow: auto;">

  <img src="../_static/sheet_wizard_ui1.png" alt="Section Wizard UI" style="float: left; margin-right: 20px; margin-top: 5px; padding-right: 10px; max-width: 45%; height: auto;">

  
<div style="text-align: justify;">

<h2 style="margin-top: 0;">Tespitler</h2>

  - İyi bir mühendislik çalışmasının ardından hazırlanmış hata barındıran yaprak paftalar, o işe harcanmış mühendislik hizmetinin de sorgulanmasına sebep olabilir.
  - Yaprak pafta oluşturma ve detay işleme süreçlerini Excel ile kontrol ederek yürüten,  verilerden giderek sunum paftalarını yaratabilen yaygın bir yazılım bulunmamaktadır. Inroads’ta Plan-Profile Generator bölümünden de toplu olarak KGM formatında bir sonuç almak mümkün değildir.
  - Çizim hata denetimlerini aramak, verilerde hataları aramaktan daha zordur. Pafta Sihirbazı buradan yola çıkarak, “tutarlı bir veri grubundan tutarlı paftalar oluşturulabilir” ana fikri ile türetilmiştir.

 

  ## Başardıkları

Pafta Sihirbazı, iki ana birimden oluşur: ilki yaprak paftaları excel vasıtasi ile oluşturan ve  detaylarını işleyen Pafta Yaratıcı’dır. İkinci birim ise yaprak paftalarda profil bölümüne işlenen çizgisel bilgileri ve yaprak pafta ortasındaki şevlerle ilgili bantları işleyen Pafta Detayları birimidir

  <img src="../_static/sheet_wizard_ui2.png" alt="Section Wizard UI" style="float: left; margin-right: 20px; margin-top: 5px; padding-right: 10px; max-width: 45%; height: auto;">

## Öne Çıkan Özellikleri

  - Paftalar yaratılırken plan çerçevesinin içerisinde kalan bölgeye karelajlar otomatik işlenir: pafta sihirbazı kendi içerisinde projenin dilim orta meridyenine göre Helmert dönüşümünü kendisi yapar ve ED50 gridleri de çizer. (Buradaki amaç projenin kendine özgü dönüşüm parametrelerinin yokluğunda global dönüşümü yaparak ED50 gridleri çizdirmektir.)
  - Paftalar oluşturulurken otomatik olarak:
  - Pafta kuzey belirteci,  
  - Plan ileri ve geri yönleri
  - Pafta antet bilgileri (proje adı, pafta no vb.)
  - Pafta kilometrajı
işlenir. Kullanıcı pafta cell’inde (örneğin A1) ve excel dosyasında, pafta antet bilgileri ile pafta kilometrajını adresler, bilgiler bu konumlara yazılır. Bu durum, tek tip KGM formatı haricinde, yapım proje işlerindeki değişik formatlı paftaların üretimine de imkan verir: Örneğin A4 antetli plan-profil paftalarının üretiminde, doğru adreslerin tarifi ile antet ve pafta bilgileri otomatik olarak doldurulur.
  - Bilindiği üzere, proje akışı içerisinde tamamlanmış hemen hemen tüm çalışmalar  (duvar, yeraltı drenajı, şev eğimi, palye poligon vb.), KGM projelerinde yaprak paftalara işlenmektedir. Pafta Sihirbazı’na ait Pafta Detayları birimi, bu listelerdeki tüm bilgileri excel’den okuyarak paftalara işler. Böylece, projenin seyri sırasında düzgün arşivlenen listeler, çizime kendiliğinden aktarılmış olur. İlave kontroller gerekmez, yalnızca çakışabilecek yazıların kontrolünün ardından çizim çalışmaları tamamlanmış olur.


## Geliştirici Notları

Pafta Detayları birçok KGM projesinde kullanımıştır, Pafta Yaratıcı ise henüz bir projede kullanılmıştır. Pafta Sihirbazı’nın bir paket olarak gelişme süreci devam etmektedir.

</div>


</div>



