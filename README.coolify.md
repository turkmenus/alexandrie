# Alexandrie — Coolify Deployment Notes (ExileLab)

Bu fork, [Smaug6739/Alexandrie](https://github.com/Smaug6739/Alexandrie)'nin MHEK/ExileLab Coolify ortamına uygun hale getirilmiş halidir.

## Upstream ile farklar

- `docker-compose.coolify.yml` eklendi: Coolify Docker Compose kurallarına uygun, host port kullanmayan, Traefik etiketleri ve `coolify` external network'ü içeren compose dosyası.
- `.env.coolify.example` eklendi: Coolify UI'den girilecek ortam değişkenleri şablonu.
- Orijinal `docker-compose.yml` ve `.env.example` dokunulmadı; gelecek upstream güncellemeleri `git fetch upstream` + rebase ile alınabilir.

## Traefik router adları

| Servis | Router adı |
|---|---|
| frontend | `exilelab-alexandrie` |
| backend | `exilelab-alexandrie-api` |
| rustfs (cdn) | `exilelab-alexandrie-cdn` |

## Ortam değişkenleri

Gerçek değerler **Coolify UI > Environment Variables** bölümünden girilmelidir. `.env` dosyasına yazılmaz.

Gerekli değişkenler `.env.coolify.example` dosyasında listelenmiştir.

## Proje / ortam

- **Coolify project:** `ExileLab`
- **Coolify environment:** `production`
- **Target server:** `uzaksunucu` (`192.168.1.101.sslip.io`)

## Domain'ler

- Frontend: `https://alexandrie.testedeli.online`
- Backend API: `https://api.alexandrie.testedeli.online`
- CDN / S3: `https://cdn.alexandrie.testedeli.online`
- Cookie domain: `testedeli.online`
