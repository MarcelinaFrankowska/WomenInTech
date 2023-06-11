Install if you do not have Git

```
https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
```

Open Docker desktop if on Windows

```
https://docs.docker.com/desktop/install/windows-install/
```

Open terminal and install Docker

```
"Docker Desktop Installer.exe" install
```

Clone the repo

```
git clone https://github.com/kkazimierska/WomenInTech.git
```

Start docker


```
docker compose build
docker compose up -d
```

in case of problems try

```
sudo docker compose -d
```

Run migrations

```
docker compose exec web python backend/manage.py migrate
```

Populate Database with sample objects

```
docker compose exec web python backend/manage.py loaddata /app/backend/windfarms/fixtures/windFarms.json
```
```
docker compose exec web python backend/manage.py loaddata /app/backend/windfarms/fixtures/windTurbines.json
```
Go to MURAL to follow the workshop process

https://app.mural.co/invitation/mural/womenintech6095/1683295253475?sender=ub9967f529429abe320475798&key=73c4c84e-1294-4867-925a-16a24b31b98a

Close containers
```
docker compose down -v
```

Running frontend tests:
```
docker compose exec frontend npm run test-headless
```
