---
tags:
  - it/ProgrammingLanguages
  - it/ProgrammingLanguages/frameworks
---
შეიქმნა - 2018 

---

> [!info]
> 35 საათიანი კურსია
რომლელიც უნდა გავიარო 2 კვიარაში = დღეში 3 საათი ვიდეოს ყურება
აჩქარებულად 
> x2 = 1.5 საათს
> x1.5 = 2 საათს

---
## ღირსებები
ასინქრონული
მონაცემების ვალიდაცია
დოკუმენტაციის გენერაცია


## ნაკლები
ცოტა ბიბლიოთეკა
- ადმინ
- ქეშირება
- მონიტორინგი

## ინსტალაცია

შეიძლება სხვადასხვანაირად

ყველაზე მარტივი მეთოდი, ამავდროულად ყველაზე ცუდი
```bash
pip install fastapi[all]
```


## აპლიკაციის შექმნა

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def home():
	return "Hey"

@app.get("/docs")
def docs():
	"""
	ამის დაწერა არ შეიძლება. რადგანაც უკვე დაკავებულია და აბრუნებს ინტერაქტიულ დოკუმენტაციას.
	Alternative API docs  /redoc
	"""
	return "Interactive documentation"

```
## აპლიკაციის გაშვება

```bash
fastapi dev main.py
```
### რა არის uvicorn
```bash
uvicorn app.main:app --reload
```

## არგუმენტები / პარამეტრები


```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/document/{document_id}")
def home(document_id: int, date_from: str, date_to: str):
	return document_id,date_from,date_to
```


## ვალიდაცია

```python
from fastapi import FastAPI, Query
from typing import Optional
from datetime import date

app = FastAPI()

@app.get("/document/{document_id}")
def home(
	document_id: int, 
	date_from: date, 
	date_to: date,
	stars: Optional[int] = Query(None,ge=1, le=5)
	):
	return document_id,date_from,date_to
```


```python
from fastapi import FastAPI
from datetime import date
from pydantic import BaseModel

app = FastAPI()


class Document(BaseModel):
	item_id: int
	date_from: date
	date_to: date 

@app.post("/document")
def add_document(Document: document):
	"""
	მაგ: ბაზაში დამატების ლოგიკა
	"""
	
	pass
```


[5. База Данных Подключение](file:///D:%5CVideos%5C[Артем%20Шумейко]%20Курс%20по%20backend%20разработке%20на%20FastAPI%20(2023)%5C1.%20Знакомство%20с%20фреймворком%5C5.%20База%20Данных%20Подключение)


## მონაცემთა ბაზები

[[SQLAlchemy]] ([[ORM]]) 


[6. База Данных Подключение – Stepik.mkv](file:///D:%5CVideos%5C[Артем%20Шумейко]%20Курс%20по%20backend%20разработке%20на%20FastAPI%20(2023)%5C1.%20Знакомство%20с%20фреймворком%5C5.%20База%20Данных%20Подключение%5C6.%20База%20Данных%20Подключение%20–%20Stepik.mkv)
```bash
pip install sqlalchemy alembic asyncpg
```

[8. База Данных Подключение – Stepik.mkv](file:///D:%5CVideos%5C[Артем%20Шумейко]%20Курс%20по%20backend%20разработке%20на%20FastAPI%20(2023)%5C1.%20Знакомство%20с%20фреймворком%5C5.%20База%20Данных%20Подключение%5C8.%20База%20Данных%20Подключение%20–%20Stepik.mkv)
```python
from sqlarchemy.ext.asyncio iport AsyncSession, create_async_engine
from sqlarchemy.orm import DeclarativeBase, sessionmaker


DB_HOST = "localhost"
DB_PORT = 5432
DB_USER = "postgres"
DB_PASS = "postgres"
DB_NAME = "postgres"


DATABASE_URL = f"posgtresql+asyncpg://{DB_USER}:{DB_PASS}@{DB_HOST}:{DB_PORT}/{DB_NAME}"

engine = create_async_engine(DATABASE_URL)

async_session_maker = sessionmaker(engine, class_=AsyncSession, expire_on_commit=False)

class Base(DeclarativeBase):
	pass


```

![[connection_to_database_sqlalchemy.png]]

[10. База Данных Подключение – Stepik.mkv](file:///D:%5CVideos%5C[Артем%20Шумейко]%20Курс%20по%20backend%20разработке%20на%20FastAPI%20(2023)%5C1.%20Знакомство%20с%20фреймворком%5C5.%20База%20Данных%20Подключение%5C10.%20База%20Данных%20Подключение%20–%20Stepik.mkv)

[[FastAPI_Settings.canvas|FastAPI_Settings]]

### მოდელები

[9. База Данных Запросы – Stepik.mkv](file:///D:%5CVideos%5C[Артем%20Шумейко]%20Курс%20по%20backend%20разработке%20на%20FastAPI%20(2023)%5C1.%20Знакомство%20с%20фреймворком%5C6.%20База%20Данных%20Запросы%5C9.%20База%20Данных%20Запросы%20–%20Stepik.mkv)

 Need to revise: 
 [[Python OOP]]
## API Router

```python
# FILE booking/router.py

from fastapi import APIRouter

router = APIRouter(
	prefix="/booking",
	tags=["დაჯავშვნა"]
)

@router.get()
def get_booking():
	pass

@router.get("/{booking_id}")
def get_booking(booking_id):
	pass

```


```python
# FILE app/main.py
from app.booking.router import router as booking_router

app = FastAPI()

app.include_router(booking_router)
```







