# Fonksiyonel Gereksinimler (Functional Requirements)

## Amaç

Bu doküman, mobil bankacılık uygulamasındaki para transferi sürecine ait fonksiyonel gereksinimleri tanımlamak amacıyla hazırlanmıştır. Fonksiyonel gereksinimler, sistemin kullanıcıdan gelen isteklere nasıl yanıt vereceğini ve hangi işlevleri yerine getireceğini açıklamaktadır.

---

## Fonksiyonel Gereksinimler

| ID | Gereksinim | Öncelik |
|----|------------|----------|
| FR-001 | Sistem, kullanıcının FAST, EFT veya Havale transfer türlerinden birini seçmesine izin vermelidir. | Yüksek |
| FR-002 | Sistem, girilen IBAN bilgisinin formatını işlem öncesinde doğrulamalıdır. | Yüksek |
| FR-003 | Sistem, kayıtlı alıcı listesinden seçim yapılmasına izin vermelidir. | Yüksek |
| FR-004 | Sistem, QR Kod ile para transferini desteklemelidir. | Orta |
| FR-005 | Sistem, transfer tutarının geçerli limitler içerisinde olup olmadığını kontrol etmelidir. | Yüksek |
| FR-006 | Sistem, işlem özeti ekranını kullanıcıya göstermelidir. | Yüksek |
| FR-007 | Sistem, transfer işlemi öncesinde güvenlik doğrulaması istemelidir. | Yüksek |
| FR-008 | Sistem, başarılı işlemlerde referans numarası oluşturmalıdır. | Orta |
| FR-009 | Sistem, işlem sonucunu kullanıcıya açık ve anlaşılır bir şekilde göstermelidir. | Yüksek |
| FR-010 | Sistem, tamamlanan transfer işlemini işlem geçmişine kaydetmelidir. | Yüksek |

---

## Fonksiyonel Gereksinimlerin Kapsamı

Bu gereksinimler aşağıdaki modülleri kapsamaktadır:

- Para Transferi
- Hesap Bilgileri
- İşlem Geçmişi
- Güvenlik Doğrulama
- Bildirim Yönetimi

---

## Bağımlılıklar

Fonksiyonel gereksinimlerin doğru şekilde çalışabilmesi için aşağıdaki sistem bileşenleriyle entegrasyon gereklidir:

- Kimlik Doğrulama Servisi
- Bankacılık Çekirdek Sistemi
- SMS / Mobil Onay Servisi
- Bildirim Servisi

---

## Sonuç

Bu dokümanda tanımlanan fonksiyonel gereksinimler, yazılım geliştirme sürecinde geliştirilecek özelliklerin temelini oluşturacaktır. Geliştirme, test ve kullanıcı kabul süreçleri bu gereksinimler doğrultusunda yürütülecektir.
