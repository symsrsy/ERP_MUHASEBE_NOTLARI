# 1. Doğrudan Borçlandırma Sistemi (DBS)

DBS, ana firmanın bayilerle banka üzerinden yaptığı anlaşmalarla, satış sonrası bedelin doğrudan bayinin banka hesabından tahsil edildiği bir sistemdir.
İşleyiş:
• Ana firma, bayi ile çalıştığı bankada DBS protokolü imzalar.
• ERP sistemine bayinin DBS limiti tanımlanır.
• Bayi siparişi geçer → ürün gönderilir → fatura kesilir.
• Fatura bankaya iletilir → banka otomatik olarak tahsilat yapar.
• DBS limiti varsa sipariş geçilir, limit aşımı varsa sipariş ERP’de engellenir veya onaylı işlem gerektirir.
ERP’de:
• Logo’da: DBS entegrasyon modülü
• SAP’de: FI-AR modülü altında Bank Direct Debit işlevi ile entegre edilir.
• Cari kartlarda DBS limit tanımlanır ve sipariş anında kontrol edilir.
Kullanıldığı Sektörler:
• Hızlı tüketim (FMCG): Coca-Cola, Ülker, Nestle
• İlaç dağıtım zinciri
• Gıda dağıtımı
Avantajları:
• Tahsilat riski yok denecek kadar azdır.
• Otomatik süreç sayesinde insan hatası azalır.
• Tahsilat zamanlaması nettir → nakit akışı öngörülebilir.
Dezavantajları:
• Banka ile protokol zorunluluğu
• Her bayi için geçerli olmayabilir (kredi geçmişi kötü olanlar dışlanabilir)
• ERP ve banka entegrasyonu gerektirir (teknik maliyet)

# 2. Ön Ödemeli Bayi Sistemi (Avanslı Sistem)
Tanım:
Bayi, ERP sisteminde işlem yapmadan önce cari hesabına ödeme yapar (avans yatırır). Bu bakiye üzerinden sipariş geçebilir.
İşleyiş:
• Bayi önce ödeme yapar → ERP’de bakiyesi artar.
• Sipariş geçerken sistem bakiye kontrolü yapar.
• Sipariş → fatura → teslimat aşamaları, bakiye yetersizse engellenir.
ERP’de:
• Cari hesapta “alacak” oluşur.
• Sipariş sırasında “bakiye kontrolü” aktif edilir.
• Logo: Avans Fişi, Sipariş Bakiye Kontrolü
• SAP: Customer Advance olarak kaydedilir ve billing block ile siparişe bağlanabilir.
Kullanıldığı Sektörler:
• Eğitim, yazılım, danışmanlık
• Küçük tedarik zincirleri (büyük pazaryerleri hariç)
Avantajları:
• Firmanın finansal riski yoktur.
• Basit ERP süreçleriyle yönetilir.
• Bayinin ödeme gücüne göre işlem yapılır.
Dezavantajları:
• Bayi için işlem esnekliği düşer.
• Sürekli ödeme takibi gerekir.

# 3. Kredili Bayi Sistemi (Risk Limitli Sistem)
Tanım:
Firma, bayilere belirli bir kredi limiti tanımlar ve bu limit dahilinde ürün/hizmet verir.
İşleyiş:
• Cari karta risk limiti tanımlanır.
• Sipariş geçildiğinde bu limitten düşülür.
• Ödeme yapılmazsa yeni sipariş engellenir.
ERP’de:
• Logo: Cari Risk Limiti, Kredi Limiti Takibi
• SAP: Credit Management (FI-AR-CM)
• Satış siparişi sırasında limit kontrol edilir.
Kullanıldığı Sektörler:
• Otomotiv, beyaz eşya, mobilya
• Yapı malzemeleri ve bayilik sistemleri
Avantajları:
• Bayiye güven verici esneklik sağlar.
• Siparişler daha hızlı geçilebilir.
Dezavantajları:
• Tahsilat riski firmaya aittir.
• Geciken ödemelerde likidite sorunu doğabilir.

# 4. Teminatlı Bayi Sistemi (Senet/Çek Karşılığı Satış)
Tanım:
Bayiler, ürün tesliminden önce ya da teslim sırasında çek veya senet verir. Siparişler bu teminatlara karşılık olarak yapılır.
İşleyiş:
• Bayiden çek/senet alınır → ERP’ye tanımlanır.
• Sipariş, bu teminatlarla eşleştirilir.
• Vadesi geldiğinde ERP tahsilat hatırlatması yapar.
ERP’de:
• Logo: Çek-Senet Modülü
• SAP: Treasury (TRM) modülünde izlenebilir
• Teminat ve sipariş eşleştirme yapılır.
Kullanıldığı Sektörler:
• Müteahhitlik, yapı sektörü
• Orta-büyük ölçekli üretici firmalar
Avantajları:
• Nakit ihtiyacı doğmadan satış yapılabilir.
• Teminatla satış riski azalır.
Dezavantajları:
• Çek/senet riski (karşılıksız çıkabilir)
• Manuel takip yapılmazsa ERP’de açık fatura kalabilir.

# 5. Postpaid (Sonradan Ödemeli) Bayi Sistemi
Tanım:
Bayi, ürünleri alır, belirli vadeyle ödeme yapar. Siparişler ve teslimatlar ödeme alınmadan yapılır.
İşleyiş:
• Sipariş geçilir → teslimat yapılır → fatura kesilir.
• ERP’de tanımlı vade sonunda ödeme beklenir.
• Ödeme yapılmazsa yeni sipariş durdurulur.
ERP’de:
• Ödeme vadesi tanımı
• Fatura vade takibi
• Gecikme faizi otomatik olarak hesaplanabilir
Kullanıldığı Sektörler:
• Toptan ticaret, teknoloji ürünleri, tekstil
Avantajları:
• Bayi için büyük esneklik
• Firma için yüksek satış hacmi
Dezavantajları:
• Tahsilat riski yüksek
• ERP’de otomatik hatırlatmalar ve takip zorunlu

# 6. Ciro Bazlı Bayi Sistemi (Hedef/Prim Sistemi)
Tanım:
Bayi belli bir satış hacmine ulaştığında geri ödeme, iskonto, prim gibi avantajlar kazanır.
İşleyiş:
• ERP’de satış hedefi belirlenir.
• Belirli aralıklarla performans değerlendirmesi yapılır.
• Hedefe ulaşan bayiye indirim/prim iade edilir.
ERP’de:
• Satış raporları, bayi performans ekranları
• Kampanya/prim modülü
• Hedef – gerçekleşen karşılaştırma
Kullanıldığı Sektörler:
• Sigorta, kozmetik, elektronik perakende
Avantajları:
• Bayiyi satışa teşvik eder
• Sadakat sağlar
Dezavantajları:
• Hesaplamalar karmaşıktır, ERP’de iyi kurgulanmalıdır
• Yanlış prim hesaplamaları şirketi zarara uğratabilir

# 7. Tahsilat Şartlı Sipariş Sistemi
Tanım:
Sipariş verilir ancak tahsilat yapılmadan sevkiyat yapılmaz. ERP’de tahsilat koşulu aktif olarak bekletilir.
İşleyiş:
• Sipariş ERP’ye girilir.
• Sipariş onayı için muhasebe/finans onayı gerekir.
• Tahsilat yapıldığında sevkiyat onaylanır.
ERP’de:
• Sipariş blokajı, ödeme onayı ekranı
• Genellikle orta/küçük firmalarda manuel süreçle çalışır
Kullanıldığı Sektörler:
• Hizmet sektörü, birebir çalışan bayi yapıları
Avantajları:
• Firma riski sıfır
• Siparişleri sistemli şekilde bekletir
Dezavantajları:
• Süreç manuel takip gerektirir
• Bayi tarafında işlem hızı yavaşlar

# Bayi Ödeme Sistemleri Karşılaştırma Tablosu
| **Sistem**                | **Riski Kim Alır?**     | **ERP Zorluğu** | **Banka Gerektirir mi?** |
|---------------------------|--------------------------|------------------|----------------------------|
| **Doğrudan Borçlandırma (DBS)** | Banka / Firma paylaşır    | Yüksek           | Evet                       |
| **Ön Ödemeli (Avanslı Sistem)** | Bayi                     | Düşük            | Hayır                      |
| **Kredili Bayi Sistemi**        | Firma                    | Orta             | Hayır                      |
| **Teminatlı Bayi Sistemi**      | Firma                    | Orta             | Hayır                      |
| **Postpaid (Sonradan Ödemeli)** | Firma                    | Düşük            | Hayır                      |
| **Ciro Bazlı Bayi Sistemi**     | Firma (dolaylı risk)     | Yüksek           | Hayır                      |
| **Tahsilat Şartlı Sipariş**     | Bayi                     | Düşük            | Hayır                      |
> Not: ERP zorluğu; entegrasyon, otomasyon ihtiyacı ve süreç karmaşıklığına göre değerlendirilmiştir.
