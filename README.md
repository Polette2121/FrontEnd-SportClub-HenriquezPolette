# 🏋️ SportClub - Proyecto Front End

## 📋 Descripción del Proyecto

**SportClub** es una plataforma web de gestión de entrenamientos y clases deportivas. Permite a usuarios, coaches y administradores interactuar en un sistema completo de reservas y gestión de actividades deportivas.

Este es un proyecto académico desarrollado como parte del curso **Programación Front End** del programa de **Informática, Ciberseguridad y Telecomunicaciones**.

---

## 👥 Tipos de Usuarios

### **1. Usuario Regular** 👤
- Visualizar clases disponibles
- Realizar reservas de entrenamientos
- Cancelar reservas
- Ver perfil personal
- Gestionar información de perfil

### **2. Coach** 🏋️
- Ver alumnos asignados
- Administrar horarios de clases
- Ver información de sus entrenamientos
- Gestionar estadísticas de alumnos

### **3. Administrador** ⚙️
- Gestionar todos los usuarios
- Ver reportes del sistema
- Administrar clases disponibles
- Configuración del sistema
- Estadísticas completas

---

## 🔐 Credenciales de Prueba

El sistema incluye 3 usuarios de prueba por defecto:

### **Usuario Regular**
```
Email: javier@example.com
Contraseña: password123
Rol: usuario
```

### **Coach**
```
Email: coach@example.com
Contraseña: coach123
Rol: coach
```

### **Administrador**
```
Email: admin@example.com
Contraseña: admin123
Rol: admin
```

---

## 📁 Estructura del Proyecto

```
FrontEnd-SportClub-HenriquezPolette/
│
├── index.html                          # Página principal / Landing page
│
├── css/
│   ├── styles.css                     # Estilos globales
│   ├── landing.css                    # Estilos página principal
│   ├── forms.css                      # Estilos formularios (login, registro)
│   └── dashboard.css                  # Estilos dashboards (usuario, coach, admin)
│
├── js/
│   ├── auth.js                        # Sistema de autenticación y usuarios
│   ├── forms.js                       # Validación de formularios
│   ├── dashboard-usuario.js           # Lógica dashboard usuario
│   ├── dashboard-coach.js             # Lógica dashboard coach
│   └── dashboard-admin.js             # Lógica dashboard administrador
│
├── pages/
│   ├── login.html                     # Página de login
│   ├── registro.html                  # Página de registro
│   ├── recuperar-contrasena.html      # Página recuperar contraseña
│   ├── dashboard-usuario.html         # Dashboard usuario
│   ├── dashboard-coach.html           # Dashboard coach
│   └── dashboard-admin.html           # Dashboard administrador
│
├── assets/                            # Carpeta para imágenes (futura)
│
├── README.md                          # Este archivo
└── IA.md                              # Documentación técnica
```

---

## 🚀 Características Principales

### **Sistema de Autenticación** 🔐
- ✅ Login con validación de credenciales
- ✅ Registro de nuevos usuarios
- ✅ Recuperación de contraseña (simulada)
- ✅ Sesiones con sessionStorage
- ✅ Protección de dashboards por rol

### **Dashboard Usuario** 📱
- ✅ Bienvenida personalizada
- ✅ Mínimo 5 reservas disponibles
- ✅ Mínimo 3 clases disponibles para reservar
- ✅ Perfil rápido con información personal
- ✅ Opción de cancelar reservas

### **Dashboard Coach** 👥
- ✅ Panel de control con estadísticas
- ✅ Mínimo 5 alumnos asignados
- ✅ Mínimo 3 clases a cargo
- ✅ Mínimo 5 horarios semanales
- ✅ Visualización de alumnos por clase

### **Dashboard Administrador** ⚙️
- ✅ 3 Tarjetas estadísticas (usuarios, coaches, clases)
- ✅ Tabla de usuarios con RUT, estado y fecha
- ✅ Panel de reportes (clases populares, usuarios activos, reservas)
- ✅ Configuración rápida (crear usuario, editar sistema)
- ✅ Gestión de clases con barras de progreso

### **Diseño Responsivo** 📱💻
- ✅ Adaptable a móvil, tablet y desktop
- ✅ Navegación hamburguesa en móvil
- ✅ Tablas scrolleables
- ✅ Cards en grid adaptable

---

## 🛠️ Tecnologías Utilizadas

| Tecnología | Versión | Uso |
|-----------|---------|-----|
| HTML5 | 5 | Estructura del sitio |
| CSS3 | 3 | Estilos y diseño responsivo |
| JavaScript | ES6 | Lógica y interactividad |
| LocalStorage | - | Persistencia de datos |
| SessionStorage | - | Manejo de sesiones |

---

## 📊 Datos Utilizados

Todos los datos se almacenan en **LocalStorage** del navegador:

### **Usuarios**
```javascript
{
  id: number,
  nombre: string,
  email: string,
  password: string,
  rol: 'usuario' | 'coach' | 'admin',
  deporte: string,
  edad: number,
  fechaRegistro: string,
  activo: boolean
}
```

### **Reservas**
```javascript
{
  clase: string,
  dia: string,
  hora: string,
  coach: string,
  id: number
}
```

### **Clases**
```javascript
{
  nombre: string,
  descripcion: string,
  icono: string,
  accion: string
}
```

---

## 🎨 Colores por Rol

- **Usuario**: Azul (#3498db)
- **Coach**: Verde (#27ae60)
- **Admin**: Rojo (#e74c3c)
- **Oro (Destaque)**: #f39c12
- **Oscuro (Fondo)**: #2c3e50

---

## 🔄 Flujo de Navegación

```
index.html (Landing Page)
    ↓
├── Login → dashboard-usuario.html
├── Login → dashboard-coach.html
├── Login → dashboard-admin.html
└── Registro → login.html
```

---

## 📝 Instrucciones de Uso

### **1. Acceder al Sitio**
- Abre `index.html` en tu navegador
- Haz clic en "Ingresar" o "Crear Cuenta"

### **2. Login**
- Usa las credenciales de prueba proporcionadas arriba
- El sistema te redirigirá a tu dashboard según tu rol

### **3. Explorar Dashboard**
- Navega usando el menú lateral
- Visualiza tus datos específicos según tu rol
- Interactúa con los botones disponibles

### **4. Cerrar Sesión**
- Haz clic en "Cerrar Sesión" en la esquina superior derecha
- Confirma la acción

---

## 💾 Almacenamiento de Datos

### **LocalStorage**
- Almacena todos los usuarios registrados
- Clave: `usuariosSportClub`
- Se inicializa con 3 usuarios por defecto

### **SessionStorage**
- Almacena la sesión actual del usuario
- Clave: `usuarioActual`
- Se borra al cerrar el navegador

---

## 🎯 Requisitos Cumplidos

### **Dashboard Usuario** ✅
- [x] Bienvenida con nombre y mensaje
- [x] Mínimo 5 reservas con todos los datos
- [x] Mínimo 3 clases disponibles con descripción
- [x] Perfil rápido con 4 datos
- [x] Navegación completa

### **Dashboard Coach** ✅
- [x] Panel resumen con 3 estadísticas
- [x] Mínimo 5 alumnos listados
- [x] Mínimo 3 clases asignadas
- [x] Mínimo 5 horarios de la semana
- [x] Navegación completa

### **Dashboard Administrador** ✅
- [x] 3 Cards estadísticas
- [x] Tabla usuarios con RUT y 5 datos
- [x] Panel reportes con 3 secciones
- [x] Botones de configuración
- [x] Gestión de clases con progreso

---

## 🐛 Notas Técnicas

- El sistema usa **variables CSS** para los colores principales
- Todos los formularios validan antes de enviar
- Las contraseñas se almacenan en texto plano (solo para desarrollo)
- Los datos se reinician al borrar LocalStorage
- Responsive design con breakpoints en 768px y 1024px

---

## 📞 Contacto / Autor

**Proyecto:** SportClub  
**Autor:** Polette2121  
**Repositorio:** [FrontEnd-SportClub-HenriquezPolette](https://github.com/Polette2121/FrontEnd-SportClub-HenriquezPolette)  
**Fecha:** Junio 2026

---

## 📄 Licencia

Este proyecto es de uso académico.

---

**¡Gracias por usar SportClub! 🏋️💪**
