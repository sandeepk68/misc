# postgres
```yaml
services:
  postgres:
    image: postgres:latest
    environment:
      - POSTGRES_USER=postgres
      - PGUSER=postgres
      - POSTGRES_NAME=postgres
      - POSTGRES_PASSWORD=postgres
    ports:
      - "5432:5432"
```


```shell
PGPASSWORD=postgres psql -U postgres -h localhost postgres
```
```postgresql
create table customers (id serial primary key, name varchar(255) not null);

insert into customers (name) values ('Sandeep');

select count(*) from customers;

\d

\d customers

\q
```
