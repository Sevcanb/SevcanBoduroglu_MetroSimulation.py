Sürücüsüz Metro Simülasyonu (Rota Optimizasyonu)

Proje Açıklaması

Bu proje, bir metro ağı üzerinde iki istasyon arasındaki en hızlı ve en az aktarmalı rotayı bulmak için tasarlanmış bir simülasyondur. Proje, BFS (Breadth-First Search) ve A algoritmalarını* kullanarak en iyi rotayı belirlemektedir.

Kullanılan Teknolojiler ve Kütüphaneler

Python 3.x (Temel programlama dili)

collections.deque (BFS algoritması için kuyruk yapısı)

heapq (A* algoritması için öncelik kuyruğu)

typing (Tip belirleme için)

Algoritmaların Çalışma Mantığı

BFS Algoritması (En Az Aktarmalı Rota)

Mantık:

Genişlik öncelikli arama (BFS) kullanarak istasyonlar arasındaki en az aktarmalı rotayı bulur.

Kuyruk (deque) kullanarak istasyonları ziyaret eder.

Ziyaret edilen istasyonlar takip edilir ve ilk ulaşılan hedef en kısa yol olur.

A* Algoritması (En Hızlı Rota)

Mantık:

Öncelikli kuyruk (heapq) kullanarak en hızlı rotayı bulur.

Toplam süre hesaplanarak en düşük maliyetli rota seçilir.

Hedefe en hızlı ulaşan rota tercih edilir.

Kullanım Örneği

metro = MetroAgi()
metro.istasyon_ekle("K1", "Kızılay", "Kırmızı Hat")
metro.istasyon_ekle("K2", "Ulus", "Kırmızı Hat")
metro.baglanti_ekle("K1", "K2", 4)

rota = metro.en_az_aktarma_bul("K1", "K2")
print("En az aktarmalı rota:", " -> ".join(i.ad for i in rota))

Test Sonuçları

Projede test senaryoları ile çalışma doğrulanmıştır:

AŞTİ -> OSB

Batıkent -> Keçiören

Keçiören -> AŞTİ

Test sonuçları başarılı şekilde alınmış ve algoritmalar doğru çalışmıştır.
