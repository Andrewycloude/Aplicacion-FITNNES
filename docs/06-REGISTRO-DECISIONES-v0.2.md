# Definite Fitnes — Registro de decisiones v0.2

| | |
|---|---|
| **Versión** | 0.2.3 — propuesta |
| **Estado** | Pendiente de aprobación del propietario. **No es definitiva.** |
| **Historial** | v0.2 en Git (commit a5d6863); v0.2.1 (commit abb3921) incorporó DEC-44 y DEC-68; **v0.2.2** corrige hallazgos de la auditoría final (AF-01, 03, 05, 06, 13, 16, 17, 24, 25, 27, 28) y añade DEC-70 a DEC-72; **v0.2.3** registra DEC-66 (aprobada), redefine DEC-72 (pendiente) y añade DEC-73 a DEC-77 (pendientes). La línea base aprobada v0.2.2 es el commit 562f7fc. |
| **Documentos relacionados** | [04 — PRD v0.2](04-PRD-v0.2-PROPUESTA.md) · [05 — Mapa v0.2](05-MAPA-NAVEGACION-v0.2-PROPUESTA.md) · [07 — Trazabilidad](07-TRAZABILIDAD-AUDITORIA-v0.2.md) |

## Estados

| Estado | Significado |
|---|---|
| **Aprobada** | La aprobaste tú (instrucciones originales o decisiones posteriores). |
| **Pendiente** | No está decidida. Incluye las **propuestas de Claude**, que no cuentan como aprobadas hasta que las apruebes. |
| **Requiere validación** | Necesita la opinión de un profesional competente (legal, técnico, nutrición, salud) antes de decidirse o aplicarse. |

Abreviaturas de documentos: **PRD** = 04-PRD-v0.2 · **MAPA** = 05-MAPA-v0.2.

---

## 1. Decisiones aprobadas

### 1.0 Aprobadas en la v0.2.1, la v0.2.2 y la v0.2.3 (decisiones expresas del propietario)

| ID | Descripción | Estado | Justificación | Documentos afectados | Consecuencias sobre el producto |
|---|---|---|---|---|---|
| **DEC-44** | El MVP y su primera beta **no admiten menores de 18 años**. Es una decisión de alcance del lanzamiento inicial: **no elimina** el objetivo futuro de admitir usuarios desde los 13 años | Aprobada | Decisión expresa del propietario; sustituye la versión pendiente de la v0.2 | PRD §3.1, §3.3, §5, §6.1, §7.3, §9, §12 · MAPA A03, A11, marcador ◆ MEN, §3.4, F27 | Las pantallas y páginas web solo necesarias para menores y tutores salen del alcance de la beta y quedan documentadas como **MEN** (habilitación futura): 5 pantallas de la app y 4 páginas web. DEC-18, DEC-30 a DEC-39, DEC-41, DEC-45 y DEC-64 dejan de bloquear la beta y siguen pendientes para la habilitación futura |
| **DEC-68** | Primera beta: **cerrada, gratuita, solo para mayores de 18 años, accesible mediante invitación y sin cobros ni suscripciones** durante esta fase. La beta gratuita **no garantiza gratuidad permanente** | Aprobada | Decisión expresa del propietario; resuelve AF-19 | PRD §1, §4.3, §5.1, §5.2, §7, §8.2, RN-141 a RN-143 · MAPA A02, A12, A17, F21, F26 | Nueva pantalla A17 (invitación); aviso de no gratuidad permanente en la invitación y en los términos de la beta; se mantienen todas las obligaciones legales y de privacidad para adultos; mecanismo de invitaciones pendiente (DEC-69); política de transición pendiente (DEC-67). Pagos y suscripciones siguen sin implementarse (DEC-01, DEC-22) |
| **DEC-70** | Los documentos legales validados son **requisito previo para invitar a usuarios reales** a la beta | Aprobada | Instrucción expresa del propietario (v0.2.2); resuelve en parte AF-18 | PRD §5.1, §8.6, RN-144 · MAPA A12, F26 | No se invita a nadie real hasta tener los documentos de DEC-71 validados y publicados en A12. Las obligaciones para adultos se mantienen (DEC-68) |
| **DEC-66** | **Compatibilidad con tablets durante la beta y el MVP:** compatibilidad básica, sin interfaces optimizadas específicamente para tablets. **Android:** adaptación a distintos tamaños de ventana y orientaciones, conservación del estado de formularios y actividades, y funcionamiento correcto en pantalla dividida. **Apple:** se prioriza iPhone; durante la beta la app se publica como aplicación para iPhone, con compatibilidad básica en iPad mediante el modo de compatibilidad para apps de iPhone. La optimización específica para tablets se evaluará antes del lanzamiento público, **sin compromiso de desarrollarla**. Requisitos técnicos TB-01 a TB-04 | Aprobada | Decisión expresa del propietario (v0.2.3) tras el análisis de ET4. Base verificada en documentación oficial: Android 16 (API 36) ignora las restricciones de orientación y tamaño en pantallas de al menos 600 dp; Google Play exige API 36 desde el 31 de agosto de 2026; Android 17 (API 37) elimina la excepción temporal | PRD §5.2, §10 (TB-01 a TB-04) · MAPA §10 | El sistema de diseño (ET3) define ancho máximo y puntos de corte; las pruebas incluyen tablets Android en vertical, horizontal y pantalla dividida. Compatible con DEC-03 (no es la optimización específica pospuesta) y no cierra DEC-59 |

### 1.1 Aprobadas para la v0.2 (mensaje del 16 de noviembre)

| ID | Descripción | Estado | Justificación | Documentos afectados | Consecuencias sobre el producto |
|---|---|---|---|---|---|
| **DEC-01** | Durante el MVP no se aplican restricciones de Premium; los pagos y límites de planes se implementan en ET10 | Aprobada | Tu decisión A. Permite probar todo el MVP sin crear límites sin forma de pagar | PRD §5.2, §6.4, §6.5, §7, RN-35, RN-138 · MAPA E04, P02, P03, P05, N07, U09 | Desaparecen los enlaces a U09 desde el MVP; los límites del plan Gratis pasan a ser propuesta para ET10 (DEC-62); surge la necesidad de definir la transición de usuarios del MVP (DEC-67) |
| **DEC-02** | La Etapa 6 se divide en tres entregas internas: ET6.1 (acceso, registro, onboarding, inicio, perfil), ET6.2 (entrenamiento y progreso), ET6.3 (nutrición) | Aprobada | Tu decisión B-A. Reduce riesgo y permite revisar cada parte | PRD §0.2, §5.1, §5.2, RN-127 · MAPA inventario, §4.2 | Las pantallas se asignan a una entrega; la barra inferior y el inicio crecen por entregas |
| **DEC-03** | Pasan a etapas posteriores, sin salir de la visión: tema claro, optimización específica para tablets, biblioteca amplia de recetas y programas de entrenamiento extensos | Aprobada | Tu decisión B-C | PRD §5.2, §6.3, §6.4, §6.6 · MAPA U04, N05, E10, §10 | El MVP tiene solo tema oscuro y diseño de teléfono; conserva recetas y programas **básicos** (cantidad: DEC-63). Etapa exacta: DEC-59 |
| **DEC-04** | El modo sin conexión se limita al registro y consulta de una sesión de entrenamiento que ya está en curso | Aprobada | Tu decisión B-D. La sincronización completa es de lo más complejo en apps móviles | PRD RN-30, §10 · MAPA E06, E07, E09, §6, F11 | Iniciar una sesión, registrar alimentos o cualquier otra acción requiere conexión en el MVP; se define el estado "pendiente de envío" |
| **DEC-05** | Base de alimentos inicial acotada, con alimentos comunes en México y fuentes verificables; no se inventan datos ni se presentan estimaciones como exactas | Aprobada | Tu decisión B-E | PRD §6.3, RN-137 · MAPA N03, N04 | Búsquedas con menos resultados al principio; el estado vacío de N04 ofrece crear un alimento propio. Fuentes y licencias: DEC-57 |
| **DEC-06** | La primera versión se diseña para México; la arquitectura permite configurar reglas por país, sin asumir que los requisitos mexicanos son universales | Aprobada | Tu decisión C | PRD §1, §4.3, §8.4, RN-124 | Se crea el servicio de políticas con configuración por país. Cómo se determina el país: DEC-43 |
| **DEC-07** | Se conserva la necesidad de una experiencia segura y sencilla para tutores, implementada por etapas, documentando qué funciones requieren web | Aprobada | Tu decisión D | PRD §9.5, RN-117 · MAPA T01–T04, §3.2 | La experiencia del tutor no se elimina; la propuesta de fases es DEC-45 |
| **DEC-08** | Crear una cuenta no depende de aceptar el tratamiento de datos de salud; sin ese consentimiento, las funciones que dependen de esos datos quedan desactivadas | Aprobada | Tu decisión E | PRD RN-129, RN-131, §8.3 · MAPA A04, A14, M01, U18, F05, §8 | A04 ya no incluye la casilla de salud; se crean A14, U18 y M01. Qué datos son "de salud": DEC-42 |
| **DEC-09** | Apple y Google como opciones de acceso; ninguna autenticación social permite saltarse la verificación de edad | Aprobada | Tu decisión F | PRD RN-128 · MAPA A03, A04, A06, F02 | Un inicio con Apple o Google sin cuenta pasa por A03 antes de crear nada |
| **DEC-10** | Se mantiene provisionalmente el nombre "Definite Fitnes" | Aprobada | Tu decisión G | PRD encabezado | Su validación como marca sigue abierta: DEC-53 |

### 1.2 Aprobadas en mensajes anteriores e instrucciones originales

| ID | Descripción | Estado | Justificación | Documentos afectados | Consecuencias sobre el producto |
|---|---|---|---|---|---|
| **DEC-11** | Privacidad por defecto y minimización de datos | Aprobada | Instrucciones originales y sección "Protección de usuarios menores" | PRD PR-1, PR-4, §8.2 | Base de RN-125, RN-133 y DEC-64 |
| **DEC-12** | Tres tramos con experiencias diferenciadas: 13–15, 16–17 y 18+, con controles por edad | Aprobada (el contenido de cada tramo está pendiente) | Tu respuesta del 15 de noviembre | PRD §3.1, §9 | El servicio de políticas trabaja por tramo; el contenido de cada tramo: DEC-32, DEC-33 |
| **DEC-13** | No promover restricciones alimentarias, objetivos calóricos restrictivos ni ideales corporales | Aprobada | Instrucciones originales y protección de menores | PRD PR-7, RN-12, RN-22, RN-23, RN-53 · MAPA O02, P03 | Sin objetivos estéticos ni restrictivos para menores; sin lenguaje moral sobre alimentos |
| **DEC-14** | No usar predicciones corporales ni médicas para menores | Aprobada | Sección "Protección de usuarios menores" | PRD RN-43 · MAPA P03, P04, §8 | P04 no muestra predicciones corporales a menores, decida lo que se decida sobre el registro de medidas (DEC-35) |
| **DEC-15** | El administrador familiar no ve automáticamente datos privados de otros integrantes | Aprobada | Tu respuesta del 15 de noviembre | PRD RN-101 · MAPA U10 | U10 solo muestra nombre, estado y fecha |
| **DEC-16** | No castigar el descanso ni fomentar el entrenamiento excesivo | Aprobada | Instrucciones originales | PRD PR-3, RN-15, RN-32, RN-33, RN-49–RN-51 | Sugerencias de descanso; días de descanso planificables; sin penalizaciones |
| **DEC-17** | La IA no diagnostica ni sustituye a profesionales | Aprobada | Instrucciones originales | PRD RN-74 | Aplica a todas las edades |
| **DEC-19** | Planes: Gratis $0; Premium $50 MXN/mes y $500 MXN/año; Familiar $200 MXN/mes, hasta 6 personas incluido el administrador, cada una con datos propios | Aprobada | Tu respuesta del 15 de noviembre | PRD §7 | Se implementan en ET10 |
| **DEC-20** | Se conserva la visión completa; solo cambia la etapa de las funciones | Aprobada | Tus respuestas del 15 y 16 de noviembre | PRD §5.2 · MAPA inventario | Ninguna función de la visión se elimina |
| **DEC-21** | Seguridad, privacidad, información esencial y ayuda nunca se bloquean por suscripción | Aprobada | Instrucciones originales | PRD PR-5, RN-91 · MAPA §8 | U12, U13, U14 y U18 siempre disponibles |
| **DEC-22** | No implementar pagos hasta definir proveedores, comisiones, reglas y condiciones de las tiendas | Aprobada | Instrucciones originales | PRD RN-95 | Pagos solo en ET10 |

---

## 2. Asuntos pendientes que indicaste expresamente

Ninguno se resuelve en esta propuesta. Las alternativas están en el PRD §9.3.

**Desde la v0.2.1 (DEC-44), ninguno bloquea la beta ni el MVP:** bloquean la habilitación futura de menores (MEN). Su estado no cambia.

| ID | Descripción | Estado | Justificación | Documentos afectados | Consecuencias sobre el producto |
|---|---|---|---|---|---|
| **DEC-30** | Requisitos legales del consentimiento parental | Requiere validación (legal) | Indicado por ti como pendiente | PRD §9.3, RN-04, RN-111 · MAPA A09, A10, T01 | Sin resolver, no pueden habilitarse menores (DEC-44) |
| **DEC-31** | Verificación de edad y mecanismos de autorización de tutores | Requiere validación (legal y técnica) | Indicado por ti | PRD §9.3, RN-01, RN-112, RN-117 · MAPA A03, T01 | Puede requerir un proveedor externo o un cargo verificador, con impacto en costo, datos y fricción |
| **DEC-32** | Experiencia y restricciones para 13–15 | Requiere validación (legal y profesional) | Indicado por ti | PRD §9.3, §9.4, RN-36, RN-57, RN-70, RN-85 · MAPA O02, E01, U07, §8 | Afecta casi todos los módulos; entretanto, funciones desactivadas para este tramo (DEC-64) |
| **DEC-33** | Experiencia y restricciones para 16–17 | Requiere validación (legal y profesional) | Indicado por ti | Ídem DEC-32 | Ídem |
| **DEC-34** | Tratamiento de datos de salud de menores | Requiere validación (legal) | Indicado por ti | PRD §9.3, §8.3 · MAPA A14, O08, O09 | Determina qué categorías de consentimiento ven los menores |
| **DEC-35** | Uso de peso, medidas y objetivos relacionados con el cuerpo en menores | Requiere validación (legal y profesional) | Indicado por ti | PRD RN-134, §9.3 · MAPA O10, P07, U02 | Las predicciones corporales para menores ya están excluidas (DEC-14); queda el registro |
| **DEC-36** | Funciones nutricionales para menores | Requiere validación (profesional) | Indicado por ti | PRD RN-27, §9.3 · MAPA N01, N03, N10, O07, O08 | Puede cambiar de forma importante lo que ve un menor en ET6.3 |
| **DEC-37** | Apple Health y Health Connect para menores | Requiere validación (legal y políticas de las tiendas) | Indicado por ti | PRD §6.11, §9.3 · MAPA U15 | Debe decidirse antes de ET10 |
| **DEC-38** | Participación de menores en planes familiares | Pendiente | Indicado por ti | PRD RN-97, RN-108 · MAPA U09, U17, F19 | Determina si una invitación puede llevar a un registro de menor |
| **DEC-39** | Acceso de tutores a información de los menores | Requiere validación (legal) | Indicado por ti | PRD RN-115, RN-116, §9.5 · MAPA T02, U16, A16 | Define el contenido de T02 y del resumen para el tutor |
| **DEC-40** | Moderación y seguridad de la comunidad | Pendiente | Indicado por ti | PRD §6.9 · MAPA S01–S11 | Debe resolverse antes de ET9; incluye herramienta interna de moderación |
| **DEC-41** | Disponibilidad del asistente de IA para menores | Requiere validación (legal y técnica) | Indicado por ti | PRD RN-80, §9.3 · MAPA I01 | Debe resolverse antes de ET8 |

---

## 3. Otras decisiones pendientes

**Nota v0.2.1:** con DEC-44 aprobada, DEC-45 y DEC-64 solo aplican a la habilitación futura de menores; su estado no cambia.

**Nota v0.2.2 (AF-01):** DEC-18 se movió aquí desde la sección de aprobadas, porque su estado es "Requiere validación". Su contenido no cambia.


Incluye las decisiones abiertas de la v0.1 que siguen vigentes y las surgidas al preparar esta propuesta. Las marcadas **(propuesta de Claude)** tienen una sugerencia en el PRD o el mapa que **no debe tomarse como aprobada**.

| ID | Descripción | Estado | Justificación | Documentos afectados | Consecuencias sobre el producto |
|---|---|---|---|---|---|
| **DEC-18** | Edad mínima de 13 años | Requiere validación | La intención la aprobaste el 15 de noviembre; en tu mensaje del 16 indicas que su implementación requiere validación legal | PRD §3.1 · MAPA A03, A11 | El valor se guarda como configuración por país (RN-124) |
| **DEC-42** | Qué datos se consideran "de salud" y granularidad de los consentimientos | Requiere validación (legal) | Necesario para aplicar DEC-08. **Bloquea ET6.1** | PRD §8.3, RN-130 · MAPA A14, §8 | Si actividad y alimentación se consideran datos de salud, gran parte de la app dependería de ese consentimiento |
| **DEC-43** | Cómo se determina el país del usuario (tienda, configuración del teléfono, pregunta explícita) | Pendiente | Necesario para DEC-06 y para la edad mínima. **Bloquea ET6.1** | PRD §8.4 | Afecta a A03 y al servicio de políticas |
| **DEC-45** | Fases de la experiencia del tutor: fase 1 con T01, T03, T04 y correos; fase 2 con el panel T02 (propuesta de Claude) | Pendiente | Desarrolla DEC-07 | PRD §9.5 · MAPA §3.2 | Fase 1 requiere igualmente una pequeña web segura |
| **DEC-46** | Pestaña "Amigos" antes de ET9 (ocultar o mostrar "Próximamente") — v0.1 D-01 | Pendiente | Sin cambios desde v0.1 | PRD RN-14 · MAPA §4.2 | Afecta a la barra inferior del MVP |
| **DEC-47** | Disciplinas con métricas propias en el MVP (propuesta: gimnasio, running, casa) — v0.1 D-02 | Pendiente | Sin aprobación todavía. **Bloquea ET6.2** | PRD §6.4 | Determina el trabajo de ET6.2 |
| **DEC-48** | Predicciones en plan Gratis o Premium — v0.1 D-03 | Pendiente | Se decide en ET10 | PRD §7.2 | Sin efecto en el MVP (DEC-01) |
| **DEC-49** | Espera entre grupos familiares (propuesta: 30 días) — v0.1 D-04 | Pendiente | Se decide en ET10 | PRD RN-105 · MAPA U10 | Prevención de reventa de lugares |
| **DEC-50** | Límites de seguridad nutricional y de ritmo de cambio de peso para adultos — v0.1 D-06 | Requiere validación (profesional de nutrición) | **Bloquea ET6.3** y las metas corporales de P03 | PRD RN-22, RN-43 · MAPA P03 | Sin valores validados, no pueden activarse metas de energía ni de peso |
| **DEC-51** | Plan Familiar anual — v0.1 D-07 | Pendiente | ET10 | PRD §7 | — |
| **DEC-52** | Prueba gratuita de Premium — v0.1 D-08 | Pendiente | ET10 | PRD §7 | — |
| **DEC-53** | Validación del nombre como marca — parte de v0.1 D-09 | Requiere validación (legal: registro de marca) | DEC-10 lo mantiene provisionalmente | PRD encabezado | Debe resolverse antes de publicar en tiendas |
| **DEC-54** | Qué activa la opción "Bienestar y hábitos" del onboarding y si da acceso a hábitos sin Nutrición | Pendiente | Hallazgo X-05 | PRD §6.3 · MAPA O03, N08 | Puede requerir un acceso a hábitos fuera de Nutrición |
| **DEC-55** | Modalidad principal sin métricas propias en el MVP: usar registro genérico con aviso (propuesta de Claude) | Pendiente | Hallazgo R-08 / v0.1 DP-06 | PRD RN-35 · MAPA O04 | Afecta a usuarios de natación, ciclismo, fútbol, etc. |
| **DEC-56** | Foto de perfil: si se incluye en el MVP y para qué edades | Pendiente | Hallazgo P-12 | PRD §6.8 · MAPA U01 | Subir fotos implica almacenamiento y, en ET9, moderación |
| **DEC-57** | Fuentes y licencias de contenido: ejercicios, imágenes, alimentos y recetas. **Fuentes de alimentos candidatas (AF-24), todas con licencia por verificar:** USDA FoodData Central (el USDA las publica como datos de dominio público; verificar condiciones y adecuación a alimentos mexicanos); Open Food Facts (según su documentación usa la licencia ODbL, con obligaciones de atribución y de compartir bases derivadas; verificar el efecto sobre la base propia); tablas de composición de alimentos publicadas por instituciones mexicanas (probablemente protegidas por derechos de autor; requieren permiso) | Requiere validación (legal y técnica) | **Bloquea ET6.2 y ET6.3** | PRD RN-18, RN-29, §10 | Sin contenido con licencia no hay biblioteca ni base de alimentos. La lista es de candidatas, no una elección |
| **DEC-58** | Qué es la "comparación de escenarios" Premium en predicciones | Pendiente | Hallazgo de la auditoría DP-17 | PRD §7.2 | ET10 |
| **DEC-59** | Etapa exacta de las funciones pospuestas (tema claro, tablets, recetas amplias, programas extensos, panel del tutor) | Pendiente | DEC-03 las pospone sin fijar etapa | PRD §5.2 · MAPA marcador POST | Planificación |
| **DEC-60** | Valores numéricos propuestos por Claude: caducidad de solicitud de tutor (14 días), contraseña (10 caracteres), periodo de gracia (30 días), umbral de predicción (6 registros en 3 semanas), caducidad de invitaciones (7 días), meta de onboarding (3 minutos) | Pendiente | Anexo A de la auditoría. Algunos requieren validación legal (14 y 30 días) | PRD RN-04, RN-05, RN-10, RN-38, RN-87, RN-102 | Se usan en ET6.1 y ET6.2; deben aprobarse antes |
| **DEC-61** | Criterios para detectar señales de riesgo alimentario y mostrar el mensaje de cuidado | Requiere validación (profesional de salud) | Hallazgo P-08 | PRD RN-25 · MAPA M02 | Sin criterios validados, M02 no puede activarse |
| **DEC-62** | Límites concretos del plan Gratis (rutinas, objetivos, historial visible, modalidades) | Pendiente | Se decide en ET10 (DEC-01) | PRD §7.2 | Sin efecto en el MVP |
| **DEC-63** | Cantidad inicial de recetas y programas básicos en el MVP | Pendiente | DEC-03 conserva los básicos | PRD §6.3, §6.4 · MAPA N05, E10 | Trabajo de contenido de ET6.2 y ET6.3 |
| **DEC-64** | Mientras una decisión sobre menores esté pendiente, la función queda desactivada para ese tramo (propuesta de Claude) | Pendiente | Deriva de DEC-11, pero es un criterio nuevo | PRD PR-8, RN-125, §9.2 | Permite construir sin decidir la experiencia de menores |
| **DEC-65** | La analítica permanece desactivada hasta que el usuario la consienta (propuesta de Claude) | Pendiente | Hallazgo E-09; deriva de DEC-11 | PRD RN-133 · MAPA A14 | Menos datos de uso al principio |
| **DEC-67** | **Política de transición de la beta gratuita a planes comerciales:** qué ocurre con las cuentas, los datos y lo creado por quienes participaron en la beta cuando se activen los planes (aviso previo, periodo de cortesía, condiciones) | Pendiente | Consecuencia de DEC-01 y DEC-68; redefinida en la v0.2.1 por instrucción del propietario | PRD RN-140, RN-141 · MAPA F21 | Debe resolverse antes de activar planes comerciales (ET10). Mínimo propuesto: no se borra nada (RN-92, propuesta). Puede requerir validación legal (protección al consumidor) |
| **DEC-69** | Mecanismo de invitaciones a la beta: quién invita, cuántas invitaciones hay, si los códigos son de un solo uso, caducidad y qué ve quien no tiene invitación | Pendiente | Necesario para aplicar DEC-68. **Bloquea ET6.1** | PRD RN-143 · MAPA A17, F26 | Define los estados de error de A17 y la comunicación a quien no tiene invitación |
| **DEC-71** | Redacción y validación legal de los documentos de la beta: Términos y condiciones, Términos de la beta (con RN-141), Aviso de privacidad para adultos (consentimientos separados de DEC-08, categorías de DEC-42, encargados como el proveedor de correo) y procedimiento ARCO; y cualquier otro que indique el abogado | Requiere validación (legal) | Necesario para cumplir DEC-70 | PRD §8.6, RN-90, RN-144 · MAPA A04, A12 | Sin ellos no se puede invitar a usuarios reales |
| **DEC-72** | **Proveedor de correo transaccional.** API como método preferido y SMTP como alternativa (no se exigen ambos). Si el servicio de autenticación elegido (DEC-76) usa su propio sistema de envío de correos, su compatibilidad con los requisitos de privacidad, seguridad y entregabilidad se evalúa por separado, sin obligar a usar un único proveedor para todos los correos. **CT-14 se aplica a todos los correos transaccionales de Definite Fitnes, independientemente del servicio que los envíe.** Candidatos, sin seleccionar ninguno: Amazon SES, Postmark, Resend, SendGrid y Mailgun. Investigar proveedores no requiere un dominio definitivo; **configurar el dominio** (SPF, DKIM, DMARC) queda pendiente hasta decidir qué dominio usar (relacionado con DEC-53) | Pendiente | Redefinida en la v0.2.3 con aprobación del propietario. Se selecciona después de DEC-74 y DEC-76, con información verificada en fuentes oficiales (precios, ubicación de datos, conservación, contrato de tratamiento). **Bloquea ET6.1** | PRD §4.2, §8.5 (CT-09, CT-14) · MAPA §9 | Debe estar seleccionado antes de completar ET6.1. Si la autenticación envía sus propios correos, DEC-72 cubre el resto (avisos de cuenta, exportación, eliminación, ARCO) |
| **DEC-73** | Tecnología de la aplicación móvil (iOS y Android) | Pendiente | Separación tecnológica aprobada por el propietario (v0.2.3). Orden de análisis: 1.º. **Bloquea ET4** | PRD §4, §12 | Registrarla como pendiente **no elige ninguna tecnología ni proveedor**; solo autoriza su análisis comparativo con criterios objetivos: rendimiento, mantenimiento, compatibilidad, ecosistema, costos y facilidad de desarrollo. Debe cumplir DEC-66 |
| **DEC-74** | Backend: dónde y cómo se ejecuta la lógica del servidor | Pendiente | Separación tecnológica aprobada por el propietario (v0.2.3). Orden de análisis: 4.º. **Bloquea ET4** | PRD §4, §12 | Registrarla como pendiente **no elige ninguna tecnología ni proveedor**; solo autoriza su análisis comparativo con criterios objetivos: rendimiento, mantenimiento, compatibilidad, ecosistema, costos y facilidad de desarrollo. Condiciona DEC-72 |
| **DEC-75** | Base de datos y almacenamiento de archivos | Pendiente | Separación tecnológica aprobada por el propietario (v0.2.3). Orden de análisis: 2.º. **Bloquea ET4** | PRD §4, §12 | Registrarla como pendiente **no elige ninguna tecnología ni proveedor**; solo autoriza su análisis comparativo con criterios objetivos: rendimiento, mantenimiento, compatibilidad, ecosistema, costos y facilidad de desarrollo. Debe considerar DEC-42 (datos de salud) |
| **DEC-76** | Autenticación: cuentas con correo, Apple y Google, y sesiones | Pendiente | Separación tecnológica aprobada por el propietario (v0.2.3). Orden de análisis: 5.º. **Bloquea ET4** | PRD §4, §12 | Registrarla como pendiente **no elige ninguna tecnología ni proveedor**; solo autoriza su análisis comparativo con criterios objetivos: rendimiento, mantenimiento, compatibilidad, ecosistema, costos y facilidad de desarrollo. Debe cumplir DEC-09 y RN-128; condiciona DEC-72 |
| **DEC-77** | Infraestructura y alojamiento: nube y región | Pendiente | Separación tecnológica aprobada por el propietario (v0.2.3). Orden de análisis: 3.º. **Bloquea ET4** | PRD §4, §12 | Registrarla como pendiente **no elige ninguna tecnología ni proveedor**; solo autoriza su análisis comparativo con criterios objetivos: rendimiento, mantenimiento, compatibilidad, ecosistema, costos y facilidad de desarrollo. Debe considerar DEC-06 y CT-12 (ubicación de los datos) |

---

## 4. Equivalencias con las decisiones de la v0.1 y la auditoría

| v0.1 / auditoría | v0.2 | Estado |
|---|---|---|
| D-01 Pestaña Amigos | DEC-46 | Pendiente |
| D-02 Disciplinas del MVP | DEC-47 | Pendiente |
| D-03 Predicciones gratis o Premium | DEC-48 | Pendiente |
| D-04 Espera entre grupos | DEC-49 | Pendiente |
| D-05 Revisión legal de menores | DEC-30, DEC-31, DEC-34, DEC-39 | Requiere validación |
| D-06 Límites nutricionales | DEC-50 | Requiere validación |
| D-07 Familiar anual | DEC-51 | Pendiente |
| D-08 Prueba gratuita | DEC-52 | Pendiente |
| D-09 Nombre | DEC-10 (provisional) + DEC-53 | Aprobada + Requiere validación |
| D-10 Apple y Google | DEC-09 | Aprobada |
| DP-01 Límites en el MVP | DEC-01 | Aprobada |
| DP-02 Alcance del MVP | DEC-01 a DEC-05 | Aprobada |
| DP-03 País | DEC-06 + DEC-43 | Aprobada + Pendiente |
| DP-04 Panel del tutor | DEC-07 + DEC-45 | Aprobada + Pendiente |
| DP-05 Bienestar y hábitos | DEC-54 | Pendiente |
| DP-06 Modalidad sin métricas | DEC-55 | Pendiente |
| DP-07 Peso 16–17 | DEC-35 | Requiere validación |
| DP-08 Nutrición 13–15 | DEC-36 | Requiere validación |
| DP-09 Entrenamiento 13–15 | DEC-32 | Requiere validación |
| DP-10 Resumen para el tutor | DEC-39 | Requiere validación |
| DP-11 Foto de perfil | DEC-56 | Pendiente |
| DP-12 Menores en Familiar | DEC-38 | Pendiente |
| DP-13 Consentimiento de salud | DEC-08 + DEC-42 | Aprobada + Requiere validación |
| DP-14 Moderación | DEC-40 | Pendiente |
| DP-15 Fuentes de contenido | DEC-57 | Requiere validación |
| DP-16 Tablets y tema claro | DEC-03 + DEC-66 | Aprobada + Requiere validación |
| DP-17 Comparación de escenarios | DEC-58 | Pendiente |
| AF-19 Lanzamiento del MVP (auditoría final) | DEC-68 | Aprobada |
| v0.2 DEC-44 Habilitación de menores en el MVP | DEC-44 (redefinida: no se admiten menores en la beta ni en el MVP) | Aprobada |
| AF-18 Documentos legales | DEC-70 (requisito) + DEC-71 (validación) | Aprobada + Requiere validación |
| AF-12 Correo transaccional | DEC-72 (proveedor); requisitos en PRD §8.5 | Pendiente |

---

## 5. Resumen

| Estado | Cantidad | IDs |
|---|---|---|
| Aprobada | 25 | DEC-01, DEC-02, DEC-03, DEC-04, DEC-05, DEC-06, DEC-07, DEC-08, DEC-09, DEC-10, DEC-11, DEC-12, DEC-13, DEC-14, DEC-15, DEC-16, DEC-17, DEC-19, DEC-20, DEC-21, DEC-22, DEC-44, DEC-66, DEC-68, DEC-70 |
| Requiere validación | 17 | DEC-18, DEC-30, DEC-31, DEC-32, DEC-33, DEC-34, DEC-35, DEC-36, DEC-37, DEC-39, DEC-41, DEC-42, DEC-50, DEC-53, DEC-57, DEC-61, DEC-71 |
| Pendiente | 28 | DEC-38, DEC-40, DEC-43, DEC-45, DEC-46, DEC-47, DEC-48, DEC-49, DEC-51, DEC-52, DEC-54, DEC-55, DEC-56, DEC-58, DEC-59, DEC-60, DEC-62, DEC-63, DEC-64, DEC-65, DEC-67, DEC-69, DEC-72, DEC-73, DEC-74, DEC-75, DEC-76, DEC-77 |
| **Total** | **70** | |

**Numeración (AF-05):** los identificadores DEC son secuenciales y **no indican estado**. Los números DEC-23 a DEC-29 no se usaron y quedan sin asignar; cada decisión nueva toma el siguiente número libre. Ningún identificador existente se renumera, para conservar la trazabilidad.

---

## 6. Qué bloquea cada decisión no aprobada (AF-17)

Fuente única para el PRD §12. "Bloquea" indica el primer hito que no puede completarse sin la decisión.

| Decisión | Tema | Estado | Bloquea | Notas |
|---|---|---|---|---|
| DEC-73 | Tecnología de la aplicación móvil | Pendiente | ET4 (arquitectura técnica) | Análisis 1.º; debe cumplir DEC-66 |
| DEC-75 | Base de datos y almacenamiento | Pendiente | ET4 (arquitectura técnica) | Análisis 2.º; considerar DEC-42 |
| DEC-77 | Infraestructura y alojamiento | Pendiente | ET4 (arquitectura técnica) | Análisis 3.º; considerar DEC-06 y CT-12 |
| DEC-74 | Backend | Pendiente | ET4 (arquitectura técnica) | Análisis 4.º; condiciona DEC-72 |
| DEC-76 | Autenticación | Pendiente | ET4 (arquitectura técnica) | Análisis 5.º; condiciona DEC-72 |
| DEC-42 | Qué datos son de salud y granularidad de consentimientos [VAL] | Requiere validación | ET6.1 (acceso, registro, onboarding, inicio y perfil) | — |
| DEC-43 | Cómo se determina el país del usuario | Pendiente | ET6.1 (acceso, registro, onboarding, inicio y perfil) | — |
| DEC-54 | Bienestar y hábitos en el onboarding | Pendiente | ET6.1 (acceso, registro, onboarding, inicio y perfil) | También afecta a ET6.3 |
| DEC-55 | Modalidad principal sin métricas propias | Pendiente | ET6.1 (acceso, registro, onboarding, inicio y perfil) | También afecta a ET6.2 |
| DEC-56 | Foto de perfil | Pendiente | ET6.1 (acceso, registro, onboarding, inicio y perfil) | — |
| DEC-60 | Valores numéricos propuestos | Pendiente | ET6.1 (acceso, registro, onboarding, inicio y perfil) | También afecta a ET6.2 (umbral de predicción) y MEN (plazo del tutor) |
| DEC-65 | Analítica desactivada hasta su consentimiento | Pendiente | ET6.1 (acceso, registro, onboarding, inicio y perfil) | — |
| DEC-69 | Mecanismo de invitaciones a la beta | Pendiente | ET6.1 (acceso, registro, onboarding, inicio y perfil) | — |
| DEC-72 | Proveedor de correo transaccional | Pendiente | ET6.1 (acceso, registro, onboarding, inicio y perfil) | Depende de DEC-74 y DEC-76; se selecciona en último lugar |
| DEC-71 | Redacción y validación de los documentos legales de la beta [VAL] | Requiere validación | Invitar a usuarios reales a la beta | — |
| DEC-47 | Disciplinas con métricas propias | Pendiente | ET6.2 (entrenamiento y progreso) | — |
| DEC-57 | Fuentes y licencias de contenido [VAL] | Requiere validación | ET6.2 (entrenamiento y progreso) | También afecta a ET6.3 |
| DEC-63 | Cantidad inicial de recetas y programas | Pendiente | ET6.2 (entrenamiento y progreso) | — |
| DEC-50 | Límites de seguridad nutricional [VAL] | Requiere validación | ET6.3 (nutrición) | — |
| DEC-61 | Criterios de señales de riesgo [VAL] | Requiere validación | ET6.3 (nutrición) | — |
| DEC-46 | Pestaña Amigos antes de la comunidad | Pendiente | Cierre del MVP | — |
| DEC-40 | Moderación y seguridad de la comunidad | Pendiente | ET9 (comunidad) | — |
| DEC-48 | Predicciones gratis o Premium | Pendiente | ET10 (planes comerciales e integraciones) | — |
| DEC-49 | Espera entre grupos familiares | Pendiente | ET10 (planes comerciales e integraciones) | — |
| DEC-51 | Plan Familiar anual | Pendiente | ET10 (planes comerciales e integraciones) | — |
| DEC-52 | Prueba gratuita | Pendiente | ET10 (planes comerciales e integraciones) | — |
| DEC-58 | Comparación de escenarios | Pendiente | ET10 (planes comerciales e integraciones) | — |
| DEC-62 | Límites del plan Gratis | Pendiente | ET10 (planes comerciales e integraciones) | — |
| DEC-67 | Transición de la beta gratuita a planes comerciales | Pendiente | ET10 (planes comerciales e integraciones) | — |
| DEC-53 | Validación del nombre como marca [VAL] | Requiere validación | Publicación en tiendas | — |
| DEC-59 | Etapa de las funciones pospuestas | Pendiente | Planificación posterior al MVP | — |
| DEC-18 | Edad mínima de 13 años [VAL] | Requiere validación | MEN (habilitación futura de menores) | — |
| DEC-30 | Consentimiento parental [VAL] | Requiere validación | MEN (habilitación futura de menores) | — |
| DEC-31 | Verificación de edad y autorización del tutor [VAL] | Requiere validación | MEN (habilitación futura de menores) | — |
| DEC-32 | Experiencia 13–15 [VAL] | Requiere validación | MEN (habilitación futura de menores) | — |
| DEC-33 | Experiencia 16–17 [VAL] | Requiere validación | MEN (habilitación futura de menores) | — |
| DEC-34 | Datos de salud de menores [VAL] | Requiere validación | MEN (habilitación futura de menores) | — |
| DEC-35 | Peso, medidas y objetivos corporales en menores [VAL] | Requiere validación | MEN (habilitación futura de menores) | — |
| DEC-36 | Nutrición para menores [VAL] | Requiere validación | MEN (habilitación futura de menores) | — |
| DEC-37 | Apple Health / Health Connect para menores [VAL] | Requiere validación | MEN (habilitación futura de menores) | También afecta a ET10 |
| DEC-38 | Menores en planes familiares | Pendiente | MEN (habilitación futura de menores) | — |
| DEC-39 | Acceso del tutor a la información del menor [VAL] | Requiere validación | MEN (habilitación futura de menores) | — |
| DEC-41 | IA para menores [VAL] | Requiere validación | MEN (habilitación futura de menores) | — |
| DEC-45 | Fases de la experiencia del tutor | Pendiente | MEN (habilitación futura de menores) | — |
| DEC-64 | Desactivado mientras esté pendiente (menores) | Pendiente | MEN (habilitación futura de menores) | — |
