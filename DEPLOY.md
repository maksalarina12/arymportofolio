# Deployment Guide dengan Docker

## Prerequisites
- Docker installed
- Docker Compose installed (optional)

## Cara Deploy

### Menggunakan Docker Compose (Recommended)

1. Build dan jalankan container:
```bash
docker-compose up -d
```

2. Website akan tersedia di: `http://localhost`

3. Stop container:
```bash
docker-compose down
```

### Menggunakan Docker langsung

1. Build image:
```bash
docker build -t arymportofolio .
```

2. Run container:
```bash
docker run -d -p 80:80 --name arymportofolio arymportofolio
```

3. Website akan tersedia di: `http://localhost`

4. Stop container:
```bash
docker stop arymportofolio
docker rm arymportofolio
```

## Deploy ke Hosting (Contoh: DigitalOcean, AWS, dll)

1. Push code ke repository (GitHub, GitLab, dll)

2. Di server hosting, clone repository:
```bash
git clone <repository-url>
cd arymportofolio
```

3. Build dan run:
```bash
docker-compose up -d
```

4. Atau gunakan Docker langsung:
```bash
docker build -t arymportofolio .
docker run -d -p 80:80 --name arymportofolio arymportofolio
```

## Catatan

- Pastikan port 80 tidak digunakan aplikasi lain
- Untuk production, pertimbangkan menggunakan HTTPS dengan reverse proxy (Nginx/Caddy)
- Update link Instagram di `contact.html` dengan link Instagram Anda yang sebenarnya

