# Güvenlik ve Moderasyon Planı

## Güvenlik prensipleri
- Kimlik doğrulama ve yetkilendirme ayrı kontrollerdir.
- Her işlemde sunucu tarafında erişim denetimi yapılır.
- Veritabanında uygun Row Level Security (RLS) politikaları uygulanır.
- Gizli anahtarlar repoya eklenmez; `.env` kullanılır ve `.env.example` yalnızca örnek değerler içerir.
- Yüklenen dosyaların türü, boyutu ve izinleri doğrulanır.
- Rate limiting ve spam önleme uygulanır.
- Kullanıcı girdileri güvenli şekilde doğrulanır ve görüntülenir.

## Moderasyon
- Şiir, yorum ve profil şikâyetleri
- Moderatör inceleme kuyruğu
- İçerik kaldırma ve hesap kısıtlama
- Denetlenebilir moderasyon kayıtları
- Telif hakkı bildirim süreci

## Gizlilik
- Gereksiz kişisel veri toplanmamalıdır.
- Hesap silme ve veri saklama süreçleri tanımlanmalıdır.
- Gizlilik, çerez ve kullanım şartları yayın öncesinde hazırlanmalıdır.
- KVKK uyumluluğu yayına alınmadan önce ayrıca değerlendirilmelidir.

Bu doküman planlama notudur; tek başına güvenlik veya hukuki uygunluk garantisi değildir.
