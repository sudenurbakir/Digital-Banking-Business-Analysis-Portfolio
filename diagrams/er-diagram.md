# ER Diagram - Dijital Bankacılık Para Transferi

## Amaç

Bu doküman, dijital bankacılık uygulamasındaki para transferi modülünde kullanılan temel veri varlıklarını (Entity) ve bu varlıklar arasındaki ilişkileri göstermektedir.

## Kapsam

Bu diyagram aşağıdaki veri yapısını kapsamaktadır:

- Müşteri bilgileri
- Banka hesapları
- Para transferleri
- Kayıtlı alıcılar
- QR Kod bilgileri
- İşlem dekontları

---

# Varlıklar (Entities)

| Entity | Açıklama |
|---------|----------|
| Customer | Mobil bankacılık uygulamasını kullanan müşteri |
| Account | Müşteriye ait banka hesapları |
| SavedRecipient | Kullanıcının kayıtlı alıcıları |
| Transfer | Gerçekleştirilen para transferleri |
| Receipt | İşlem sonunda oluşturulan dekont |
| QRCode | QR ile yapılan transferlerde kullanılan bilgiler |

---

# ER Diagram

```mermaid
erDiagram

CUSTOMER ||--o{ ACCOUNT : owns

ACCOUNT ||--o{ TRANSFER : sends

ACCOUNT ||--o{ SAVED_RECIPIENT : has

TRANSFER ||--|| RECEIPT : creates

SAVED_RECIPIENT ||--o{ TRANSFER : receives

QRCODE ||--o{ TRANSFER : used_for

CUSTOMER {

int customer_id PK

string first_name

string last_name

string email

string phone

datetime created_at

}

ACCOUNT {

int account_id PK

int customer_id FK

string iban

decimal balance

string currency

string status

}

SAVED_RECIPIENT {

int recipient_id PK

int account_id FK

string recipient_name

string recipient_iban

}

TRANSFER {

int transfer_id PK

int sender_account_id FK

int recipient_id FK

int qr_code_id FK

decimal amount

datetime transfer_date

string transfer_type

string status

}

RECEIPT {

int receipt_id PK

int transfer_id FK

string reference_number

datetime created_at

}

QRCODE {

int qr_code_id PK

string qr_value

datetime created_at

}
```

---

# İlişkiler (Relationships)

| Kaynak | Hedef | İlişki |
|----------|--------|---------|
| Customer | Account | Bir müşteri birden fazla hesaba sahip olabilir. |
| Account | SavedRecipient | Bir hesap birden fazla kayıtlı alıcıya sahip olabilir. |
| Account | Transfer | Bir hesap birçok transfer işlemi başlatabilir. |
| SavedRecipient | Transfer | Bir kayıtlı alıcı birçok transfer alabilir. |
| Transfer | Receipt | Her başarılı transfer için bir dekont oluşturulur. |
| QRCode | Transfer | QR kod kullanılarak transfer gerçekleştirilebilir. |

---

# İş Kuralları

- Her müşteri en az bir banka hesabına sahip olmalıdır.
- Her hesap yalnızca bir müşteriye aittir.
- Bir transfer yalnızca bir gönderen hesap tarafından başlatılabilir.
- Dekont yalnızca başarılı transferler için oluşturulur.
- QR kod yalnızca QR ile transfer senaryosunda kullanılır.
- Transfer türü (IBAN, Kayıtlı Alıcı, QR Kod) sistem tarafından saklanmalıdır.

---

# Sonuç

Bu ER Diagram, dijital bankacılık uygulamasındaki para transferi modülü için temel veri modelini göstermektedir. Veri varlıkları ve aralarındaki ilişkiler, sistem geliştirme, API tasarımı ve veritabanı modelleme çalışmalarına temel oluşturacak şekilde hazırlanmıştır.
