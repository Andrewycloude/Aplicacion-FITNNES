# Definitely Fitness — Trazabilidad de la auditoría hacia la v0.2

| | |
|---|---|
| **Versión** | 0.2.4 — propuesta (no definitiva) |
| **Auditoría de origen** | [03-AUDITORIA-CRUZADA.md](03-AUDITORIA-CRUZADA.md) (59 hallazgos: 14 altos, 32 medios, 13 bajos) |
| **Documentos relacionados** | [04 — PRD v0.2](04-PRD-v0.2-PROPUESTA.md) · [05 — Mapa v0.2](05-MAPA-NAVEGACION-v0.2-PROPUESTA.md) · [06 — Registro de decisiones](06-REGISTRO-DECISIONES-v0.2.md) |

## Estados

| Estado | Significado |
|---|---|
| **Resuelto** | La corrección está en la propuesta v0.2 y se apoya en una decisión aprobada o es una corrección documental que no necesita decisión de producto. Sigue sujeta a tu aprobación de la v0.2 en conjunto. |
| **Parcial** | Se eliminó la contradicción o se definió la estructura, pero queda una decisión o validación. |
| **Abierto** | Depende de una decisión pendiente; solo se documentaron alternativas. |
| **Requiere validación** | Depende de la opinión de un profesional competente. |
| **Resuelto (propuesta)** | Nuevo en v0.2.2 (AF-27). La corrección se apoya en una regla [PROP]: solo queda resuelta si apruebas esa regla. |
| **Diferido (MEN)** | Nuevo en v0.2.1. Afecta solo a menores o tutores. Con DEC-44 queda fuera de la beta y del MVP. **No está resuelto:** debe resolverse antes de la habilitación futura de menores. |

Según tu regla de control de calidad, **ningún hallazgo se marca como resuelto si aún falta una decisión o validación**.

Abreviaturas: **PRD** = 04-PRD-v0.2 · **MAPA** = 05-MAPA-v0.2.

---

## 1. Contradicciones (X)

| Hallazgo | Sev. | Resolución propuesta | Dónde se refleja | Decisión | Estado | ¿Revisión posterior? |
|---|---|---|---|---|---|---|
| **X-01** Límites Gratis en el MVP sin pagos | Alta | Sin restricciones comerciales en el MVP; se quitan los enlaces a U09 desde el MVP; límites como propuesta para ET10 | PRD §5.2, §7, RN-35, RN-138 · MAPA E04, P02, P03, P05, N07 | DEC-01 | Resuelto | Sí, en ET10 (DEC-62, DEC-67) |
| **X-02** Peso y medidas para 16–17 | Alta | Ambos documentos dicen lo mismo: medidas solo para adultos de forma provisional; menores pendiente; predicción corporal excluida | PRD RN-134, §9.3 · MAPA O10, P07, U02, §8 | DEC-14 (aprobada), DEC-35 · DEC-44 (fuera de la beta) | Diferido (MEN) | Sí, antes de habilitar menores |
| **X-03** Integraciones de salud para 13–15 | Alta | El panel del tutor ya no lista interruptores concretos; integraciones para menores marcadas como pendientes en ambos documentos | PRD §6.11, §9.3 · MAPA T02, U15 | DEC-37 · DEC-44 (fuera de la beta) | Diferido (MEN) | Sí, antes de habilitar menores |
| **X-04** Alimento propio 16+ sin respaldo en el PRD | Media | La restricción deja de ser regla y pasa a la decisión sobre nutrición para menores | PRD §6.3 · MAPA N10 | DEC-36 · DEC-44 (fuera de la beta) | Diferido (MEN) | Sí, antes de habilitar menores |
| **X-05** "Bienestar y hábitos" sin módulo | Media | Se conserva la opción en O03 marcada como pendiente; alternativas documentadas | PRD §6.3 · MAPA O03, N08 | DEC-54 | Abierto | Sí, antes de ET6.1 (afecta a O03) |
| **X-06** Mostrar/ocultar tarjetas Gratis vs H03 en ET10 | Media | En el MVP el inicio se adapta a los módulos activos; la organización manual queda en ET10 | PRD RN-136 · MAPA H01, H03 | DEC-01 | Resuelto (propuesta) | No |
| **X-07** Contenido nutricional para 13–15 | Media | N01 y N03 remiten a la decisión pendiente; principio aprobado sin metas restrictivas | PRD RN-27, §9.3 · MAPA N01, N03 | DEC-13 (aprobada), DEC-36 · DEC-44 (fuera de la beta) | Diferido (MEN) | Sí, antes de habilitar menores |
| **X-08** Bloqueo de amistades por el tutor (16–17) | Media | Se retiran funciones concretas del tutor hasta decidir su alcance | PRD §9.3 · MAPA T02, S01 | DEC-39, DEC-40 · DEC-44 (fuera de la beta) | Diferido (MEN) | Sí, antes de habilitar menores |
| **X-09** Recetas en la columna equivocada | Baja | Recetas básicas en ET6.3; biblioteca amplia POST | PRD §5.2, §6.3 · MAPA N05 | DEC-03 | Resuelto | Sí: cantidad inicial (DEC-63) |
| **X-10** Botón Comunidad y pestaña Amigos antes de ET9 | Baja | El mapa muestra los botones y pestañas por entrega; Comunidad solo desde ET9; pestaña Amigos según decisión | PRD RN-13, RN-14 · MAPA §4.2, H01 | DEC-46 | Parcial | Sí, antes de cerrar ET6.3 |

## 2. Pantallas y recorridos incompletos (P)

| Hallazgo | Sev. | Resolución propuesta | Dónde se refleja | Decisión | Estado | ¿Revisión posterior? |
|---|---|---|---|---|---|---|
| **P-01** A01 sin enrutamiento completo | Alta | Tabla de enrutamiento de 12 estados, aplicada también por A06 | MAPA §4.3 | — (corrección documental) | Resuelto | No (el paso 1 depende de E-12) |
| **P-02** Apple/Google sin verificar edad | Alta | Toda autenticación social sin cuenta pasa por A03 antes de crear nada | PRD RN-128 · MAPA A03, A04, A06, F02 | DEC-09 | Resuelto | No |
| **P-03** Sin pantalla de reactivación | Alta | Nueva pantalla A13; flujo F09 | PRD RN-87 · MAPA A13, F09 | DEC-60 (plazo) | Parcial | Sí: aprobar el plazo de gracia y validarlo legalmente |
| **P-04** Aceptar invitación familiar sin ID | Media | Nueva pantalla U17 con aviso de doble pago; flujos F18 y F19 | PRD RN-102, RN-107 · MAPA U17, F18, F19 | DEC-38 (menores) | Parcial | Sí: caso de menores |
| **P-05** Vista previa al compartir sin pantalla | Media | Nueva pantalla S11; flujo F23 | PRD RN-62 · MAPA S11, F23 | — (corrección documental) | Resuelto | Sí, al diseñar ET9 (DEC-40) |
| **P-06** Sin pantalla al bajar a Gratis | Media | Nueva pantalla U19; flujo F21 | PRD RN-92 · MAPA U19, F21 | DEC-62, DEC-67 | Parcial | Sí, en ET10 |
| **P-07** Sin transición al cumplir 16 y 18 | Media | Nuevas pantallas A15 y A16; flujos F16 y F17 | PRD Anexo A (RN-114) · MAPA A15, A16, F16, F17 | DEC-32, DEC-33, DEC-39, DEC-44 · DEC-44 (fuera de la beta) | Diferido (MEN) | Sí, antes de habilitar menores |
| **P-08** Mensaje de cuidado sin componente | Media | Nuevo componente M02 enlazado a U14 | PRD RN-25 · MAPA M02, N01 | DEC-61 | Requiere validación | Sí: criterios por un profesional |
| **P-09** Canal del resumen para el tutor | Media | Se documenta como pendiente; sin pantalla hasta decidir | PRD §9.5 · MAPA U16, T02 | DEC-39 · DEC-44 (fuera de la beta) | Diferido (MEN) | Sí, antes de habilitar menores |
| **P-10** Solicitud de permiso al tutor sin canal | Media | Correo + página T03 y estado visible en U16; flujo F07 | PRD §9.5 · MAPA T03, U16, F07 | DEC-07 (aprobada), DEC-45, DEC-31 · DEC-44 (fuera de la beta) | Diferido (MEN) | Sí, antes de habilitar menores |
| **P-11** Desconectar integración sin diálogo | Media | Componente M04 | PRD RN-83 · MAPA M04, U15, F25 | — (corrección documental) | Resuelto (propuesta) | No |
| **P-12** Foto de perfil sin pantalla | Media | Se documenta como pendiente; el MVP usa inicial o avatar simple | PRD §6.8 · MAPA U01 | DEC-56 | Abierto | Sí |
| **P-13** Fecha del último cálculo en P04 | Baja | Añadida a P04 | PRD RN-42 · MAPA P04 | — | Resuelto (propuesta) | No |
| **P-14** Plazo de cambio de modalidad en U02 | Baja | En el MVP la modalidad no limita funciones; el límite pasa a ET10 | PRD RN-35 | DEC-01 | Resuelto | Sí, si ET10 adopta el límite (DEC-62) |

## 3. IDs e inventario (I)

| Hallazgo | Sev. | Resolución propuesta | Dónde se refleja | Decisión | Estado | ¿Revisión posterior? |
|---|---|---|---|---|---|---|
| **I-01** "P" con dos significados | Media | Premium se marca con ★ | MAPA §1.2 | — | Resuelto | No |
| **I-02** Panel del tutor contado como pantalla de la app | Media | Inventario separado para páginas web (T01–T04) | MAPA §3.2, §3.4 | DEC-07 | Resuelto | No |
| **I-03** Falta N09 | Baja | N09 = Alternativas | MAPA §1.3, N09 | — | Resuelto | No |
| **I-04** N03b y N01d fuera del inventario | Baja | N03b pasa a N09; N01d es una vista de N01 | MAPA §1.3 | — | Resuelto | No |
| **I-05** T00 y E00 | Baja | Tutor numerado T01–T04; E00 pasa a ser un nodo de decisión sin ID | MAPA §1.1, §1.3 | — | Resuelto | No |
| **I-06** S10 fuera del diagrama de Comunidad | Baja | S10 en el inventario con su acceso (U05); el diagrama de Comunidad se sustituye por la tabla de inventario y el flujo F24 | MAPA §3.1, F24 | — | Resuelto | No |
| **I-07** Inventario desactualizado | Baja | Inventario rehecho: 102 pantallas de la app + 4 web + 4 componentes (v0.2); en la v0.2.1, 103 + 4 + 4 | MAPA §3.4 | — | Resuelto | No |

## 4. Reglas sin reflejo en la navegación (R)

| Hallazgo | Sev. | Resolución propuesta | Dónde se refleja | Decisión | Estado | ¿Revisión posterior? |
|---|---|---|---|---|---|---|
| **R-01** Bloqueo de menores de 13 en el dispositivo | Alta | Comportamiento de A11 y de A01 descrito, condicionado a validación | PRD RN-02 · MAPA A11, §4.3 | DEC-18, DEC-31 | Requiere validación | Sí |
| **R-02** Restricciones de entrenamiento por edad | Alta | La regla v0.1 queda suspendida; E01 remite a la decisión; entretanto, DEC-64 (propuesta) | PRD RN-36, §9.3, §9.4 · MAPA E01, §8 | DEC-32, DEC-33 · DEC-44 (fuera de la beta) | Diferido (MEN) | Sí, antes de habilitar menores |
| **R-03** Fecha límite en A10 | Media | A10 muestra la fecha de caducidad | MAPA A10 | DEC-60 (14 días) · DEC-44 (fuera de la beta) | Diferido (MEN) | Sí, antes de habilitar menores |
| **R-04** Estado de demasiados intentos | Media | Estado definido en A05, A06, A07 y en §6 | PRD RN-07 · MAPA A05–A07, §6 | — | Resuelto (propuesta) | No |
| **R-05** Advertencias de seguridad en rutinas y sesión | Media | Advertencias en E03, E05 y E06 (con consentimiento); precauciones generales siempre | PRD RN-34 · MAPA E03, E05 | DEC-08 | Resuelto (propuesta) | No |
| **R-06** Mínimos de seguridad en P03 | Media | P03 explica y propone un ritmo seguro si la meta incumple los límites | PRD RN-22 · MAPA P03 | DEC-50 | Requiere validación | Sí: valores por un profesional |
| **R-07** Ubicación de la sugerencia de descanso | Media | En H01 (recomendaciones) y E09 | PRD RN-15, RN-33 · MAPA H01, E09 | DEC-16 | Parcial | Sí: umbrales con validación profesional |
| **R-08** Modalidad principal en Gratis | Media | En el MVP no limita funciones; el caso sin métricas propias pasa a DEC-55 | PRD RN-35 · MAPA O04 | DEC-01, DEC-55 | Parcial | Sí |
| **R-09** Herramienta de moderación | Media | Documentada como necesidad de ET9 | PRD §3.3, §6.9 | DEC-40 | Abierto | Sí, antes de ET9 |
| **R-10** Derechos ARCO incompletos | Media | Acceso desde U05, U18 y U14 con flujo F10 | PRD RN-90 · MAPA U14, U18, F10 | — | Requiere validación | Sí: procedimiento legal |
| **R-11** Ofertas de compra a menores | Media | En el MVP no hay compras (DEC-01); en ET10, para menores: no aplica en la beta (DEC-44); futuro: DEC-38 | PRD RN-97 · MAPA U09 | DEC-01, DEC-38, DEC-44 · DEC-44 (fuera de la beta) | Diferido (MEN) | Sí, antes de habilitar menores |
| **R-12** Espera y aviso de doble pago en U10 | Media | U10 muestra la espera; U17 muestra el aviso de doble pago | MAPA U10, U17 | DEC-49 | Parcial | Sí, en ET10 |
| **R-13** Eventos de XP desde ET6 | Baja | Registro de eventos desde ET6.2 como servicio transversal | PRD §4.2, RN-56 | — | Resuelto (propuesta) | Sí, en ET5 (modelo de datos) |
| **R-14** Indicador de IA por mensaje | Baja | Cada respuesta se identifica como IA | PRD RN-76 · MAPA I01 | — | Resuelto (propuesta) | No |
| **R-15** Notificaciones sin datos sensibles | Baja | Documentado como comportamiento | PRD RN-84 | — | Resuelto (propuesta) | No |

## 5. Edad y privacidad (E)

| Hallazgo | Sev. | Resolución propuesta | Dónde se refleja | Decisión | Estado | ¿Revisión posterior? |
|---|---|---|---|---|---|---|
| **E-01** No se determina el país | Alta | México como primer país y reglas configurables por país; el mecanismo de detección queda pendiente | PRD §8.4, RN-124 | DEC-06 (aprobada), DEC-43 | Parcial | Sí, antes de ET6.1 |
| **E-02** Autenticación social sin edad | Alta | Igual que P-02 | PRD RN-128 · MAPA F02 | DEC-09 | Resuelto | No |
| **E-03** Menores en plan Familiar | Alta | Flujo F19 llega hasta la decisión y se detiene; alternativas documentadas | PRD RN-108, §9.3 · MAPA U17, F19 | DEC-38 · DEC-44 (fuera de la beta) | Diferido (MEN) | Sí, antes de habilitar menores |
| **E-04** Datos recogidos antes del consentimiento parental | Alta | Documentado para la consulta legal; A10 permite cancelar y eliminar | PRD RN-04 · MAPA A10 | DEC-30 · DEC-44 (fuera de la beta) | Diferido (MEN) | Sí, antes de habilitar menores |
| **E-05** Consentimiento de salud atado al registro | Alta | Registro separado del consentimiento de salud; pantalla A14, U18 y M01 | PRD RN-129–RN-132 · MAPA A04, A14, U18, M01, F05 | DEC-08 (aprobada), DEC-42 | Parcial | Sí: clasificación legal de los datos |
| **E-06** Detección de adultos en amistades de menores | Alta | Documentado dentro de la decisión de moderación | PRD §9.3 | DEC-40, DEC-32, DEC-33 · DEC-44 (fuera de la beta) | Diferido (MEN) | Sí, antes de habilitar menores |
| **E-07** Redundancia en amistades de 13–15 | Media | Pasa a la decisión sobre 13–15 | PRD §9.3 | DEC-32 · DEC-44 (fuera de la beta) | Diferido (MEN) | Sí, antes de habilitar menores |
| **E-08** Fotos de perfil | Media | Igual que P-12 | PRD §6.8 | DEC-56 | Abierto | Sí |
| **E-09** Analítica sin consentimiento inicial | Media | Analítica desactivada hasta su consentimiento en A14 | PRD RN-133 · MAPA A14 | DEC-65 | Parcial | Sí: aprobar la propuesta |
| **E-10** Alimentos propios de 16–17 | Media | Pasa a la decisión sobre nutrición para menores | PRD §9.3 | DEC-36 · DEC-44 (fuera de la beta) | Diferido (MEN) | Sí, antes de habilitar menores |
| **E-11** IA en modo restringido para 13–15 | Media | Pasa a la decisión sobre IA para menores | PRD §9.3 | DEC-41 · DEC-44 (fuera de la beta) | Diferido (MEN) | Sí, antes de habilitar menores |
| **E-12** Marca de bloqueo de menores de 13 | Media | Documentado para la consulta legal | PRD RN-02 · MAPA §4.3 | DEC-18, DEC-31 | Requiere validación | Sí |
| **E-13** Aviso al tutor al cumplir 16 | Baja | Flujo F16 con aviso por correo; alcance del tutor pendiente | MAPA A15, F16 | DEC-39 · DEC-44 (fuera de la beta) | Diferido (MEN) | Sí, antes de habilitar menores |

---

## 6. Resumen

| Estado | Altos | Medios | Bajos | Total |
|---|---|---|---|---|
| Resuelto | 4 | 3 | 7 | **14** |
| Resuelto (propuesta) | 0 | 4 | 4 | **8** |
| Parcial | 3 | 6 | 1 | **10** |
| Abierto | 0 | 4 | 0 | **4** |
| Requiere validación | 1 | 4 | 0 | **5** |
| Diferido (MEN) | 6 | 11 | 1 | **18** |
| **Total** | **14** | **32** | **13** | **59** |

Conteo verificado automáticamente contra las tablas anteriores y contra las severidades de la auditoría original.

**Hallazgos altos por estado (v0.2.2):**
- Resuelto: E-02, P-01, P-02, X-01.
- Resuelto (propuesta): —.
- Parcial: E-01, E-05, P-03.
- Abierto: —.
- Requiere validación: R-01.
- Diferido (MEN): E-03, E-04, E-06, R-02, X-02, X-03.

Los hallazgos diferidos **no se consideran resueltos**: salen del alcance de la beta por DEC-44 y deben resolverse antes de admitir menores.

### 6.1 Recorridos señalados en la auditoría sin código propio

La auditoría (§2) indicó tres recorridos incompletos que no recibieron código de hallazgo:

| Recorrido | Resolución | Dónde |
|---|---|---|
| F2 v0.1: tutor rechaza la solicitud | Estados "rechazado" y "caducado" en A10 | MAPA A10, F03 |
| F9 v0.1: persona invitada sin cuenta | Flujo completo con verificación de edad | MAPA F19 (menores: DEC-38) |
| Falta el recorrido de recuperación | Flujo F04 | MAPA F04 |

---

## 7. Auditoría final (AF) — estado en la v0.2.2

La auditoría final se entregó como informe en la conversación del 16 de noviembre y no estaba guardada en el repositorio. Se registra aquí para mantener la trazabilidad. En la v0.2.2 se aplicaron las correcciones autorizadas por el propietario (AF-01, 03, 05, 06, 13, 16, 17, 24, 25, 27, 28) y se documentaron el correo transaccional y los documentos legales. **AF-04, AF-21, AF-22, AF-23 y AF-26 siguen abiertos.**

| Hallazgo | Sev. | Problema | Estado v0.2.1 | Nota |
|---|---|---|---|---|
| **AF-01** | Media | DEC-18 aparece en la sección de aprobadas del registro | Resuelto | DEC-18 movida a la sección de pendientes del registro |
| **AF-02** | Media | El §12 del PRD omitía decisiones no aprobadas | Resuelto | PRD §12 generado desde la tabla única de bloqueos; incluye todas las decisiones no aprobadas |
| **AF-03** | Media | DEC-65 no se cita en el PRD ni en el mapa | Resuelto | DEC-65 citada en RN-133 y en A14 |
| **AF-04** | Media | Reglas con validación sin decisión registrada | Abierto | Requiere tu autorización para crear decisiones |
| **AF-05** | Baja | Rangos de numeración con significado | Resuelto | Numeración secuencial sin significado de estado; sin renumerar |
| **AF-06** | Media | Colisión E10/E11 entre pantallas y etapas | Resuelto | Etapas con prefijo ET; pantallas E01–E11 sin cambios |
| **AF-07** | Baja | T01 cambia de significado entre versiones | Diferido (MEN) | Las páginas web del tutor salen de la beta |
| **AF-08** | Baja | A11 sin acceso desde A01 en el inventario | Resuelto | Inventario de A11 actualizado al ajustar el flujo de edad |
| **AF-09** | Baja | El total mezclaba pantallas y páginas web | Parcial | El conteo separa 103 pantallas de la app y 4 páginas web; el §11 del mapa sigue remitiendo a un informe externo |
| **AF-10** | Baja | Diferencia entre 69 y 74 pantallas | Resuelto | Sustituida por el conteo de la beta: 70 pantallas de la app (38 + 22 + 10), sin páginas web |
| **AF-11** | Alta | La web del tutor no figuraba en el plan de etapas | Diferido (MEN) | Fuera de la beta; debe incluirse en el plan cuando se habiliten menores |
| **AF-12** | Alta | Falta el servicio de correo transaccional | Parcial | Requisitos formales en PRD §8.5; proveedor pendiente (DEC-72) |
| **AF-13** | Alta | Objetivos corporales de menores presentados como aprobados | Resuelto | Objetivos corporales de menores: [PEND DEC-35] en PRD y mapa |
| **AF-14** | Media | El comportamiento para menores depende de DEC-64 | Diferido (MEN) | DEC-64 deja de bloquear la beta |
| **AF-15** | Media | Bloqueos condicionales de menores no listados | Resuelto | PRD §12.5 lista las decisiones de la habilitación futura de menores |
| **AF-16** | Baja | RN-114 remite a F11/F12 en lugar de F16/F17 | Resuelto | RN-114 remite a F16 y F17 |
| **AF-17** | Alta | Lista de bloqueos de ET6.1 incoherente e incompleta | Resuelto | Tabla única de bloqueos (registro §6) y PRD §12 generado desde ella; las decisiones siguen pendientes |
| **AF-18** | Alta | Sin decisión sobre documentos legales | Parcial | Requisito previo aprobado (DEC-70, RN-144); redacción y validación pendientes (DEC-71) |
| **AF-19** | Alta | No estaba definido si el MVP se publica | Resuelto | DEC-68: beta cerrada, gratuita, por invitación, solo 18+, sin cobros |
| **AF-20** | Media | Transición a planes sin decidir y sin salvaguarda aprobada | Parcial | DEC-67 redefinida y RN-141 aprobada; la política sigue pendiente antes de ET10 |
| **AF-21** | Baja | IVA y precios exactos en las tiendas | Abierto | ET10 |
| **AF-22** | Alta | Sin línea de trabajo para conseguir contenido con licencia | Abierto | Requiere tu autorización |
| **AF-23** | Media | Ejercicios y programas sin validación profesional | Abierto | Requiere tu autorización |
| **AF-24** | Media | Fuentes de alimentos candidatas no trasladadas a DEC-57 | Resuelto | Fuentes candidatas listadas en DEC-57 con licencia por verificar; la elección sigue pendiente |
| **AF-25** | Baja | Valores de recetas no marcados como estimación | Resuelto | N06 identifica los valores como estimación |
| **AF-26** | Baja | Sin mínimo de contenido para el MVP | Abierto | Requiere tu autorización |
| **AF-27** | Baja | "Resuelto" apoyado en reglas propuestas | Resuelto | Nuevo estado "Resuelto (propuesta)" aplicado a 8 hallazgos |
| **AF-28** | Baja | RN-118 a RN-120 sin formato de regla | Resuelto | RN-118 a RN-120 con formato de regla |

| Estado | Altos | Medios | Bajos | Total |
|---|---|---|---|---|
| Resuelto | 3 | 6 | 7 | **16** |
| Parcial | 2 | 1 | 1 | **4** |
| Abierto | 1 | 2 | 2 | **5** |
| Diferido (MEN) | 1 | 1 | 1 | **3** |
| **Total** | **7** | **10** | **11** | **28** |

---

## 8. Auditoría cruzada de la v0.2.2 (AC)

Hallazgos de la auditoría cruzada realizada tras la v0.2.2. Por autorización del propietario solo se corrigieron AC-01 y AC-02.

| Hallazgo | Sev. | Problema | Estado | Nota |
|---|---|---|---|---|
| **AC-01** | Media | Tres referencias presentaban DEC-44 como pendiente ("[PEND DEC-38/44]") | Resuelto | Mapa U09 (inventario y detalle) y trazabilidad R-11 dicen ahora "no aplica en la beta (DEC-44); futuro: DEC-38". R-11 sigue "Diferido (MEN)" |
| **AC-02** | Baja | El perfil "Madre, padre o tutor" no indicaba que es habilitación futura | Resuelto | PRD §3.2 lo marca como MEN, fuera de la beta |
| **AC-03** | Baja | Las notas de cambios de la v0.2.1 muestran la notación ET | Aceptado sin cambios | Diferencia histórica aceptada por el propietario |

---

## 9. Cambios de la v0.2.3

Cambios aprobados expresamente por el propietario. No resuelven ni reabren hallazgos de las auditorías anteriores; se registran aquí para mantener la trazabilidad.

| Cambio | Decisión | Documentos | Verificación |
|---|---|---|---|
| Compatibilidad básica con tablets y requisitos TB-01 a TB-04 | DEC-66 → Aprobada | PRD §5.2, §10 · MAPA §10 | En la línea base (562f7fc) DEC-66 figuraba como "Requiere validación" y estaba contada entre las 18 de validación; los conteos pasan a 25 / 17 / 28 = 70 |
| Proveedor de correo: API preferida, SMTP alternativa, evaluación separada de la autenticación, dominio pendiente | DEC-72 → Pendiente (redefinida) | PRD §8.5 · registro §3 | Sin proveedor seleccionado |
| Conservación de mensajes precisada | CT-09 [PROP] | PRD §8.5 | Sin cifras: valor por definir |
| Sin rastreo de aperturas ni clics en todos los correos transaccionales | CT-14 [APR] | PRD §8.5 | Se aplica también al envío propio de la autenticación |
| Separación de las decisiones tecnológicas | DEC-73 a DEC-77 → Pendientes | PRD §4, §12 · registro §3, §6 | Ninguna tecnología seleccionada |

---

## 10. Cambios de la v0.2.4

Cambio aprobado expresamente por el propietario. No resuelve ni reabre hallazgos de auditorías anteriores.

| Cambio | Decisión | Documentos | Verificación |
|---|---|---|---|
| Nombre comercial "Definitely Fitness" | DEC-78 → Aprobada (sujeta a DEC-53) | PRD, mapa, registro, trazabilidad, README | 11 referencias vigentes sustituidas; documentos históricos 01–03 sin cambios |
| Nombre anterior "Definite Fitnes" | DEC-10 → Sustituida | Registro §7 | Conservada como registro histórico, vinculada a DEC-78 |
| Nuevo estado "Sustituida" | — | Registro (estados y resumen) | Conteos: 25 aprobadas, 17 requieren validación, 28 pendientes, 1 sustituida = 71 |
| Validación de marca | DEC-53 → Requiere validación (sin cambio de estado) | Registro | Ahora referida a "Definitely Fitness" |
