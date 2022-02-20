

```
docker-compose up -d
docker exec -it kafka-connect_mysql_1 bash
mysql -uroot -p fullcycle
create table categories (id int auto_increment primary key, name varchar(255));
show tables;
insert into categories (name) values('Eletronicos');

insert into categories (name) values('Cama');
```