# CNC_XY_Integrated_Ventilation

❮img src="Mechanic_60x100/Media/Perspective.png" width="600" ❯
Kapalı ve kısıtlı alanda diyot lazer işlemleri gerçekleştirilebilmesi esas alınarak tasarlandı. 

❮img src="Mechanic_60x100/Media/DevicesPerspective.png" width="400" ❯
Çalışması için, ihtiyaç duyduğu tüm materyalleri bütün olarak üzerinde barındırması,
Üzerinde bütünleşik bulunan ızgara ile, hava akımı yönlendirilmesi yanısıra, bal peteği ihtiyacının karşılanması,
Parça aydınlatma şiddeti, Havalandırma akış hızı, kompresör hava akış hız kontrolcüleri bulunması,
Tüm elektronik kontrolcülerin manuel ve ayrık yönetilmesi yanısıra, operasyonla birlikte de otomatik olarak bütünleşik çalışabilmesi,
Standart çalışma masası üzerinde, güç soketi ve havalandırma borusu takılmasına takriben kullanıma hazır olması,
Üretime uygunluğu ve mekanik dayanımı belirgin niteliklerdir.

Mekanik tasarımlar için FreeCad, Elektronik tasarımlar için ise Kicad, tamamen ücretsiz tasarım programları kullanılarak gerçekleştirildi.

❮img src="Mechanic_60x100/Media/DynamicData.png" width="200" ❯
CNC Mekanik boyutlar CNC_XY.FCStd dosyası ana sekmede dd (dynamic data) içerisinde ddSigmaX ve ddSigmaY değişkenleri üzerinden güncellenebilmektedir.
Bu değişkenler tasarımda bulunan x ve y eksenlerinde ki sigma profillerin birebir boylarına eştir. Sigma boylarına bağlı olan tüm parçalar otomatik güncellenecektir.
Bu durumda dikkat edilmesi gereken husus, büküm yapılacak metal parçalarda değişiklik meydana geldiğinge, üretime ilişkin  lazer kesim ve büküm rehberleri,
"./pr_.." dosyaları da ayrıca açılarak el ile güncellenmelidir. 3 boyutlu parçanın lazer kesime ve büküm rehberine uygunluğu için, 
yeniden "unfold" işlemi gerçekleştirilir. Yeniden meydana gelen kesim ve büküm eskiz'leri ilgili parçanın alanına sürüklenir. 
Teknik çizim dosyalarında, view sekmeleri içerisinde, ilişik olduğu eskiz ler, XSource properties üzerinden kesim ve büküm sıralaması ile güncellenir. 
Eski kesim ve büküm eskizleri silinebilir. Bazı durumda teknik çizimde ki ölçü belirteçleri de yeniden belirtilmesi gerekebilmektedir.

❮img src="Mechanic_60x100/Media/DynamicDataMove.png" width="200" ❯
ddmove değişkenleri ile lazer hareket ettirilebilir. Sigma boyları ve diğer parametreler değerlendirilerek çalışma alanı otomatik hesaplanır, 
sonuç değerleri ddLimitX ddLimitY parametrelerinde görülür.

❮img src="HW/MSConn/Media/MSConn_Diagram.png" width="600" ❯
Elektriksel bağlantılar, Diyagram takip edilerek gerçekleştirilebilir. Diyagram MSConn board içerisinde tasarlandı, kicad projesi üzerinden detaylı incelenebilir.
❮img src="HW/MSConn/Media/MSConn_PerspectiveFront.png" width="200" ❯ ❮img src="HW/MSConn/Media/MSConn_PerspectiveRear.png" width="200" ❯

Üretim için öncelikle BOM dosyası incelenebilir.
Satın alınması gerekli materyallerin, satın alma linkleri ve yaklaşık fiyatlandırmaları Dolar cinsinde görülebilir.
1. sayfada genel toplam ve alt sayfaların sonuç fiyatlandırmaları görülmektedir.
2. sayfada Aygıt kutusu içerisinde kullanılan satın alınması gerekli parçalar görülmektedir.
3. sayfada satın alınması gerekli mekanik parçalar görülmektedir.
4. sayfada Projeye özgün metal parçaların üretilmesi için metal kesim, metal büküm listesi görülmektedir. 
    Dosya isimlerinden, metal kesimde kullanılacak materyalin cinsi ve kalınlığı anlaşılmaktadır.
    İhtiyaç duyulan kesim dosyaları, büküm rehberleri ve diş açma rehberleri "./Mechanic_60x100/Production_.." klasörlerinde bulunabilir.
5. sayfada "Multi Speed Controller and Connections" kartının üretiminde kullanılacak elektronik komponentlerin listesi bulunmaktadır.
    PCB üretiminde ihtiyaç duyulacak gerber dosyası "./HW/MSConn/FabOut_MSConn.zip" bulunabilir. 
    PCB Prototiplemede kullanılmak üzere detaylı MSConn bom listesi "./HW/MSConn/bom/ibom_MSConn.html"bulunabilir.
    Kart üzerinde konnektör pin isimleri anlamları ile birlikte yazmaktadır.


