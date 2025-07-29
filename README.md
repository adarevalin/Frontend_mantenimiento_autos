🚗 Sistema de Mantenimiento de Automóviles – Frontend
Este repositorio contiene el frontend del sistema web de mantenimiento de automóviles, una aplicación moderna desarrollada en React.js que permite a los usuarios autenticados visualizar, gestionar y registrar mantenimientos asociados a automóviles.

Este sistema forma parte de una arquitectura full stack que interactúa con un backend construido en Python (FastAPI) y una base de datos PostgreSQL. Este repositorio se enfoca únicamente en la interfaz de usuario.

🧠 Motivación del Proyecto
La necesidad de mantener registros ordenados y seguros sobre los mantenimientos, daños, reportes y estado general de los vehículos impulsó el desarrollo de este sistema. El objetivo es facilitar la digitalización de procesos, garantizar el acceso seguro y centralizado a la información, y permitir futuras integraciones con sistemas de análisis de datos e inteligencia artificial.

🛠️ Tecnologías Utilizadas
⚛️ React.js – Librería principal para construir la interfaz.

🧠 React Context API – Para manejo global del estado de autenticación.

🧭 React Router Dom – Para gestionar la navegación y rutas protegidas.

🎨 CSS personalizado – Estilos adaptados y modulares.

🔒 Protección de rutas – Mediante componentes que restringen el acceso a usuarios autenticados.

frontend/
│
├── public/                  # Archivos públicos estáticos
│   └── index.html           # HTML base del frontend
│
├── src/                     # Código fuente principal
│   ├── components/          # Componentes reutilizables (Login, formularios, etc.)
│   │   └── Login.js         # Componente para autenticación de usuario
│   │
│   ├── pages/               # Páginas principales de la app
│   │   ├── home.js          # Vista principal tras iniciar sesión
│   │   └── Mantenimiento.js # Página para visualizar o registrar mantenimientos
│   │
│   ├── context/             # Contextos globales
│   │   └── AuthContext.js   # Lógica de autenticación global (login/logout)
│   │
│   ├── Methods/             # (Opcional) Lógica de utilidades, fetch API, etc.
│   │
│   ├── App.js               # Componente principal con ruteo y protección de rutas
│   ├── App.css              # Estilos generales
│   ├── index.js             # Entrada principal de React
│   ├── index.css            # Estilos globales
│   ├── logo.svg             # Logo de la aplicación
│   └── setupTests.js        # Configuración para pruebas
│
└── package.json             # Dependencias y scripts del proyecto
🔐 Rutas Protegidas
El archivo App.js implementa un sistema de rutas protegidas. Solo los usuarios autenticados pueden acceder a las páginas /home y /mantenimiento, mientras que los usuarios no autenticados son redirigidos automáticamente al login (/).

js

<Route path="/home" element={<ProtectedRoute component={Home} />} />
<Route path="/mantenimiento" element={<ProtectedRoute component={Mantenimiento} />} />
🚀 Cómo Ejecutar el Proyecto
1. Clonar el repositorio
bash

git clone https://github.com/tu-usuario/automoviles-frontend.git
cd automoviles-frontend
2. Instalar dependencias
bash

npm install
3. Iniciar el servidor de desarrollo
bash

npm start
