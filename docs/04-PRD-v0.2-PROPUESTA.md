# Definite Fitnes — PRD v0.2 (PROPUESTA)

| | |
|---|---|
| **Versión** | 0.2.2 — propuesta |
| **Estado** | **Pendiente de aprobación del propietario. No es definitiva** y no autoriza el inicio del desarrollo. |
| **Sustituye a** | Nada todavía. `docs/01-PRD.md` (v0.1) sigue vigente e intacto hasta que apruebes esta propuesta. Las versiones anteriores se conservan en Git (v0.2: a5d6863; v0.2.1: abb3921). |
| **Documentos relacionados** | [05 — Mapa de navegación v0.2](05-MAPA-NAVEGACION-v0.2-PROPUESTA.md) · [06 — Registro de decisiones](06-REGISTRO-DECISIONES-v0.2.md) · [07 — Trazabilidad de la auditoría](07-TRAZABILIDAD-AUDITORIA-v0.2.md) · [03 — Auditoría cruzada](03-AUDITORIA-CRUZADA.md) |
| **Nombre** | "Definite Fitnes" es **provisional**: su validación como marca está pendiente (DEC-10, DEC-53). |

---

## 0. Cómo leer este documento

### 0.1 Etiquetas de estado

Cada regla y cada decisión lleva una etiqueta. **Ninguna regla sin la etiqueta [APR] debe tratarse como aprobada.**

| Etiqueta | Significado |
|---|---|
| **[APR]** | Aprobada por ti: procede de tus instrucciones originales o de tus decisiones posteriores. |
| **[PROP]** | Propuesta de Claude. Pendiente de tu aprobación. |
| **[VAL]** | Requiere validación legal, técnica o profesional antes de aplicarse. Puede combinarse con las anteriores. |
| **[PEND]** | Decisión abierta. El documento describe alternativas, pero no elige. |

### 0.2 Etiquetas de etapa

| Etiqueta | Significado |
|---|---|
| **ET1–ET11** | Etapas del plan. **Desde la v0.2.2 las etapas llevan el prefijo ET** (AF-06) para no confundirse con las pantallas E01–E11 de Entrenamiento. Los documentos 01–03 y las versiones anteriores usan la notación E1–E11 |
| **ET6.1** | MVP, entrega 1: acceso, registro, onboarding, inicio y perfil |
| **ET6.2** | MVP, entrega 2: entrenamiento y progreso |
| **ET6.3** | MVP, entrega 3: nutrición |
| **ET7** | Gamificación y avatar |
| **ET8** | Asistente de IA |
| **ET9** | Comunidad |
| **ET10** | Suscripciones e integraciones |
| **POST** | Pospuesto fuera del MVP; etapa exacta por definir (DEC-59) |
| **MEN** | Habilitación futura de menores (13–17) y de la experiencia del tutor. **Fuera de la beta y del MVP** (DEC-44); etapa por definir |
| **β** | Solo durante la beta cerrada (DEC-68) |

### 0.3 Identificadores

- **RN-01 a RN-121** conservan el número de la v0.1 para mantener la trazabilidad. Las reglas nuevas empiezan en **RN-122**.
- Una regla de la v0.1 que pasa a ser decisión pendiente se marca **"Suspendida → DEC-xx"**: no se elimina, queda como alternativa documentada.
- **DEC-xx** remite al [registro de decisiones](06-REGISTRO-DECISIONES-v0.2.md). **X-, P-, I-, R-, E-** remiten a hallazgos de la [auditoría](03-AUDITORIA-CRUZADA.md).

### 0.4 Cambios principales respecto a la v0.1

1. El MVP no aplica restricciones de Premium (DEC-01).
2. La Etapa 6 se divide en tres entregas internas (DEC-02).
3. Tema claro, optimización para tablets, biblioteca amplia de recetas y programas extensos pasan a etapas posteriores sin salir de la visión (DEC-03).
4. El modo sin conexión se limita a la sesión de entrenamiento en curso (DEC-04).
5. La base de alimentos inicial es acotada, centrada en México y con fuentes verificables (DEC-05).
6. México es el primer país; las reglas por país son configurables (DEC-06).
7. El consentimiento de datos de salud se separa de la creación de la cuenta (DEC-08).
8. Apple y Google se incluyen sin permitir saltarse la verificación de edad (DEC-09).
9. **Todas las experiencias específicas para menores pasan a decisiones pendientes** (DEC-30 a DEC-41). Las reglas de la v0.1 sobre menores quedan como alternativas, no como reglas.
10. Se añade una **arquitectura funcional** con un servicio central de políticas (edad, país, consentimientos, permisos del tutor, plan y etapa).
11. Se corrigen las contradicciones, huecos e identificadores señalados por la auditoría.

### 0.5 Cambios en la v0.2.1

Incorpora **solo** las dos decisiones aprobadas por el propietario; ninguna otra decisión cambia.

1. **DEC-68:** la primera beta es cerrada, gratuita, solo para mayores de 18, por invitación y sin cobros ni suscripciones. La gratuidad de la beta no es permanente (RN-141).
2. **DEC-44 (aprobada):** el MVP y la beta no admiten menores de 18. El objetivo futuro de admitir desde los 13 años se conserva.
3. Las funciones solo necesarias para menores y tutores pasan al marcador **MEN** (habilitación futura), documentadas y sin eliminar.
4. Nuevas reglas RN-141 (no gratuidad permanente), RN-142 (edad mínima 18 en la beta) y RN-143 (acceso por invitación); RN-01 y RN-140 ajustadas.
5. DEC-67 se redefine como política de transición de la beta gratuita a planes comerciales (pendiente) y se añade DEC-69 (mecanismo de invitaciones, pendiente).
6. Se reordena §12 según lo que bloquea la beta y lo que bloquea la habilitación futura de menores.

### 0.6 Cambios en la v0.2.2

Correcciones documentales de la auditoría final y dos incorporaciones pedidas por el propietario. **Ninguna decisión aprobada cambia y ninguna propuesta pasa a ser regla aprobada.**

1. **AF-06:** las etapas se escriben con el prefijo **ET** (ET1–ET11, ET6.1–ET6.3) para no confundirse con las pantallas E01–E11. Los documentos 01–03 y las versiones anteriores conservan la notación E.
2. **AF-13:** los objetivos corporales de menores vuelven a figurar como pendientes (DEC-35); DEC-14 solo excluye las predicciones corporales.
3. **AF-17:** §12 se genera desde la tabla única de bloqueos del registro (sección 6) y ahora incluye DEC-54, DEC-55, DEC-56 y DEC-65 en ET6.1.
4. **AF-03, AF-16, AF-28:** DEC-65 citada en RN-133; referencia de RN-114 corregida a F16/F17; RN-118 a RN-120 con formato de regla.
5. **Correo transaccional:** requisitos formales en §8.5; proveedor pendiente (DEC-72).
6. **Documentos legales:** requisito previo para invitar a usuarios reales (DEC-70, RN-144); redacción y validación pendientes (DEC-71).

---

## 1. Descripción del producto

**Definite Fitnes** es una plataforma fitness integral para iOS y Android que reúne entrenamiento multidisciplinario, nutrición, bienestar, seguimiento de progreso con predicciones transparentes, gamificación, avatar, personalización visual, comunidad privada y un asistente de IA, todo alrededor de un perfil central que adapta la experiencia a cada persona. [APR]

- **Lemas:** "Fitness, a tu manera." · "Tu vida. Tus objetivos. Tu progreso." [APR]
- **Plataformas:** iOS y Android, prioridad móvil. Optimización específica para tablets: **POST** (DEC-03). [APR]
- **Primer mercado:** México, en español. Arquitectura preparada para otros países e idiomas (DEC-06). [APR]
- **Primer lanzamiento:** beta cerrada, gratuita, por invitación, solo para mayores de 18 años y sin cobros ni suscripciones (DEC-68, DEC-44). La gratuidad de la beta no es permanente (RN-141). [APR]
- **Modelo de negocio:** freemium con suscripción; los pagos se implementan en ET10 (DEC-01, DEC-22). [APR]

### 1.1 Qué no es [APR]

- No es una app limitada al gimnasio ni una calculadora de calorías.
- No es un servicio médico: no diagnostica, no prescribe y no sustituye a profesionales de salud.
- No es una red social: la comunidad es opcional, secundaria y privada por defecto.

### 1.2 Principios de producto

| N.º | Principio | Estado |
|---|---|---|
| PR-1 | La persona elige qué módulos usa; solo se piden los datos que esas funciones necesitan (minimización). | [APR] DEC-11 |
| PR-2 | No se inventan datos nutricionales, fechas ni resultados. Si no hay datos suficientes, se dice. | [APR] |
| PR-3 | Se premia la constancia y los hábitos; nunca se castiga el descanso ni se fomenta el exceso. | [APR] DEC-16 |
| PR-4 | Privacidad por defecto: nada se comparte sin una acción explícita del usuario. | [APR] DEC-11 |
| PR-5 | Seguridad, privacidad, información esencial y ayuda nunca se bloquean por suscripción. | [APR] DEC-21 |
| PR-6 | Protección reforzada de menores, con controles por edad. | [APR] DEC-12 (los controles concretos están pendientes) |
| PR-7 | No se promueven restricciones alimentarias, objetivos calóricos restrictivos ni ideales corporales. | [APR] DEC-13 |
| PR-8 | **Mientras una decisión sobre menores esté pendiente, la función afectada permanece desactivada para ese tramo de edad.** | [PROP] DEC-64, derivada de PR-4 |

---

## 2. Propuesta de valor y diferenciación [APR]

Una plataforma que combina entrenamiento personalizado, nutrición, bienestar, IA, seguimiento de progreso y gamificación, y que se adapta a las actividades y preferencias de cada persona.

**Cinco pilares:**

1. Entrenamiento multidisciplinario, con métricas propias de cada disciplina.
2. Nutrición y hábitos saludables con información de fuentes confiables.
3. Inteligencia artificial híbrida: la app funciona sin IA; la IA añade explicación y organización.
4. Seguimiento de progreso con **predicciones transparentes** y gamificación sana.
5. Comunidad social opcional y privada.

**Diferenciador principal:** el módulo de progreso con predicciones basadas en datos registrados, rangos, calidad de datos e incertidumbre explícita, sin promesas.

---

## 3. Público objetivo

### 3.1 Tramos de edad

| Tramo | Estado |
|---|---|
| **18+** | Experiencia completa. [APR] |
| **16–17** | Experiencia diferenciada. **El contenido concreto está pendiente** (DEC-33). **No admitido en la beta ni en el MVP** (DEC-44). [APR] tramo · [PEND] contenido |
| **13–15** | Experiencia diferenciada. **El contenido concreto está pendiente** (DEC-32). **No admitido en la beta ni en el MVP** (DEC-44). [APR] tramo · [PEND] contenido |
| **< 13** | No admitidos. La edad mínima de 13 años es la intención de producto **pendiente de validación legal** (DEC-18). [APR][VAL] |

**Alcance de la beta y del MVP:** solo personas de **18 años o más** (DEC-44). [APR] Es una decisión de alcance del lanzamiento inicial: **no elimina** el objetivo de admitir usuarios desde los 13 años con experiencias diferenciadas (DEC-12, DEC-18). Todo lo necesario para menores y tutores se conserva documentado como **habilitación futura de menores (MEN)**, que requiere resolver antes DEC-18, DEC-30 a DEC-39, DEC-41, DEC-45 y DEC-64.

### 3.2 Perfiles de uso (ejemplos) [PROP]

- Principiante que quiere empezar: guía simple, rutinas en casa, motivación.
- Deportista de una disciplina: métricas propias de su deporte.
- Usuario de gimnasio con experiencia: registro rápido de series, historial y estadísticas.
- Persona enfocada en hábitos: alimentación, hidratación, descanso y constancia.
- Familia: varias personas con cuentas independientes bajo un mismo pago (ET10).
- Madre, padre o tutor: autoriza y gestiona permisos de la cuenta de un menor (detalle pendiente).

### 3.3 Roles

| Rol | Descripción | Estado |
|---|---|---|
| **Usuario** | Titular de una cuenta y dueño único de sus datos. | [APR] |
| **Tutor** | Adulto que autoriza la cuenta de un menor. Sus funciones exactas están pendientes (DEC-30, DEC-31, DEC-39). **No existe en la beta ni en el MVP** (DEC-44); habilitación futura (MEN). | [APR] rol · [PEND] alcance |
| **Administrador familiar** | Adulto que paga el plan Familiar. Gestiona integrantes y suscripción; **no tiene acceso automático a datos personales** de los integrantes. | [APR] DEC-15 |
| **Integrante familiar** | Usuario dentro de un plan Familiar con cuenta, perfil, progreso y datos propios. | [APR] |
| **Soporte y moderación** | Personal de Definite Fitnes con acceso mínimo y registrado. Herramientas por definir (DEC-40). | [PROP] |

- **RN-122** Tutor y administrador familiar son roles independientes: uno no implica el otro. [PROP]

---

## 4. Arquitectura funcional

> Esta sección describe **responsabilidades**, no tecnologías. La elección tecnológica corresponde a la Etapa 4 y no está tomada.

### 4.1 Capas [APR]

| Capa | Responsabilidad |
|---|---|
| **Interfaz** | Pantallas y componentes. No contiene reglas de negocio ni decide permisos. |
| **Lógica de negocio** | Reglas de cada módulo (por ejemplo, cómo se calcula una tendencia). |
| **Servicios** | Operaciones expuestas por el servidor; cada una comprueba identidad, permisos y políticas. |
| **Datos** | Almacenamiento con aislamiento por usuario. |

**RN-121** (sin cambios) Los módulos se comunican mediante servicios definidos, nunca leyendo directamente los datos de otro módulo. [PROP]

### 4.2 Servicios transversales

| Servicio | Responsabilidad | Etapa |
|---|---|---|
| **Identidad y acceso** | Registro, inicio de sesión (correo, Apple, Google), sesiones, recuperación | ET6.1 |
| **Servicio de políticas** | Decide si una función está disponible para un usuario concreto (ver 4.3) | ET6.1 |
| **Consentimientos** | Registra qué consintió cada usuario o tutor, cuándo y con qué versión del aviso; permite retirarlo | ET6.1 |
| **Perfil central** | Datos de perfil, módulos activos, preferencias | ET6.1 |
| **Derechos sobre los datos** | Exportación, eliminación, periodo de gracia, solicitudes ARCO | ET6.1 |
| **Notificaciones** | Recordatorios y avisos, respetando las políticas | ET6.1 (uso real desde ET6.2) |
| **Correo transaccional** | Mensajes de cuenta y seguridad (verificación, recuperación, avisos). Requisitos en §8.5; proveedor pendiente (DEC-72) | ET6.1 |
| **Catálogo de contenido** | Ejercicios, alimentos, recetas y programas, cada elemento con su fuente | ET6.2 / ET6.3 |
| **Eventos de actividad** | Registro de hechos (sesión completada, hábito cumplido) que usarán Progreso y, desde ET7, la gamificación | ET6.2 |
| **Derechos de plan** | Qué incluye cada plan; en el MVP todos los usuarios tienen las funciones disponibles (DEC-01) | ET6.1 (estructura) / ET10 (planes reales) |
| **Registro de auditoría** | Eventos de seguridad y accesos de soporte, sin datos sensibles | ET6.1 |
| **Pasarela de IA** | Acceso de la IA a datos autorizados mediante funciones limitadas | ET8 |
| **Compartir y comunidad** | Publicación explícita, amistades, bloqueos, reportes | ET9 |
| **Integraciones** | Apple Health, Health Connect, wearables, Spotify | ET10 |

### 4.3 Servicio de políticas

Es la pieza central para cumplir con edades, países y consentimientos sin reconstruir la app cada vez que cambie una regla.

**Cada función** tiene una clave (por ejemplo `nutrition.food_log`, `progress.body_measurements`, `community.enable`). Antes de mostrarla o ejecutarla, el servidor evalúa:

| Factor | Ejemplo | Fuente |
|---|---|---|
| País | México | DEC-06, DEC-43 |
| Tramo de edad | 13–15, 16–17, 18+ | Fecha de nacimiento |
| Consentimientos otorgados | Datos de salud: sí/no | Servicio de consentimientos |
| Permisos del tutor | Comunidad habilitada: sí/no | Pendiente (DEC-39); no aplica en la beta |
| Plan | En el MVP, todos iguales | DEC-01 |
| Disponibilidad por etapa | La función existe o no todavía | Plan de etapas |
| Fase de lanzamiento | Beta cerrada: solo 18+, acceso por invitación, sin planes | DEC-68, DEC-44 |

**Reglas del servicio de políticas**

- **RN-123** La decisión se toma en el servidor. El teléfono solo muestra lo que el servidor permite. [APR] (autorización en servidor)
- **RN-124** Las reglas se guardan como **configuración por país y tramo de edad**, no escritas dentro del código, para poder cambiarlas tras una validación legal sin publicar una versión nueva. [PROP] (deriva de DEC-06)
- **RN-125** Si una regla no está definida para una combinación (por ejemplo, una función para 13–15 en un país), el resultado es **"no disponible"**. [PROP] DEC-64
- **RN-126** Cuando una función no está disponible, la interfaz explica el motivo de forma neutral (por ejemplo, "Esta función requiere tu permiso para usar datos de salud" o "Esta función no está disponible para tu edad"), sin culpa ni presión. [PROP]

### 4.4 Módulos y conexiones

El **perfil central** alimenta a todos los módulos; cada módulo produce datos que otros aprovechan a través de servicios.

| Origen | Destino | Qué fluye | Etapa |
|---|---|---|---|
| Perfil / onboarding | Todos | Tramo de edad, objetivos, módulos activos, actividades, preferencias | ET6.1 |
| Consentimientos y políticas | Todos | Qué funciones están disponibles | ET6.1 |
| Entrenamiento | Progreso | Sesiones → estadísticas, marcas, tendencias, predicciones | ET6.2 |
| Entrenamiento | Inicio | Resumen del día y próximas actividades | ET6.2 |
| Nutrición | Progreso | Hábitos y promedios | ET6.3 |
| Nutrición | Inicio | Resumen del día y hábitos | ET6.3 |
| Progreso | Inicio | Objetivos activos y avance | ET6.2 |
| Entrenamiento, nutrición, progreso | Gamificación | Eventos de constancia | Registro desde ET6.2; uso en ET7 |
| Gamificación | Avatar / personalización | Recompensas | ET7 |
| Progreso | Asistente | Resúmenes autorizados | ET8 |
| Gamificación / entrenamiento | Comunidad | Lo que el usuario decide compartir | ET9 |
| Integraciones | Entrenamiento / progreso | Datos importados con su origen | ET10 |
| Plan | Todos | Funciones incluidas | ET10 |

---

## 5. Etapas de desarrollo y alcance

### 5.1 Etapas

| Etapa | Contenido | Estado |
|---|---|---|
| ET1 | Diagnóstico | Completada |
| ET2 | PRD y mapa de navegación | En curso (esta propuesta) |
| ET3 | Design System y prototipos | Pendiente |
| ET4 | Tecnologías y arquitectura técnica | Pendiente |
| ET5 | Modelo de datos y backend | Pendiente |
| **ET6.1** | Acceso por invitación (β), registro, verificación de edad (18+), consentimientos, onboarding, inicio, perfil, privacidad, exportación y eliminación | Pendiente |
| **ET6.2** | Entrenamiento, actividad (calendario e historial) y progreso con predicciones | Pendiente |
| **ET6.3** | Nutrición con base de alimentos acotada | Pendiente |
| **Beta cerrada** | Primera salida del MVP (ET6.1–ET6.3) a personas adultas invitadas; gratuita y sin cobros (DEC-68). **Requisito previo para invitar a usuarios reales:** documentos legales validados (DEC-70, DEC-71) | Pendiente |
| ET7 | Gamificación y avatar | Pendiente |
| ET8 | Asistente de IA | Pendiente |
| ET9 | Comunidad | Pendiente |
| ET10 | Suscripciones, pagos e integraciones | Pendiente |
| ET11 | Pruebas y lanzamiento | Pendiente |
| MEN | Habilitación futura de menores y experiencia del tutor (incluidas sus páginas web) | Etapa por definir; requiere validación legal |

**RN-127** Cada entrega del MVP se prueba y se revisa contigo antes de empezar la siguiente. [APR] DEC-02

### 5.2 Alcance por módulo

La visión completa se conserva. Esta tabla separa lo que entra en el MVP de lo que viene después.

| Módulo | MVP | Posterior |
|---|---|---|
| 1. Registro y onboarding | **ET6.1**: invitación a la beta, correo, Apple y Google, verificación de edad (18+), consentimientos separados, onboarding condicional | Consentimiento parental y experiencias por edad (MEN); verificación en dos pasos (POST) |
| 2. Inicio | **ET6.1** estructura; tarjetas de cada módulo al llegar su entrega | Organización personalizada del inicio (ET10); recomendaciones con IA (ET8) |
| 3. Nutrición | **ET6.3**: resumen, registro, base acotada, detalle con fuente, alternativas, alimento propio, hábitos, historial, **recetas básicas** | **Biblioteca amplia de recetas (POST)**; código de barras y foto de platillos (POST) |
| 4. Entrenamiento | **ET6.2**: disciplinas con métricas propias (cuáles: DEC-47) + registro genérico para cualquier actividad; biblioteca, rutinas, sesión, historial, **programas básicos** | **Programas extensos (POST)**; más disciplinas con métricas propias (POST); GPS en vivo (POST); programas avanzados (ET10) |
| 5. Progreso | **ET6.2**: objetivos, registros, gráficos, tendencias, predicciones con rango y calidad | Comparación de periodos y estadísticas ampliadas (ET10) |
| 6. Personalización | **ET6.1**: tema oscuro, color de acento básico, tamaño de texto, reducción de animaciones | **Tema claro (POST)**; paletas, tarjetas, organización (ET10) |
| 7. Gamificación | Registro de eventos desde ET6.2 | Todo el módulo (ET7) |
| 8. Avatar | Inicial o avatar simple por defecto (foto: DEC-56) | Avatar personalizable (ET7) |
| 9. Comunidad | — | Todo el módulo (ET9) |
| 10. Asistente IA | — | Todo el módulo (ET8) |
| 11. Integraciones | Notificaciones | Apple Health, Health Connect, wearables, Spotify (ET10) |
| Suscripciones | **Sin restricciones comerciales** (DEC-01) | Planes y pagos (ET10) |
| Tablets | La app se usa en tablets **sin optimización específica** (viabilidad técnica: DEC-66) | **Diseños de dos paneles y barra lateral (POST)** |
| Modo sin conexión | **Solo la sesión de entrenamiento en curso** (DEC-04) | Sincronización sin conexión completa (POST) |
| Menores y tutores | **No incluidos** (DEC-44): beta y MVP solo 18+ | Consentimiento parental, experiencias 13–15 y 16–17, páginas web del tutor (MEN) |
| Acceso | **Solo por invitación** durante la beta (DEC-68); mecanismo: DEC-69 | Condiciones de acceso posteriores a la beta: por definir |

---

## 6. Requisitos funcionales por módulo

### 6.1 Módulo 1 — Registro, acceso y onboarding [ET6.1]

**Funciones:** bienvenida; **invitación a la beta** (β); verificación de edad antes de cualquier dato personal; registro con correo o con Apple/Google; verificación de correo; inicio de sesión; recuperación de cuenta; consentimientos separados; onboarding condicional. La solicitud de consentimiento parental queda para la habilitación futura de menores (MEN).

**Verificación de edad y acceso**

- **RN-01** (modificada en v0.2.1) La fecha de nacimiento se pide antes de cualquier otro dato personal (en la beta, justo después de validar la invitación, que no es un dato personal), en una pantalla neutra que no sugiere qué edad "sirve". [PROP] · *La suficiencia de este método se valida en DEC-31.* [VAL]
- **RN-02** (modificada) Si la edad es menor que la mínima del país, no se crea cuenta ni se guardan datos personales. Si el dispositivo debe recordar ese bloqueo y cómo, se decide con validación legal (E-12). [PROP][VAL]
- **RN-03** La fecha de nacimiento no la puede editar el usuario; la corrección se solicita a soporte. [PROP]
- **RN-128** **Ningún método de autenticación permite crear una cuenta sin pasar por la verificación de edad.** Si alguien entra con Apple o Google y no tiene cuenta, se le lleva a la verificación de edad antes de crear nada; durante la beta, antes debe validar una invitación (A17). [APR] DEC-09, DEC-68
- **RN-142** Durante la beta y el MVP, la edad mínima configurada es **18 años** (DEC-44). Con menos de 18 no se crea cuenta ni se guardan datos personales, y A11 explica que la beta es solo para personas adultas, sin sugerir cambiar la fecha. [APR] edad · [PROP] texto y comportamiento
- **RN-143** Durante la beta solo se crea una cuenta con una invitación válida (A17), comprobada antes de pedir la fecha de nacimiento. Quién invita, cuántas invitaciones hay, si son de un solo uso y si caducan: DEC-69. [APR] acceso por invitación · [PEND] mecanismo
- **RN-05** Contraseña de al menos 10 caracteres, rechazada si aparece en listas de contraseñas filtradas, sin reglas arbitrarias de símbolos. [PROP]
- **RN-06** Los mensajes de inicio de sesión y recuperación no revelan si un correo está registrado. [PROP]
- **RN-07** Límite de intentos de inicio de sesión y recuperación; al superarlo, se muestra un estado de espera con el tiempo restante. [PROP]

**Menores — habilitación futura (MEN), fuera de la beta y del MVP (DEC-44)**

- **RN-04** (modificada) Un menor no accede a la app hasta que su tutor otorgue el consentimiento. La cuenta queda en estado "pendiente" y no recoge más datos. Plazo de caducidad propuesto: 14 días. [PROP][VAL]
- **RN-111** **Suspendida → DEC-30.** (v0.1 proponía consentimiento para todos los menores de 18.)
- **RN-112** **Suspendida → DEC-31.** (Método de verificación del tutor.)
- **RN-113** Se guarda evidencia de cada consentimiento: quién, cuándo y qué versión del aviso. [PROP][VAL]

**Consentimientos de datos**

- **RN-129** La creación de la cuenta requiere aceptar los Términos y conocer el Aviso de privacidad, pero **no depende** de consentir el tratamiento de datos de salud. [APR] DEC-08 (independencia del consentimiento de salud) · [PROP] (aceptación de Términos)
- **RN-130** Los consentimientos se solicitan por separado y por categoría, en una pantalla propia (A14), y se pueden otorgar después o retirar en cualquier momento (U18). [PROP] (la granularidad exacta: DEC-42 [VAL])
- **RN-131** Si el usuario no otorga un consentimiento, **las funciones que dependen de esos datos permanecen desactivadas** y la app explica cómo activarlas; el resto funciona con normalidad. [APR] DEC-08
- **RN-132** Al intentar usar una función que requiere un consentimiento no otorgado, se muestra la solicitud en contexto (M01), nunca de forma insistente. [PROP]
- **RN-133** La analítica de uso permanece desactivada hasta que el usuario la consienta. [PROP] DEC-65 (deriva de DEC-11)

**Onboarding**

- **RN-08** El onboarding es condicional: solo aparecen las preguntas de los módulos que el usuario eligió. [APR]
- **RN-09** Todo paso no esencial puede omitirse. Esenciales: nombre, objetivos, al menos un módulo. [PROP]
- **RN-10** Una decisión por pantalla y barra de progreso; meta de menos de 3 minutos. [APR] (formularios no interminables) · meta de tiempo [PROP]
- **RN-11** (modificada) Las consideraciones de seguridad (lesiones, condiciones) sirven solo para adaptar y advertir; nunca generan diagnóstico. **Solo se preguntan si el usuario otorgó el consentimiento de datos de salud**; si no, se omiten y se muestran siempre las precauciones generales de cada ejercicio. [APR] no diagnóstico · [PROP] resto
- **RN-12** (modificada) Los objetivos disponibles dependen del tramo de edad. Para menores **no se ofrecen objetivos estéticos ni de restricción** (DEC-13). Qué otros objetivos se ofrecen a cada tramo está pendiente (DEC-32, DEC-33, DEC-35). [APR] principio · [PEND] detalle
- **RN-134** Las medidas corporales (estatura, peso) se piden solo a adultos, son opcionales y requieren el consentimiento de datos de salud. Para menores: DEC-35. [PROP] adultos · [PEND] menores
- **RN-135** El permiso de notificaciones del sistema se solicita cuando exista un recordatorio útil que activar, con explicación previa. [PROP]

**Datos del onboarding y su finalidad**

| Dato | Obligatorio | Finalidad | Consentimiento de salud | Tramos |
|---|---|---|---|---|
| Código de invitación | Sí durante la beta | Acceso a la beta | No | Beta (β) |
| Fecha de nacimiento | Sí | Edad y políticas | No | Todos |
| Correo / cuenta Apple o Google | Sí | Cuenta | No | Todos |
| Nombre o apodo | Sí | Saludo y perfil | No | Todos |
| Objetivos | Sí | Personalización | No* | Todos (lista según tramo) |
| Módulos de interés | Sí | Qué mostrar | No | Todos |
| Actividades y experiencia | Si eligió entrenamiento | Métricas y sugerencias | No* | Todos |
| Disponibilidad | No | Planificación | No | Todos |
| Preferencias alimentarias | No | Filtros | No* | Según DEC-36 |
| Alergias | No | Advertencias | **Sí*** | Según DEC-34 |
| Consideraciones de seguridad | No | Adaptar y advertir | **Sí** | Según DEC-34 |
| Estatura y peso | No | Estimaciones de energía y objetivos | **Sí** | Adultos; menores: DEC-35 |
| Correo del tutor | Solo en la habilitación futura de menores | Consentimiento | No | MEN (fuera de la beta) |

\* La clasificación definitiva de qué datos son "de salud" requiere validación legal (DEC-42). La tabla muestra la propuesta inicial.

### 6.2 Módulo 2 — Inicio [ET6.1, ampliado en cada entrega]

**Contenido de H01:**

1. Encabezado: avatar o inicial, saludo, notificaciones.
2. Saludo: **"Bienvenido, [nombre], ¿qué planeas hacer?"** [APR]
3. Accesos grandes por módulo: **Nutrición** (morado), **Entrenamiento** (amarillo), **Progreso y recompensas** (rosa), **Comunidad** (gris). [APR]
4. Resumen de hoy, próximas actividades, objetivos activos, recomendaciones. [APR]

**Reglas**

- **RN-13** Solo aparecen los accesos y tarjetas de los módulos activos **y ya disponibles** en la entrega actual. [PROP]
- **RN-14** El acceso a Comunidad no aparece antes de ET9. La pestaña "Amigos" antes de ET9: DEC-46. [PEND]
- **RN-15** (modificada) Las recomendaciones del MVP se generan con reglas explicables ("¿por qué veo esto?"). Nunca recomiendan entrenar más tras varios días seguidos de actividad intensa; en su lugar sugieren descanso (aparece en H01 y en el resumen de sesión E09). [APR] no fomentar exceso · [PROP] mecanismo
- **RN-16** Estados vacíos útiles: cada tarjeta explica cómo empezar. [PROP]
- **RN-17** (modificada) El saludo por defecto es exactamente el texto aprobado. Una variante de género neutro ("Te damos la bienvenida, [nombre]") queda **como propuesta** pendiente de tu aprobación. [APR] texto · [PROP] variante
- **RN-136** Durante el MVP, el inicio se adapta automáticamente a los módulos activos; la organización manual de tarjetas llega en ET10 (H03). Activar o desactivar módulos se hace desde el perfil. [PROP] (resuelve X-06)

**Navegación inferior** [APR] propuesta original: Inicio · Actividad · Amigos · Perfil. Aparición por entrega en el mapa (§4.2).

### 6.3 Módulo 3 — Nutrición [ET6.3]

| Función | Etapa |
|---|---|
| Resumen nutricional del día | ET6.3 |
| Registro de alimentos (recientes, favoritos, mis alimentos) | ET6.3 |
| Base de alimentos **acotada** con fuente visible | ET6.3 (DEC-05) |
| Detalle de alimento con información y fuente | ET6.3 |
| Alternativas de alimentos (N09) | ET6.3 |
| Alimento propio, marcado "no verificado" | ET6.3 (menores: DEC-36) |
| Hábitos (agua, frutas y verduras, horarios) | ET6.3 (acceso sin nutrición: DEC-54) |
| Historial | ET6.3 |
| Recetas básicas | ET6.3 (cantidad inicial: DEC-63) |
| **Biblioteca amplia de recetas** | **POST** |
| Recomendaciones personalizadas | Reglas en ET6.3; IA en ET8 |
| Código de barras, foto de platillos | POST |

**Reglas**

- **RN-18** Todo dato nutricional procede de una fuente identificada que se muestra al usuario. **Nunca se generan valores nutricionales con IA.** [APR] · fuentes concretas y licencias: DEC-57 [VAL]
- **RN-19** Si falta un dato, se muestra "sin dato", no cero ni una estimación. [APR]
- **RN-137** La base inicial prioriza alimentos comunes en México. Toda estimación (por ejemplo, de una porción casera) se identifica como tal y nunca se presenta como dato exacto. [APR] DEC-05
- **RN-20** Los alimentos creados por usuarios no entran al catálogo general. [PROP]
- **RN-21** Las referencias de energía para **adultos** usan fórmulas públicas identificadas y se presentan como estimación orientativa. [PROP][VAL]
- **RN-22** No se sugieren ni se permiten metas de energía por debajo de un mínimo de seguridad ni ritmos de pérdida de peso agresivos. **Los valores los define un profesional** (DEC-50). [APR] principio (no dietas extremas) · [VAL] valores
- **RN-23** Sin etiquetas morales para alimentos ni colores de alarma. [PROP] (deriva de DEC-13)
- **RN-24** Advertencias de alérgenos declarados, aclarando que la información puede ser incompleta. Requiere el consentimiento correspondiente (DEC-42). [PROP]
- **RN-25** Ante señales de riesgo (por ejemplo, registros de energía muy bajos y sostenidos), no hay felicitaciones ni rachas: aparece un mensaje de cuidado (M02) con enlace a ayuda (U14). **Los criterios de detección los valida un profesional** (DEC-61). [PROP][VAL]
- **RN-26** Aviso visible: "Información educativa. No sustituye a profesionales de salud." [APR]
- **RN-27** **Suspendida → DEC-36.** Qué funciones nutricionales ven los menores está pendiente. Principio vigente: sin objetivos calóricos restrictivos para menores (DEC-13). [APR] principio · [PEND] detalle

### 6.4 Módulo 4 — Entrenamiento [ET6.2]

**Disciplinas**

| Disciplina | Métricas propias | Etapa |
|---|---|---|
| Registro genérico (cualquier actividad) | Tipo, duración, esfuerzo percibido, notas | ET6.2 [APR] (ninguna actividad queda fuera) |
| Gimnasio | Series, repeticiones, peso, descanso, esfuerzo; volumen y marcas | ET6.2 — propuesta (DEC-47) |
| Running | Distancia, tiempo, ritmo, desnivel manual, esfuerzo | ET6.2 — propuesta (DEC-47) |
| Entrenamiento en casa | Repeticiones o tiempo, circuitos, rondas | ET6.2 — propuesta (DEC-47) |
| Calistenia | Progresiones, repeticiones, isométricos | POST |
| Ciclismo | Distancia, tiempo, velocidad, desnivel | POST |
| Natación | Distancia, largos, estilo, tiempo | POST |
| Fútbol y deportes de equipo | Duración, tipo, posición, notas | POST |

**Funciones**

| Función | Etapa |
|---|---|
| Centro de entrenamiento, biblioteca y detalle de ejercicios | ET6.2 |
| Rutinas propias y sugeridas | ET6.2 |
| Sesión en curso con temporizador de descanso | ET6.2 |
| Registro manual de actividad realizada | ET6.2 |
| Resumen de sesión | ET6.2 |
| Calendario, planificación e historial | ET6.2 |
| Programas básicos | ET6.2 (cantidad: DEC-63) |
| **Programas extensos** | **POST** |
| Programas avanzados y especializados | ET10 |
| GPS en vivo | POST |

**Reglas**

- **RN-28** Cada disciplina tiene su propio formulario y sus estadísticas; no se usa un único modelo para todas. [APR]
- **RN-29** El contenido de ejercicios es propio o con licencia verificada, con nivel y precauciones. [APR] fuentes confiables · licencias: DEC-57 [VAL]
- **RN-30** (modificada) **Modo sin conexión limitado:** una sesión que ya está en curso puede seguir registrándose y consultándose sin conexión; se guarda en el teléfono y se envía al recuperar la conexión. Iniciar una sesión o usar otras funciones requiere conexión en el MVP. [APR] DEC-04
- **RN-31** Se puede editar o eliminar una sesión; estadísticas y predicciones se recalculan. [PROP]
- **RN-32** Los días de descanso se pueden planificar y cuentan como parte del plan, no como fallos. [APR] DEC-16
- **RN-33** Ante muchos días seguidos de alta intensidad o volúmenes inusuales, la app sugiere descanso y no felicita el exceso. Umbrales: validación profesional. [APR] principio · [VAL] umbrales
- **RN-34** Si el usuario declaró consideraciones de seguridad (con consentimiento), los ejercicios relacionados muestran advertencia en el detalle, al añadirlos a una rutina y durante la sesión, y no se sugieren automáticamente. [PROP]
- **RN-35** (modificada) La "modalidad principal" sirve en el MVP solo para personalizar; **no limita funciones** (DEC-01). El límite de una modalidad para el plan Gratis queda como propuesta para ET10 (DEC-62). Si la modalidad elegida aún no tiene métricas propias, se usa el registro genérico con aviso (DEC-55). [APR] sin límites en MVP · [PROP] resto
- **RN-36** **Suspendida → DEC-32 / DEC-33.** Restricciones de entrenamiento por edad pendientes de validación profesional y legal.

### 6.5 Módulo 5 — Progreso y predicciones [ET6.2]

| Función | Etapa |
|---|---|
| Resumen por categoría: actividad, rendimiento, nutrición, bienestar, objetivos | ET6.2 (nutrición desde ET6.3) |
| Crear, seguir, pausar, completar y archivar objetivos | ET6.2 |
| Registrar avances y mediciones | ET6.2 |
| Gráficos, historiales, tendencias | ET6.2 |
| Predicción de fecha con rango y calidad | ET6.2 |
| Explicación del método | ET6.2 |
| Comparación de periodos | ET10 |

**Tipos de objetivo:** constancia, rendimiento, acumulación, bienestar, personal libre [APR]; medida corporal: adultos [PROP], con salvaguardas (RN-22); menores: [PEND DEC-35]. Lo aprobado para menores es que no hay predicciones corporales (DEC-14) ni objetivos estéticos o restrictivos (DEC-13).

**Reglas de predicción**

- **RN-37** Las predicciones usan solo datos registrados por el usuario y métodos estadísticos transparentes. No se usa IA generativa para calcular fechas. [APR]
- **RN-38** Sin datos suficientes no hay predicción; se informa cuántos registros faltan aproximadamente. [APR] · umbral inicial (6 registros en 3 semanas) [PROP][VAL técnica]
- **RN-39** Toda predicción es un **rango de fechas** con indicador de calidad de datos y la frase "Estimación basada en tus registros; no es una garantía". [APR]
- **RN-40** Si la tendencia es plana o contraria, no se muestra fecha; se informa con lenguaje neutro. [APR]
- **RN-41** Si el rango es demasiado amplio para ser útil, se dice así. [APR]
- **RN-42** Se recalcula al cambiar los datos y se muestra la fecha del último cálculo. [PROP]
- **RN-43** (modificada) **No se generan predicciones corporales ni médicas para menores.** Para adultos, las predicciones de peso o medidas nunca prometen resultados y no se muestran si el ritmo implícito supera los límites de seguridad (DEC-50). [APR] DEC-14 · [VAL] límites
- **RN-44** Ninguna comunicación convierte una predicción en promesa. [APR]
- **RN-45** La explicación del método es comprensible para cualquier persona. [APR]
- **RN-138** Durante el MVP no hay límite de objetivos activos ni de historial visible (DEC-01). [APR]

### 6.6 Módulo 6 — Personalización visual

| Opción | Etapa |
|---|---|
| Tema oscuro (identidad predeterminada: negra, moderna, tecnológica) | ET6.1 [APR] |
| Tamaño de texto y reducción de animaciones | ET6.1 |
| Color de acento básico | ET6.1 |
| **Tema claro** | **POST** (DEC-03) |
| Paletas, colores secundarios, estilos de tarjeta | ET10 (posibles funciones Premium) |
| Organización del inicio | ET10 |
| Avatar y accesorios | ET7 |

- **RN-46** Toda combinación de colores ofrecida mantiene un contraste accesible. [APR] · Nivel concreto propuesto: WCAG AA [PROP]
- **RN-47** Las opciones de accesibilidad nunca son Premium. [APR]
- **RN-48** Los colores de módulo son la identidad por defecto. [APR]

### 6.7 Módulo 7 — Gamificación [ET7]

XP, niveles, logros, insignias, retos, misiones, objetivos semanales, recompensas, inventario. [APR]

- **RN-49** Se premian hábitos saludables y constancia, incluido respetar los descansos planificados. [APR]
- **RN-50** Tope diario de XP por actividad física para no incentivar el exceso. [APR] principio · [PROP] mecanismo
- **RN-51** No se pierde XP, nivel ni recompensas por descansar o dejar de usar la app. [APR]
- **RN-52** Rachas semanales con pausa. [PROP]
- **RN-53** Nada de XP ni logros por comer menos, bajar de peso o métricas corporales. [PROP] (deriva de DEC-13)
- **RN-54** Recompensas solo estéticas; sin cajas aleatorias de pago. [PROP]
- **RN-55** El XP se calcula en el servidor. [APR] (autorización en servidor)
- **RN-56** (modificada) Los eventos de actividad se registran desde ET6.2 para no perder historial cuando llegue ET7. [PROP]
- **RN-57** **Suspendida → DEC-32 / DEC-33.** Misiones específicas para menores.

### 6.8 Módulo 8 — Avatar [ET7]

- **RN-58** El avatar es simbólico; su cuerpo no cambia según el peso, las medidas ni el progreso. [APR]
- **RN-59** Opciones inclusivas disponibles gratis. [PROP]
- **RN-60** La progresión se expresa con accesorios y efectos, nunca con un cuerpo "mejor". [APR]
- En el MVP: inicial o avatar simple por defecto. Foto de perfil: DEC-56 [PEND].

### 6.9 Módulo 9 — Comunidad [ET9]

Perfiles, amigos, solicitudes, retos y logros compartidos, rankings opcionales, bloqueo, reportes y controles de privacidad. [APR]

- **RN-61** Desactivada por defecto; activarla es explícito y reversible. [APR]
- **RN-62** Nada se publica automáticamente; cada elemento compartido requiere una acción y muestra una **vista previa** (S11). [APR] · pantalla [PROP]
- **RN-63** Nunca se comparten datos de salud: peso, medidas, alimentos, consideraciones de seguridad, bienestar. [APR]
- **RN-64** Amigos por código, enlace o nombre de usuario exacto; sin acceso a contactos ni ubicación. [PROP]
- **RN-65** Rankings opcionales, entre amigos o dentro de un reto, basados en constancia. [APR] opcionales · [PROP] criterio
- **RN-66** Sin mensajes de texto libre en la primera versión de la comunidad. [PROP] → DEC-40
- **RN-67** Bloqueo inmediato y reporte a un toque. [APR]
- **RN-68** Revisión de reportes con plazo publicado y prioridad para menores. [PROP] → DEC-40
- **RN-69** Filtro de lenguaje ofensivo. [PROP] → DEC-40
- **RN-70** **Suspendida → DEC-32, DEC-33, DEC-40.** Comunidad para menores.

### 6.10 Módulo 10 — Asistente de IA [ET8]

Explica el progreso, ayuda a organizar actividades, explica ejercicios, ofrece información nutricional del catálogo, resuelve dudas de la app, sugiere actividades generales y ayuda con objetivos. [APR]

- **RN-71** Accede solo a datos autorizados mediante servicios específicos y limitados. [APR]
- **RN-72** Las cifras salen de los servicios de la app; la IA no las calcula ni las inventa. [APR]
- **RN-73** Si no tiene un dato, lo dice. [APR]
- **RN-74** No diagnostica ni prescribe tratamientos, dietas terapéuticas, suplementos ni medicamentos. [APR] DEC-17
- **RN-75** Ante señales de crisis muestra recursos de ayuda del país. [PROP][VAL]
- **RN-76** Cada respuesta se identifica como generada por IA; se puede valorar y reportar. [PROP]
- **RN-77** Las conversaciones no se usan para entrenar modelos de terceros; se pueden borrar. [PROP][VAL técnica: condiciones del proveedor]
- **RN-78** Las acciones que proponga requieren confirmación. [PROP]
- **RN-79** Límite diario de mensajes según plan (en ET8 sin plan: límite técnico de costo). [PROP]
- **RN-80** **Suspendida → DEC-41.** Disponibilidad de la IA para menores.

### 6.11 Módulo 11 — Integraciones

| Integración | Etapa | Estado |
|---|---|---|
| Notificaciones | ET6.1 (uso desde ET6.2) | [APR] |
| Apple Health / Health Connect | ET10 | [APR] explorar · menores: DEC-37 [PEND] |
| Wearables (vía las anteriores) | ET10 | [PROP] |
| Spotify | ET10 | [APR] explorar, sin almacenar ni distribuir música |

- **RN-81** Antes de implementar cada integración se revisan su documentación y condiciones oficiales vigentes. [APR]
- **RN-82** Los datos de salud importados no se usan para publicidad ni se comparten con terceros. [PROP]
- **RN-83** Al desconectar una integración se pregunta si conservar o eliminar los datos importados (M04). [PROP]
- **RN-84** Las notificaciones no muestran datos sensibles en la pantalla de bloqueo ni usan lenguaje de culpa. [PROP] (deriva de DEC-16)
- **RN-85** **Suspendida → DEC-32 / DEC-33.** (v0.1 proponía silencio nocturno para menores.)

### 6.12 Perfil, privacidad y cuenta [ET6.1]

- **RN-86** Exportación y eliminación de datos gratuitas para todos. [APR]
- **RN-87** Eliminación con periodo de gracia (propuesta: 30 días) con pantalla de reactivación (A13). Se conserva solo lo que la ley obligue. [PROP][VAL]
- **RN-88** Cambiar correo o contraseña exige reautenticación y avisa al correo anterior. [PROP]
- **RN-89** El usuario ve y cierra sus sesiones abiertas. [PROP]
- **RN-90** (modificada) Derechos ARCO (acceso, rectificación, cancelación, oposición) y revocación del consentimiento: acceso desde U05, U18 y U14, con canal de contacto publicado. **El procedimiento requiere validación legal.** [APR] eliminación y exportación · [VAL] procedimiento
- **RN-139** U18 muestra todos los consentimientos del usuario con su estado y fecha, y permite retirarlos; al retirar uno, las funciones dependientes se desactivan y se informa qué ocurre con los datos ya guardados. [PROP][VAL]

---

## 7. Modelo de suscripción previsto (ET10)

> **En el MVP no hay pagos ni restricciones comerciales** (DEC-01). La beta cerrada es gratuita y sin cobros ni suscripciones (DEC-68). Todo esta sección se implementa en ET10; **no se implementan cobros ni suscripciones antes**.

### 7.1 Planes [APR] DEC-19

| Plan | Precio | Personas |
|---|---|---|
| Gratis | $0 | 1 |
| Premium mensual | $50 MXN/mes | 1 |
| Premium anual | $500 MXN/año | 1 |
| Familiar mensual | $200 MXN/mes | Hasta 6, incluido el administrador |

### 7.2 Distribución Gratis / Premium — propuesta para ET10 [PROP]

| Área | Gratis | Premium / Familiar |
|---|---|---|
| Seguridad, privacidad, ayuda, exportar y eliminar | **Siempre completo** [APR] | Completo |
| Modalidades | Una principal + registro genérico | Todas |
| Rutinas propias | Límite por definir (v0.1: 3) | Ilimitadas |
| Objetivos activos | Límite por definir (v0.1: 3) | Ilimitados |
| Historial | Todo se conserva; vista limitada por definir (v0.1: 90 días) | Completo |
| Predicciones | DEC-48 | DEC-48 |
| Estadísticas | Básicas | Ampliadas y comparación de periodos |
| Personalización | Básica + accesibilidad completa | Ampliada |
| Programas | Básicos | Avanzados y especializados |
| Asistente IA | Límite diario menor | Límite ampliado |

Las cifras concretas son la decisión DEC-62.

### 7.3 Reglas de suscripción

- **RN-91** Nunca se bloquean seguridad, privacidad, información esencial, ayuda, recursos de crisis, exportación ni eliminación. [APR]
- **RN-92** Los datos nunca se retienen como rehén: al bajar de plan nada se borra; lo que excede queda en solo lectura y exportable, y el usuario elige qué mantener activo (U19). [PROP]
- **RN-140** (modificada en v0.2.1) **Transición de la beta gratuita a planes comerciales:** qué ocurre con las cuentas, los datos y lo creado por quienes participaron en la beta cuando se activen los planes (por ejemplo, aviso previo, periodo de cortesía, conservar lo creado) es una política pendiente (DEC-67). RN-92 (no borrar nada) sigue siendo una propuesta. [PEND]
- **RN-141** **La beta gratuita no garantiza gratuidad permanente.** Se informa de forma clara en la invitación (A17), en los términos de la beta (A12) y antes de crear la cuenta, sin presentar la gratuidad actual como permanente. [APR] DEC-68
- **RN-93** El derecho a Premium se valida en el servidor. [APR]
- **RN-94** Precios, renovación y cancelación claros; cancelar tan fácil como contratar. [PROP]
- **RN-95** No se implementan pagos hasta definir proveedores, comisiones, reglas y condiciones de las tiendas. [APR] DEC-22 · Uso de los sistemas de compra de Apple y Google para bienes digitales [PROP][VAL]
- **RN-96** Sin presión artificial en la pantalla de planes. [PROP]
- **RN-97** Compras de menores: no aplica en la beta ni en el MVP (DEC-44); para la habilitación futura: DEC-38. [PEND] (v0.1 proponía no mostrarles ofertas)

### 7.4 Plan Familiar

- **RN-99** Máximo 6 personas incluido el administrador. [APR]
- **RN-100** Cada integrante tiene cuenta, perfil, progreso y datos propios; solo se comparte la suscripción. [APR]
- **RN-101** El administrador ve solo nombre visible, estado de la invitación y fecha de ingreso; no tiene acceso automático a ningún dato personal. [APR] principio DEC-15 · [PROP] lista exacta
- **RN-98** El administrador debe ser adulto. [PROP]
- **RN-102** Invitación por enlace o código de un solo uso, con caducidad (propuesta: 7 días); la persona debe aceptarla en U17. [PROP]
- **RN-103** Un integrante puede salir cuando quiera; el administrador puede retirarlo; en ambos casos pasa a Gratis sin perder datos. [PROP]
- **RN-104** Una persona pertenece a un solo grupo a la vez. [PROP]
- **RN-105** Espera entre grupos (propuesta: 30 días) → DEC-49. [PEND]
- **RN-106** Si el pago falla o se cancela, todos pasan a Gratis al final del periodo, con aviso. [PROP]
- **RN-107** Si un integrante ya paga Premium individual, U17 se lo avisa antes de aceptar. [PROP]
- **RN-108** **Suspendida → DEC-38.** Participación de menores en planes familiares.
- **RN-109** Los integrantes no ven datos de otros integrantes. [APR]
- **RN-110** La administración se puede transferir a otro adulto que acepte. [PROP]

---

## 8. Privacidad, consentimiento y seguridad

### 8.1 Seguridad [APR] (referencias: OWASP MASVS, ASVS y API Security Top 10)

- Autenticación segura; tokens de corta duración; almacenamiento seguro en el dispositivo.
- Autorización en el servidor y aislamiento de datos por usuario.
- Cifrado en tránsito y en reposo; protección adicional para datos sensibles.
- Validación de entradas en el servidor; límites de uso.
- Secretos fuera del código y del repositorio.
- Copias de seguridad con pruebas de restauración.
- Registro de eventos de seguridad sin datos sensibles; monitoreo.
- Actualización de dependencias; pruebas de seguridad antes del lanzamiento.
- Exportación y eliminación de datos.

### 8.2 Privacidad

- Privacidad por defecto y minimización [APR] DEC-11.
- **Beta:** se mantienen todas las obligaciones legales y de privacidad aplicables a personas adultas (aviso de privacidad, consentimientos, derechos ARCO, exportación y eliminación, seguridad). Que la beta sea gratuita y cerrada no las reduce. [APR] DEC-68
- Aviso de privacidad por capas; aviso específico para tutores [PROP][VAL].
- **Consentimientos separados y granulares** (RN-129 a RN-133, RN-139).
- **RN-118** Sin publicidad de terceros en la primera versión y sin venta de datos personales. [PROP]
- **RN-119** Datos de menores: mínima cantidad posible y sin analítica más allá de métricas agregadas y anónimas. [PROP] → validación en DEC-34 (MEN)
- **RN-120** Sin contenido de "antes y después" corporal ni lenguaje de cuerpo ideal para ninguna edad. [APR] DEC-13

### 8.3 Clasificación de datos (propuesta) [PROP][VAL] DEC-42

| Categoría | Ejemplos | ¿Datos de salud? | Consentimiento propuesto |
|---|---|---|---|
| Cuenta | Correo, credenciales | No | Necesario para el servicio |
| Perfil | Nombre, fecha de nacimiento, objetivos, módulos | No (por validar los objetivos) | Necesario para el servicio |
| Actividad física | Sesiones, marcas | **Por validar** | Por validar |
| Alimentación | Registros de comidas, preferencias | **Por validar** | Por validar |
| Alergias y consideraciones de seguridad | Lesiones, condiciones, alergias | **Sí (propuesta)** | Expreso |
| Medidas corporales | Peso, estatura | **Sí (propuesta)** | Expreso |
| Bienestar | Sueño, ánimo, energía | **Por validar** | Por validar |
| Datos importados | Apple Health, Health Connect | **Sí (propuesta)** | Expreso + permiso del sistema |
| Uso de la app | Analítica | No | Opcional (RN-133) |

**Riesgo importante:** si la validación legal concluye que la actividad física y la alimentación son datos de salud, la mayor parte de la app dependería de ese consentimiento. Esto cambiaría la experiencia de quien no lo otorga y debe resolverse antes de ET6.1 (DEC-42).

### 8.4 Reglas por país [APR] DEC-06

- México es el primer país. Los requisitos legales mexicanos **no se asumen universales**.
- Edad mínima, edad de consentimiento, textos legales, recursos de ayuda y fuentes de alimentos se configuran por país (RN-124).
- Cómo se determina el país del usuario: DEC-43 [PEND].

### 8.5 Servicio de correo transaccional

> **Estado:** la necesidad del servicio está documentada por instrucción del propietario. Los requisitos son **propuestas** [PROP] salvo que se indique otra cosa. **La selección del proveedor está pendiente (DEC-72).** No se fijan plazos, volúmenes ni límites: donde hacen falta, figuran como "valor por definir".

**Mensajes que el servicio debe enviar**

| Mensaje | Pantalla o regla | Etapa | Estado |
|---|---|---|---|
| Código de verificación de correo | A05 | ET6.1 | [PROP] |
| Enlace de recuperación de contraseña | A07 → A08 | ET6.1 | [PROP] |
| Aviso al correo anterior tras cambiar correo o contraseña | RN-88, U06 | ET6.1 | [PROP] |
| Aviso de exportación de datos lista | U12 | ET6.1 | [PROP] |
| Confirmación de la solicitud de eliminación de la cuenta | U13, A13 | ET6.1 | [PROP] |
| Respuesta a solicitudes de derechos ARCO | U14, RN-90 | ET6.1 | [PROP][VAL] |
| Invitación a la beta | A17 | ET6.1 | [PEND DEC-69]: depende de si las invitaciones se envían por correo |
| Correos al tutor | T01, T03, T04 | MEN | Fuera de la beta |
| Avisos de plan e invitaciones familiares | U17, U19 | ET10 | Fuera de la beta |

**Requisitos**

| ID | Requisito | Estado |
|---|---|---|
| CT-01 | Los mensajes de verificación y recuperación se entregan de forma fiable; el usuario puede pedir un reenvío (A05). Plazo objetivo de entrega: valor por definir | [PROP] |
| CT-02 | El dominio remitente se autentica con los estándares habituales de correo (SPF, DKIM y DMARC) para reducir suplantación y envíos a spam | [PROP] |
| CT-03 | Los correos **no incluyen datos de salud** ni datos de otras personas; solo el mínimo necesario (código o enlace) | [PROP] (deriva de DEC-11) |
| CT-04 | Los enlaces y códigos son de un solo uso y caducan; duración: valor por definir | [PROP] |
| CT-05 | Los mensajes de inicio de sesión y recuperación no revelan si un correo está registrado (RN-06) | [PROP] |
| CT-06 | Textos en español, gestionados fuera del código para poder traducirse | [APR] DEC-06 · [PROP] detalle |
| CT-07 | Las credenciales del proveedor se guardan como secretos, nunca en el código ni en el repositorio | [APR] (gestión segura de secretos) |
| CT-08 | Límites de envío por persona y por dirección para evitar abuso; valores por definir | [PROP] |
| CT-09 | Se registra qué se envió y cuándo, sin guardar el contenido del mensaje; conservación: valor por definir | [PROP][VAL] |
| CT-10 | Se gestionan rebotes y errores de entrega, con reintento y aviso en la app cuando no se pueda entregar | [PROP] |
| CT-11 | Los correos transaccionales no incluyen publicidad; cualquier comunicación comercial sería otra decisión con su propio consentimiento | [PROP][VAL] |
| CT-12 | El proveedor actúa como encargado del tratamiento: contrato, ubicación de los datos y posibles transferencias internacionales deben validarse legalmente y figurar en el Aviso de privacidad (DEC-71) | [VAL] |
| CT-13 | Mensajes legibles y accesibles, con versión de texto plano | [PROP] |

**Criterios para elegir el proveedor (DEC-72)** [PROP]: cumplimiento de CT-01 a CT-13, soporte de dominio propio y autenticación, entregabilidad en México, condiciones de tratamiento de datos, ubicación de los servidores, costo y facilidad de integración. La elección se hace en ET4.

### 8.6 Documentos legales previos a la beta

- **RN-144** **No se invita a usuarios reales a la beta** hasta que los documentos legales estén redactados, validados por un profesional competente y publicados en A12. [APR] DEC-70
- Documentos necesarios, sujetos a lo que indique la validación (DEC-71) [VAL]:
  - Términos y condiciones.
  - Términos de la beta, que incluyen que la gratuidad no es permanente (RN-141).
  - Aviso de privacidad para personas adultas, con los consentimientos separados (DEC-08), las categorías de datos (DEC-42) y los encargados del tratamiento (por ejemplo, el proveedor de correo, CT-12).
  - Procedimiento para ejercer los derechos ARCO (RN-90).
- El aviso para tutores es parte de la habilitación futura de menores (MEN).

---

## 9. Consideraciones por edad

> **Alcance (v0.2.1):** la beta y el MVP no admiten menores (DEC-44). Esta sección documenta la **habilitación futura de menores (MEN)**: los principios siguen vigentes como objetivo de producto y las decisiones pendientes deben resolverse antes de admitir a menores.

### 9.1 Principios aprobados [APR]

| Principio | Decisión |
|---|---|
| Privacidad por defecto y minimización de datos | DEC-11 |
| Controles adecuados por tramo de edad | DEC-12 |
| No promover restricciones alimentarias, objetivos calóricos restrictivos ni ideales corporales | DEC-13 |
| No usar predicciones corporales ni médicas para menores | DEC-14 |
| El administrador familiar no ve automáticamente datos privados de otros integrantes | DEC-15 |
| No castigar el descanso ni fomentar el exceso de entrenamiento | DEC-16 |
| La IA no diagnostica ni sustituye a profesionales | DEC-17 |

### 9.2 Diseño provisional mientras haya decisiones pendientes [PROP] DEC-64

Toda función cuyo tratamiento para menores esté pendiente queda **desactivada para menores** en el servicio de políticas. Así, cuando se tome la decisión, se cambia la configuración, no el diseño. Esto no es una decisión sobre la experiencia final de los menores.

### 9.3 Asuntos pendientes

> **Ninguno de estos asuntos está resuelto.** Las alternativas proceden en parte de la propuesta v0.1 y se presentan para facilitar la decisión, no como recomendación aprobada. Los marcados [VAL] requieren profesionales competentes: abogado de protección de datos en México y, cuando se indica, profesionales de nutrición, pediatría o medicina del deporte.

#### DEC-30 · Requisitos legales del consentimiento parental [VAL legal]

- **Alternativas:** (a) consentimiento del tutor para todos los menores de 18; (b) consentimiento del tutor solo para algunos tramos; (c) consentimiento del tutor solo para ciertas categorías de datos (por ejemplo, salud).
- **Riesgos:** un consentimiento inválido puede acarrear sanciones; demasiada fricción provoca abandono o que los menores mientan sobre su edad.
- **Preguntas:** ¿qué exige la legislación mexicana vigente sobre datos personales de menores (verificar la versión actual de la ley y su reglamento)? ¿Cambia según la categoría de datos? ¿Qué evidencia hay que conservar?

#### DEC-31 · Verificación de edad y autorización del tutor [VAL legal y técnica]

- **Alternativas:** (a) autodeclaración de edad y confirmación del tutor por correo con declaración; (b) verificación mediante un cargo mínimo reembolsable; (c) proveedor externo de verificación; (d) señales de edad que ofrezcan las tiendas de apps, si están disponibles en México.
- **Riesgos:** las verificaciones fuertes recogen más datos (tensión con la minimización), cuestan dinero y añaden fricción; las débiles pueden no ser suficientes.
- **Preguntas:** ¿qué nivel de verificación es razonable para este tipo de servicio? ¿Cómo se comprueba que quien autoriza es el tutor?

#### DEC-32 · Experiencia para 13–15 [VAL legal y profesional]

- **Alternativas:** (a) experiencia centrada en hábitos, movimiento y aprendizaje, con funciones reducidas (matriz de la v0.1); (b) experiencia igual a 16–17 con límites adicionales; (c) no habilitar este tramo en el primer lanzamiento.
- **Incluye:** objetivos disponibles, restricciones de entrenamiento (cargas, intensidad), notificaciones, gamificación, comunidad, IA.
- **Riesgos:** lesiones por cargas inadecuadas, presión social, exposición a contenido no apropiado.

#### DEC-33 · Experiencia para 16–17 [VAL legal y profesional]

- **Alternativas:** (a) casi completa, con restricciones en nutrición, cuerpo y comunidad (matriz de la v0.1); (b) igual a 13–15; (c) igual a adultos salvo los principios aprobados.
- **Riesgos:** similares a 13–15, con mayor autonomía esperada por el usuario.

#### DEC-34 · Tratamiento de datos de salud de menores [VAL legal]

- **Alternativas:** (a) no tratar datos de salud de menores; (b) tratarlos con consentimiento del tutor; (c) tratar solo ciertas categorías.
- **Depende de:** DEC-30 y DEC-42.

#### DEC-35 · Peso, medidas y objetivos corporales en menores [VAL legal y profesional]

- **Ya aprobado:** sin predicciones corporales para menores (DEC-14) y sin ideales corporales (DEC-13).
- **Alternativas para el registro:** (a) no disponible para menores; (b) registro privado sin objetivo, sin gráfico destacado ni predicción; (c) disponible solo con autorización del tutor.
- **Riesgos:** fomentar preocupación por el cuerpo o conductas alimentarias de riesgo.

#### DEC-36 · Funciones nutricionales para menores [VAL profesional]

- **Ya aprobado:** sin objetivos calóricos restrictivos ni restricciones alimentarias (DEC-13).
- **Alternativas:** (a) solo contenido educativo (grupos de alimentos, hidratación, variedad), sin cifras; (b) información por alimento sin totales diarios; (c) totales sin metas.
- **Incluye:** alimentos propios (N10), alérgenos, hábitos.

#### DEC-37 · Apple Health y Health Connect para menores [VAL legal y políticas de las tiendas]

- **Alternativas:** (a) no disponible para menores; (b) disponible con autorización del tutor; (c) solo lectura de datos básicos (pasos).
- **Nota:** las integraciones son ET10; la decisión puede esperar, pero debe estar tomada antes de ET10.

#### DEC-38 · Menores en planes familiares

- **Alternativas:** (a) no admitidos inicialmente; (b) admitidos con autorización del tutor, que puede no ser el administrador; (c) admitidos si el administrador es su tutor.
- **Preguntas:** ¿un menor sin cuenta puede registrarse desde una invitación? ¿Quién autoriza su ingreso?

#### DEC-39 · Acceso del tutor a la información del menor [VAL legal]

- **Alternativas:** (a) el tutor gestiona permisos pero no ve la actividad (v0.1); (b) el menor puede compartir voluntariamente un resumen; (c) el tutor ve un resumen limitado; (d) el tutor ve todo.
- **Riesgos:** pérdida de confianza y de privacidad del adolescente frente a los derechos legales del tutor.
- **Preguntas:** ¿qué derechos de acceso tiene legalmente el tutor? ¿Por qué canal recibiría un resumen (correo, panel web)?

#### DEC-40 · Moderación y seguridad de la comunidad

- **Alternativas para la interacción:** (a) solo reacciones y mensajes predefinidos (v0.1); (b) chat libre solo entre adultos; (c) chat con moderación automática.
- **Necesidades:** herramienta interna de moderación, plazos de respuesta, filtros, procedimiento ante contenido que involucre a menores.
- **Nota:** ET9; debe resolverse antes de ET9.

#### DEC-41 · Asistente de IA para menores [VAL legal y técnica]

- **Alternativas:** (a) no disponible para menores; (b) modo restringido (solo dudas de la app y explicaciones de ejercicios); (c) disponible con autorización del tutor y filtros.
- **Preguntas:** ¿qué hace el asistente si un menor pregunta por peso o dietas? ¿Qué condiciones de uso del proveedor de IA aplican a menores?

### 9.4 Funciones afectadas por los asuntos pendientes

| Función | 18+ | 16–17 | 13–15 |
|---|---|---|---|
| Registro y onboarding | Sí | No en la beta ni en el MVP (DEC-44); futuro: DEC-30, DEC-31 | No en la beta ni en el MVP (DEC-44); futuro: DEC-30, DEC-31 |
| Entrenamiento | Sí | DEC-33 | DEC-32 |
| Progreso: objetivos no corporales y predicciones de constancia y rendimiento | Sí | DEC-33 | DEC-32 |
| Progreso: medidas y predicciones corporales | Sí (con consentimiento) | **No** (predicción, DEC-14) · registro: DEC-35 | **No** (predicción, DEC-14) · registro: DEC-35 |
| Nutrición | Sí | DEC-36 | DEC-36 |
| Gamificación y avatar | Sí | DEC-33 | DEC-32 |
| Comunidad | Sí | DEC-33, DEC-40 | DEC-32, DEC-40 |
| Asistente IA | Sí | DEC-41 | DEC-41 |
| Integraciones de salud | Sí (con consentimiento) | DEC-37 | DEC-37 |
| Plan Familiar | Sí | DEC-38 | DEC-38 |
| Funciones del tutor | — | DEC-39 | DEC-39 |

### 9.5 Experiencia del tutor por fases [APR] necesidad · [PROP] fases (DEC-07, DEC-45)

**Fuera de la beta y del MVP (DEC-44).** La necesidad se conserva (DEC-07) para la habilitación futura de menores; las fases siguientes se aplicarán entonces.

| Función del tutor | ¿Requiere interfaz web? | Fase propuesta |
|---|---|---|
| Recibir la solicitud y otorgar o rechazar el consentimiento | **Sí** (T01): el tutor no tiene la app y debe realizar una acción verificable | Fase 1 (cuando se habiliten menores) |
| Retirar el consentimiento y pedir la eliminación | **Sí** (T04), enlazada desde todos los correos | Fase 1 |
| Responder solicitudes puntuales de permiso del menor | **Sí** (T03), desde un correo | Fase 1 |
| Recibir avisos (cambio de tramo, solicitudes) | No: correo | Fase 1 |
| Ver y cambiar todos los permisos en un solo lugar | **Sí** (T02, panel) | Fase 2 |
| Solicitar exportación de datos del menor | Sí (T02) o canal de soporte | Fase 2 (fase 1: por soporte) |
| Recibir un resumen de actividad del menor | Depende de DEC-39 | Pendiente |

**RN-117** (modificada) El tutor gestiona sus funciones sin instalar la app ni crear una cuenta propia, mediante enlaces seguros de un solo uso. [PROP][VAL] DEC-31

---

## 10. Requisitos no funcionales

| Área | Requisito | Estado |
|---|---|---|
| Rendimiento | Pantalla útil en menos de 3 s en teléfono de gama media; animaciones fluidas con opción de reducirlas | [PROP] |
| Conexión | Solo la sesión de entrenamiento en curso funciona sin conexión (RN-30); el resto muestra un estado "sin conexión" claro y no pierde lo escrito sin avisar | [APR] DEC-04 · [PROP] estado |
| Accesibilidad | WCAG AA, texto escalable, lectores de pantalla, áreas táctiles de al menos 44 puntos, no depender solo del color | [APR] accesibilidad · [PROP] detalle |
| Plataformas | iOS y Android, teléfonos; tablets sin optimización específica en el MVP | [APR] DEC-03 · viabilidad: DEC-66 |
| Internacionalización | Textos fuera del código, unidades, formatos y reglas por país configurables | [APR] DEC-06 |
| Seguridad | §8.1 | [APR] |
| Calidad | Pruebas automáticas de la lógica crítica: políticas por edad, consentimientos, predicciones, eventos, derechos sobre los datos. Cada regla [APR] debe poder verificarse con una prueba. | [APR] |
| Contenido | Fuente identificada para alimentos y ejercicios | [APR] · licencias [VAL] |

---

## 11. Indicadores de éxito (propuesta) [PROP]

Onboarding completado, activación en 48 h, retención a 4 semanas, semanas con objetivo cumplido, porcentaje de usuarios con predicción disponible, tiempo de respuesta a reportes (ET9) y conversión a Premium (ET10). No se optimiza el tiempo en la app.

---

## 12. Decisiones pendientes (resumen)

El detalle completo, con estado, justificación y consecuencias, está en el [registro de decisiones](06-REGISTRO-DECISIONES-v0.2.md). **Esta sección se genera desde la tabla única de bloqueos del registro (sección 6, AF-17).**

### 12.1 Bloquean: ET4 (arquitectura técnica)

| Decisión | Tema |
|---|---|
| DEC-66 | Comportamiento en tablets [VAL] |
| DEC-72 | Proveedor de correo transaccional |

### 12.2 Bloquean: ET6.1 (acceso, registro, onboarding, inicio y perfil)

| Decisión | Tema |
|---|---|
| DEC-42 | Qué datos son de salud y granularidad de consentimientos [VAL] |
| DEC-43 | Cómo se determina el país del usuario |
| DEC-54 | Bienestar y hábitos en el onboarding |
| DEC-55 | Modalidad principal sin métricas propias |
| DEC-56 | Foto de perfil |
| DEC-60 | Valores numéricos propuestos |
| DEC-65 | Analítica desactivada hasta su consentimiento |
| DEC-69 | Mecanismo de invitaciones a la beta |

### 12.3 Bloquean: Invitar a usuarios reales a la beta

| Decisión | Tema |
|---|---|
| DEC-71 | Redacción y validación de los documentos legales de la beta [VAL] |

### 12.4 Bloquean: ET6.2 (entrenamiento y progreso)

| Decisión | Tema |
|---|---|
| DEC-47 | Disciplinas con métricas propias |
| DEC-57 | Fuentes y licencias de contenido [VAL] |
| DEC-63 | Cantidad inicial de recetas y programas |

### 12.5 Bloquean: ET6.3 (nutrición)

| Decisión | Tema |
|---|---|
| DEC-50 | Límites de seguridad nutricional [VAL] |
| DEC-61 | Criterios de señales de riesgo [VAL] |

### 12.6 Bloquean: Cierre del MVP

| Decisión | Tema |
|---|---|
| DEC-46 | Pestaña Amigos antes de la comunidad |

### 12.7 Bloquean: ET9 (comunidad)

| Decisión | Tema |
|---|---|
| DEC-40 | Moderación y seguridad de la comunidad |

### 12.8 Bloquean: ET10 (planes comerciales e integraciones)

| Decisión | Tema |
|---|---|
| DEC-48 | Predicciones gratis o Premium |
| DEC-49 | Espera entre grupos familiares |
| DEC-51 | Plan Familiar anual |
| DEC-52 | Prueba gratuita |
| DEC-58 | Comparación de escenarios |
| DEC-62 | Límites del plan Gratis |
| DEC-67 | Transición de la beta gratuita a planes comerciales |

### 12.9 Bloquean: Publicación en tiendas

| Decisión | Tema |
|---|---|
| DEC-53 | Validación del nombre como marca [VAL] |

### 12.10 Bloquean: Planificación posterior al MVP

| Decisión | Tema |
|---|---|
| DEC-59 | Etapa de las funciones pospuestas |

### 12.11 Bloquean: MEN (habilitación futura de menores)

| Decisión | Tema |
|---|---|
| DEC-18 | Edad mínima de 13 años [VAL] |
| DEC-30 | Consentimiento parental [VAL] |
| DEC-31 | Verificación de edad y autorización del tutor [VAL] |
| DEC-32 | Experiencia 13–15 [VAL] |
| DEC-33 | Experiencia 16–17 [VAL] |
| DEC-34 | Datos de salud de menores [VAL] |
| DEC-35 | Peso, medidas y objetivos corporales en menores [VAL] |
| DEC-36 | Nutrición para menores [VAL] |
| DEC-37 | Apple Health / Health Connect para menores [VAL] |
| DEC-38 | Menores en planes familiares |
| DEC-39 | Acceso del tutor a la información del menor [VAL] |
| DEC-41 | IA para menores [VAL] |
| DEC-45 | Fases de la experiencia del tutor |
| DEC-64 | Desactivado mientras esté pendiente (menores) |

**Nota:** DEC-30, DEC-31, DEC-45 y DEC-64 no bloquean la beta (DEC-44).

---

## 13. Glosario

- **MVP:** primera versión funcional con la que usuarios reales obtienen valor.
- **Entrega interna:** parte del MVP que se construye y prueba antes de seguir; no es un lanzamiento público.
- **Servicio de políticas:** componente del servidor que decide qué funciones puede usar cada persona según su edad, país, consentimientos, permisos y plan.
- **Consentimiento granular:** permiso separado para cada tipo de dato, en lugar de un único "acepto todo".
- **ARCO:** derechos de Acceso, Rectificación, Cancelación y Oposición sobre los datos personales.
- **Rango de predicción:** intervalo de fechas entre las que es probable que ocurra algo.
- **POST:** función conservada en la visión, pero programada después del MVP.
- **Beta cerrada:** primera salida del MVP a un grupo de personas adultas invitadas, gratuita y sin cobros (DEC-68).
- **MEN:** funciones para menores y tutores conservadas para una habilitación futura; fuera de la beta y del MVP (DEC-44).
- **Correo transaccional:** mensajes automáticos ligados a la cuenta (verificación, recuperación, avisos), distintos de los mensajes comerciales.
- **ET:** prefijo de las etapas desde la v0.2.2 (por ejemplo, ET6.1), para no confundirlas con las pantallas E01–E11.

---

## Anexo A. Estado de las reglas de la v0.1

| Reglas v0.1 | Estado en v0.2 |
|---|---|
| RN-01 a RN-10 | Conservadas; RN-01 (v0.2.1), RN-02, RN-04, RN-10 modificadas |
| RN-11, RN-12 | Modificadas (consentimiento y principios por edad) |
| RN-13 a RN-17 | Conservadas; RN-15 y RN-17 modificadas |
| RN-18 a RN-26 | Conservadas |
| RN-27 | Suspendida → DEC-36 |
| RN-28 a RN-29 | Conservadas |
| RN-30, RN-35 | Modificadas (DEC-04, DEC-01) |
| RN-31 a RN-34 | Conservadas |
| RN-36 | Suspendida → DEC-32 / DEC-33 |
| RN-37 a RN-45 | Conservadas; RN-43 modificada (DEC-14) |
| RN-46 a RN-56 | Conservadas; RN-56 modificada |
| RN-57 | Suspendida → DEC-32 / DEC-33 |
| RN-58 a RN-69 | Conservadas; RN-66, RN-68, RN-69 vinculadas a DEC-40 |
| RN-70 | Suspendida → DEC-32 / DEC-33 / DEC-40 |
| RN-71 a RN-79 | Conservadas |
| RN-80 | Suspendida → DEC-41 |
| RN-81 a RN-84 | Conservadas |
| RN-85 | Suspendida → DEC-32 / DEC-33 |
| RN-86 a RN-89 | Conservadas |
| RN-90 | Modificada (validación legal) |
| RN-91 a RN-96 | Conservadas; RN-92 ampliada con U19 |
| RN-97 | Pendiente → DEC-38 / DEC-44 |
| RN-98 a RN-107 | Conservadas; RN-105 → DEC-49 |
| RN-108 | Suspendida → DEC-38 |
| RN-109, RN-110 | Conservadas |
| RN-111, RN-112 | Suspendidas → DEC-30, DEC-31 |
| RN-113 | Conservada [VAL] |
| RN-114 | Sustituida por los flujos de cambio de tramo del mapa (F16, F17); contenido pendiente de DEC-32/33/39 |
| RN-115, RN-116 | Suspendidas → DEC-39 |
| RN-117 | Modificada (fases del tutor) |
| RN-118 a RN-120 | Conservadas (§8.2); con formato de regla desde v0.2.2 |
| RN-121 | Conservada (§4.1) |
| RN-122 a RN-140 | Nuevas en v0.2 (RN-140 modificada en v0.2.1) |
| RN-141 a RN-143 | Nuevas en v0.2.1 (beta) |
| RN-144 | Nueva en v0.2.2 (documentos legales previos a invitar) |

La matriz de experiencias por edad de la v0.1 (§6.4) **no se elimina**: queda como fuente de las alternativas de DEC-32 a DEC-41.
