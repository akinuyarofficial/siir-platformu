# Veritabanı Taslağı
Supabase/PostgreSQL hedefiyle başlangıç modelidir; geliştirme sırasında revize edilebilir.

## Tablolar
- **profiles:** id (auth user UUID), username (unique), display_name, bio, avatar_url, cover_url, created_at, updated_at
- **poems:** id, author_id, title, content, visibility (public/private/unlisted), cover_url, created_at, updated_at, published_at
- **categories:** id, name, slug, description
- **poem_categories:** poem_id, category_id
- **tags:** id, name, slug
- **poem_tags:** poem_id, tag_id
- **likes:** id, user_id, poem_id, created_at; user_id + poem_id unique
- **comments:** id, poem_id, author_id, parent_id (optional), content, created_at, updated_at
- **follows:** follower_id, following_id, created_at; pair unique, self-follow prohibited
- **collections:** id, owner_id, title, description, cover_url, visibility, created_at
- **collection_poems:** collection_id, poem_id, position, added_at
- **notifications:** id, recipient_id, actor_id (optional), type, entity_id (optional), read_at, created_at
- **reports:** id, reporter_id, target_type, target_id, reason, details, status, created_at, resolved_at

## İlkeler
- UUID ve foreign key kullanımı
- İlişkili alanlarda indeksler
- Row Level Security (RLS) politikaları
- Kullanıcılar sadece izin verilen kendi taslak/özel içeriklerini görür ve yönetir
- Yetkilendirme sunucu tarafında doğrulanır
- İstemciye gereksiz hassas veri gönderilmez
