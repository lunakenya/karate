# 🚀 Demoblaze API Automation Challenge

Automatización de pruebas para los servicios **Signup** y **Login** de la plataforma Demoblaze, desarrollada bajo estándares de calidad de software y buenas prácticas de QA Automation.

## 📖 Descripción

Este proyecto implementa una suite automatizada de pruebas para validar los endpoints de autenticación de **Demoblaze**.

La solución fue desarrollada utilizando **Karate DSL**, una herramienta moderna para pruebas de APIs REST que permite escribir escenarios de prueba de forma declarativa, reduciendo significativamente el código repetitivo y mejorando la mantenibilidad.

### Objetivos de la Automatización

✅ Validar creación exitosa de usuarios.

✅ Detectar intentos de registro duplicado.

✅ Verificar autenticaciones válidas.

✅ Validar manejo de contraseñas incorrectas.

✅ Comprobar comportamiento ante usuarios inexistentes.

✅ Generar reportes ejecutivos y técnicos automáticamente.

---
## 🛠️ Stack Tecnológico

| Tecnología | Versión | Propósito               |
| ---------- | ------- | ----------------------- |
| Karate DSL | 1.5.2   | Automatización de APIs  |
| Java       | 17+     | Plataforma de ejecución |
| Maven      | 3.8+    | Gestión de dependencias |
| JUnit      | 5       | Ejecución de pruebas    |
| Git        | Última  | Control de versiones    |
---
## 📂 Estructura del Proyecto

```text
.
├── src
│   └── test
│       ├── java
│       │   └── runners
│       │       └── TestRunner.java
│       │
│       └── resources
│           └── features
│               ├── signup.feature
│               └── login.feature
│
├── target
│   └── karate-reports
│
├── pom.xml
├── README.md
├── readme.txt
├── conclusiones.txt
└── .gitignore
```

### Descripción de Archivos

| Archivo            | Descripción                               |
| ------------------ | ----------------------------------------- |
| `signup.feature`   | Casos de prueba para registro de usuarios |
| `login.feature`    | Casos de prueba para autenticación        |
| `TestRunner.java`  | Runner principal de ejecución             |
| `pom.xml`          | Configuración Maven                       |
| `README.md`        | Documentación principal                   |
| `readme.txt`       | Guía rápida solicitada por el reto        |
| `conclusiones.txt` | Hallazgos y recomendaciones QA            |

---

## 📋 Requisitos Previos

Antes de ejecutar la suite, asegúrese de contar con:

### Java

```bash
java -version
```

Versión requerida:

```text
Java 17 o superior
```

### Maven

```bash
mvn -version
```
Versión requerida:

```text
Maven 3.8 o superior
```
### Conexión a Internet

Necesaria para:

* Descarga inicial de dependencias.
* Consumo de los endpoints públicos de Demoblaze.
---

## 🚀 Instalación y Ejecución

### 1️⃣ Clonar el repositorio

```bash
git clone https://github.com/lunakenya/tu-repositorio.git
```

Ingresar al proyecto:

```bash
cd tu-repositorio
```
---

### 2️⃣ Ejecutar todas las pruebas

```bash
mvn clean test
```

Este comando:

* Limpia compilaciones anteriores.
* Descarga dependencias.
* Ejecuta todos los escenarios.
* Genera reportes automáticos.
---

### 3️⃣ Ejecutar con parámetros personalizados (Opcional)

```bash
mvn test \
-DtestUser=usuario_custom \
-DtestPassword=password_custom123
```
---

## 📊 Matriz de Cobertura de Pruebas

| ID     | Endpoint     | Escenario                   | Resultado Esperado                   |
| ------ | ------------ | --------------------------- | ------------------------------------ |
| TC-001 | POST /signup | Registro exitoso de usuario | 200 OK + creación exitosa            |
| TC-002 | POST /signup | Usuario duplicado           | 200 OK + "This user already exists." |
| TC-003 | POST /login  | Login exitoso               | 200 OK + Auth_token                  |
| TC-004 | POST /login  | Contraseña incorrecta       | 200 OK + "Wrong password."           |
| TC-005 | POST /login  | Usuario inexistente         | 200 OK + "User does not exist."      |

---

## 🧪 Casos Cubiertos

### Signup

* Registro de usuario nuevo.
* Validación de usuario existente.
* Verificación de mensajes de respuesta.

### Login

* Inicio de sesión exitoso.
* Password incorrecto.
* Usuario inexistente.
* Validación de token de autenticación.

---

## 🏗️ Consideración Arquitectónica

> La API de Demoblaze devuelve siempre un estado HTTP **200 OK**, incluso cuando ocurre un error de negocio.

Por este motivo, las validaciones automatizadas se realizan principalmente sobre el contenido del payload JSON y no únicamente sobre el código HTTP.

Ejemplo:

```json
{
  "errorMessage": "Wrong password."
}
```

---

## 📈 Reportes de Ejecución

Karate genera reportes HTML automáticamente después de cada ejecución.

Ubicación:

```text
target/karate-reports/karate-summary.html
```

Abrir en cualquier navegador:

* Google Chrome
* Firefox
* Microsoft Edge
* Safari

---

## 📊 Ejemplo de Resultado Esperado

```text
Tests run: 5
Passed: 5
Failed: 0
Skipped: 0
```

## 🎯 Buenas Prácticas Aplicadas

✔ Uso de datos dinámicos.

✔ Escenarios independientes.

✔ Código mantenible.

✔ Validaciones explícitas.

✔ Separación de responsabilidades.

✔ Reportería automática.

---

## 👨‍💻 Autor

**Luna Kenya**

📫 Especializada en automatización de pruebas, calidad de software y validación de APIs REST.

---
