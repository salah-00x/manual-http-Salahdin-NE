# Desarrollo Web en entorno Cliente - 2º DAW DAW - IES HLanz  
**Profesor: Isaías FL**  

---

# 🚀 Ejercicio: CRUD HTTP Manual con cURL y Herramientas Visuales  

## 📋 Descripción del ejercicio  
Implementarás un sistema completo de gestión de estudiantes mediante peticiones HTTP, utilizando una API local con `json-server`.  
Documentarás todas las operaciones CRUD (Create, Read, Update, Delete) usando tres herramientas diferentes:  

- **cURL** (línea de comandos)  
- **Thunder Client** (interfaz gráfica)  
- **REST Client** (archivos `.http`)  

---

## 🎯 Objetivos de aprendizaje  
- ✅ Comprender la anatomía completa de las peticiones HTTP  
- ✅ Dominar los métodos HTTP: GET, POST, PUT, PATCH, DELETE  
- ✅ Practicar con cURL desde la terminal  
- ✅ Utilizar herramientas visuales (Thunder Client y REST Client)  
- ✅ Gestionar variables de entorno con dotenv  
- ✅ Aplicar buenas prácticas de Git y documentación  

---

## 🛠 Requisitos previos  
- 📦 Node.js instalado (v18 o superior)  
- 🌿 Git instalado  
- 💻 Visual Studio Code  
- 🔌 Extensiones de VS Code instaladas:  
  - ⚡ Thunder Client  
  - 📝 REST Client  
- 🖥 Terminal (Git Bash en Windows, bash/zsh en Linux/Mac)  

---

## 📁 Estructura del proyecto requerida  

manual-http-[nombre-iniciales-apellidos]/
├── 📂 src/
│ ├── 📂 db/
│ │ └── 📄 db.json # Base de datos json-server
│ └── 📄 crud-curl.js # Script con funciones CRUD
├── 📂 scripts/
│ └── 📄 validate.sh # Script de validación bash
├── 📂 images/ # Capturas Thunder Client
├── 📄 peticiones-crud.http # Peticiones REST Client
├── 🔐 .env # Variables de entorno (NO versionar)
├── 📋 .env.example # Template de variables
├── 🚫 .gitignore
├── 📖 README.md # Documentación completa
├── ✅ checklist.md # Control de progreso
└── 📦 package.json


---

## 🎬 Parte 1: Configuración inicial del proyecto  

### 1.1 🏗 Inicialización del proyecto  
- Crear carpeta del proyecto: `manual-http-[tu-nombre-iniciales-apellidos]`  
- Inicializar proyecto Node.js con `npm init`  
- Completar los datos del proyecto:  
  - 📛 Nombre: `manual-http-nombre-iniciales-apellidos`  
  - 🔢 Version: `1.0.0`  
  - 📝 Description: Descripción apropiada del proyecto  
  - 👤 Author: Tu nombre  

### 1.2 📦 Instalación de dependencias  
- Instalar `json-server` como dependencia  
- Instalar `dotenv` como dependencia  

💡 **Nota sobre los paquetes**:  
- `json-server`: Crea una API REST completa a partir de un archivo JSON  
- `dotenv`: Permite cargar variables de entorno desde un archivo `.env`  

### 1.3 ⚙ Configuración de `package.json`  
- Usar **ESM (ES Modules)** en lugar de CommonJS  
- Añadir los siguientes scripts:  

```json
"scripts": {
  "server:up": "json-server --watch src/db/db.json --port 4000",
  "crud:curl": "node src/crud-curl.js",
  "validate": "bash scripts/validate.sh"
}

1.4 📂 Estructura de carpetas

Crear todas las carpetas según la estructura requerida

1.5 🔧 Archivos de configuración

Crear .env con:

PORT=4000
API_BASE_URL=http://localhost
NODE_ENV=development


Crear .env.example

Crear .gitignore con:

node_modules/

.env

Archivos de logs

Archivos de sistema operativo

Carpetas de editores

1.6 🗄 Base de datos json-server

Crear src/db/db.json con las colecciones:

students (7 estudiantes)

courses (4 cursos)

enrollments (4 inscripciones)

💻 Parte 2: Script CRUD con funciones JavaScript
2.1 📄 Archivo src/crud-curl.js

Importar y configurar dotenv

Cargar variables de entorno

Construir BASE_URL

2.2 🔧 Funciones CRUD requeridas

➕ createStudent(studentData)

📋 readAllStudents()

🔍 readStudentById(id)

🔄 updateStudent(id, studentData)

✏ patchStudent(id, partialData)

🗑 deleteStudent(id)

Cada función debe:

Tener comentario JSDoc

Imprimir el comando cURL correspondiente

Mostrarlo bien formateado

2.3 ▶ Ejecución del script

Ejecutar todas las funciones en orden

Mostrar mensajes claros en consola

📚 Parte 3: Documentación CRUD con cURL

Incluir en README.md:

🏷 Título de la operación

📝 Descripción

💻 Comando cURL

🔍 Explicación de flags y headers

✅ Respuesta real

📊 Explicación del status code

⚡ Parte 4: Thunder Client

Crear colección CRUD Students API

Configurar variables (baseUrl, port, fullUrl)

Crear peticiones:

➕ CREATE Student

📋 GET All Students

🔍 GET Student by ID

🔄 UPDATE Student

✏ PATCH Student

🗑 DELETE Student

Capturas en /images

Documentar en el README

📝 Parte 5: REST Client

Crear archivo peticiones-crud.http

Definir variables @baseUrl, @port, @apiUrl

Implementar todas las operaciones CRUD con separadores ###

Probar cada petición desde VS Code

✅ Parte 6: Script de validación
6.1 📄 Archivo scripts/validate.sh

Debe validar:

Existencia de archivos y carpetas

Dependencias instaladas

Scripts en package.json

Mínimo 6 capturas en images/

6.2 ⚙ Configuración

Dar permisos de ejecución

Ejecutar desde terminal

📋 Parte 7: Checklist de progreso

Crear archivo checklist.md con checkboxes para:

Configuración inicial

Scripts requeridos

Funciones CRUD

Documentación

Thunder Client

REST Client

Validación

Git

🌿 Parte 8: Git y GitHub

Crear repositorio manual-http-[tu-nombre]

Añadir profesor como colaborador

Subir código inicial en main

Crear rama m1/http-request-response

Hacer commits incrementales (feat:, docs:, fix:)

Crear Pull Request con resumen, división de trabajo y dificultades

📊 Rúbrica de Evaluación
Criterio	Peso	🔴 Nivel 1	🟡 Nivel 2	🟢 Nivel 3	Nota
🏗 Configuración	1.0	Archivos faltantes	Errores menores	Todo perfecto	☐ __/1.0
💻 Script CRUD	2.0	Comandos incorrectos	Errores sintácticos	Perfecto	☐ __/2.0
📚 Doc. README	2.0	Incompleta	Superficial	Detallada con respuestas	☐ __/2.0
⚡ Thunder Client	2.0	< 4 peticiones	6 peticiones básicas	Colección completa	☐ __/2.0
📝 REST Client	1.5	< 4 peticiones	CRUD básico	CRUD + filtros	☐ __/1.5
🌿 Git workflow	1.0	< 3 commits	Commits básicos	Commits descriptivos + PR	☐ __/1.0
✅ Validación	0.5	No funciona	Valida < 10 elementos	Completa	☐ __/0.5
📈 Nota Final

Escala:

⚫ Sin realizar = 0

🔴 Nivel 1 = 33%

🟡 Nivel 2 = 66%

🟢 Nivel 3 = 100%

🎯 Nota máxima: 10.0 puntos
✅ Requisito mínimo: 5.0 puntos + script de validación funcionando

📚 Recursos de consulta

📖 Módulo 1 - Fundamentos HTTP y Herramientas

📖 Módulo 2 - Herramientas Visuales para APIs

🔗 json-server Docs

🔗 cURL Docs

🔗 Thunder Client Docs

🔗 REST Client Docs

📤 Entrega

📅 Método: Pull Request en GitHub

⏰ Fecha límite: [Definida por el profesor]

⚠ Importante:

✅ PR creado antes de la fecha

✅ Script de validación debe pasar

🚫 .env NO en el repo

👥 Trabajo en pareja (opcional)

❓ Preguntas frecuentes

❔ ¿Las funciones deben ejecutar los comandos?
👉 No, solo imprimirlos.

❔ ¿Qué significa recibir parámetros?
👉 Que las funciones deben aceptar datos dinámicos (readStudentById(id)).

❔ ¿Qué puerto usa json-server?
👉 El definido en .env (por defecto 4000).

❔ ¿Cómo sé si mi script de validación funciona?
👉 Ejecuta y verifica todos los checks en verde.

❔ ¿Debo usar Git Bash en Windows?
👉 Sí, para ejecutar .sh.

❔ ¿Puedo modificar el db.json?
👉 Sí, puedes añadir estudiantes, pero no eliminar los 7 iniciales.
