Pixel-Based Manual Image Editor

This project is a desktop-based image processing application developed to extend the fundamental principles of digital image processing at both conceptual and practical levels. The most important feature of the project is that it is built entirely from scratch, without using high-level image processing libraries such as OpenCV or PIL.

The application treats digital images as M×N two-dimensional matrix structures (three-channel for color images), and all operations are performed directly on pixel intensity values (RGB) using low-level processing techniques.

🚀 Core Features

• From-Scratch Algorithm Development
All image processing operations (grayscale conversion, filtering, edge detection, etc.) are implemented manually without using built-in functions, using nested loops and custom models.

• Direct Pixel Manipulation
All operations are performed by directly accessing image matrix indices such as img[i][j]. NumPy is used only for data structure handling and basic memory management.

• Academic-Level Image Processing Techniques
Advanced techniques such as histogram stretching, double thresholding, and noise reduction are implemented to increase theoretical depth.

🛠️ Technologies Used
Programming Language: Python
Matrix Operations: NumPy (used only as a data structure)
GUI: Tkinter & CustomTkinter
Visualization: Matplotlib (for before/after comparisons)
I/O Operations: OpenCV (used only for image reading/writing; no high-level processing functions are used)

🧪 Implemented Algorithms

Basic and Geometric Transformations
Grayscale Conversion: A brightness (luminance) model is used to compute grayscale values for each pixel:
Gray = 0.299R + 0.587G + 0.114B

Geometric Transformations:
Manual rotation
Cropping
Scaling using nearest-neighbor interpolation (zoom in/out)

Filtering and Noise Reduction
Convolution Operation: Implemented manually using 3×3 kernel matrices.

Filtering Techniques:
Mean filter
Median filter
Salt-and-pepper noise reduction
Motion blur using a custom directional kernel matrix

Advanced Operations

Edge Detection: Edge components are extracted using gradient-based operators (Sobel-like masks).

Morphological Operations:
Dilation
Erosion
Opening
Closing

Histogram Stretching (Contrast Enhancement): Pixel values are linearly stretched based on the minimum and maximum intensity values in the image.

📊 System Architecture and Workflow

The application loads images selected by the user into NumPy arrays and performs each image processing step in a user-triggered manner.

To prevent UI freezing during computationally expensive operations (e.g., median filtering or edge detection), a multithreading structure is used.

📂 Data Management and Storage Structure

An Entity-Relationship (ER) model was designed to ensure traceability of processing steps within the system. This structure enables:

Tracking applied operations and their parameters
Storing kernel matrices for reproducibility
Ensuring full repeatability of processing pipelines

🔗 Download and Demo

The source code and executable version of the project can be accessed via the link below:

https://drive.google.com/file/d/1lFE_1vFKF1_B-u1IsTSI0ARfhJhFXAr0/view?usp=sharing

📌 Note

This work was developed for academic purposes. The main goal is to demonstrate that digital images are not only visual objects but also structured, processable digital data.

 **********
TÜRKÇE

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
