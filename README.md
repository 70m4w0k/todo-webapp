## Dev Test

```sh
# test for model
cargo watch -q -c -w src/ -x 'test model_ -- --test-threads=1 --nocapture'

# test for web
cargo watch -q -c -w src/ -x 'test web_ -- --test-threads=1 --nocapture'

```

## Dev Web

```sh
cargo watch -q -c -w src/ -x 'run -- ../frontend/web-folder'

# start front-end localhost:8080
npm run build -- -w
```

## DB

```sh
# start the database
docker run --rm -p 5432:5432 -e "POSTGRES_PASSWORD=postgres" --name pg postgres:14

# optional psql (other terminal)
docker exec -it -u postgres pg psql
```

## Erreur 'port already in use'

```sh
# lister les ports en utilisation
sudo netstat -tunlp

# eteindre un port
sudo kill <PID>
```
