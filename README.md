# Segundo Trabalho de Técnicas de Programação VI - Node.js


## Clonando o repositório

```bash
git clone https://github.com/Felipe-Costaa/univas-si-8p-tp6-t2
cd univas-si-8p-tp6-t2
```

## Rodando a API separadamente

```bash
npm install
npm run start
```

### Endpoints


#### GET ALL MATCHES
```bash
http://localhost:8087/api/v1/jogos
```

#### GET GAME BY TEAM NAME
```bash
http://localhost:8087/api/v1/jogos/time/:time
```
> EXAMPLE
```bash
http://localhost:8087/api/v1/jogos/time/Santos
```

#### GET GAME BY MATCH DATE
> **_NOTA:_** A data deve ser passada no formato **YYYY-MM-DD**
```bash
http://localhost:8087/api/v1/jogos/data/:data
```
> EXAMPLE
```bash
http://localhost:8087/api/v1/jogos/data/2019-05-05
```

#### CREATE A NEW MATCH - POST
> **_NOTA:_** Na criação de partida - ambos os times começam com 0 gols, independente do resultado passado no json.
```bash
http://localhost:8087/api/v1/jogos
```
> EXAMPLE
```json
{
    "mandante": "Santos",
    "visitante": "Corinthians",
    "gols_mandante": 4,
    "gols_visitante": 2,
    "data": "2022-05-05",
    "estadio": "Vila Belmiro",
    "horario": "20:00"
}
```

#### UPDATE SCORE OF A MATCH BY ID - PUT
```bash
http://localhost:8087/api/v1/jogos/:id
```
> EXAMPLE
```bash
http://localhost:8087/api/v1/jogos/15
```

```json
{
    "gols_mandante": 3,
    "gols_visitante": 1
}
```

#### DELETE A MATCH BY ID - DELETE
```bash
http://localhost:8087/api/v1/jogos/:id
```
> EXAMPLE
```bash
http://localhost:8087/api/v1/jogos/15
```

