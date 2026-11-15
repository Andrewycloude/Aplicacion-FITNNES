# Definite Fitnes — Documento de Requisitos de Producto (PRD)

| | |
|---|---|
| **Versión** | 0.1 (borrador para revisión) |
| **Etapa** | 2 — PRD y mapa de navegación |
| **Estado** | Pendiente de aprobación |
| **Documento hermano** | [02-MAPA-NAVEGACION.md](02-MAPA-NAVEGACION.md) |

> **Cómo leer este documento.** Cada funcionalidad lleva una etiqueta de etapa: **[E6]** MVP, **[E7]** gamificación y avatar, **[E8]** asistente IA, **[E9]** comunidad, **[E10]** suscripciones e integraciones. Nada de la visión se elimina: solo se ordena. Las reglas de negocio están numeradas (RN-xx) para poder referirnos a ellas al programar y al probar. Los identificadores de pantalla (A01, H01…) corresponden al mapa de navegación.

---

## 1. Resumen

**Definite Fitnes** es una plataforma fitness integral para iOS y Android que une entrenamiento multidisciplinario, nutrición, bienestar, seguimiento de progreso con predicciones transparentes, gamificación, avatar, comunidad privada y un asistente de inteligencia artificial, todo alrededor de un perfil central que personaliza la experiencia.

- **Lemas:** "Fitness, a tu manera." · "Tu vida. Tus objetivos. Tu progreso."
- **Modelo:** freemium con suscripción individual y familiar.
- **Primera versión:** en español, orientada a México, preparada para otros idiomas y países.
- **Edad mínima:** 13 años, con tres experiencias: 13–15, 16–17 y 18+.

### 1.1 Qué NO es

- No es una app solo de gimnasio ni una calculadora de calorías.
- No es un servicio médico: no diagnostica, no prescribe y no sustituye a profesionales de salud.
- No es una red social: la comunidad es opcional, secundaria y privada por defecto.

### 1.2 Principios de producto

1. **La persona primero.** Cada usuario elige qué módulos usa; la app solo pide los datos que esas funciones necesitan.
2. **Honestidad con los datos.** No se inventan datos nutricionales, fechas ni resultados. Cuando no hay datos suficientes, se dice.
3. **Bienestar antes que rendimiento.** Se premia la constancia y el descanso; nunca se castiga parar ni se fomenta el exceso.
4. **Privacidad por defecto.** Nada se comparte sin una acción explícita del usuario.
5. **Seguridad nunca de pago.** Privacidad, seguridad, ayuda, exportación y eliminación de datos son gratis siempre.
6. **Protección reforzada de menores.** Ante la duda, se aplica la opción más protectora.

---

## 2. Usuarios

### 2.1 Segmentos por edad

| Segmento | Descripción | Enfoque de la experiencia |
|---|---|---|
| **13–15** | Adolescentes tempranos | Hábitos, movimiento y aprendizaje. Sin métricas de peso como objetivo, sin déficit calórico, comunidad muy limitada y controlada por el tutor. |
| **16–17** | Adolescentes mayores | Más autonomía en entrenamiento y estadísticas; nutrición informativa sin objetivos de restricción; comunidad solo entre amigos. |
| **18+** | Adultos | Experiencia completa. |

### 2.2 Perfiles de uso (ejemplos)

- **Principiante que quiere empezar** — necesita guía simple, rutinas en casa y motivación.
- **Deportista de una disciplina** (corredor, ciclista, futbolista) — necesita métricas propias de su deporte.
- **Usuario de gimnasio con experiencia** — necesita registro rápido de series, historial y estadísticas.
- **Persona enfocada en hábitos** — le interesa nutrición, hidratación, sueño y constancia más que el rendimiento.
- **Familia** — varias personas con cuentas independientes bajo un mismo pago.
- **Madre, padre o tutor** — autoriza y configura la cuenta de un menor.

### 2.3 Roles del sistema

| Rol | Qué es | Notas |
|---|---|---|
| **Usuario** | Titular de una cuenta | Dueño único de sus datos. |
| **Tutor** | Adulto que autoriza la cuenta de un menor | Controla permisos del menor; ver sección 6. |
| **Administrador familiar** | Adulto que paga el plan Familiar | Gestiona integrantes y pago; **no** ve datos de nadie. |
| **Integrante familiar** | Usuario dentro de un plan Familiar | Cuenta, perfil y datos totalmente propios. |
| **Soporte / moderación** | Personal de Definite Fitnes | Acceso mínimo, registrado y solo para atender reportes o solicitudes. |

Tutor y administrador familiar son roles **independientes**: una misma persona puede tener ambos, pero uno no implica el otro.

---

## 3. Alcance por etapa

| Módulo | E6 — MVP | Etapas posteriores |
|---|---|---|
| 1. Registro y onboarding | Completo, incluida verificación de edad y consentimiento parental | Inicio de sesión con Apple/Google (E6 si el tiempo lo permite; obligatorio antes de publicar si se ofrece Google) |
| 2. Inicio | Saludo, accesos, resumen, próximas actividades, objetivos, recomendaciones por reglas | Reorganización de la pantalla (E10), recomendaciones con IA (E8) |
| 3. Nutrición | Resumen, registro, biblioteca, detalle, hábitos, historial | Recetas y alternativas (E6 básico, ampliado después), escáner de código de barras (posterior) |
| 4. Entrenamiento | 3 disciplinas con métricas propias (gimnasio, running, casa) + registro genérico para cualquier otra actividad; biblioteca, rutinas, calendario, sesiones, historial | Calistenia, ciclismo, natación, fútbol y más con métricas propias; programas avanzados (E10); GPS en vivo (posterior) |
| 5. Progreso y predicciones | Objetivos, registros, gráficos, tendencias, predicción con intervalo y calidad de datos | Comparación de periodos y estadísticas ampliadas (E10, Premium) |
| 6. Personalización visual | Tema oscuro y claro, color de acento básico | Temas, tarjetas, organización del inicio (E7/E10) |
| 7. Gamificación | — (se registran los eventos desde E6 para no perder historial) | XP, niveles, logros, retos, misiones, inventario (E7) |
| 8. Avatar | Foto o inicial de perfil | Avatar personalizable y desbloqueables (E7) |
| 9. Comunidad | — | Completo (E9) |
| 10. Asistente IA | — | Completo (E8) |
| 11. Integraciones | Notificaciones locales y push | Apple Health, Health Connect, wearables, Spotify (E10) |
| Suscripciones | Todo el MVP funciona sin pagos; los límites Gratis/Premium se diseñan desde ya | Pagos reales (E10) |
| Seguridad y privacidad | Completo desde el primer día | Auditorías y pruebas de penetración (E11) |

---

## 4. Requisitos funcionales por módulo

### 4.1 Módulo 1 — Registro y onboarding [E6]

**Objetivo:** que una persona pase de abrir la app a ver un inicio personalizado en pocos minutos, entregando solo los datos necesarios.

**Funciones**

- Bienvenida con propuesta de valor (A02).
- Verificación de edad **antes** de pedir cualquier otro dato (A03).
- Registro con correo y contraseña; verificación del correo (A04, A05).
- Inicio de sesión y recuperación de cuenta (A06–A08).
- Flujo de consentimiento parental para menores (A09, A10).
- Onboarding condicional (O01–O12).

**Reglas de negocio**

- **RN-01** La fecha de nacimiento se pide primero, en una pantalla neutra que no sugiere qué edad "sirve".
- **RN-02** Si la edad es menor de 13, no se crea cuenta ni se guarda ningún dato personal. El dispositivo recuerda el bloqueo para que no baste con cambiar la fecha y reintentar.
- **RN-03** La fecha de nacimiento no puede editarla el usuario después. Corregirla requiere contactar a soporte.
- **RN-04** Un menor (13–17) no puede usar la app hasta que su tutor otorgue el consentimiento. Mientras tanto la cuenta queda "pendiente" y sin recopilar datos adicionales. Si no hay consentimiento en 14 días, la cuenta pendiente se elimina.
- **RN-05** Contraseña: mínimo 10 caracteres, se rechaza si aparece en listas de contraseñas filtradas. Sin reglas arbitrarias de símbolos.
- **RN-06** Los mensajes de inicio de sesión y recuperación nunca revelan si un correo está registrado.
- **RN-07** Límite de intentos de inicio de sesión y de recuperación para frenar ataques automatizados.
- **RN-08** El onboarding es condicional: las preguntas de nutrición solo aparecen si el usuario elige usar nutrición; las de experiencia, solo para las actividades elegidas; las medidas corporales, solo si una función elegida las necesita, y siempre son opcionales.
- **RN-09** Todo paso de onboarding no esencial se puede omitir y completar después desde el perfil. Esenciales: nombre, objetivos y al menos un módulo de interés.
- **RN-10** Máximo una decisión por pantalla y barra de progreso visible. Meta: completar en menos de 3 minutos.
- **RN-11** Las "consideraciones de seguridad" (lesiones, condiciones, embarazo, etc.) sirven solo para adaptar y advertir. Si el usuario marca alguna, se muestra la recomendación de consultar a un profesional antes de empezar y se evitan sugerencias de alta intensidad. Nunca se emite un diagnóstico.
- **RN-12** Los objetivos disponibles dependen de la edad (ver sección 6): a menores no se les ofrece "bajar de peso" ni objetivos estéticos.

**Datos que se piden y para qué**

| Dato | Obligatorio | Para qué | Condición |
|---|---|---|---|
| Fecha de nacimiento | Sí | Edad y protecciones | Siempre |
| Correo y contraseña | Sí | Cuenta | Siempre |
| Nombre o apodo | Sí | Saludo y perfil | Siempre |
| Objetivos | Sí | Personalización | Siempre |
| Módulos de interés | Sí | Qué mostrar | Siempre |
| Actividades | Sí si eligió entrenamiento | Métricas y biblioteca | Entrenamiento |
| Experiencia por actividad | No | Nivel de las sugerencias | Entrenamiento |
| Disponibilidad (días, minutos) | No | Planificación | Entrenamiento |
| Preferencias alimentarias | No | Filtros de recetas y alimentos | Nutrición |
| Alergias y restricciones | No | Advertencias | Nutrición |
| Consideraciones de seguridad | No | Adaptar y advertir | Entrenamiento o nutrición |
| Estatura y peso | No | Estimaciones de energía | Solo 18+ con nutrición u objetivo relacionado |
| Correo del tutor | Sí para 13–17 | Consentimiento | Menores |

### 4.2 Módulo 2 — Pantalla principal [E6]

**Objetivo:** responder en un vistazo "¿qué hago hoy y cómo voy?".

**Contenido de H01 (de arriba abajo)**

1. Encabezado: avatar, saludo **"Bienvenido, [nombre], ¿qué planeas hacer?"**, campana de notificaciones.
2. Cuatro accesos grandes con el color de cada módulo: **Nutrición** (morado), **Entrenamiento** (amarillo), **Progreso y recompensas** (rosa), **Comunidad** (gris).
3. Resumen de hoy: actividad realizada, hábitos, registro de alimentos.
4. Próximas actividades planificadas.
5. Objetivos activos con su avance.
6. Recomendaciones.
7. Acceso al asistente [E8].

**Reglas de negocio**

- **RN-13** Solo aparecen accesos y tarjetas de los módulos que el usuario activó. Puede activar más desde el perfil.
- **RN-14** El acceso "Comunidad" se muestra solo cuando el módulo existe [E9] y la edad lo permite; si el usuario no ha activado la comunidad, lleva a la pantalla de activación, no a contenido social.
- **RN-15** Las recomendaciones del MVP se generan con reglas claras (por ejemplo, "llevas 3 días sin registrar agua") y cada una explica por qué aparece. Nunca recomiendan entrenar más si el usuario ya entrenó ese día o lleva varios días seguidos: en ese caso sugieren descanso.
- **RN-16** Estados vacíos útiles: sin datos, cada tarjeta explica qué hacer para empezar.
- **RN-17** El saludo usa el género gramatical neutro si el usuario lo prefiere ("Te damos la bienvenida, [nombre]"); se configura en el perfil.

**Navegación inferior:** Inicio · Actividad · Amigos · Perfil. Ver decisión abierta D-01 sobre la pestaña Amigos antes de E9.

### 4.3 Módulo 3 — Nutrición [E6]

**Objetivo:** ayudar a entender y mejorar la alimentación con información confiable, sin obsesión por los números.

**Funciones**

| Función | Descripción | Etapa |
|---|---|---|
| Resumen nutricional (N01) | Lo registrado hoy: comidas, energía y macronutrientes (según edad), agua, hábitos | E6 |
| Registro de alimentos (N02) | Buscar, elegir porción, asignar a desayuno/comida/cena/colación; recientes y favoritos | E6 |
| Biblioteca de alimentos (N04) | Catálogo con buscador y categorías | E6 |
| Información nutricional (N03) | Ficha por alimento con **fuente citada** | E6 |
| Alimento personalizado (N10) | El usuario crea uno propio, visible solo para él y marcado como "no verificado" | E6 |
| Hábitos (N08) | Agua, frutas y verduras, horarios regulares; marcar cumplimiento diario | E6 |
| Historial (N07) | Días anteriores y promedios semanales | E6 |
| Recetas (N05, N06) | Recetas con ingredientes del catálogo y valores calculados | E6 básico |
| Alternativas (en N03) | Alimentos parecidos de la misma categoría, con comparación neutral | E6 básico |
| Recomendaciones personalizadas | Por reglas en E6; con IA en E8 | E6 / E8 |
| Código de barras, foto de platillos | — | Posterior |

**Reglas de negocio**

- **RN-18** Todo dato nutricional proviene de una fuente identificada que se muestra al usuario (candidatas: USDA FoodData Central, tablas mexicanas de composición de alimentos, Open Food Facts). Las licencias se validan en la Etapa 4. **Nunca se generan valores nutricionales con IA.**
- **RN-19** Si un dato falta en la fuente, se muestra "sin dato", no cero ni una estimación.
- **RN-20** Los alimentos creados por usuarios no entran al catálogo general.
- **RN-21** Las referencias de energía para adultos se calculan con fórmulas públicas (se muestra cuál) y se presentan como **estimación orientativa**, no como prescripción.
- **RN-22** La app nunca sugiere ni permite fijar una meta de energía por debajo de un mínimo de seguridad, ni ritmos de pérdida de peso agresivos. Los valores exactos se definirán con asesoría profesional antes del lanzamiento (decisión D-06).
- **RN-23** No se usan etiquetas morales para alimentos ("bueno/malo", "prohibido", "tramposo"). Tampoco colores de alarma por pasarse de una referencia.
- **RN-24** Alergias: los alimentos y recetas que contienen un alérgeno declarado muestran advertencia. Se aclara que la información puede ser incompleta y que debe revisarse la etiqueta del producto.
- **RN-25** Señales de riesgo (registros de energía muy bajos y sostenidos, por ejemplo) no generan felicitaciones ni rachas; muestran un mensaje de cuidado con recursos de ayuda. Sin diagnóstico.
- **RN-26** Aviso permanente y discreto: "Información educativa. No sustituye a profesionales de salud."
- **RN-27** Restricciones por edad: ver sección 6.

### 4.4 Módulo 4 — Entrenamiento [E6]

**Objetivo:** registrar y planificar cualquier actividad física con las métricas que le corresponden.

**Disciplinas y métricas**

| Disciplina | Métricas propias | Etapa |
|---|---|---|
| Gimnasio (fuerza) | Ejercicio, series, repeticiones, peso, descanso, esfuerzo percibido; volumen y mejores marcas | E6 |
| Running | Distancia, tiempo, ritmo, desnivel (manual), esfuerzo percibido; tipo de sesión | E6 |
| Entrenamiento en casa | Ejercicios por repeticiones o por tiempo, circuitos, rondas | E6 |
| Otra actividad (genérico) | Tipo, duración, esfuerzo percibido, notas | E6 |
| Calistenia | Progresiones, repeticiones, tiempo en isométricos | Posterior |
| Ciclismo | Distancia, tiempo, velocidad, desnivel | Posterior |
| Natación | Distancia, largos, estilo, tiempo | Posterior |
| Fútbol y deportes de equipo | Duración, tipo (partido/entrenamiento), posición, notas | Posterior |

El registro genérico garantiza que **ninguna actividad queda fuera** desde el primer día, aunque todavía no tenga métricas especializadas.

**Funciones**

| Función | Descripción | Etapa |
|---|---|---|
| Centro de entrenamiento (E01) | Acceso a iniciar sesión, rutinas, biblioteca, programas | E6 |
| Biblioteca (E02, E03) | Actividades y ejercicios con explicación paso a paso, músculos implicados, errores comunes y precauciones | E6 |
| Rutinas (E04, E05) | Rutinas predefinidas y propias; crear, duplicar, editar | E6 |
| Sesión en curso (E06, E07) | Registro en vivo adaptado a la disciplina; temporizador de descanso | E6 |
| Registro manual (E08) | Anotar una actividad ya realizada | E6 |
| Resumen de sesión (E09) | Totales, marcas personales, nota opcional | E6 |
| Calendario y planificación (C01–C03) | Planificar actividades y recordatorios | E6 |
| Historial y estadísticas (C04, P05) | Sesiones pasadas y tendencias por disciplina | E6 |
| Programas (E10, E11) | Planes de varias semanas | E6 básico; avanzados en E10 |
| Registro con GPS | Ruta y ritmo en vivo | Posterior |

**Reglas de negocio**

- **RN-28** Cada disciplina tiene su propio formulario y sus propias estadísticas. No se fuerzan "series y repeticiones" en actividades de resistencia ni al revés.
- **RN-29** El contenido de ejercicios (texto e imágenes) es propio o con licencia verificada. Cada ejercicio indica nivel y precauciones.
- **RN-30** Una sesión en curso se guarda continuamente en el teléfono: si la app se cierra o no hay internet, no se pierde y se sincroniza después.
- **RN-31** Se puede editar o eliminar una sesión registrada; las estadísticas y predicciones se recalculan.
- **RN-32** Los días de descanso se pueden planificar y cuentan como parte del plan, no como "días fallados".
- **RN-33** Si el usuario registra muchos días consecutivos de alta intensidad o volúmenes inusuales, la app sugiere descanso; nunca felicita el exceso.
- **RN-34** Si el usuario marcó consideraciones de seguridad, los ejercicios relacionados muestran advertencia y la app no los sugiere automáticamente.
- **RN-35** Plan Gratis: una modalidad principal con métricas completas; el resto de actividades se registran en formato genérico. Cambiar de modalidad principal es posible cada 30 días y **no borra** el historial de la anterior (ver sección 5).
- **RN-36** Restricciones por edad (cargas máximas, contenidos): ver sección 6.

### 4.5 Módulo 5 — Progreso y predicciones [E6]

**Objetivo:** mostrar con honestidad cómo va la persona y, cuando los datos lo permiten, hacia dónde apunta la tendencia.

**Funciones**

| Función | Descripción | Etapa |
|---|---|---|
| Resumen de progreso (P01) | Panorama por categoría: actividad, rendimiento, nutrición, bienestar, objetivos | E6 |
| Objetivos (P02–P04) | Crear, seguir, pausar, completar y archivar | E6 |
| Registro de avances (P07) | Mediciones manuales (marcas, bienestar, medidas opcionales) | E6 |
| Gráficos e historiales (P04, P05) | Por métrica y periodo | E6 |
| Tendencias | Dirección y ritmo de cambio | E6 |
| Predicción de fecha (P04) | Rango estimado para alcanzar el objetivo | E6 |
| "Cómo se calcula" (P08) | Explicación del método en lenguaje llano | E6 |
| Comparar periodos (P06) | Este mes vs. el anterior, etc. | E10 (Premium) |

**Tipos de objetivo**

- **De constancia:** "entrenar 3 veces por semana", "tomar agua 5 días a la semana".
- **De rendimiento:** "correr 5 km en 30 minutos", "sentadilla con 80 kg".
- **De acumulación:** "correr 100 km este mes".
- **De bienestar:** "dormir 7 horas", valoración de energía o ánimo.
- **De medida corporal:** solo 18+, con las salvaguardas de RN-22.
- **Personal libre:** el usuario define métrica, unidad y meta.

**Reglas de negocio — predicciones**

- **RN-37** Las predicciones se calculan solo con datos registrados por el usuario y con métodos estadísticos estándar y explicables (tendencia sobre los registros recientes con su margen de error). No se usa IA generativa para calcular fechas.
- **RN-38** No se muestra predicción si no hay datos suficientes. Umbral inicial propuesto: al menos 6 registros distribuidos en al menos 3 semanas; se ajustará en la Etapa 5 con pruebas. En su lugar aparece: "Aún no hay datos suficientes para una estimación confiable. Faltan aproximadamente N registros."
- **RN-39** Toda predicción se muestra como **rango de fechas**, nunca como un día exacto, acompañada de un indicador de calidad de datos (baja / media / alta) y la frase "Estimación basada en tus registros; no es una garantía."
- **RN-40** Si la tendencia es plana o va en sentido contrario al objetivo, no se muestra fecha. Se informa con lenguaje neutro ("con el ritmo actual no es posible estimar una fecha") y se ofrece ajustar el objetivo o el plan.
- **RN-41** Si el rango resultante es demasiado amplio para ser útil, se dice así en lugar de mostrar una fecha poco fiable.
- **RN-42** Las predicciones se recalculan al añadir, editar o borrar datos; se indica la fecha del último cálculo.
- **RN-43** Predicciones sobre peso o medidas corporales: solo 18+, nunca prometen resultados, y no se muestran si el ritmo implícito supera los límites de seguridad de RN-22.
- **RN-44** Ninguna comunicación (pantalla, notificación, marketing dentro de la app) convierte una predicción en promesa.
- **RN-45** P08 explica el método, qué datos usa y sus límites, de forma comprensible para cualquier persona.

### 4.6 Módulo 6 — Personalización visual [E6 básico · E7/E10 ampliado]

| Opción | Gratis | Premium | Etapa |
|---|---|---|---|
| Tema oscuro (predeterminado) y claro | Sí | Sí | E6 |
| Tamaño de texto y reducción de animaciones | Sí | Sí | E6 |
| Color de acento principal (paleta básica) | Sí | Sí | E6 |
| Paletas adicionales y color secundario | — | Sí | E10 |
| Estilos de tarjeta | 1 estilo | Varios | E10 |
| Reorganizar la pantalla principal | Mostrar/ocultar tarjetas | Orden libre y tarjetas extra | E10 |
| Avatar y accesorios | Básicos y los ganados | Catálogo ampliado | E7 |

- **RN-46** Toda combinación de colores ofrecida cumple contraste mínimo de accesibilidad (WCAG AA). No se permiten combinaciones ilegibles.
- **RN-47** Las opciones de accesibilidad nunca son Premium.
- **RN-48** Los colores de módulo (morado, amarillo, rosa, gris) son la identidad por defecto; los temas pueden variarlos conservando la distinción entre módulos.

### 4.7 Módulo 7 — Gamificación [E7]

**Elementos:** XP, niveles, logros, insignias, retos, misiones, objetivos semanales, recompensas e inventario.

- **RN-49** Se gana XP por hábitos saludables y constancia: registrar, completar lo planificado, cumplir hábitos, aprender (leer un ejercicio o artículo), y **respetar los descansos planificados**.
- **RN-50** Tope diario de XP por actividad física: entrenar más allá de un límite razonable no da más XP. Así no se incentiva el exceso.
- **RN-51** No existen penalizaciones: no se pierde XP, nivel ni recompensas por descansar, enfermar o dejar de usar la app.
- **RN-52** Las rachas son flexibles: se miden por semanas con objetivo cumplido, no por días consecutivos, y admiten "pausa" (vacaciones, enfermedad) sin romperse.
- **RN-53** Nada de XP ni logros por comer menos, por bajar de peso ni por métricas corporales.
- **RN-54** Las recompensas son solo estéticas (accesorios de avatar, temas, insignias). No se venden ventajas ni existen cajas de recompensa aleatorias de pago.
- **RN-55** El XP se calcula en el servidor a partir de registros reales; el teléfono no puede otorgarse XP.
- **RN-56** Los eventos que darán XP se guardan desde E6, para que quienes usen el MVP no pierdan su historial al llegar la gamificación.
- **RN-57** Para menores, las misiones se orientan a hábitos, variedad y aprendizaje.

### 4.8 Módulo 8 — Avatar [E7]

- Editor de apariencia, vestimenta y accesorios; elementos desbloqueables por logros.
- **RN-58** El avatar es simbólico y estilizado. Su cuerpo **no cambia** según el peso, las medidas ni el progreso del usuario.
- **RN-59** Opciones inclusivas (tonos de piel, peinados, complexiones, prótesis, silla de ruedas, prendas sin distinción de género), todas disponibles gratis.
- **RN-60** La progresión se expresa con accesorios, fondos y efectos, nunca con un cuerpo "mejor".

### 4.9 Módulo 9 — Comunidad [E9]

**Funciones:** perfil social, amigos, solicitudes, retos compartidos, compartir logros y actividades, rankings opcionales, bloqueo, reportes y controles de privacidad.

- **RN-61** La comunidad está **desactivada por defecto**. Activarla es una decisión explícita (S02) y se puede desactivar en cualquier momento, lo que oculta al usuario de inmediato.
- **RN-62** Nada se publica automáticamente. Compartir un logro o una actividad requiere una acción por cada elemento, con vista previa de lo que verán los demás.
- **RN-63** Nunca se pueden compartir datos de salud sensibles: peso, medidas, registros de alimentos, consideraciones de seguridad ni datos de bienestar.
- **RN-64** Los amigos se agregan por código, enlace o nombre de usuario exacto. No hay sugerencias basadas en contactos ni en ubicación. No se pide acceso a la agenda del teléfono.
- **RN-65** Los rankings son opcionales, solo entre amigos o dentro de un reto, y se basan en constancia (por ejemplo, semanas cumplidas), no en peso, calorías ni volumen extremo.
- **RN-66** En E9 no hay mensajes privados de texto libre. La interacción se limita a reacciones y mensajes predefinidos de ánimo. Esto reduce drásticamente los riesgos de acoso y de contacto indebido con menores. (Chat libre: decisión futura, solo adultos.)
- **RN-67** Bloquear es inmediato, silencioso y mutuo en efecto. Reportar está a un toque desde cualquier perfil o contenido.
- **RN-68** Los reportes se revisan con un plazo objetivo que se publicará; los que involucren a menores tienen prioridad.
- **RN-69** Nombres de usuario y textos visibles pasan por filtro de lenguaje ofensivo.
- **RN-70** Restricciones por edad: ver sección 6.

### 4.10 Módulo 10 — Asistente de IA [E8]

**Enfoque híbrido:** la app funciona completa sin IA. El asistente añade valor explicando y organizando.

**Puede:** explicar el progreso con los datos del usuario, ayudar a organizar la semana, explicar ejercicios de la biblioteca, dar información nutricional general tomada del catálogo, resolver dudas sobre la app, sugerir actividades generales y ayudar a redactar objetivos.

- **RN-71** El asistente solo accede a los datos del usuario a través de funciones específicas y limitadas (por ejemplo, "leer resumen de entrenamiento de la última semana"), nunca con acceso directo a la base de datos, y solo a las categorías que el usuario autorizó en I02.
- **RN-72** Las cifras (nutricionales, estadísticas, predicciones) salen siempre de los servicios de la app; el asistente las explica, no las calcula ni las inventa.
- **RN-73** Si no tiene un dato, lo dice. No afirma saber lo que no sabe.
- **RN-74** No diagnostica, no prescribe tratamientos, dietas terapéuticas, suplementos ni medicamentos. Ante síntomas o temas médicos, recomienda acudir a un profesional.
- **RN-75** Ante señales de crisis (autolesión, trastornos alimentarios, emergencia médica), interrumpe el flujo normal y muestra recursos de ayuda apropiados al país.
- **RN-76** Toda respuesta se identifica como generada por IA. El usuario puede valorar o reportar una respuesta.
- **RN-77** Las conversaciones no se usan para entrenar modelos de terceros y el usuario puede borrar su historial.
- **RN-78** Las acciones que el asistente proponga (crear un objetivo, planificar una sesión) requieren confirmación del usuario antes de ejecutarse.
- **RN-79** Límite de mensajes por día según el plan, para controlar costos. Las dudas de ayuda y seguridad no cuentan para el límite.
- **RN-80** Restricciones por edad: ver sección 6.

### 4.11 Módulo 11 — Integraciones [E6 notificaciones · E10 resto]

| Integración | Uso previsto | Etapa | Condiciones |
|---|---|---|---|
| Notificaciones | Recordatorios y avisos | E6 | Permiso solicitado con contexto; todo configurable |
| Apple Health / Health Connect | Leer pasos, entrenamientos, sueño; escribir sesiones | E10 | Permiso por tipo de dato; cumplir políticas de Apple y Google |
| Wearables | A través de Apple Health y Health Connect primero | E10 | Integraciones directas solo si se justifican |
| Spotify | Controlar la reproducción del usuario durante la sesión | E10 | Solo mediante su SDK y condiciones oficiales; sin almacenar ni distribuir música |

- **RN-81** Antes de implementar cada integración se revisa su documentación y condiciones oficiales vigentes.
- **RN-82** Los datos de salud importados no se usan para publicidad ni se comparten con terceros.
- **RN-83** Cada integración se puede desconectar; al hacerlo se pregunta si conservar o eliminar los datos importados.
- **RN-84** Las notificaciones no muestran datos sensibles en la pantalla de bloqueo. No se envían notificaciones que generen culpa ("¡fallaste hoy!").
- **RN-85** Menores: sin notificaciones en horario nocturno (22:00–07:00 hora local).

### 4.12 Perfil, ajustes y cuenta [E6]

- Perfil (U01, U02): nombre, avatar, objetivos, actividades, preferencias; activar o desactivar módulos.
- Ajustes: apariencia (U04), privacidad (U05), seguridad de la cuenta (U06), notificaciones (U07), suscripción (U08), integraciones (U15).
- **Exportar mis datos (U12):** archivo descargable con toda la información del usuario en formato legible.
- **Eliminar cuenta (U13):** desde la app, con confirmación y periodo de gracia.
- Ayuda y seguridad (U14): preguntas frecuentes, contacto, recursos de ayuda, documentos legales.

- **RN-86** Exportación y eliminación son gratuitas y accesibles para todos los planes y edades.
- **RN-87** Eliminación: periodo de gracia de 30 días en que la cuenta queda desactivada e invisible; después se borran definitivamente los datos personales. Se conserva solo lo que la ley obligue (por ejemplo, comprobantes de pago).
- **RN-88** Cambiar correo o contraseña exige volver a autenticarse y notifica al correo anterior.
- **RN-89** El usuario puede ver y cerrar sus sesiones abiertas en otros dispositivos.
- **RN-90** Derechos de acceso, rectificación, cancelación y oposición (ARCO) atendidos desde la app o por un canal de contacto publicado.

---

## 5. Suscripciones

### 5.1 Planes

| Plan | Precio | Personas |
|---|---|---|
| **Gratis** | $0 | 1 |
| **Premium mensual** | $50 MXN al mes | 1 |
| **Premium anual** | $500 MXN al año (equivale a pagar 10 meses) | 1 |
| **Familiar mensual** | $200 MXN al mes | Hasta 6, incluido el administrador (≈ $33 por persona) |

Cada integrante del plan Familiar tiene todas las funciones Premium.

### 5.2 Qué incluye cada plan

| Área | Gratis | Premium / Familiar |
|---|---|---|
| Cuenta, perfil y onboarding | Completo | Completo |
| **Seguridad, privacidad, ayuda, exportar y eliminar datos** | **Completo, siempre** | Completo |
| Modalidades de entrenamiento | 1 principal con métricas completas + registro genérico ilimitado del resto | Todas, sin límite |
| Biblioteca de ejercicios e información de seguridad | Completa | Completa |
| Rutinas propias | Hasta 3 | Ilimitadas |
| Programas | Básicos | Avanzados y especializados |
| Planificación | Calendario y recordatorios | Planificación avanzada (plantillas semanales, reprogramación automática) |
| Nutrición | Registro, biblioteca, información, hábitos, recetas básicas | Recetas ampliadas, análisis por periodos, recomendaciones ampliadas |
| Historial | **Todo se conserva**; vista de gráficos de los últimos 90 días | Vista completa sin límite |
| Objetivos activos | Hasta 3 | Ilimitados |
| Predicciones | En todos los objetivos activos, con rango y calidad | Igual, más comparación de escenarios |
| Estadísticas | Básicas | Ampliadas y comparación de periodos |
| Personalización | Temas claro/oscuro, acento básico, accesibilidad completa | Paletas, tarjetas y organización avanzada |
| Gamificación | Completa | Completa + cosméticos exclusivos |
| Avatar | Opciones básicas e inclusivas + lo ganado | Catálogo ampliado |
| Comunidad | Amigos, retos básicos, bloqueo y reportes | Crear retos personalizados, más retos simultáneos |
| Asistente IA | Mensajes limitados por día | Límite ampliado |
| Integraciones de salud | Conexión básica | Sincronización y análisis ampliados |

**Sobre las predicciones:** se propone que sean gratuitas porque son el principal diferenciador y la mejor razón para que alguien adopte la app; el valor Premium está en la profundidad (más objetivos, más historia, comparaciones). Ver decisión abierta D-03.

### 5.3 Reglas de negocio — suscripciones

- **RN-91** Nunca se bloquea por pago: seguridad, privacidad, información esencial (precauciones de ejercicios, advertencias de alérgenos), ayuda, recursos de crisis, exportación y eliminación de datos.
- **RN-92** **Los datos del usuario nunca se retienen como rehén.** Al pasar de Premium a Gratis no se borra nada: lo que excede los límites queda en solo lectura y exportable; el usuario elige qué mantiene activo.
- **RN-93** El derecho a Premium se valida en el servidor; el teléfono no decide si alguien es Premium.
- **RN-94** Los precios, la renovación automática y la forma de cancelar se muestran con claridad antes de pagar. Sin patrones engañosos: cancelar es tan fácil como contratar.
- **RN-95** Los pagos dentro de la app usarán los sistemas de compra de Apple y Google, como exigen sus tiendas para bienes digitales. Las comisiones, impuestos, pruebas gratuitas y reembolsos se definirán en E10; **no se implementan pagos antes**.
- **RN-96** Las pantallas de planes (U09) no usan presión artificial (cuentas regresivas falsas, culpa) y no se muestran de forma insistente.
- **RN-97** A menores de 18 no se les muestran ofertas de compra directas: se les indica que un adulto puede contratar o invitarles a un plan Familiar.

### 5.4 Reglas de negocio — plan Familiar

- **RN-98** El administrador debe ser mayor de 18 años.
- **RN-99** Máximo 6 personas en total contando al administrador.
- **RN-100** Cada integrante tiene su propia cuenta, perfil, progreso y datos. El grupo familiar solo comparte la suscripción.
- **RN-101** El administrador ve únicamente: nombre visible de cada integrante, estado de la invitación y fecha de ingreso. **No ve** entrenamientos, nutrición, progreso, objetivos, conversaciones ni ningún otro dato.
- **RN-102** Invitar se hace por enlace o código de un solo uso con caducidad de 7 días. La persona invitada debe aceptar expresamente.
- **RN-103** Un integrante puede salir cuando quiera, sin permiso del administrador. El administrador puede retirar a un integrante. En ambos casos la cuenta pasa a Gratis conservando todos sus datos (RN-92) y se notifica a la persona.
- **RN-104** Una persona solo puede pertenecer a un grupo familiar a la vez.
- **RN-105** Para evitar la reventa de lugares: tras salir de un grupo, una persona debe esperar 30 días para unirse a otro distinto. (Decisión abierta D-04.)
- **RN-106** Si el pago falla o se cancela, todos los integrantes pasan a Gratis al terminar el periodo pagado, con aviso previo.
- **RN-107** Si un integrante ya tenía Premium individual, se le avisa para que cancele su suscripción propia y no pague doble.
- **RN-108** Los menores pueden ser integrantes. Ser administrador familiar **no** convierte a alguien en su tutor: el consentimiento parental es un proceso separado (sección 6).
- **RN-109** Los integrantes no ven los datos de los demás. Si quieren interactuar, lo hacen por la comunidad como cualquier usuario, respetando las restricciones de edad.
- **RN-110** La administración del grupo se puede transferir a otro integrante adulto que acepte y registre su propio método de pago.

---

## 6. Protección de menores y experiencias por edad

> **Aviso importante.** Lo siguiente es un diseño prudente basado en principios generales de protección de datos de menores y en las políticas de las tiendas de apps. **No es asesoría legal.** Antes del lanzamiento debe revisarlo un abogado especializado en protección de datos en México (decisión D-05), y de nuevo para cada país al que se expanda.

### 6.1 Marco a considerar

- **México:** Ley Federal de Protección de Datos Personales en Posesión de los Particulares y su reglamento; Ley General de los Derechos de Niñas, Niños y Adolescentes. Los datos de salud son datos sensibles y requieren consentimiento expreso; el tratamiento de datos de menores requiere consentimiento de quien ejerce la patria potestad o tutela.
- **Tiendas:** políticas de Apple App Store y Google Play sobre apps usadas por menores, datos de salud, clasificación por edad y compras.
- **Expansión internacional:** normas como el RGPD europeo (edad de consentimiento digital entre 13 y 16 según el país), COPPA en Estados Unidos (menores de 13, que aquí no se admiten) y leyes locales equivalentes. El sistema debe permitir configurar la edad mínima y la edad de consentimiento **por país**.

### 6.2 Consentimiento parental

1. El menor indica su fecha de nacimiento y crea sus credenciales.
2. Se le pide el correo de su madre, padre o tutor (A09).
3. El tutor recibe un enlace, lee un resumen claro de qué datos se tratan y para qué, declara ser mayor de edad y responsable del menor, y acepta o rechaza.
4. Mientras tanto la cuenta del menor permanece bloqueada (A10).
5. El tutor puede retirar el consentimiento en cualquier momento, lo que desactiva la cuenta e inicia el proceso de eliminación.

- **RN-111** Se propone exigir consentimiento parental para **todos los menores de 18** en México (opción más prudente). Ver D-05.
- **RN-112** El método para verificar que quien consiente es realmente un adulto responsable se definirá con asesoría legal (opciones: confirmación por correo con declaración, verificación mediante un cargo mínimo reembolsable con tarjeta, u otro). El sistema se diseña para poder cambiar de método.
- **RN-113** Se guarda evidencia del consentimiento: quién, cuándo, qué versión del aviso de privacidad.
- **RN-114** Al cumplir 18 años, la cuenta pasa a la experiencia adulta, se desvincula del tutor y se le piden al usuario sus propios consentimientos. Al cumplir 16, pasa a la experiencia 16–17 notificando al tutor.

### 6.3 Qué puede hacer el tutor

- **RN-115** El tutor **controla permisos**: activar o no la comunidad, el asistente de IA, las notificaciones, las integraciones; retirar el consentimiento; solicitar exportación o eliminación de los datos del menor.
- **RN-116** El tutor **no ve por defecto** el detalle de la actividad del menor dentro de la app. El menor puede compartirle voluntariamente un resumen semanal. Esto protege la confianza del adolescente; los derechos legales de acceso del tutor se atienden por el canal formal de RN-90. (Punto a validar en D-05.)
- **RN-117** El tutor gestiona todo desde un panel web accesible por enlace seguro (T01), sin necesidad de instalar la app ni tener cuenta propia.

### 6.4 Matriz de experiencias por edad

| Área | 13–15 | 16–17 | 18+ |
|---|---|---|---|
| Consentimiento parental | Obligatorio | Obligatorio (D-05) | No aplica |
| Objetivos disponibles | Constancia, habilidades, rendimiento moderado, hábitos, bienestar | Lo anterior + rendimiento | Todos |
| Objetivos de peso o estéticos | **No** | **No** | Sí, con salvaguardas |
| Registro de peso y medidas | No disponible | Opcional, sin objetivo ni predicción, sin protagonismo visual | Opcional |
| Nutrición: enfoque | Educativo: grupos de alimentos, variedad, hábitos, hidratación | Educativo + información nutricional completa de alimentos | Completo |
| Nutrición: conteo de energía | **No se muestra** conteo diario ni metas de calorías | Se muestra la información de cada alimento; **sin** meta diaria ni concepto de déficit | Referencia orientativa con mínimos de seguridad |
| Dietas restrictivas, ayuno, suplementos | Sin contenido | Sin contenido | Solo información general, sin promoción |
| Entrenamiento | Énfasis en técnica, juego, variedad; fuerza con peso corporal y cargas ligeras; sin pruebas de carga máxima | Todas las disciplinas; sin promoción de cargas máximas; recomendación de supervisión | Completo |
| Predicciones | Constancia y habilidades | Constancia y rendimiento | Todas (peso con salvaguardas) |
| Gamificación | Sí, orientada a hábitos y aprendizaje | Sí | Sí |
| Avatar | Sí | Sí | Sí |
| Comunidad | Desactivada; solo si el tutor la habilita. Amigos solo por código, cada amistad aprobada por el tutor. Sin rankings. No aparece en búsquedas | Opcional con permiso del tutor. Amigos por código o enlace. Rankings solo entre amigos. No aparece en búsquedas | Opcional; todas las funciones |
| Amistad con adultos | Solo con aprobación del tutor | Aviso al menor y posibilidad de bloqueo por el tutor | — |
| Perfil social | Apodo y avatar; nunca foto, edad, escuela ni ubicación | Igual | Configurable |
| Asistente IA | Solo si el tutor lo habilita; modo restringido (app, ejercicios, hábitos); sin temas de peso o dietas | Habilitado por el tutor; filtros reforzados | Completo |
| Notificaciones | Sin horario nocturno; mínimas | Sin horario nocturno | Configurables |
| Compras | Sin ofertas directas | Sin ofertas directas | Sí |
| Publicidad y rastreo | Sin publicidad ni rastreo con fines comerciales | Igual | Sin publicidad de terceros en la v1; analítica con consentimiento |
| Integraciones de salud | No | Con permiso del tutor | Sí |

- **RN-118** Para todas las edades: no se muestra publicidad de terceros en la primera versión, y nunca se venden datos personales.
- **RN-119** Los datos de menores se recogen en la mínima cantidad posible y no se usan para analítica de producto más allá de métricas agregadas y anónimas.
- **RN-120** El contenido sensible (imágenes corporales tipo "antes y después", lenguaje de culpa o de cuerpo ideal) no existe en la app para ninguna edad.

---

## 7. Conexiones entre módulos

El **perfil central** es la fuente de personalización; cada módulo lee de él y produce datos que otros aprovechan.

| Origen | Destino | Qué fluye |
|---|---|---|
| Onboarding / Perfil | Todos | Edad, objetivos, módulos activos, actividades, preferencias, consideraciones de seguridad, plan |
| Entrenamiento | Progreso | Sesiones → estadísticas, marcas, tendencias, predicciones |
| Entrenamiento | Inicio | Resumen del día y próximas actividades |
| Nutrición | Progreso | Hábitos y promedios → categoría Nutrición |
| Nutrición | Inicio | Resumen del día y hábitos pendientes |
| Progreso | Inicio | Objetivos activos y su avance |
| Progreso | Asistente IA | Resúmenes autorizados para explicar el progreso |
| Entrenamiento, Nutrición, Progreso | Gamificación | Eventos de constancia → XP, logros, misiones |
| Gamificación | Avatar / Personalización | Recompensas desbloqueadas → inventario |
| Gamificación / Entrenamiento | Comunidad | Logros y actividades que el usuario **decide** compartir |
| Comunidad | Gamificación | Retos compartidos completados |
| Suscripción | Todos | Límites y funciones disponibles |
| Edad y tutor | Todos | Restricciones de la sección 6 |
| Integraciones | Entrenamiento / Progreso | Datos importados, identificados por su origen |

**Regla general RN-121:** los módulos se comunican por servicios definidos, no leyendo directamente los datos de otro. Así se pueden añadir disciplinas o módulos sin reconstruir la app.

---

## 8. Requisitos no funcionales

### 8.1 Seguridad (referencias: OWASP MASVS, ASVS, API Security Top 10)

- Autenticación segura con tokens de corta duración y renovación; almacenamiento en el llavero seguro del sistema.
- **Autorización en el servidor**: cada petición comprueba que el usuario solo accede a sus propios datos (seguridad a nivel de fila en la base de datos).
- Cifrado en tránsito (TLS) y en reposo. Protección adicional para datos sensibles.
- Validación de entradas en el servidor; límites de uso por usuario y por IP.
- Secretos fuera del código y del repositorio; nunca claves privadas dentro de la app.
- Copias de seguridad automáticas de la base de datos con pruebas periódicas de restauración.
- Registro de eventos de seguridad sin datos sensibles; monitoreo de errores.
- Revisión y actualización regular de dependencias.
- Pruebas de seguridad antes del lanzamiento.
- Verificación en dos pasos opcional (posterior a E6).

### 8.2 Privacidad

- Aviso de privacidad claro y por capas; consentimiento expreso para datos sensibles.
- Minimización: no se recoge lo que no se usa.
- Analítica solo con consentimiento y sin datos de salud.
- Exportación y eliminación (RN-86, RN-87).

### 8.3 Rendimiento y fiabilidad

- Arranque hasta pantalla útil en menos de 3 segundos en un teléfono de gama media.
- Registro de entrenamientos y alimentos **funciona sin conexión** y se sincroniza después.
- Animaciones fluidas (60 cuadros por segundo) con opción de reducirlas.

### 8.4 Accesibilidad

- Contraste WCAG AA, texto escalable, compatibilidad con lectores de pantalla (VoiceOver, TalkBack), áreas táctiles de al menos 44 puntos, no depender solo del color para comunicar.

### 8.5 Plataformas e internacionalización

- iOS y Android, teléfonos primero, diseño adaptable a tablets.
- Todos los textos fuera del código desde el primer día, para poder traducir.
- Unidades (kg/lb, km/mi), moneda, formatos de fecha y reglas de edad configurables por país.
- Catálogo de alimentos con soporte para fuentes por región.

### 8.6 Calidad

- Pruebas automáticas de la lógica de negocio crítica (predicciones, XP, permisos, límites de plan, reglas de edad).
- Cada regla RN de este documento debe poder verificarse con una prueba.

---

## 9. Indicadores de éxito (propuestos)

| Indicador | Qué mide |
|---|---|
| Onboarding completado | % de registros que llegan al inicio |
| Activación | % que registra una primera actividad o comida en 48 h |
| Retención semana 4 | % que sigue activo al mes |
| Constancia | Semanas con objetivo semanal cumplido por usuario |
| Uso de predicciones | % de usuarios con al menos un objetivo con datos suficientes |
| Conversión a Premium | % de usuarios activos que pagan (desde E10) |
| Seguridad | Tiempo de respuesta a reportes; incidentes |

No se optimiza el "tiempo en la app": el objetivo es que la persona registre rápido y vuelva a su vida.

---

## 10. Decisiones abiertas para tu revisión

| N.º | Decisión | Recomendación |
|---|---|---|
| **D-01** | ¿Qué hace la pestaña "Amigos" antes de que exista la comunidad (E9)? | Ocultarla hasta E9 y mostrar 3 pestañas; alternativa: mostrarla con "Próximamente". |
| **D-02** | Disciplinas con métricas propias en el MVP | Gimnasio, running y casa, más registro genérico. |
| **D-03** | ¿Predicciones gratis o Premium? | Gratis en hasta 3 objetivos; Premium amplía profundidad. |
| **D-04** | Espera de 30 días para cambiar de grupo familiar | Mantenerla para evitar abuso. |
| **D-05** | Revisión legal: consentimiento parental (¿todos los menores de 18?), método de verificación y nivel de acceso del tutor | Aplicar la opción más protectora hasta tener asesoría legal. |
| **D-06** | Límites de seguridad nutricional y de ritmo de cambio de peso | Definirlos con un profesional de nutrición antes del lanzamiento. |
| **D-07** | ¿Plan Familiar anual? | No definido; decidir en E10. |
| **D-08** | ¿Periodo de prueba gratuita de Premium? | Decidir en E10. |
| **D-09** | Nombre oficial: "Definite Fitnes" (el repositorio dice "FITNNES") | Confirmar grafía antes de registrar marca y fichas de tienda. |
| **D-10** | Inicio de sesión con Apple y Google | Incluirlos; Apple lo exige si se ofrece otro inicio de sesión de terceros. |

---

## 11. Glosario

- **MVP:** primera versión funcional mínima con la que usuarios reales pueden obtener valor.
- **Onboarding:** preguntas iniciales para configurar la app.
- **Freemium:** modelo con parte gratuita y parte de pago.
- **XP:** puntos de experiencia de la gamificación.
- **Autorización en servidor:** el control de quién puede ver qué se hace en nuestros sistemas, no en el teléfono, donde podría manipularse.
- **ARCO:** derechos de Acceso, Rectificación, Cancelación y Oposición sobre los datos personales.
- **Intervalo o rango de predicción:** fechas entre las que es probable que ocurra algo, en lugar de una fecha única.
