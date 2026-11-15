# Definite Fitnes — Auditoría cruzada del PRD y el mapa de navegación

| | |
|---|---|
| **Versión** | 1.0 |
| **Documentos auditados** | `docs/01-PRD.md` v0.1 y `docs/02-MAPA-NAVEGACION.md` v0.1 |
| **Alcance** | Solo revisión. No se modificó ningún documento ni se escribió código. |
| **Estado** | Pendiente de tu revisión |

> **Cómo leer este informe.** Cada hallazgo tiene un código (por ejemplo **X-03**) y una severidad:
> - **Alta:** bloquea el desarrollo o puede causar un problema legal o de seguridad si no se resuelve.
> - **Media:** genera ambigüedad; hay que resolverla antes de construir esa parte.
> - **Baja:** corrección de redacción o consistencia.
>
> Las columnas "Propuesta" son **sugerencias de corrección**, no decisiones. Nada de lo propuesto se aplicará sin tu aprobación, y ninguna propuesta elimina funcionalidades de la visión.

---

## 0. Resumen ejecutivo

| Área | Hallazgos | Altas | Medias | Bajas |
|---|---|---|---|---|
| 1. Contradicciones entre documentos | 10 | 3 | 5 | 2 |
| 2. Pantallas, botones y recorridos incompletos | 14 | 3 | 9 | 2 |
| 3. IDs e inventario | 7 | 0 | 2 | 5 |
| 4. Reglas de negocio sin reflejo en la navegación | 15 | 2 | 10 | 3 |
| 5. Edad y privacidad | 13 | 6 | 6 | 1 |
| **Total** | **59** | **14** | **32** | **13** |

**Conclusiones principales**

1. **Los documentos son coherentes en lo esencial.** Los módulos, la mayoría de las reglas y las etapas coinciden. Los problemas están en los bordes: casos de menores, transiciones entre etapas y pantallas que se mencionan pero no existen.
2. **El hallazgo más importante es de alcance:** el MVP (Etapa 6) incluye unas 70 pantallas, un **panel web para tutores** (una segunda plataforma), contenido que hay que producir o licenciar (ejercicios, programas, recetas, base de alimentos) y funciones exigentes como el modo sin conexión. Para un desarrollo con Claude Code y una sola persona decidiendo, es grande. Ver sección 6.
3. **Hay una contradicción de fondo sin resolver:** el MVP no tiene pagos, pero varias pantallas del MVP aplican límites del plan Gratis y enlazan a la pantalla de planes, que no existe hasta la Etapa 10 (X-01).
4. **Varios huecos afectan a menores y a la ley:** cómo se detecta el país, el inicio de sesión con Apple o Google sin verificar la edad, la entrada de menores a un plan Familiar, y cómo recibe el tutor la información. Deben resolverse antes de programar el registro.
5. **El PRD contiene decisiones que propuse yo y que aún no has aprobado** (plazos, límites, umbrales). Están listadas en el anexo A para que no se tomen por aprobadas.

---

## 1. Contradicciones entre el PRD y el mapa de navegación

| Código | Sev. | Contradicción | Dónde | Propuesta |
|---|---|---|---|---|
| **X-01** | Alta | El PRD dice que "todo el MVP funciona sin pagos", pero el mapa aplica límites Gratis en pantallas del MVP (E04: 3 rutinas; P02: 3 objetivos; P05 y N07: 90 días) y P03 enlaza a **U09 Planes**, que es de la Etapa 10. No está definido si durante el MVP los límites se aplican (sin forma de pagar) o no. | PRD §3; Mapa E04, P02, P03, P05, N07 | Decidir una de dos: (a) en el MVP todos tienen acceso completo y los límites se activan en E10; (b) los límites se aplican desde el MVP con un mensaje "Premium disponible próximamente". Ver decisión **DP-01**. |
| **X-02** | Alta | **Peso y medidas para 16–17.** La matriz de edad del PRD dice "registro de peso opcional" para 16–17, pero la tabla de datos del onboarding (RN-08) dice "solo 18+", O10 es "18+" y U02 muestra "Medidas (18+)". Solo P07 dice "16–17 limitado". | PRD §4.1 tabla de datos y §6.4; Mapa O10, U02, P07 | Unificar en un solo criterio. Ver **DP-07**. |
| **X-03** | Alta | **Integraciones de salud para 13–15.** La matriz del PRD dice "No" para 13–15, pero el panel del tutor (T01) muestra el interruptor "Integraciones de salud" para cualquier menor, lo que permitiría a un tutor activarlas a un menor de 13–15. | PRD §6.4; Mapa T01 | Mostrar ese interruptor en T01 solo para 16–17. |
| **X-04** | Media | **Alimento propio (N10)** está restringido a **16+** en el mapa, pero el PRD no establece esa restricción en ninguna parte. | Mapa N10; PRD §4.3 y §6.4 | Confirmar si la restricción se mantiene y, si es así, añadirla a la matriz de edad del PRD. |
| **X-05** | Media | **"Bienestar y hábitos"** aparece como un módulo seleccionable en el onboarding (O03), pero el PRD no tiene un módulo de Bienestar: los hábitos están dentro de Nutrición (N08) y el bienestar es una categoría de Progreso. Si alguien activa solo "Bienestar y hábitos", no está claro qué ve ni si puede acceder a N08 sin activar Nutrición. | Mapa O03, N08; PRD §4.2, §4.3, §4.5 | Ver **DP-05**. |
| **X-06** | Media | El PRD (§4.6) dice que en el plan Gratis se pueden **mostrar u ocultar tarjetas del inicio**, pero el mapa ubica esa función en H03, que es de la Etapa 10. En el MVP no habría forma de hacerlo. | PRD §4.6; Mapa H03 | Aclarar si mostrar/ocultar tarjetas entra en el MVP. |
| **X-07** | Media | **Contenido nutricional para 13–15.** La matriz dice que 13–15 tiene un enfoque educativo y que la "información nutricional completa de alimentos" empieza en 16–17. Pero N03 (detalle de alimento) solo dice "según edad", sin definir qué se muestra a 13–15 (¿calorías por alimento?, ¿macronutrientes?, ¿solo grupo de alimento?). | PRD §6.4; Mapa N01, N03 | Ver **DP-08**. |
| **X-08** | Media | **Bloqueo de amistades por el tutor (16–17).** La matriz dice que el tutor puede bloquear amistades con adultos de un menor de 16–17, pero T01 solo contempla aprobar solicitudes de 13–15. No hay función equivalente para 16–17. | PRD §6.4; Mapa T01 | Añadir la función a T01 o retirarla de la matriz (tu decisión). |
| **X-09** | Baja | El PRD (§3) pone "Recetas y alternativas (E6 básico, ampliado después)" en la columna de **etapas posteriores**, mientras que §4.3 y el mapa (N05, N06) las incluyen en el MVP. | PRD §3 y §4.3 | Mover la mención a la columna del MVP para evitar confusión. |
| **X-10** | Baja | El mapa marca en H01 el botón **Comunidad** como "S01 o S02 [E9]", y la sección 1.1 dice que los cuatro botones de color se abren desde el inicio; pero según RN-14 el botón no debe mostrarse antes de E9. El diagrama general también dibuja S01 dentro de la barra inferior sin advertencia. | Mapa §1, §1.1, H01; PRD RN-14, D-01 | Se resuelve con la decisión D-01 del PRD. |

---

## 2. Pantallas, botones, destinos y recorridos incompletos

| Código | Sev. | Hueco | Dónde | Propuesta |
|---|---|---|---|---|
| **P-01** | Alta | **A01 (Splash) solo decide entre H01 y A02.** No contempla: onboarding incompleto (debe ir a O-xx), consentimiento parental pendiente (A10), cuenta en periodo de eliminación (ver P-03) ni correo sin verificar (A05). A06 sí contempla algunos de estos casos, A01 no. | Mapa A01, diagrama §1 | Definir la tabla completa de destinos de A01 según el estado de la cuenta. |
| **P-02** | Alta | **Inicio de sesión con Apple o Google desde A06** permitiría crear una cuenta nueva **sin pasar por A03** (fecha de nacimiento) y por tanto sin la verificación de edad ni el consentimiento parental. | Mapa A04, A06; PRD RN-01, D-10 | Si un inicio de sesión social no corresponde a una cuenta existente, redirigir a A03 antes de crear nada. |
| **P-03** | Alta | **Reactivación durante el periodo de gracia.** El recorrido F10 dice "30 días para arrepentirse iniciando sesión", pero no existe la pantalla que informa "tu cuenta está programada para eliminarse el [fecha]" con **Reactivar** / **Mantener eliminación**. | Mapa F10, A06; PRD RN-87 | Añadir una pantalla en el grupo A (por ejemplo A13). |
| **P-04** | Media | **Aceptar invitación familiar** se menciona en §13 como "Pantalla de aceptación" pero **no tiene ID ni contenido** (quién invita, qué implica, aviso de RN-107 si ya paga Premium, Aceptar/Rechazar). | Mapa §13, F9, U10 | Añadir pantalla con ID (por ejemplo U17). |
| **P-05** | Media | **Vista previa al compartir** (RN-62) se menciona en E09 y G02 ("→ vista previa [E9]") pero no es una pantalla definida. | Mapa E09, G02; PRD RN-62 | Añadir pantalla con ID en el grupo S. |
| **P-06** | Media | **Cambio de plan a Gratis** (RN-92): "el usuario elige qué mantiene activo" no tiene pantalla. ¿Qué pasa con la 4.ª rutina o el 4.º objetivo? | PRD RN-92; Mapa U08 | Definir pantalla de selección tras bajar de plan. |
| **P-07** | Media | **Transición a la mayoría de edad y a 16 años** (RN-114): no hay pantalla para que el usuario que cumple 18 otorgue sus propios consentimientos, ni aviso al cumplir 16. | PRD RN-114 | Añadir pantalla o modal de transición. |
| **P-08** | Media | **Mensaje de cuidado ante señales de riesgo** en nutrición (RN-25) no tiene pantalla ni componente; solo la IA (E8) tiene un flujo de crisis definido. | PRD RN-25, RN-75; Mapa N01, U14 | Definir un componente de "mensaje de cuidado" que enlace a U14. |
| **P-09** | Media | **Resumen semanal para el tutor** (RN-116): el menor puede activarlo en U16, pero el tutor no tiene app ni cuenta (RN-117) y T01 no muestra ningún resumen. No se sabe por qué canal lo recibe. | PRD RN-116, RN-117; Mapa U16, T01 | Ver **DP-10**. |
| **P-10** | Media | **Solicitud de permiso del menor al tutor** (S02 "Pide permiso a tu tutor", U16 "Pedir permiso"): no está definido cómo llega al tutor ni cómo ve el menor la respuesta. | Mapa S02, U16, T01 | Definir canal (correo con enlace a T01) y estado visible en U16. |
| **P-11** | Media | **Desconectar una integración** (RN-83) debe preguntar si conservar o eliminar los datos importados; U15 solo dice "Conectar / Desconectar". | PRD RN-83; Mapa U15 | Añadir el diálogo a U15. |
| **P-12** | Media | **Foto de perfil en el MVP.** El PRD (§3, módulo 8) dice "Foto o inicial de perfil" en E6, pero ninguna pantalla permite subir la foto (U02 no la incluye) y el PRD prohíbe fotos en perfiles sociales de menores. | PRD §3, §6.4; Mapa U01, U02 | Ver **DP-11**. |
| **P-13** | Baja | **Fecha de último cálculo de la predicción** (RN-42) no aparece en P04. | PRD RN-42; Mapa P04 | Añadir a la descripción de P04. |
| **P-14** | Baja | **Plazo para cambiar de modalidad principal** (RN-35, cada 30 días): U02 permite cambiarla pero no indica que muestre cuándo podrá volver a cambiarse. | PRD RN-35; Mapa U02 | Añadir el aviso en U02. |

**Recorridos (sección 12 del mapa) que necesitan completarse**

- **F2 (registro de menor):** no indica qué pasa si el tutor **rechaza** (¿se elimina la cuenta?, ¿qué ve el menor?).
- **F9 (grupo familiar):** "la persona invitada… se registra" no aclara que una persona nueva debe pasar por A03 y, si es menor, por A09 y la espera del tutor.
- **Falta un recorrido de recuperación de cuenta** (A07 → correo → A08 → A06), aunque las pantallas existen.

---

## 3. IDs e inventario de pantallas

**Conteo verificado:** la suma del inventario es correcta (95), y la cifra de "unas 70 pantallas del MVP" coincide con el recuento por etapa (70 exactas: A 12, T 2, O 12, H 2, N 9, E 11, C 4, P 7, U 11).

| Código | Sev. | Hallazgo | Propuesta |
|---|---|---|---|
| **I-01** | Media | **La letra "P" tiene dos significados:** prefijo de Progreso (P01–P08) y marca de Premium en la columna "Plan". En filas como "P04 … Plan: P" se presta a confusión. | Usar otro marcador para Premium (por ejemplo ★ o "Prem."). |
| **I-02** | Media | **El panel del tutor (T00–T01) se cuenta entre las 95 pantallas** pero es una **aplicación web aparte**, con su propio desarrollo, hospedaje y seguridad. El inventario no lo distingue de las pantallas de la app. | Separarlo en el inventario como "plataforma web". |
| **I-03** | Baja | **Falta N09** en la secuencia de Nutrición (N01–N08, N10). | Renumerar N10 a N09 o dejar constancia de que el hueco es intencional. |
| **I-04** | Baja | El diagrama de Nutrición usa **N03b** (Alternativas) y **N01d** (Día anterior), que no están en la tabla ni en el inventario. | Definir si son pantallas propias o vistas dentro de N03 y N01, y nombrarlas de forma consistente. |
| **I-05** | Baja | **T00 y E00** empiezan en cero, a diferencia del resto. E00 además es un punto de decisión, no una pantalla. | Renombrar T00 a T01 (y T01 a T02); marcar E00 como decisión. |
| **I-06** | Baja | **S10 (Bloqueados)** pertenece a Comunidad (E9) pero se accede desde U05 (E6). Es correcto, pero el diagrama de Comunidad no la incluye. | Añadirla al diagrama. |
| **I-07** | Baja | Las pantallas propuestas en este informe (P-03, P-04, P-05, P-06, P-07) cambiarían el total. | Actualizar el inventario cuando se aprueben. |

---

## 4. Reglas de negocio sin reflejo en la navegación

De las 121 reglas, la mayoría son de servidor o de contenido y no necesitan pantalla. Estas sí deberían verse en el mapa:

| Código | Sev. | Regla | Qué falta en la navegación |
|---|---|---|---|
| **R-01** | Alta | **RN-02** Bloqueo de menores de 13 recordado en el dispositivo | No se describe qué ve una persona bloqueada al reabrir la app, ni que A03 no debe permitir reintentar. |
| **R-02** | Alta | **RN-36 y matriz §6.4** Restricciones de entrenamiento por edad (13–15: sin pruebas de carga máxima, cargas ligeras) | Las tablas de Entrenamiento (E01–E11) **no tienen columna de edad**. No está definido cómo se aplica la restricción en E06 ni en E10 (¿avisos?, ¿programas ocultos?). Ver **DP-09**. |
| **R-03** | Media | **RN-04** Cuenta pendiente eliminada a los 14 días | A10 no muestra la fecha límite. |
| **R-04** | Media | **RN-07** Límite de intentos | A06 y A07 no describen el estado de "demasiados intentos". |
| **R-05** | Media | **RN-11 y RN-34** Advertencias por consideraciones de seguridad | Se citan en O09 y E03, pero no en E05/E06 al añadir un ejercicio sensible a una rutina. |
| **R-06** | Media | **RN-22** Mínimos de seguridad en metas de energía y ritmo de peso | P03 no describe qué ocurre si la meta propuesta los incumple. |
| **R-07** | Media | **RN-33** Sugerencia de descanso ante exceso | No está indicado en qué pantalla aparece (H01, E09 o ambas). |
| **R-08** | Media | **RN-35** Modalidad principal en Gratis | E01 no indica qué ve un usuario Gratis al seleccionar otra disciplina. |
| **R-09** | Media | **RN-68** Revisión de reportes con plazo | No existe herramienta de moderación ni de soporte (rol "Soporte / moderación" del PRD §2.3). Ver **DP-14**. |
| **R-10** | Media | **RN-90** Derechos ARCO | Solo cubiertos parcialmente (U12, U13, U14). Faltan rectificación y oposición. |
| **R-11** | Media | **RN-97** Menores sin ofertas de compra | P03 envía a U09 al alcanzar el límite, también a menores. |
| **R-12** | Media | **RN-105 y RN-107** Plan Familiar | U10 no muestra la espera de 30 días ni el aviso de doble pago. |
| **R-13** | Baja | **RN-56** Eventos de XP desde E6 | Correcto sin pantalla; anotarlo como requisito técnico para la Etapa 5. |
| **R-14** | Baja | **RN-76** Indicador de respuesta de IA | I01 lo cubre con el aviso general, pero no por mensaje. |
| **R-15** | Baja | **RN-84** Notificaciones sin datos sensibles en pantalla de bloqueo | U07 no lo menciona (es comportamiento, no ajuste; aceptable). |

---

## 5. Restricciones por edad y privacidad

| Código | Sev. | Hallazgo | Propuesta |
|---|---|---|---|
| **E-01** | Alta | **No se determina el país del usuario.** El PRD exige reglas de edad configurables por país (§6.1, §8.5), pero ninguna pantalla pregunta o detecta el país. Sin eso no se puede aplicar la edad mínima ni la de consentimiento correctas. | Ver **DP-03**. |
| **E-02** | Alta | **Inicio de sesión social sin verificación de edad** (igual que P-02). | Ídem P-02. |
| **E-03** | Alta | **Menores en un plan Familiar.** El PRD permite que menores sean integrantes (RN-108), pero no define si un menor sin cuenta puede registrarse desde una invitación, ni si el tutor debe autorizar que se una al grupo. | Ver **DP-12**. |
| **E-04** | Alta | **Datos recogidos antes del consentimiento.** El menor entrega correo, contraseña y fecha de nacimiento (A04, A05) antes de que el tutor autorice. RN-04 dice "sin recopilar datos adicionales", lo cual es razonable, pero debe validarlo la revisión legal (D-05). | Incluir en la consulta legal. |
| **E-05** | Alta | **Consentimiento de datos de salud agrupado.** A04 exige marcar "consentimiento expreso para datos de salud" para crear la cuenta. No está definido qué pasa si alguien no lo acepta. Atar un consentimiento sensible al registro puede no ser válido legalmente. | Ver **DP-13** e incluir en la consulta legal. |
| **E-06** | Alta | **Detección de adultos en amistades de menores.** La matriz exige aprobación del tutor para amistades de 13–15 con adultos y aviso a 16–17. Para saber que el otro es adulto, el sistema debe conocer su rango de edad, pero los perfiles sociales nunca muestran la edad. No está definido cómo se informa sin revelar la edad. | El servidor conoce el rango; definir qué mensaje ve el menor sin revelar la edad exacta. |
| **E-07** | Media | **El tutor ya decide todas las amistades de 13–15** (S03), lo que hace redundante la regla específica sobre adultos para ese rango. | Confirmar que es intencional. |
| **E-08** | Media | **Fotos de perfil** (igual que P-12). | Ídem. |
| **E-09** | Media | **Analítica:** el consentimiento solo aparece en U05 (ajustes), no al registrarse. Si la analítica se activa por defecto antes de que el usuario la vea, contradice §8.2. | Pedir consentimiento en el registro o mantenerla desactivada hasta que se otorgue. |
| **E-10** | Media | **Alimentos propios de menores** (N10 16+) y **alimentos sin verificar**: no se define si un menor de 16–17 ve advertencias adicionales. | Menor; confirmar. |
| **E-11** | Media | **Asistente IA en modo restringido para 13–15:** no se define qué responde cuando el menor pregunta por peso o dietas (¿se niega?, ¿redirige?). | Definir en la Etapa 8; anotarlo como pendiente. |
| **E-12** | Media | **Recordatorio de bloqueo de menores de 13 en el dispositivo** (RN-02): guardar esa marca es, en sí, un dato sobre un menor. | Incluir en la consulta legal. |
| **E-13** | Baja | **Aviso al tutor al cumplir 16** (RN-114): se notifica, pero no se dice si el tutor puede oponerse a algún cambio. | Aclarar. |

**Lo que está bien resuelto:** privacidad por defecto en comunidad, ausencia de chat libre, rankings basados en constancia, no compartir datos de salud, separación entre tutor y administrador familiar, administrador sin acceso a datos, exportación y eliminación gratuitas, y ausencia de publicidad.

---

## 6. ¿Es demasiado grande el MVP?

**Respuesta corta: sí, para la forma de trabajo actual** (Claude Code más tus decisiones de producto, sin equipo). No es inviable, pero lleva riesgo de tardar mucho en tener algo usable y de acumular errores.

### 6.1 Qué hace grande al MVP

| Elemento | Por qué pesa |
|---|---|
| ~70 pantallas | Cada una con sus estados (carga, vacío, error, sin conexión) |
| **Panel web del tutor (T00–T01)** | Es una segunda plataforma: web, autenticación propia por enlace, seguridad y hospedaje |
| Flujo de consentimiento parental | Correos, estados, plazos, evidencia legal y transición por edades |
| Modo sin conexión con sincronización (§8.3, RN-30) | Técnicamente de lo más complejo en apps móviles (conflictos, reintentos) |
| **Contenido que hay que producir o licenciar** | Biblioteca de ejercicios con imágenes, programas, recetas, base de alimentos con fuentes. No es código: requiere tiempo, licencias y, en salud, revisión profesional |
| Tres disciplinas con métricas propias | Tres modelos de registro y estadísticas distintos |
| Predicciones con intervalos | Bien acotado, pero requiere pruebas cuidadosas |
| Tema claro además del oscuro | Duplica la verificación visual y de contraste |
| Adaptación a tablets (§14 sin etapa asignada) | Diseños de dos paneles |
| Exportación de datos | Necesaria, pero es trabajo de backend adicional |

### 6.2 Opciones para reducir el riesgo sin eliminar funcionalidades

Ninguna está decidida; todas mueven funciones de etapa, no las eliminan.

| Opción | Qué implica | Pros | Contras |
|---|---|---|---|
| **A. Dividir la Etapa 6 en entregas internas** (6a acceso, onboarding, inicio y perfil; 6b entrenamiento y progreso; 6c nutrición) | Se prueba cada entrega antes de seguir | Avance visible y verificable | No reduce el total |
| **B. Beta cerrada solo para adultos** antes del lanzamiento público con menores | El panel del tutor y los flujos de menores se construyen en paralelo y se activan al lanzar | Permite validar el producto antes y con menos riesgo legal | **Cambia temporalmente tu decisión de 13+**; requiere tu aprobación expresa |
| **C. Mover a una etapa posterior** al MVP: tema claro, tablets, recetas, programas, comparaciones | Se conservan en la visión con etiqueta de etapa | Reduce contenido y diseño | El MVP es menos completo visualmente |
| **D. Sincronización sin conexión limitada** a la sesión de entrenamiento en curso (lo más crítico) | El resto requiere conexión en el MVP | Reduce mucho la complejidad | Peor experiencia sin señal fuera del entrenamiento |
| **E. Empezar con una base de alimentos acotada** (alimentos comunes en México, fuente verificable) | Ampliación posterior | Evita depender de licencias complejas desde el inicio | Búsquedas con menos resultados al principio |

**Mi recomendación:** A + C + D + E. La opción B es una decisión de negocio y legal que te corresponde.

---

## 7. Decisiones pendientes antes del desarrollo

Se incluyen las diez del PRD (D-01 a D-10) y las nuevas que salen de esta auditoría (DP-xx).

### 7.1 Bloquean el inicio de la Etapa 6 (acceso, registro y onboarding)

| Código | Decisión | Relacionado |
|---|---|---|
| **D-05** | Revisión legal: consentimiento para menores de 18, método de verificación del tutor, acceso del tutor | E-04, E-05, E-12 |
| **D-10** | Inicio de sesión con Apple y Google | P-02 |
| **DP-01** | ¿Se aplican los límites del plan Gratis durante el MVP sin pagos? | X-01 |
| **DP-02** | Alcance final del MVP (opciones A–E de la sección 6) | §6 |
| **DP-03** | Cómo se determina el país (pregunta explícita, configuración del teléfono o tienda) | E-01 |
| **DP-04** | ¿El panel del tutor es web (como dice el mapa) o se usa otra vía, como correo con enlaces? | I-02, P-09, P-10 |
| **DP-13** | Qué ocurre si alguien no acepta el consentimiento de datos de salud | E-05 |
| **D-09** | Nombre oficial de la marca | — |

### 7.2 Deben resolverse antes de construir el módulo correspondiente

| Código | Decisión | Relacionado |
|---|---|---|
| **D-01** | Pestaña "Amigos" antes de E9 | X-10 |
| **D-02** | Disciplinas con métricas propias en el MVP | — |
| **D-03** | Predicciones gratis o Premium | — |
| **D-06** | Límites de seguridad nutricional (con profesional) | R-06 |
| **DP-05** | Qué es "Bienestar y hábitos" en O03 y si da acceso a hábitos sin activar Nutrición | X-05 |
| **DP-06** | ¿Qué pasa si un usuario elige como modalidad principal una disciplina **sin métricas propias en el MVP** (por ejemplo natación)? RN-35 promete métricas completas para la modalidad principal | R-08 |
| **DP-07** | Peso y medidas para 16–17 | X-02 |
| **DP-08** | Qué información nutricional ve un menor de 13–15 | X-07 |
| **DP-09** | Cómo se aplican las restricciones de entrenamiento a 13–15 | R-02 |
| **DP-10** | Canal del resumen semanal para el tutor | P-09 |
| **DP-11** | Foto de perfil en el MVP: sí o no, y para qué edades | P-12 |
| **DP-15** | Fuentes y licencias del contenido: ejercicios, imágenes, recetas y alimentos | §6.1 |
| **DP-16** | ¿Las tablets y el tema claro entran en el MVP? | §6.1 |

### 7.3 Pueden esperar a su etapa

| Código | Decisión | Etapa |
|---|---|---|
| **D-04** | Espera de 30 días entre grupos familiares | E10 |
| **D-07** | ¿Plan Familiar anual? | E10 |
| **D-08** | Prueba gratuita | E10 |
| **DP-12** | Menores en plan Familiar: registro desde invitación y autorización del tutor | E10 |
| **DP-14** | Herramienta de moderación y soporte (interna) | E9 |
| **DP-17** | Qué es la "comparación de escenarios" Premium en predicciones (aparece en el PRD §5.2 y en P04 sin definirse) | E10 |

---

## 8. Siguientes pasos sugeridos

1. Revisas este informe y respondes las decisiones de la sección 7.1.
2. Con tus respuestas, preparo la **versión 0.2** del PRD y del mapa de navegación, corrigiendo los hallazgos aprobados y marcando los cambios.
3. Solo después pasamos a la Etapa 3 (Design System y prototipos).

---

## Anexo A. Propuestas incluidas en el PRD que aún no has aprobado

El PRD v0.1 es un borrador y no ha sido aprobado. Para evitar que estas cifras se tomen por decisiones firmes, aquí están las que **propuse yo** sin que vinieran de tus instrucciones:

| Regla | Propuesta | Tipo |
|---|---|---|
| RN-04 | Cuenta pendiente de consentimiento eliminada a los 14 días | Plazo |
| RN-05 | Contraseña de mínimo 10 caracteres | Seguridad |
| RN-17 | Saludo alternativo neutro ("Te damos la bienvenida, [nombre]"). **Tu texto original es "Bienvenido, [nombre del usuario], ¿qué planeas hacer?"** | Texto de producto |
| RN-35 | Cambio de modalidad principal cada 30 días | Límite de plan |
| RN-38 | Mínimo 6 registros en 3 semanas para predecir | Umbral técnico |
| RN-50 | Tope diario de XP por actividad física | Gamificación |
| RN-52 | Rachas semanales con pausa | Gamificación |
| RN-66 | Sin chat de texto libre en la comunidad | Seguridad |
| RN-85 | Silencio nocturno 22:00–07:00 para menores | Protección |
| RN-87 | Periodo de gracia de 30 días al eliminar la cuenta | Plazo |
| RN-102 | Invitaciones familiares caducan en 7 días | Plazo |
| RN-105 | 30 días de espera entre grupos familiares | Límite de plan |
| RN-111 | Consentimiento parental para todos los menores de 18 | Legal (D-05) |
| RN-116 | El tutor no ve por defecto la actividad del menor | Privacidad (D-05) |
| §5.2 | Límites Gratis: 3 rutinas, 3 objetivos, 90 días de gráficos | Límite de plan |
| §6.4 | Matriz completa de experiencias por edad | Protección (D-05, D-06) |
| §8.3 | Arranque en menos de 3 s, 60 cuadros por segundo | Rendimiento |
| §9 | Indicadores de éxito | Métricas |
| Mapa O03 | Opción "Bienestar y hábitos" en el onboarding | Producto |
| Mapa N10 | Alimento propio solo para 16+ | Edad |
| Mapa §14 | Comportamiento en tablets | Diseño |

Todo lo demás en el PRD procede directamente de tus instrucciones o de tus respuestas del 15 de noviembre (edad mínima, tramos de edad, planes y precios, plan Familiar, lanzamiento en México, alcance completo).
