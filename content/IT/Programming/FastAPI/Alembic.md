---
tags:
  - it/ProgrammingLanguages
---
[Alembic Introduction](https://youtu.be/i9RX03zFDHU?si=TnFRt1N9xlwACu_0)
[Documentation](https://alembic.sqlalchemy.org/en/latest/)

```shell
alembic init migrations
```
 
`alembic.ini` - Should be edited 
sqlalchemy.url = `put you database url`
 
`env.py`
`target_metadate` = Base.metadata [Autogenerate docs](https://alembic.sqlalchemy.org/en/latest/autogenerate.html)

```shell
.
├── alembic.ini  
└── migrations  
	├── README  
	├── env.py  
	├── script.py.mako  
	└── versions
```

```shell
# First - autogenerate// the "making database needs to be specific to what you are doing"  
alembic revision --autogenerate -m "making database"  # it's like git commit -m "The message for context"
# Autogenerate - from sqlalchemy model (I guess) 
# After modifying sqlalchemy model you always need to run revisions with --autogenerate 


# Second - command to generate migration  
alembic upgrade head
```


- Display the current revision for a database: `alembic current`. Shows Hash of current `revision/commit`
- View migrations history: `alembic history --verbose`.  Similar to `git log` 
- Revert all migrations:`alembic downgrade base`.
- Revert migrations one by one: `alembic downgrade -1`.
- Apply all migrations:`alembic upgrade head`.
- Apply migrations one by one: `alembic upgrade +1`.
- Display all raw SQL: `alembic upgrade head --sql`.
- Reset the database: `alembic downgrade base && alembic upgrade head`