⸻

Hugo + Netlify CMS (Docker)

Toto je jednoduchý Hugo projekt s Netlify CMS na správu obsahu, pripravený na lokálny vývoj pomocou Dockeru.

⸻

🚀 Ako začať (lokálny setup)

1. Klonovanie repozitára

git clone git@github.com:hujco/hugo-netlify-test.git
cd hugo-netlify-test

2. Spustenie Hugo + Netlify CMS lokálne (Docker)

Spusti tento príkaz na štart lokálneho vývoja:

docker-compose -f docker/development/docker-compose.yml -p hugo-netlify-test up --build

Web bude dostupný na:
	•	🌍 Hugo web: http://localhost:1313
	•	✏️ Netlify CMS: http://localhost:1313/admin

⸻

📄 Správa obsahu cez Netlify CMS

Obsah blogu spravuješ priamo cez Netlify CMS:
	•	Prihlás sa cez GitHub.
	•	Vytvor/editoj články v intuitívnom rozhraní.
	•	Zmeny sa ukladajú automaticky do repozitára na GitHube cez Pull Requesty.

⸻

🔨 Vygenerovanie statického webu pre produkciu

Keď chceš web vygenerovať pre deploy:

docker-compose -f docker/development/docker-compose.yml -p hugo-netlify-test run build

Produkčný web nájdeš v priečinku /public.

⸻

📂 Štruktúra projektu

hugo-netlify-test/
├── content/          # Obsah stránok/blogu (Markdown)
├── layouts/          # HTML šablóny Hugo
├── static/admin/     # Konfigurácia Netlify CMS
├── docker/           # Docker konfigurácia pre lokálny vývoj
├── config.toml       # Hugo konfiguračný súbor
└── public/           # Produkčný build (automaticky generované)



⸻

🐳 Docker workflow
	•	docker compose up: lokálny vývoj s automatickým reloadom obsahu
	•	docker compose run build: build produkčnej verzie webu

⸻

🔗 GitHub repozitár

➡️ https://github.com/hujco/hugo-netlify-test

⸻

📝 Pridávanie nových šablón a stránok
	•	Hugo šablóny vytváraš v priečinku layouts.
	•	Nové články/pages v priečinku content.

⸻

Teraz už máš všetko pripravené! 🚀
