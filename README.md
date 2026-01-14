# envanter_dedektifi
# 🕵️ Envanter Dedektifi  
### Multimodal AI Agent for Smart Inventory & Stock Management

**Envanter Dedektifi**, depo ve stok yönetiminde sıkça karşılaşılan  
*“Bu ürün neredeydi?”*, *“Hangi kutuda olabilir?”* gibi soruları çözmek için geliştirilmiş  
**çok modlu (multimodal) bir yapay zeka ajanıdır**.

Bu proje; görsel algı, mantık yürütme, bağlamsal hafıza, yapılandırılmış veri doğrulama ve sesli yanıt bileşenlerini  
**tek bir uçtan uca sistem** içerisinde birleştirir.

---

## 🚀 Temel Özellikler

- 📷 **Görsel Tanıma (Vision)**  
  Ürün fotoğrafını analiz ederek marka/model seviyesinde ürün tespiti yapar.

- 🧠 **Akıl Yürütme & RAG (Reasoning + Knowledge Base)**  
  Tespit edilen ürünü yerel envanter bilgileriyle karşılaştırır ve mantık yürüterek en olası eşleşmeyi bulur.

- 🗂️ **Depo / Raf / Kutu Eşleştirme**  
  Ürünün fiziksel lokasyonunu net bir şekilde belirtir.

- 💬 **Hafızalı Sohbet (Context Management)**  
  Önceki soruları hatırlayarak çok adımlı bir diyalog kurar.

- 🧾 **Yapılandırılmış Çıktı (Pydantic)**  
  Model yanıtlarını tip güvenli ve doğrulanmış veri yapılarıyla işler.

- 🔊 **Sesli Yanıt (Text-to-Speech)**  
  Nihai cevabı sesli asistan çıktısı olarak sunar.

- 🖥️ **Ürün Benzeri Arayüz (Streamlit)**  
  Geliştirici modu (debug) ve kullanıcı modu ayrımıyla temiz bir deneyim sağlar.

---

## 🧠 Sistem Mimarisi (Özet)

```text
Kullanıcı
   │
   ├─► Ürün Görseli
   │     └─► Vision Model (Ürün Tespiti)
   │
   ├─► Kullanıcı Sorusu
   │     └─► Reasoning Model + Yerel Bilgi Tabanı (RAG)
   │
   ├─► Yapılandırılmış Yanıt (Pydantic)
   │
   └─► Metin + Sesli Yanıt (TTS)
