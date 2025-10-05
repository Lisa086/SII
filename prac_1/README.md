# AI Systems Lab 1 — NBA (Docker + PostgreSQL)

Развернуть PostgreSQL в Docker, загрузить данные NBA, выполнить анализ в Jupyter Notebook

Задание 1 
1. docker compose up -d
2. docker compose ps
3. cd ..
pgloader sqlite:///$(pwd)/nba.sqlite postgresql://postgres:postgres@localhost:5432/nba
cd prac_1
4. psql "postgresql://postgres:postgres@localhost:5432/nba" -c "\dt"
5. docker ps -a
6. from sqlalchemy import create_engine
engine = create_engine("postgresql+psycopg2://postgres:postgres@localhost:5432/nba")



## Docker (PostgreSQL)
```bash
docker compose up -d
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
