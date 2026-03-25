Piksel Tabanlı Manuel Görüntü Editörü

Bu proje, dijital görüntü işlemenin temel prensiplerini kavramsal ve uygulamalı düzeyde incelemek amacıyla geliştirilmiş, masaüstü tabanlı bir görüntü işleme uygulamasıdır. Projenin en önemli özelliği, OpenCV, PIL gibi yüksek seviyeli görüntü işleme kütüphanelerinin hazır fonksiyonları kullanılmadan tamamen sıfırdan geliştirilmiş olmasıdır.

Uygulama, dijital görüntüleri M×N boyutlu iki boyutlu (renkli görüntüler için üç kanallı) matris yapıları olarak ele almakta ve tüm işlemleri piksel yoğunluk değerleri (RGB) üzerinde doğrudan matematiksel işlemlerle gerçekleştirmektedir.

🚀 Temel Özellikler

• Sıfırdan Algoritma Geliştirme
Görüntü işleme süreçlerinin tamamı (gri seviye dönüşümü, filtreleme, kenar belirleme vb.) hazır fonksiyonlar kullanılmadan, iç içe döngüler (nested loops) ve matematiksel modeller aracılığıyla manuel olarak gerçekleştirilmiştir.

• Doğrudan Piksel Manipülasyonu
Tüm işlemler, görüntü matrisine ait img[i][j] indisleri üzerinden doğrudan erişim sağlanarak yürütülmüştür. NumPy yalnızca veri yapısı oluşturma ve temel bellek yönetimi amacıyla kullanılmıştır.

• Akademik Düzeyde Görüntü İşleme Teknikleri
Histogram germe, çift eşikleme (double thresholding) ve gürültü azaltma gibi ileri seviye teknikler uygulanarak projenin teorik derinliği artırılmıştır.

🛠️ Kullanılan Teknolojiler
Programlama Dili: Python
Matris İşlemleri: NumPy (yalnızca veri yapısı olarak)
Grafik Arayüz: Tkinter & CustomTkinter
Görselleştirme: Matplotlib (önce/sonra karşılaştırmaları için)
Girdi/Çıktı İşlemleri: OpenCV (yalnızca görüntü okuma/yazma işlemleri için; yüksek seviyeli fonksiyonlar kullanılmamıştır)
🧪 Gerçekleştirilen Algoritmalar
1. Temel ve Geometrik Dönüşümler

Gri Seviye Dönüşümü:
Parlaklık (luminance) modeli kullanılarak her piksel için gri değer hesaplanmıştır:
Gray=0.299R+0.587G+0.114B
Geometrik Dönüşümler:
Manuel döndürme (rotation)
Görüntü kırpma (cropping)
Nearest neighbor interpolasyonu ile ölçekleme (zoom in/out)
2. Filtreleme ve Gürültü Azaltma
Konvolüsyon İşlemi:
3×3 çekirdek (kernel) matrisleri kullanılarak manuel olarak uygulanmıştır.
Filtreleme Teknikleri:
Mean (ortalama) filtresi
Median (ortanca) filtresi
Salt & Pepper gürültü azaltma
Motion Blur:
Belirli bir yön doğrultusunda oluşturulan özel kernel matrisi ile hareket bulanıklığı efekti uygulanmıştır.
3. İleri Seviye İşlemler
Kenar Belirleme:
Gradyan tabanlı operatörler (Sobel benzeri maskeler) kullanılarak kenar tespiti yapılmıştır.
Morfolojik İşlemler:
Genişleme (Dilation)
Aşınma (Erosion)
Açma (Opening)
Kapama (Closing)
Histogram Germe (Contrast Stretching):
Görüntüdeki minimum ve maksimum piksel değerleri belirlenerek dinamik aralık lineer olarak genişletilmiştir.

📊 Sistem Mimarisi ve Çalışma Akışı

Uygulama, kullanıcı tarafından seçilen görüntüyü NumPy dizisi olarak belleğe alır ve her bir görüntü işleme adımı kullanıcı tetiklemeli olarak gerçekleştirilir.

Hesaplama maliyeti yüksek işlemler (örneğin median filtreleme veya kenar belirleme) sırasında kullanıcı arayüzünün donmasını engellemek amacıyla çok iş parçacıklı (multithreading) yapı kullanılmıştır.

📂 Veri Yönetimi ve Kayıt Yapısı

Sistem içerisinde gerçekleştirilen işlemlerin izlenebilirliğini sağlamak amacıyla bir ER (Entity-Relationship) modeli tasarlanmıştır. Bu yapı sayesinde:

Uygulanan işlemler
Kullanılan parametreler (örneğin eşik değeri T) Kernel (çekirdek) matrisleri kayıt altına alınarak süreçlerin tekrar üretilebilirliği sağlanmıştır.

🔗 İndirme ve Demo

Projenin kaynak kodlarına ve çalıştırılabilir sürümüne aşağıdaki bağlantı üzerinden erişilebilir:

https://drive.google.com/file/d/1lFE_1vFKF1_B-u1IsTSI0ARfhJhFXAr0/view?usp=sharing

📌 Not

Bu çalışma akademik amaçlı geliştirilmiştir. Temel hedef, dijital görüntülerin yalnızca görsel bir yapı değil, aynı zamanda işlenebilir bir sayısal veri kümesi olduğunu göstermektir.
