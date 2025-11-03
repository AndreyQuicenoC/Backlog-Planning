# 📊 Guía de Estimación de Esfuerzo - Proyecto Charlaton

## Story Points por Historia de Usuario

### Sprint 1 - Gestión de Usuarios + GUI Base (201 pts)

| Código | Título                   |   UX   | Design | Front  |  Back  |  Total  |
| ------ | ------------------------ | :----: | :----: | :----: | :----: | :-----: |
| US-1   | Sign-up básico           |   3    |   5    |   8    |   5    | **21**  |
| US-2   | Login con credenciales   |   2    |   5    |   5    |   5    | **17**  |
| US-3   | Login con Google OAuth   |   1    |   3    |   5    |   3    | **12**  |
| US-4   | Login con Facebook OAuth |   1    |   3    |   5    |   3    | **12**  |
| US-5   | Logout                   |   1    |   2    |   3    |   2    |  **8**  |
| US-6   | Recuperar contraseña     |   2    |   3    |   5    |   3    | **13**  |
| US-7   | Editar perfil            |   2    |   5    |   8    |   5    | **20**  |
| US-8   | Eliminar cuenta          |   2    |   3    |   5    |   8    | **18**  |
| US-9   | Crear reunión            |   3    |   5    |   8    |   8    | **24**  |
|        | **SUBTOTAL S1**          | **17** | **34** | **60** | **44** | **201** |

### Sprint 2 - Chat en Tiempo Real + Gestión de Reuniones (225 pts)

| Código | Título                          |   UX   | Design | Front  |  Back  |  Total  |
| ------ | ------------------------------- | :----: | :----: | :----: | :----: | :-----: |
| US-10  | Unirse a reunión por ID         |   2    |   3    |   5    |   5    | **15**  |
| US-11  | Unirse a reunión por enlace     |   1    |   2    |   5    |   5    | **13**  |
| US-12  | Ver lista de participantes      |   2    |   5    |   8    |   5    | **20**  |
| US-13  | Copiar enlace de invitación     |   2    |   3    |   5    |   2    | **12**  |
| US-14  | Finalizar reunión (host)        |   2    |   3    |   5    |   8    | **18**  |
| US-15  | Salir de reunión (participante) |   2    |   2    |   5    |   5    | **14**  |
| US-16  | Enviar mensaje en chat          |   2    |   5    |   8    |   13   | **28**  |
| US-17  | Recibir mensajes en tiempo real |   1    |   3    |   5    |   13   | **22**  |
| US-18  | Ver historial de chat           |   2    |   3    |   8    |   8    | **21**  |
|        | **SUBTOTAL S2**                 | **16** | **29** | **56** | **64** | **225** |

### Sprint 3 - Transmisión de Audio (91 pts)

| Código | Título                                |  UX   | Design | Front  |  Back  | Total  |
| ------ | ------------------------------------- | :---: | :----: | :----: | :----: | :----: |
| US-19  | Activar micrófono                     |   3   |   5    |   13   |   13   | **34** |
| US-20  | Desactivar micrófono                  |   1   |   2    |   5    |   3    | **11** |
| US-21  | Escuchar audio de otros participantes |   2   |   5    |   13   |   13   | **33** |
|        | **SUBTOTAL S3**                       | **6** | **12** | **31** | **29** | **91** |

### Sprint 4 - Transmisión de Video (111 pts)

| Código | Título                            |  UX   | Design | Front  |  Back  |  Total  |
| ------ | --------------------------------- | :---: | :----: | :----: | :----: | :-----: |
| US-22  | Activar cámara                    |   3   |   8    |   13   |   13   | **37**  |
| US-23  | Desactivar cámara                 |   1   |   2    |   5    |   3    | **11**  |
| US-24  | Ver videos de otros participantes |   3   |   8    |   13   |   13   | **37**  |
|        | **SUBTOTAL S4**                   | **7** | **18** | **36** | **32** | **111** |

---

## 📈 Resumen Ejecutivo

### Totales por Sprint

| Sprint    |   UX   | Design |  Front  |  Back   | **Total** |
| --------- | :----: | :----: | :-----: | :-----: | :-------: |
| S1        |   17   |   34   |   60    |   44    |  **201**  |
| S2        |   16   |   29   |   56    |   64    |  **225**  |
| S3        |   6    |   12   |   31    |   29    |  **91**   |
| S4        |   7    |   18   |   36    |   32    |  **111**  |
| **TOTAL** | **46** | **93** | **183** | **169** |  **628**  |

### Distribución Porcentual por Disciplina

- **Frontend:** 183 pts (29.1%) - Mayor carga de trabajo
- **Backend:** 169 pts (26.9%) - Segunda mayor carga
- **Design:** 93 pts (14.8%)
- **UX:** 46 pts (7.3%)

### Características por Sprint

**Sprint 1 (201 pts)** - Más complejo

- Autenticación múltiple (credenciales, OAuth)
- CRUD completo de usuarios
- Creación de reuniones
- Base de UI/UX del proyecto

**Sprint 2 (225 pts)** - Más denso

- Chat en tiempo real (Socket.io)
- Gestión completa de reuniones
- Conexiones P2P iniciales
- Mayor complejidad en backend (13 pts en chat)

**Sprint 3 (91 pts)** - Más ligero

- WebRTC para audio
- Peer.js integration
- Menos historias pero alta complejidad técnica
- US-19 y US-21 son las más complejas (13 pts front/back)

**Sprint 4 (111 pts)** - Medio-alto

- WebRTC para video
- Streaming de cámara
- Galería de participantes
- Similar a S3 pero con UI más compleja

---

## 🎯 Criterios de Estimación Utilizados

### Escala Fibonacci-Like

- **1 pt:** Cambio trivial (toggle, estado simple)
- **2 pts:** Cambio pequeño (validación simple, UI básica)
- **3 pts:** Tarea simple (formulario básico, endpoint CRUD)
- **5 pts:** Tarea moderada (formulario con validaciones, lógica de negocio)
- **8 pts:** Tarea compleja (integración de servicios, UI avanzada)
- **13 pts:** Tarea muy compleja (WebRTC, Socket.io, tiempo real)

### Por Disciplina

**UX (46 pts total)**

- Investigación de usuarios
- Flujos de usuario
- Wireframes
- Testing de usabilidad
- Accesibilidad (WCAG)

**Design (93 pts total)**

- UI Design (Figma/Sketch)
- Sistema de diseño
- Iconografía
- Responsive design
- Heurísticas de Nielsen

**Frontend (183 pts total)**

- HTML/CSS/JavaScript
- Formularios y validaciones
- Integración con APIs
- Estado de aplicación
- WebRTC (peer.js)
- Socket.io cliente
- Responsive implementation

**Backend (169 pts total)**

- API REST endpoints
- Firebase Auth & Firestore
- Node.js/TypeScript
- Socket.io server
- WebRTC signaling
- Validación de datos
- Seguridad

---

## 💡 Recomendaciones de Planificación

### Velocity Sugerido

- **Equipo pequeño (3-4 devs):** 40-60 pts/sprint
- **Equipo mediano (5-7 devs):** 80-100 pts/sprint
- **Equipo grande (8+ devs):** 120-150 pts/sprint

### Distribución de Recursos Recomendada

**Sprint 1 (201 pts) - 3-4 semanas**

- 1 UX Researcher
- 2 UI Designers
- 3 Frontend Developers
- 2 Backend Developers
- 1 QA Engineer

**Sprint 2 (225 pts) - 4 semanas**

- 1 UX Researcher
- 2 UI Designers
- 3 Frontend Developers
- 3 Backend Developers (Socket.io complexity)
- 1 QA Engineer

**Sprint 3 (91 pts) - 2 semanas**

- 1 UI Designer
- 2 Frontend Developers (WebRTC)
- 2 Backend Developers (WebRTC)
- 1 QA Engineer

**Sprint 4 (111 pts) - 2-3 semanas**

- 1 UX Researcher
- 2 UI Designers (video gallery)
- 2 Frontend Developers
- 2 Backend Developers
- 1 QA Engineer

### Riesgos por Sprint

**S1 - Riesgo Medio**

- OAuth integration puede tomar más tiempo
- Configuración inicial de Firebase

**S2 - Riesgo Alto**

- Socket.io requiere expertise
- Testing de concurrencia complejo
- Sincronización de estado en tiempo real

**S3 - Riesgo Alto**

- WebRTC tiene curva de aprendizaje empinada
- Issues de NAT/firewall
- Configuración de STUN servers

**S4 - Riesgo Medio-Alto**

- Streaming de video pesado
- Optimización de ancho de banda
- UX de galería compleja

---

## 📝 Notas de Uso

Este documento debe actualizarse después de cada sprint para:

1. Comparar story points estimados vs. reales
2. Ajustar velocity del equipo
3. Refinar escala de estimación
4. Documentar lecciones aprendidas

**Última actualización:** 2024  
**Próxima revisión:** Después del Sprint 1
