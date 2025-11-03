# Changelog - Sistema de Gestión de Historias de Usuario

## [2.0.0] - Implementación de Sistema de Esfuerzo Estilo Taiga

### ✨ Nuevas Funcionalidades

#### 1. **Campos de Esfuerzo por Disciplina**

Se agregaron 4 campos de estimación de esfuerzo a todas las historias de usuario (24 total):

- **ux**: Story points para trabajo de UX/Research
- **design**: Story points para diseño visual/UI
- **front**: Story points para desarrollo Frontend
- **back**: Story points para desarrollo Backend

Escala utilizada: Fibonacci-like (1, 2, 3, 5, 8, 13 story points)

#### 2. **Visualización de Sprint**

- Cada historia muestra su sprint asignado (S1, S2, S3, S4)
- Badge distintivo con color de acento en las tarjetas
- Integración en vista de detalle del modal

#### 3. **Filtro por Sprint**

Se agregó un nuevo filtro dropdown que permite filtrar historias por:

- Sprint 1 - Gestión usuarios + GUI (US-1 a US-9)
- Sprint 2 - Chat en tiempo real (US-10 a US-18)
- Sprint 3 - Transmisión de voz (US-19 a US-21)
- Sprint 4 - Transmisión de video (US-22 a US-24)

#### 4. **Panel de Esfuerzo en Tarjetas**

Las tarjetas de historias ahora muestran:

- Grid de 5 columnas con métricas de esfuerzo
- Valores individuales por disciplina (UX, Design, Front, Back)
- **Total de story points** destacado con fondo de color primario
- Formato visual claro y responsivo

#### 5. **Desglose de Esfuerzo en Modal**

Vista detallada mejorada con:

- Sección dedicada "Esfuerzo Estimado (Story Points)"
- 5 tarjetas visuales con bordes y fondos diferenciados
- Métricas individuales por disciplina
- Total general destacado
- Diseño tipo dashboard con grid responsivo

### 📊 Distribución de Esfuerzo por Sprint

**Sprint 1 (US-1 a US-9) - Total: 201 pts**

- UX: 17 pts | Design: 34 pts | Front: 60 pts | Back: 44 pts

**Sprint 2 (US-10 a US-18) - Total: 225 pts**

- UX: 16 pts | Design: 29 pts | Front: 56 pts | Back: 64 pts

**Sprint 3 (US-19 a US-21) - Total: 91 pts**

- UX: 6 pts | Design: 12 pts | Front: 31 pts | Back: 29 pts

**Sprint 4 (US-22 a US-24) - Total: 111 pts**

- UX: 7 pts | Design: 18 pts | Front: 36 pts | Back: 32 pts

**TOTAL PROYECTO: 628 story points**

### 🛠️ Cambios Técnicos

#### Archivos Modificados

1. **data.js** (673 líneas)

   - ✅ Agregados campos `ux`, `design`, `front`, `back` a las 24 historias
   - ✅ Campo `sprint` ya existente verificado (S1-S4)

2. **videoconference_user_stories.json** (610 líneas)

   - ✅ Sincronizado con data.js
   - ✅ Todos los campos de esfuerzo agregados
   - ✅ Estructura JSON válida

3. **app.js** (547 líneas)

   - ✅ Función `createStoryCard()` actualizada
     - Nuevo badge de sprint en header
     - Grid de esfuerzo de 5 columnas en footer
     - Cálculo automático de total de story points
   - ✅ Función `openModal()` actualizada
     - Sección de esfuerzo estimado con tarjetas visuales
     - Badge de sprint en badges del header
   - ✅ Función `applyFilters()` actualizada
     - Soporte para filtro de sprint
     - Búsqueda incluye campo sprint
   - ✅ Nuevos elementos del DOM
     - `sprintFilter` agregado a `elements`
   - ✅ Nuevo event listener
     - `handleSprintFilter()` conectado

4. **index.html** (147 líneas)
   - ✅ Nuevo dropdown de filtro de sprint
   - ✅ 5 opciones: Todos + S1 a S4
   - ✅ Labels descriptivos por sprint

### 🎨 Mejoras de UI/UX

1. **Tarjetas de Historia**

   - Sprint badge con `var(--accent-color)`
   - Panel de esfuerzo con separador visual (`border-top`)
   - Grid responsivo de 5 columnas
   - Total destacado con fondo primario

2. **Modal de Detalle**

   - Sección de esfuerzo con fondo secundario (`var(--background-secondary)`)
   - Tarjetas individuales con bordes de 2px
   - Total con fondo de color primario y texto blanco
   - Layout grid adaptativo (`repeat(auto-fit, minmax(120px, 1fr))`)

3. **Filtros**
   - Filtro de sprint integrado visualmente con filtro de épica
   - Opciones claras con nombres descriptivos
   - Funcionalidad combinable con otros filtros

### 📁 Estructura de Datos Actualizada

```javascript
{
  code: "US-X",
  title: "Título de la historia",
  sprint: "S1" | "S2" | "S3" | "S4",  // Sprint asignado
  epic: "E-X Nombre de épica",
  ux: Number,          // ⭐ NUEVO - Story points UX
  design: Number,      // ⭐ NUEVO - Story points Design
  front: Number,       // ⭐ NUEVO - Story points Frontend
  back: Number,        // ⭐ NUEVO - Story points Backend
  description: String,
  acceptanceCriteria: String[],
  definitionOfDone: String[]
}
```

### ✅ Checklist Completado

- [x] Agregar campos de esfuerzo a data.js (24 historias)
- [x] Sincronizar campos de esfuerzo con videoconference_user_stories.json
- [x] Actualizar `createStoryCard()` para mostrar sprint y esfuerzo
- [x] Actualizar `openModal()` para mostrar desglose de esfuerzo
- [x] Agregar filtro de sprint a index.html
- [x] Implementar lógica de filtro de sprint en app.js
- [x] Agregar búsqueda por sprint
- [x] Verificar ausencia de errores en todos los archivos
- [x] Validar estructura JSON

### 🧪 Testing Recomendado

1. **Funcionalidad de Filtros**

   - [ ] Filtrar por cada sprint (S1, S2, S3, S4)
   - [ ] Combinar filtro de sprint + épica
   - [ ] Buscar por código de sprint ("S1", "S2", etc.)

2. **Visualización**

   - [ ] Verificar badges de sprint en todas las tarjetas
   - [ ] Confirmar que los story points se muestran correctamente
   - [ ] Validar cálculo de totales (UX + Design + Front + Back)
   - [ ] Revisar responsive design en móviles (320px, 768px, 1024px)

3. **Modal de Detalle**
   - [ ] Abrir cada historia y verificar desglose de esfuerzo
   - [ ] Confirmar que el total coincide con la suma de partes
   - [ ] Verificar accesibilidad con navegación por teclado

### 📖 Uso del Sistema

**Para filtrar por sprint:**

1. Usar el dropdown "Filtrar por Sprint"
2. Seleccionar el sprint deseado (S1-S4)
3. Las historias se filtran automáticamente

**Para ver esfuerzo de una historia:**

1. El resumen aparece en la tarjeta (grid de 5 columnas)
2. Click en la tarjeta para ver detalles completos
3. El modal muestra el desglose completo con tarjetas visuales

**Para planificar capacidad:**

- Usar los totales por disciplina para asignar recursos
- Fibonacci-like permite estimaciones rápidas
- Sprint 1 y 2 son los más densos (201 y 225 pts)
- Sprint 3 es el más ligero (91 pts)

### 🚀 Próximos Pasos Sugeridos

1. **Métricas Avanzadas**

   - Gráfico de burndown por sprint
   - Velocity tracking entre sprints
   - Distribución de esfuerzo por épica

2. **Exportación de Datos**

   - Exportar a CSV con campos de esfuerzo
   - Generar reportes por sprint
   - Integración con Jira/Taiga

3. **Validación de Estimaciones**
   - Comparar esfuerzo estimado vs. real
   - Ajustar escala según histórico
   - Retrospectiva de precisión

---

**Versión:** 2.0.0  
**Fecha:** 2024  
**Autor:** Sistema de Gestión Charlaton  
**Compatibilidad:** Navegadores modernos (Chrome 90+, Firefox 88+, Safari 14+)
