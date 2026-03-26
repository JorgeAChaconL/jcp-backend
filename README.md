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

- dev: nodemon src/server.js -> Desarrollo, actualizacion continua.
- start: node src/server.js -> Deploy del backend funciona en produccion.
- prisma:migrate: "prisma migrate dev",
- prisma:generate: "prisma generate"



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

 # Flujo de trabajo Git / GitHub
 ### 📌 Ramas principales
<ol>
 <li> main → rama de producción (estable,   siempre deployable)
 <li> develop → rama de integración (trabajo activo del equipo)
</ol>

### 🧩 Ramas temporales

Se crean desde develop y se eliminan al terminar:

 - feature/* → nuevas funcionalidades
 - fix/* → corrección de errores

    Ejemplos:

        feature/users-endpoint
        feature/inventory-lots
        fix/margin-calculation
### 🔁 Flujo de desarrollo
<ol>
<li> Crear rama desde develop <br>

        - git checkout develop <br>
        - git pull origin develop <br>
        - git checkout -b feature/nombre-feature
<li>Trabajar en la funcionalidad <br>

       -  git add .
        - git commit -m "feat: descripción del cambio" 

<li> Subir rama a GitHub <br>

        - git push -u origin feature/nombre-feature 
<li> Crear Pull Request (PR) 
    
    * En GitHub: 
            - feature/nombre-feature → develop 
            - Revisar cambios 
            - Validar funcionalidad 
            - Mantener historial limpio 
<li> Merge a develop
    
    Una vez aprobado el PR:

            - Se integra la funcionalidad a develop
<li> Actualizar entorno local
            
            -git checkout develop
            -git pull origin develop
<li> Eliminar rama (cleanup)
    
    *Local
        - git branch -d feature/nombre-feature
    * Remota
        - git push origin --delete feature/nombre-feature

</ol>


### 🚀 Paso a producción

#### ```Cuando develop esté estable:```

<ol>Crear Pull Request:

### develop → main

Esto representa una versión lista para producción.

# ⚠️ Reglas importantes
- ❌ No hacer push directo a main 
- ❌ No hacer merge de feature/* a main
- ✅ Todo cambio pasa por develop
- ✅ Usar Pull Requests para integrar cambios
- ✅ Eliminar ramas después de mergearlas
- ✅ Mantener ramas pequeñas y específicas
- 🧠 Buenas prácticas
    - Una rama = una funcionalidad o tarea
    - Evitar ramas grandes o de larga duración
    - Hacer commits claros y descriptivos
    - Mantener sincronizado develop antes de crear nuevas ramas

# 📊 Resumen visual
### develop → feature/* → develop → main


