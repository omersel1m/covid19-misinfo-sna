# covid19-misinfo-sna
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

🔶 DÜĞÜMLER
Tür	Kaynak Sütun	Açıklama
Kullanıcı	original_author, user_mentions	Tweet atan ve mentionlanan kişiler
Tweet	clean_tweet	Her tweet potansiyel düğüm
Hashtag	hashtags	İçerikte kullanılan hashtag'ler
Bilgi Türü	pred_label (özellik olarak)	Tweet’in yanlış veya doğru bilgi taşıması
🔷 KENARLAR
Tür	Açıklama
Kullanıcı → Tweet	Tweet atan kişi ile tweet arasında
Kullanıcı → Kullanıcı	Mention ilişkisi
Tweet → Hashtag	Tweet ile hashtag arasındaki bağlantı
Kullanıcı → Hashtag	Kullanıcının belirli bir hashtagi kullanması
Tweet → Tweet (opsiyonel)	Benzer içerikli tweet’ler arası içerik benzerliği bağlantısı
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

