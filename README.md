# jcp-backend

## Dependencias Instaladas.

- prisma: 7.5
- @prisma/client: 7.5
- jsonwebtoken: 9.0
- express: 5.2
- dotenv: 17.3
- cors: 2.8
- bcrypt: 6.0

## Dependencias Desarrollo

- nodemon: 3.1.14


## Scripts para Iniciar.

dev: nodemon src/server.js -> Desarrollo, actualizacion continua.
start: node src/server.js -> Deploy del backend funciona en produccion.
prisma:migrate: "prisma migrate dev",
prisma:generate: "prisma generate"



### Roles

# Enums
| Name           |   content       |
| -------------- | --------------- |
| UserRole       |  SUPERADMIN, ADMIN, SALES, LOGISTICS, WAREHOUSE|
| CustomerType   |  MINERA, REVENDEDOR, CONSTRUCTORA, GENERAL |
| ProductUnit    | PIEZA|
| ProductKind    | SINGLE, SET|
| LotType        | CONTENEDOR, PEDIMENTO, REPOSICION |
| InventoryOrigin| OWN, CONSIGNMENT |
| LotStatus      | OPEN, PARTIAL, CLOSED, CANCELED |
| SaleStatus     | DRAFT, CONFRMED, PARTIAL, FULFILLED, CANCELED |
| CurrencyCode   | MXN, USD |
| InventoryMovementType | IN, OUT, ADJUSTMENT, MANUAL |
| InventoryReferenceType | LOT, SALE, ADJUSTMENT, MANUAL |



