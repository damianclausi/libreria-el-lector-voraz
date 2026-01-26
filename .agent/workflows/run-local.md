---
description: Cómo ejecutar El Lector Voraz localmente
---

Para ejecutar el proyecto en tu máquina local, sigue estos pasos:

### 1. Instalar Dependencias
Asegúrate de tener Node.js instalado y ejecuta:
```bash
npm install
```

### 2. Configurar Variables de Entorno
Crea un archivo `.env` en la raíz del proyecto. Puedes usar los valores por defecto para desarrollo:
```bash
PORT=3000
MONGO_URI=mongodb://localhost:27017/el_lector_voraz
SESSION_SECRET=el-lector-voraz-super-secret-key-2024
```

### 3. Iniciar MongoDB
Asegúrate de que MongoDB esté instalado y corriendo en tu sistema. Si usas Docker, puedes iniciar un contenedor:
```bash
docker run -d --name mongodb -p 27017:27017 mongo
```

### 4. Poblar la Base de Datos (Opcional pero recomendado)
Ejecuta el script de semilla para cargar datos de prueba y usuarios iniciales:
// turbo
```bash
node crear_base_el_lector_voraz.js
```

### 5. Iniciar la Aplicación
Para desarrollo (con reinicio automático):
// turbo
```bash
npm run dev
```

O para producción:
```bash
npm start
```

### 6. Acceder
Abre tu navegador en [http://localhost:3000](http://localhost:3000).

---
**Usuarios de prueba (Contraseña: 1234):**
- Admin: `admin` o `juan.perez@lectorvoraz.com`
- Empleado: `antonio.gill@lectorvoraz.com`, `cristian.descosido@lectorvoraz.com`, `damian.clausi@lectorvoraz.com`
