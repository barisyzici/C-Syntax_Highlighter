# 🖥️ Real-Time C Syntax Highlighter & Parser

Bu proje, C diline özel gerçek zamanlı sözdizimi ve sözcüksel analiz yapan bir web uygulamasıdır. Kullanıcı arayüzü üzerinden yazılan C kodları anlık olarak renklendirilir ve hatalar gösterilir.

Projeye ulaşmak için [tıklayınız.](https://barisyzici.github.io/C-Syntax_Highlighter/)

## 🚀 Özellikler

- Gerçek zamanlı sözdizimi analizi (Top-Down Parser)
- Token bazlı sözcüksel analiz (Lexical Analyzer)
- C diline özgü renklendirme (highlighting)
- Hatalı ifadelerin anında tespiti ve uyarı gösterimi
- Karanlık tema ile sade ve modern arayüz

## 📚 Teknik Detaylar

### ✅ Kullanılan Gramer

Uygulama, aşağıdaki C yapılarının analizini desteklemektedir:

- Değişken tanımlamaları (`int`, `float`, `char`)
- Kontrol yapıları (`if`, `else`, `while`)
- Fonksiyon tanımları (`void`, `return`)
- Struct tanımları (`struct`)
- Atama ve işleçler (`=`, `+`, `-`, `*`, `/`)

### 🧠 Sözdizimi Analizi

Kod, satır satır analiz edilerek yapısal kontrol yapılır. Her yapı için özel tanımlanmış parse fonksiyonları vardır:

```js
function parseStatement(tokens) {
    // token dizisini analiz eder
}
```

Bu sistem top-down bir yaklaşım kullanır; yani kod yukarıdan aşağı doğru, blok blok analiz edilir.

### 🧩 Sözcüksel Analiz

JavaScript kullanılarak, regex tabanlı bir tokenizer tasarlanmıştır. Her kelime (token), aşağıdaki türlerden biri olarak sınıflandırılır:

- `keyword` → Örn: `int`, `if`, `return`
- `identifier` → Değişken/fonksiyon adları
- `operator` → Örn: `=`, `+`
- `number` → Sayılar
- `string` → Tırnak içi ifadeler
- `comment` → `//` ile başlayan satırlar
- `error` → Hatalı yapılar

### 🎨 Vurgulama Kuralları

Her token, HTML içinde `span` etiketiyle sarılır ve CSS sınıfına göre renklendirilir.

| Token Türü   | Renk          |
|--------------|---------------|
| `keyword`    | Mor           |
| `number`     | Açık yeşil    |
| `identifier` | Mavi          |
| `operator`   | Gri           |
| `string`     | Turuncu       |
| `comment`    | Yeşil italik  |
| `error`      | Kırmızı arka  |

## 🖼️ Arayüz & Gerçek Zamanlı İşleyiş

- Kullanıcı bir `textarea` içinde kod yazar.
- Her tuş vuruşunda `parse()` ve `tokenize()` fonksiyonları tetiklenir.
- Kod, eş zamanlı olarak analiz edilir ve `div` içinde renklendirilmiş biçimde gösterilir.
- Hatalı yapılar kırmızı ile vurgulanır.

## 🧪 Demo

### 🎬 Video Gösterimi

Projeyi canlı izlemek için kısa demo videosunu izleyin:  
🔗 [Demo Videosu](https://www.youtube.com/watch?v=0vyxMH5l6Kc)

### 📖 Makale

Projenin detaylı çözüm sürecini ve tasarım kararlarını anlattığım yazıya göz atın:  
📝 [Makale Bağlantısı](https://link_to_your_article)

## 📂 Proje Yapısı

```
project-root/
├── index.html
└── README.md
```

## 🛠️ Kullanılan Teknolojiler

- **HTML5 / CSS3 / JavaScript**
- Basitleştirilmiş **C Grameri**
- `RegExp` tabanlı Tokenizer
- Custom Top-Down Parser

## ⚠️ Bilgilendirme

Bu uygulama, C dilinin **tam gramerini** değil, temel yapılarını analiz etmektedir. Geniş kapsamlı C desteği için özel parser kütüphaneleri önerilir.
