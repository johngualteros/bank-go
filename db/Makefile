postgres:
	docker run --name postgres12 -p 5432:5432 -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=secret -d postgres:12-alpine

createDb:
	docker exec -it postgres12 createdb --username=postgres --owner=postgres bank

dropDb:
	docker exec -it postgres12 dropdb bank

migrateUp:
	migrate -path db/migration -database "postgresql://postgres:secret@localhost:5432/bank?sslmode=disable" -verbose up

migrateDown:
	migrate -path db/migration -database "postgresql://postgres:secret@localhost:5432/bank?sslmode=disable" -verbose down

.PHONY: postgres createDb dropDb migrateUp migrateDown