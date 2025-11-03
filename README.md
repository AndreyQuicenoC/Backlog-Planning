# 📋 Visualizador de Historias de Usuario - Charlaton

Página web interactiva para visualizar, filtrar y explorar historias de usuario de los proyectos **Plataforma de Videoconferencias** y **Plataforma de Películas**.

---

## ✨ Características

### 🎨 Interfaz Moderna

- **Diseño responsivo**: se adapta a móviles (320px), tablets (768px) y escritorio (1024px+)
- **Tema claro/oscuro**: alterna entre modos con persistencia en localStorage
- **Animaciones suaves**: transiciones y efectos visuales fluidos
- **Tipografía profesional**: fuente Inter de Google Fonts

### 🔍 Funcionalidades de Búsqueda y Filtrado

- **Búsqueda en tiempo real**: filtra por código, título, descripción o épica
- **Filtro por épica**: visualiza historias de una épica específica
- **Selector de proyecto**: cambia entre videoconferencias y películas
- **Estadísticas en vivo**: muestra total de historias y resultados filtrados

### 📱 Experiencia de Usuario

- **Tarjetas interactivas**: hover con elevación y borde de color
- **Modal de detalles**: muestra criterios de aceptación y definición de hecho completos
- **Estados de carga**: spinner animado mientras se cargan los datos
- **Estado vacío**: mensaje amigable cuando no hay resultados
- **Manejo de errores**: interfaz para reintentar si falla la carga

### ♿ Accesibilidad (WCAG)

- **Navegación por teclado**: todos los elementos interactivos accesibles
- **Atributos ARIA**: roles, labels y live regions implementados
- **Contraste adecuado**: cumple con WCAG AA en ambos temas
- **Screen reader friendly**: etiquetas descriptivas para lectores de pantalla

---

## 🚀 Cómo Usar

### Opción 1: Abrir directamente

1. Navega a la carpeta `Planeación`
2. Haz doble clic en `index.html`
3. Se abrirá en tu navegador predeterminado

### Opción 2: Servidor local (recomendado)

```bash
# Con Python 3
cd "c:/Users/lu/Downloads/Proyectos/Proyecto integrador/Charlaton/Planeación"
python -m http.server 8000

# Con Node.js (usando npx)
npx serve

# Con PHP
php -S localhost:8000
```

Luego abre: `http://localhost:8000`

### Opción 3: Live Server (VS Code)

1. Instala la extensión "Live Server" en VS Code
2. Haz clic derecho en `index.html`
3. Selecciona "Open with Live Server"

---

## 📂 Estructura de Archivos

```
Planeación/
├── index.html                          # Página principal
├── styles.css                          # Estilos CSS
├── app.js                              # Lógica JavaScript
├── user_stories.json                   # Historias del proyecto de películas (23)
├── videoconference_user_stories.json   # Historias del proyecto de videoconferencias (25)
└── README.md                           # Este archivo
```

---

## 🎯 Funcionalidades Principales

### 1. **Cambiar entre Proyectos**

- Usa el selector en el header para alternar entre:
  - 🎥 Videoconferencias (25 historias)
  - 🎬 Plataforma de Películas (23 historias)

### 2. **Buscar Historias**

- Escribe en el campo de búsqueda para filtrar en tiempo real
- Busca por: código (US-1), título, descripción o épica

### 3. **Filtrar por Épica**

- Selecciona una épica específica del dropdown:
  - E-1: Gestión de cuentas
  - E-2: Gestión de reuniones / películas
  - E-3: Chat / Favoritos y valoraciones
  - E-4: Transmisión de audio / Interacción social
  - E-5: Transmisión de video / Experiencia de visualización

### 4. **Ver Detalles**

- Haz clic en cualquier tarjeta para abrir el modal
- El modal muestra:
  - ✅ Criterios de Aceptación completos
  - 🎯 Definición de Hecho
  - 📝 Descripción detallada
- Cierra con el botón × o presiona `Escape`

### 5. **Tema Oscuro/Claro**

- Haz clic en el botón 🌙/☀️ en el header
- La preferencia se guarda automáticamente

---

## 🛠️ Tecnologías Utilizadas

- **HTML5**: estructura semántica y accesible
- **CSS3**: Grid, Flexbox, Custom Properties, animaciones
- **JavaScript (ES6+)**: Fetch API, módulos, async/await
- **Google Fonts**: Inter (300, 400, 500, 600, 700)

---

## 📊 Estructura de Datos JSON

Cada historia de usuario sigue este formato:

```json
{
  "code": "US-1",
  "title": "Título de la historia",
  "epic": "E-1 Nombre de la épica",
  "description": "Como [rol]\nQuiero [acción]\nPara [beneficio]",
  "acceptanceCriteria": ["Criterio 1", "Criterio 2"],
  "definitionOfDone": ["Tarea 1", "Tarea 2"]
}
```

---

## 🎨 Personalización

### Cambiar Colores

Edita las variables CSS en `styles.css`:

```css
:root {
  --primary-color: #6366f1; /* Color principal */
  --primary-hover: #4f46e5; /* Color hover */
  --success-color: #10b981; /* Color éxito */
  /* ... más variables ... */
}
```

### Agregar Más Proyectos

Edita el objeto `PROJECTS` en `app.js`:

```javascript
const PROJECTS = {
  miProyecto: {
    file: "mi_proyecto_stories.json",
    name: "Mi Proyecto",
  },
};
```

Y añade la opción en el `<select>` del HTML.

---

## ⚡ Optimizaciones

- **Debounce en búsqueda**: evita búsquedas excesivas (300ms delay)
- **CSS Variables**: cambio de tema instantáneo
- **Lazy rendering**: solo renderiza historias visibles
- **LocalStorage**: guarda preferencia de tema

---

## 🐛 Solución de Problemas

### Las historias no cargan

- **Verifica** que los archivos JSON estén en la misma carpeta que `index.html`
- **Usa un servidor local** (no abras el archivo directamente si hay problemas CORS)

### El tema no cambia

- **Borra el caché** del navegador (Ctrl+Shift+R)
- **Verifica localStorage** en DevTools → Application → Local Storage

### La búsqueda no funciona

- **Abre la consola** (F12) y verifica errores
- **Recarga la página** (Ctrl+R)

---

## 📱 Soporte de Navegadores

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ⚠️ IE 11 (no soportado)

---

## 📝 Notas de Desarrollo

### Accesibilidad implementada

- ✅ Navegación por teclado completa
- ✅ ARIA labels y roles
- ✅ Contraste WCAG AA
- ✅ Focus visible en todos los elementos interactivos
- ✅ Screen reader compatible

### Responsividad

- **Mobile**: 320px - 767px (1 columna)
- **Tablet**: 768px - 1023px (2 columnas)
- **Desktop**: 1024px+ (3-4 columnas auto-fit)

---

## 🤝 Contribuciones

Para agregar nuevas historias:

1. Edita el archivo JSON correspondiente
2. Recarga la página
3. Las nuevas historias aparecerán automáticamente

---

## 📄 Licencia

Proyecto Integrador - Charlaton © 2025

---

## 🎓 Créditos

Desarrollado para el curso de Proyecto Integrador  
**Plataforma**: Charlaton  
**Fecha**: Noviembre 2025

---

## 📞 Soporte

Si encuentras algún problema o tienes sugerencias:

1. Revisa la sección de solución de problemas arriba
2. Abre la consola del navegador (F12) para ver errores
3. Verifica que los archivos JSON estén correctamente formateados

---

**¡Disfruta explorando tus historias de usuario! 🚀**
