<img width="943" height="334" alt="image" src="https://github.com/user-attachments/assets/4f75c3b5-cfd4-40e0-81da-1b7d5a1a8c74" /># covid19-misinfo-sna
🧠 COVID-19 Misinformation Network Analysis

Bu proje, COVID-19 ile ilgili Twitter verileri üzerinden yanlış ve doğru bilgi yayılımının sosyal ağ analizini amaçlamaktadır. Heterojen bir ağ yapısı kurulmuş, kullanıcılar, tweetler ve hashtag'ler gibi farklı türde düğümler kullanılmıştır.

📁 Veri Seti Özeti

Kullanılan veri: Covid-19 Twitter Dataset (Apr-Jun 2020).csv

Kullanılan sütunlar:

clean_tweet: Temizlenmiş tweet metni

original_author: Tweet’i atan kullanıcı

user_mentions: Mention edilen kullanıcı(lar)

hashtags: Tweet’te geçen hashtag’ler

retweet_count, favorite_count: Etkileşim metrikleri

created_at: Zaman bilgisi

pred_label: Model tarafından tahmin edilen bilgi türü (fake / real)

pred_prob_real: Tahminin doğruluğu (olasılık değeri)

Tweet’ler, daha önce eğitilen bir model ile fake ya da real olarak etiketlenmiştir.

🌐 Heterojen Ağ Yapısı

Bu analizde farklı tipte düğüm ve kenarlar içeren bir ağ kurulmuştur. Aşağıda tanımlanan yapı bu ağın temelini oluşturur:

<img width="943" height="334" alt="image" src="https://github.com/user-attachments/assets/99253059-f8cf-4dbb-aa45-a0ad39daabee" />

🔷 KENARLAR
<img width="922" height="409" alt="image" src="https://github.com/user-attachments/assets/01a08768-4335-4af6-8f4e-413dac0ccdc8" />

📊 Yapılabilecek Ağ Analizi Türleri
1. Ağ Ölçümleri
Mikro Ölçümler

Derece (Degree)

Yerel Öbeklenme Katsayısı (Clustering Coefficient)

Düğüm Merkeziliği (Node Centrality)

Makro Ölçümler

Derece Dağılımı

Yol Uzunluğu ve Çap (Diameter)

Bağlantı Yoğunluğu (Density)

Global Öbeklenme Katsayısı

Orta Ölçümler

Bağlı Bileşenler (Connected Components)

Dev Bileşen (Giant Component)

Grup Merkeziliği

Komüniteler (Community Detection)

2. Kümelenme Analizi

Kümelenme Katsayısı

Komünite Algoritmaları: Louvain, k-core, k-clique, k-club

3. Merkezilik Ölçümleri

Derece Merkeziliği (Degree Centrality)

Yakınlık Merkeziliği (Closeness Centrality)

Arasındalık Merkeziliği (Betweenness Centrality)

4. Diğer Ağ Analizleri

Asortatif Karma (Assortative Mixing)

Yapısal Eşdeğerlik: Jaccard Benzerliği, Kosinüs Benzerliği

PageRank

5. Link Analizi

HITS

PageRank

SimRank

DivRank

PathSim

🧠 Etiketleme Süreci

Veride doğrudan fake/real etiketleri bulunmadığından dolayı, ayrı bir veri seti ile eğitilen makine öğrenmesi modeli ile içerikler otomatik olarak etiketlenmiştir. pred_label sütunu bu tahminleri göstermektedir.

🔧 Kullanım
# repoyu klonlayın
git clone https://github.com/kullaniciadi/misinfo-net-analysis.git

# ortamı oluşturun ve bağımlılıkları yükleyin
pip install -r requirements.txt

