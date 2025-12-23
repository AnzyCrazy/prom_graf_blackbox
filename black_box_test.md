На одном инстансе с ubuntu поднял:
prometheus + grafana + black_box:
структура мониторинга:
```bash
.
├── blackbox
│   └── blackbox.yml
├── docker-compose.yml
└── prometheus
    └── prometheus.yml
```
Поднимаем все c помощью docker compose
```bash
docker compose up
```
На другом инстансе поднял простое приложение для генерации qr-code
```bash
docker run -d -p 8080:8080 -it --rm --name qr-generator rmarcello/qr-generator:latest
```
Ссылка на проект с приложением:
https://github.com/marcelloraffaele/qr-generator

ID борды, которую импортировал: 13659

Графики с метриками и просто метрики с релейблингом:
![[Pasted image 20251223215340.png]]
![[Pasted image 20251223215404.png]]