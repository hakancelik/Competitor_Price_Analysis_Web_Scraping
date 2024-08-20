# Web Kazıma ile Rakip ve Fiyat Analizi

Bu proje, **Travel** ve **Nonfiction** kitap kategorilerindeki ürünlerin verilerini kazıyıp analiz etmek için hazırlanmıştır. **Selenium** ve **BeautifulSoup** kütüphaneleri kullanılarak **books.toscrape.com** sitesinden veri kazınmıştır. Proje, kitapların fiyatlarını, yıldız derecelendirmelerini ve diğer bilgilerini analiz etmek için kullanılır.

## İçindekiler

1. [Proje Hedefi](#proje-hedefi)
2. [Kurulum](#kurulum)
3. [Kullanım](#kullanım)
4. [Kod Açıklamaları](#kod-açıklamaları)
5. [Görselleştirme](#görselleştirme)
6. [Yazarlar](#yazarlar)
7. [Lisans](#lisans)

## Proje Hedefi

Bu projede, **Travel** ve **Nonfiction** kitap kategorilerindeki kitapların detaylarını kazıyıp, fiyat ve yıldız derecelendirmeleri ile ilgili analizler yapılacaktır. Elde edilen verilerle çeşitli grafikler oluşturulacak ve analizler yapılacaktır.

## Kurulum

Projenin çalışabilmesi için gerekli olan kütüphaneleri yüklemek gerekmektedir. Aşağıdaki komutları kullanarak gerekli kütüphaneleri yükleyebilirsiniz:

```bash
pip install selenium beautifulsoup4 pandas matplotlib seaborn
```

Ayrıca, ChromeDriver uygulamasını indirip bilgisayarınıza uygun bir yere yerleştirmeniz gerekmektedir. ChromeDriver'ın yolunu setup_driver fonksiyonundaki executable_path değişkenine girin.

## Kullanım

### Tarayıcıyı Başlatma ve Konfigüre Etme
Tarayıcıyı başlatın ve gerekli ayarları yapın.

### Ana Sayfayı İnceleme ve Kategori Linklerini Çıkarma
Ana sayfayı açın ve "Travel" ve "Nonfiction" kategorilerinin bağlantılarını kazıyın.

### Kategori Sayfasını İnceleme ve Kitap Linklerini Çıkarma
Her kategori sayfasında kitapların detay sayfalarına giden bağlantıları alın. Sayfalandırmayı yöneterek tüm kitapların linklerini çıkarın.

### Ürün Detay Sayfasını İnceleme ve Verileri Çıkarma
Her kitap detay sayfasına gidin ve kitap adı, fiyat, yıldız sayısı, açıklama ve ürün bilgilerini kazıyın.

### Verileri Analiz Etme ve Görselleştirme
Elde edilen verileri bir pandas DataFrame'e dönüştürün ve çeşitli grafiklerle analiz edin.

### Tarayıcıyı Kapatma
Tüm işlemler tamamlandıktan sonra tarayıcıyı kapatın ve kaynakları serbest bırakın.

## Kod Açıklamaları

Proje, aşağıdaki temel işlevlere sahip Python kodlarından oluşur:

- `setup_driver()`: Tarayıcıyı konfigüre eder ve başlatır.
- `get_category_urls(driver)`: Kategori sayfalarının URL'lerini çıkarır.
- `get_book_urls(driver, category_url, max_pagination=3)`: Kategori sayfasındaki kitapların detay URL'lerini çıkarır.
- `get_book_details(driver, book_url)`: Bir kitap detay sayfasından bilgileri kazır.
- `scrape_books(driver)`: Tüm kitapları kazır ve verileri toplar.
- `visualize_data(df)`: Elde edilen verileri analiz eder ve görselleştirir.

## Görselleştirme

Projede elde edilen verilerle aşağıdaki görselleştirmeler yapılır:

- **Kitap Fiyatları ve Yıldız Derecelendirmeleri**: Fiyatlar ile yıldız derecelendirmeleri arasındaki ilişkiyi gösterir.
- **Fiyat Dağılımı**: Fiyatların kategorilere göre dağılımını gösterir.
- **Yıldız Derecelendirme Dağılımı**: Yıldız derecelendirmelerinin dağılımını gösterir.

## Yazarlar

- Hakan Çelik - Proje Yöneticisi ve Geliştirici

## Lisans

Bu proje MIT Lisansı altında lisanslanmıştır. Daha fazla bilgi için LICENSE dosyasına bakabilirsiniz.
