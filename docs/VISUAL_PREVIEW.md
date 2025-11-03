# 🎨 Vista Previa del Sistema de Esfuerzo - Charlaton

## Cambios Visuales en la Interfaz

### 1. 🏷️ Tarjeta de Historia - Vista Mejorada

```
┌─────────────────────────────────────────────────────┐
│ US-1              E-1 Gestión de cuentas      [S1]  │ ← Badge de Sprint
│                                                      │
│ Sign-up básico                                      │
│                                                      │
│ Como visitante de la plataforma                     │
│ Quiero registrarme con mis datos personales...     │
│                                                      │
│ [5 criterios]  [5 DoD]                             │
│ ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ │ ← Separador
│                                                      │
│  UX    Design   Front   Back   [Total]             │ ← Grid de Esfuerzo
│  3      5       8       5       21                  │
│                                                      │
└─────────────────────────────────────────────────────┘
```

**Características:**

- Badge de Sprint (S1-S4) con color de acento
- Grid de 5 columnas con métricas
- Total destacado con fondo primario
- Diseño responsivo (se adapta a móvil)

---

### 2. 📱 Filtros - Nueva Opción de Sprint

```
┌─────────────────────────────────────────────────────────────┐
│ 🔍 Buscar por título, código o descripción...              │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│ Filtrar por Épica: [Todas las épicas ▼]                   │
│                                                             │
│ Filtrar por Sprint: [Todos los sprints ▼]   ← NUEVO       │
│                     • Todos los sprints                     │
│                     • Sprint 1 - Gestión usuarios + GUI     │
│                     • Sprint 2 - Chat en tiempo real        │
│                     • Sprint 3 - Transmisión de voz         │
│                     • Sprint 4 - Transmisión de video       │
│                                                             │
│ 24 historias  •  24 mostradas                              │
└─────────────────────────────────────────────────────────────┘
```

**Funcionalidad:**

- Dropdown con 5 opciones
- Se puede combinar con filtro de épica
- Búsqueda también incluye sprint
- Contadores se actualizan en tiempo real

---

### 3. 🔍 Modal de Detalle - Sección de Esfuerzo

```
┌──────────────────────────────────────────────────────────────────┐
│ [X] Cerrar                                                       │
│                                                                  │
│ US-1 - Sign-up básico                                           │
│ [US-1] [E-1 Gestión de cuentas] [S1] ← Badges con Sprint      │
│                                                                  │
│ ┌──────────────────────────────────────────────────────────┐   │
│ │ Esfuerzo Estimado (Story Points)                         │   │
│ │                                                           │   │
│ │  ┌──────┐  ┌──────┐  ┌──────┐  ┌──────┐  ┌──────┐     │   │
│ │  │  UX  │  │Design│  │Front-│  │Back- │  │Total │     │   │
│ │  │      │  │      │  │ end  │  │ end  │  │      │     │   │
│ │  │  3   │  │  5   │  │  8   │  │  5   │  │  21  │     │   │
│ │  │ pts  │  │ pts  │  │ pts  │  │ pts  │  │ pts  │     │   │
│ │  └──────┘  └──────┘  └──────┘  └──────┘  └──────┘     │   │
│ │                                             ^^^         │   │
│ │                                        Destacado        │   │
│ └──────────────────────────────────────────────────────────┘   │
│                                                                  │
│ Descripción                                                     │
│ Como visitante de la plataforma...                             │
│                                                                  │
│ Criterios de Aceptación                                        │
│ • Visualización del formulario...                              │
│ • Validación en tiempo real...                                 │
│ ...                                                             │
└──────────────────────────────────────────────────────────────────┘
```

**Características:**

- Sección dedicada con fondo destacado
- 5 tarjetas visuales con bordes
- Total con fondo de color primario
- Layout grid adaptativo
- Información clara y jerárquica

---

## 🎯 Interacciones del Usuario

### Flujo 1: Ver Esfuerzo de una Historia

```
1. Usuario ve la lista de historias
   └─→ Cada tarjeta muestra el grid de esfuerzo
       └─→ UX: 3, Design: 5, Front: 8, Back: 5, Total: 21

2. Usuario hace clic en una tarjeta
   └─→ Se abre el modal
       └─→ Sección "Esfuerzo Estimado" visible en la parte superior
           └─→ 5 tarjetas con métricas detalladas
```

### Flujo 2: Filtrar por Sprint

```
1. Usuario abre dropdown "Filtrar por Sprint"
   └─→ Selecciona "Sprint 1 - Gestión usuarios + GUI"
       └─→ Lista se filtra automáticamente
           └─→ Muestra solo US-1 a US-9 (9 historias)
               └─→ Contador actualiza: "9 mostradas de 24 historias"

2. Usuario puede combinar con filtro de épica
   └─→ Selecciona "E-1 Gestión de cuentas"
       └─→ Refinamiento adicional
           └─→ Solo historias que cumplen ambos criterios
```

### Flujo 3: Buscar por Sprint

```
1. Usuario escribe "S2" en el buscador
   └─→ Lista se filtra a historias del Sprint 2
       └─→ US-10 a US-18 (9 historias)

2. Usuario escribe "Sprint 2"
   └─→ Mismo resultado por coincidencia en badges
```

---

## 📊 Ejemplos por Tipo de Historia

### Historia Simple - US-5 (Logout)

```
┌─────────────────────────────────────────┐
│ US-5    E-1 Gestión...    [S1]         │
│                                         │
│ Logout                                  │
│ Como usuario autenticado...             │
│                                         │
│ [4 criterios]  [5 DoD]                 │
│ ─────────────────────────────────────── │
│  UX  Design  Front  Back  [Total]      │
│  1    2      3      2      8           │ ← Esfuerzo bajo
└─────────────────────────────────────────┘
```

### Historia Compleja - US-16 (Chat)

```
┌─────────────────────────────────────────┐
│ US-16   E-3 Chat...       [S2]         │
│                                         │
│ Enviar mensaje en chat                 │
│ Como participante de una reunión...     │
│                                         │
│ [7 criterios]  [5 DoD]                 │
│ ─────────────────────────────────────── │
│  UX  Design  Front  Back  [Total]      │
│  2    5      8     13      28          │ ← Esfuerzo alto
│                    ^^                   │
│                Backend                  │
│                complejo                 │
└─────────────────────────────────────────┘
```

### Historia Muy Compleja - US-19 (Audio)

```
┌─────────────────────────────────────────┐
│ US-19   E-4 Audio...      [S3]         │
│                                         │
│ Activar micrófono                      │
│ Como participante de una reunión...     │
│                                         │
│ [8 criterios]  [6 DoD]                 │
│ ─────────────────────────────────────── │
│  UX  Design  Front  Back  [Total]      │
│  3    5     13     13      34          │ ← Máxima complejidad
│              ^^     ^^                  │
│            WebRTC                       │
└─────────────────────────────────────────┘
```

---

## 🎨 Paleta de Colores Utilizada

### Badges

- **Sprint Badge:** `var(--accent-color)` (color de acento del tema)
- **Epic Badge:** `var(--border-color)` con texto primario
- **Story Code:** `var(--primary-color)` con texto blanco

### Grid de Esfuerzo (Tarjeta)

- **Labels UX/Design/Front/Back:** `var(--text-secondary)`
- **Valores numéricos:** `var(--text-primary)`
- **Total:** Fondo `var(--primary-color)`, texto blanco

### Modal de Esfuerzo

- **Contenedor:** Fondo `var(--background-secondary)`
- **Tarjetas individuales:** Fondo `var(--background-primary)`, borde `var(--border-color)`
- **Tarjeta Total:** Fondo `var(--primary-color)`, texto blanco
- **Valores:** Color `var(--primary-color)` para destacar

---

## 📱 Responsive Design

### Desktop (>1024px)

```
┌─────────┬─────────┬─────────┬─────────┐
│ Story 1 │ Story 2 │ Story 3 │ Story 4 │
│  [Grid] │  [Grid] │  [Grid] │  [Grid] │
│  5 cols │  5 cols │  5 cols │  5 cols │
├─────────┼─────────┼─────────┼─────────┤
│ Story 5 │ Story 6 │ Story 7 │ Story 8 │
└─────────┴─────────┴─────────┴─────────┘
```

### Tablet (768-1023px)

```
┌─────────────┬─────────────┐
│  Story 1    │  Story 2    │
│  [Grid]     │  [Grid]     │
│  5 cols     │  5 cols     │
├─────────────┼─────────────┤
│  Story 3    │  Story 4    │
└─────────────┴─────────────┘
```

### Mobile (320-767px)

```
┌─────────────────┐
│    Story 1      │
│    [Grid]       │
│    5 cols       │
│  (scrollable)   │
├─────────────────┤
│    Story 2      │
│    [Grid]       │
└─────────────────┘
```

**Nota:** El grid de esfuerzo se mantiene en 5 columnas en móvil pero puede hacer scroll horizontal si es necesario.

---

## ✨ Animaciones y Transiciones

### Hover en Tarjetas

```
Estado normal → Hover
┌─────────────┐    ┌─────────────┐
│   Story 1   │    │   Story 1   │
│             │ => │   [Elevado] │ (shadow aumenta)
│   [Grid]    │    │   [Grid]    │
└─────────────┘    └─────────────┘
```

### Apertura de Modal

```
Click en tarjeta
    ↓
Fade in del overlay (0.3s)
    ↓
Scale in del modal (0.3s, ease-out)
    ↓
Contenido visible
```

### Filtrado

```
Cambio de filtro
    ↓
Fade out de historias no coincidentes (0.2s)
    ↓
Reorganización del grid
    ↓
Fade in de nuevas historias (0.2s)
```

---

## 🔍 Detalles de Accesibilidad

### ARIA Labels

- Sprint filter: `aria-label="Filtrar por sprint"`
- Effort metrics: Anunciados como "UX: 3 puntos, Design: 5 puntos..."
- Total: `aria-label="Total de esfuerzo: 21 story points"`

### Navegación por Teclado

- `Tab`: Navegar entre filtros y tarjetas
- `Enter/Space`: Abrir modal de historia
- `Escape`: Cerrar modal
- `Arrow keys`: Navegar dropdown de sprint

### Contraste

- Todos los colores cumplen WCAG AA (4.5:1)
- Texto en badges: Alto contraste
- Total destacado: Blanco sobre color primario

---

## 📸 Capturas Conceptuales

### Vista General

```
┌──────────────────────────────────────────────────────────────┐
│  🏠 Historias de Usuario         Charlaton        [🌙 Tema]  │
├──────────────────────────────────────────────────────────────┤
│  🔍 Buscar...                                                 │
│  Épica: [Todas ▼]  Sprint: [Todos ▼]   24 historias        │
├──────────────────────────────────────────────────────────────┤
│  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐      │
│  │ US-1 [S1]│ │ US-2 [S1]│ │ US-3 [S1]│ │ US-4 [S1]│      │
│  │ Sign-up  │ │ Login    │ │ Google   │ │ Facebook │      │
│  │ 3|5|8|5  │ │ 2|5|5|5  │ │ 1|3|5|3  │ │ 1|3|5|3  │      │
│  │ Total:21 │ │ Total:17 │ │ Total:12 │ │ Total:12 │      │
│  └──────────┘ └──────────┘ └──────────┘ └──────────┘      │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐      │
│  │ US-5 [S1]│ │ US-6 [S1]│ │ US-7 [S1]│ │ US-8 [S1]│      │
│  │ ...      │ │ ...      │ │ ...      │ │ ...      │      │
└──────────────────────────────────────────────────────────────┘
```

### Filtrado por Sprint 2

```
┌──────────────────────────────────────────────────────────────┐
│  Sprint: [Sprint 2 - Chat en tiempo real ▼]                 │
├──────────────────────────────────────────────────────────────┤
│  ┌──────────┐ ┌──────────┐ ┌──────────┐                    │
│  │US-10 [S2]│ │US-11 [S2]│ │US-12 [S2]│  9 mostradas      │
│  │ Unirse ID│ │ Unirse   │ │ Lista    │                    │
│  │ 2|3|5|5  │ │ enlace   │ │ partic.  │                    │
│  │ Total:15 │ │ 1|2|5|5  │ │ 2|5|8|5  │                    │
│  └──────────┘ │ Total:13 │ │ Total:20 │                    │
│               └──────────┘ └──────────┘                     │
└──────────────────────────────────────────────────────────────┘
```

---

**Documento:** Vista Previa del Sistema  
**Versión:** 2.0.0  
**Para testing visual:** Abrir `index.html` en navegador moderno
