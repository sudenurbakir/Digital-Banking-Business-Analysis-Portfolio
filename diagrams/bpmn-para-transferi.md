# BPMN - Para Transferi Süreci

## Amaç

Bu diyagram, mobil bankacılık uygulamasındaki para transferi sürecinin uçtan uca iş akışını görselleştirmek amacıyla hazırlanmıştır.

---

## Süreç Akışı

```mermaid
flowchart LR

A([Başlangıç])

B[Mobil Bankacılık Uygulamasına Giriş Yap]

C[Para Transferi Menüsünü Aç]

D[Transfer Türünü Seç]

E[IBAN veya Kayıtlı Alıcı Seç]

F[Transfer Tutarını Gir]

G[İşlem Özetini Görüntüle]

H{Bilgiler Doğru mu?}

I[İşlemi Düzenle]

J[Güvenlik Doğrulaması]

K{Doğrulama Başarılı mı?}

L[Transferi Gerçekleştir]

M[Referans Numarasını Oluştur]

N[Başarı Mesajını Göster]

O([Bitiş])

A --> B
B --> C
C --> D
D --> E
E --> F
F --> G
G --> H

H -- Hayır --> I
I --> E

H -- Evet --> J

J --> K

K -- Hayır --> G

K -- Evet --> L

L --> M
M --> N
N --> O
```

---

## Süreç Açıklaması

1. Kullanıcı mobil bankacılık uygulamasına giriş yapar.
2. Para transferi ekranını açar.
3. Transfer türünü belirler.
4. Alıcı bilgilerini girer veya kayıtlı alıcı seçer.
5. Transfer tutarını girer.
6. İşlem özetini kontrol eder.
7. Güvenlik doğrulamasını tamamlar.
8. Sistem transfer işlemini gerçekleştirir.
9. Referans numarası oluşturulur.
10. İşlem başarıyla tamamlanır.

---

## Notlar

- Bu diyagram hedeflenen (To-Be) süreci temsil etmektedir.
- Süreç, kullanıcı deneyimini iyileştirmek amacıyla tasarlanmıştır.
- İş kuralları ve fonksiyonel gereksinimler dikkate alınarak hazırlanmıştır.
