# AI Systems Lab 1 — NBA (Docker + PostgreSQL)

Развернуть PostgreSQL в Docker, загрузить данные NBA, выполнить анализ в Jupyter Notebook


## Docker (PostgreSQL)
```bash
docker compose up -d
# или:
# docker run --name pg-nba -e POSTGRES_PASSWORD=postgres -e POSTGRES_USER=postgres -e POSTGRES_DB=nba -p 5432:5432 -d postgres:16
docker ps
```

## Загрузка данных (pgloader)
```bash
pgloader sqlite:////Users/vasilisaelina/Desktop/sii/nba.sqlite postgresql://postgres:postgres@localhost:5432/nba
```

## Ноутбук
```bash
jupyter notebook
```
Открыть AISP1.ipynb, в первой ячейке подключение:
```python
engine = create_engine("postgresql+psycopg2://postgres:postgres@localhost:5432/nba")
```

## Содержимое
- Задание 2–7: графики и таблицы уже выполнены в ноутбуке.
