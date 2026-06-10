# Demoblaze API — Automatización con Karate DSL

Proyecto de automatización de pruebas API para los endpoints de **signup** y **login** de [Demoblaze](https://www.demoblaze.com/), implementado con **Karate DSL 1.5.2**, **JUnit 5** y **Maven**.

## Stack

| Herramienta | Versión |
|---|---|
| Java | 17 |
| Maven | 3.8+ |
| Karate DSL | 1.5.2 (io.karatelabs) |
| JUnit | 5.10.1 |

## Ejecución rápida

```bash
# Suite completa (10 escenarios)
mvn test

# Solo escenarios críticos (2 escenarios)
mvn test -Dtest=SmokeTest

# Con credenciales personalizadas
mvn test -DtestUser=mi_usuario -DtestPassword=mi_password
```

## Casos cubiertos

| TC | Endpoint | Descripción |
|---|---|---|
| TC-001 | POST /signup | Crear usuario nuevo (dinámico) |
| TC-002 | POST /signup | Usuario duplicado → errorMessage (autónomo) |
| TC-005 | POST /login | Login válido → Auth_token |
| TC-006 | POST /login | Password incorrecto → Wrong password. |
| TC-007 | POST /login | Usuario inexistente → User does not exist. |
| TC-003/004/008/009/010 | ambos | Scenario Outline con variantes |

## Reporte

```
target/surefire-reports/karate-reports/karate-summary.html
```

Consulta **`readme.txt`** para instrucciones detalladas paso a paso y **`conclusiones.txt`** para los hallazgos técnicos completos.
