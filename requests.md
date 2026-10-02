# Тестовые запросы PZ4 (CRUD ToDo на chi)

```bash
cd ~/Downloads/pz4-todo
go run .
```

## Health

```bash
curl -i http://localhost:8080/health
```

## Create

```bash
curl -i -X POST http://localhost:8080/api/tasks \
  -H "Content-Type: application/json" \
  -d '{"title":"Выучить chi"}'
```

## List

```bash
curl -i http://localhost:8080/api/tasks
```

## Get by id

```bash
curl -i http://localhost:8080/api/tasks/1
```

## Update

```bash
curl -i -X PUT http://localhost:8080/api/tasks/1 \
  -H "Content-Type: application/json" \
  -d '{"title":"Выучить chi глубже","done":true}'
```

## Delete

```bash
curl -i -X DELETE http://localhost:8080/api/tasks/1
```

## Errors

```bash
curl -i -X POST http://localhost:8080/api/tasks \
  -H "Content-Type: application/json" \
  -d '{"title":""}'

curl -i http://localhost:8080/api/tasks/9999
```
