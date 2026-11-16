# Definite Fitnes — Trazabilidad de la auditoría hacia la v0.2

| | |
|---|---|
| **Versión** | 0.2 — propuesta |
| **Auditoría de origen** | [03-AUDITORIA-CRUZADA.md](03-AUDITORIA-CRUZADA.md) (59 hallazgos: 14 altos, 32 medios, 13 bajos) |
| **Documentos relacionados** | [04 — PRD v0.2](04-PRD-v0.2-PROPUESTA.md) · [05 — Mapa v0.2](05-MAPA-NAVEGACION-v0.2-PROPUESTA.md) · [06 — Registro de decisiones](06-REGISTRO-DECISIONES-v0.2.md) |

## Estados

| Estado | Significado |
|---|---|
| **Resuelto** | La corrección está en la propuesta v0.2 y se apoya en una decisión aprobada o es una corrección documental que no necesita decisión de producto. Sigue sujeta a tu aprobación de la v0.2 en conjunto. |
| **Parcial** | Se eliminó la contradicción o se definió la estructura, pero queda una decisión o validación. |
| **Abierto** | Depende de una decisión pendiente; solo se documentaron alternativas. |
| **Requiere validación** | Depende de la opinión de un profesional competente. |

Según tu regla de control de calidad, **ningún hallazgo se marca como resuelto si aún falta una decisión o validación**.

Abreviaturas: **PRD** = 04-PRD-v0.2 · **MAPA** = 05-MAPA-v0.2.

---

## 1. Contradicciones (X)

| Hallazgo | Sev. | Resolución propuesta | Dónde se refleja | Decisión | Estado | ¿Revisión posterior? |
|---|---|---|---|---|---|---|
| **X-01** Límites Gratis en el MVP sin pagos | Alta | Sin restricciones comerciales en el MVP; se quitan los enlaces a U09 desde el MVP; límites como propuesta para E10 | PRD §5.2, §7, RN-35, RN-138 · MAPA E04, P02, P03, P05, N07 | DEC-01 | Resuelto | Sí, en E10 (DEC-62, DEC-67) |
| **X-02** Peso y medidas para 16–17 | Alta | Ambos documentos dicen lo mismo: medidas solo para adultos de forma provisional; menores pendiente; predicción corporal excluida | PRD RN-134, §9.3 · MAPA O10, P07, U02, §8 | DEC-14 (aprobada), DEC-35 | Parcial | Sí: validación legal y profesional |
| **X-03** Integraciones de salud para 13–15 | Alta | El panel del tutor ya no lista interruptores concretos; integraciones para menores marcadas como pendientes en ambos documentos | PRD §6.11, §9.3 · MAPA T02, U15 | DEC-37 | Requiere validación | Sí, antes de E10 |
| **X-04** Alimento propio 16+ sin respaldo en el PRD | Media | La restricción deja de ser regla y pasa a la decisión sobre nutrición para menores | PRD §6.3 · MAPA N10 | DEC-36 | Requiere validación | Sí |
| **X-05** "Bienestar y hábitos" sin módulo | Media | Se conserva la opción en O03 marcada como pendiente; alternativas documentadas | PRD §6.3 · MAPA O03, N08 | DEC-54 | Abierto | Sí, antes de E6.1 (afecta a O03) |
| **X-06** Mostrar/ocultar tarjetas Gratis vs H03 en E10 | Media | En el MVP el inicio se adapta a los módulos activos; la organización manual queda en E10 | PRD RN-136 · MAPA H01, H03 | DEC-01 | Resuelto | No |
| **X-07** Contenido nutricional para 13–15 | Media | N01 y N03 remiten a la decisión pendiente; principio aprobado sin metas restrictivas | PRD RN-27, §9.3 · MAPA N01, N03 | DEC-13 (aprobada), DEC-36 | Requiere validación | Sí |
| **X-08** Bloqueo de amistades por el tutor (16–17) | Media | Se retiran funciones concretas del tutor hasta decidir su alcance | PRD §9.3 · MAPA T02, S01 | DEC-39, DEC-40 | Abierto | Sí, antes de E9 |
| **X-09** Recetas en la columna equivocada | Baja | Recetas básicas en E6.3; biblioteca amplia POST | PRD §5.2, §6.3 · MAPA N05 | DEC-03 | Resuelto | Sí: cantidad inicial (DEC-63) |
| **X-10** Botón Comunidad y pestaña Amigos antes de E9 | Baja | El mapa muestra los botones y pestañas por entrega; Comunidad solo desde E9; pestaña Amigos según decisión | PRD RN-13, RN-14 · MAPA §4.2, H01 | DEC-46 | Parcial | Sí, antes de cerrar E6.3 |

## 2. Pantallas y recorridos incompletos (P)

| Hallazgo | Sev. | Resolución propuesta | Dónde se refleja | Decisión | Estado | ¿Revisión posterior? |
|---|---|---|---|---|---|---|
| **P-01** A01 sin enrutamiento completo | Alta | Tabla de enrutamiento de 12 estados, aplicada también por A06 | MAPA §4.3 | — (corrección documental) | Resuelto | No (el paso 1 depende de E-12) |
| **P-02** Apple/Google sin verificar edad | Alta | Toda autenticación social sin cuenta pasa por A03 antes de crear nada | PRD RN-128 · MAPA A03, A04, A06, F02 | DEC-09 | Resuelto | No |
| **P-03** Sin pantalla de reactivación | Alta | Nueva pantalla A13; flujo F09 | PRD RN-87 · MAPA A13, F09 | DEC-60 (plazo) | Parcial | Sí: aprobar el plazo de gracia y validarlo legalmente |
| **P-04** Aceptar invitación familiar sin ID | Media | Nueva pantalla U17 con aviso de doble pago; flujos F18 y F19 | PRD RN-102, RN-107 · MAPA U17, F18, F19 | DEC-38 (menores) | Parcial | Sí: caso de menores |
| **P-05** Vista previa al compartir sin pantalla | Media | Nueva pantalla S11; flujo F23 | PRD RN-62 · MAPA S11, F23 | — (corrección documental) | Resuelto | Sí, al diseñar E9 (DEC-40) |
| **P-06** Sin pantalla al bajar a Gratis | Media | Nueva pantalla U19; flujo F21 | PRD RN-92 · MAPA U19, F21 | DEC-62, DEC-67 | Parcial | Sí, en E10 |
| **P-07** Sin transición al cumplir 16 y 18 | Media | Nuevas pantallas A15 y A16; flujos F16 y F17 | PRD Anexo A (RN-114) · MAPA A15, A16, F16, F17 | DEC-32, DEC-33, DEC-39, DEC-44 | Parcial | Sí: el contenido depende de decisiones pendientes |
| **P-08** Mensaje de cuidado sin componente | Media | Nuevo componente M02 enlazado a U14 | PRD RN-25 · MAPA M02, N01 | DEC-61 | Requiere validación | Sí: criterios por un profesional |
| **P-09** Canal del resumen para el tutor | Media | Se documenta como pendiente; sin pantalla hasta decidir | PRD §9.5 · MAPA U16, T02 | DEC-39 | Abierto | Sí |
| **P-10** Solicitud de permiso al tutor sin canal | Media | Correo + página T03 y estado visible en U16; flujo F07 | PRD §9.5 · MAPA T03, U16, F07 | DEC-07 (aprobada), DEC-45, DEC-31 | Parcial | Sí: aprobar fases y validar la autorización |
| **P-11** Desconectar integración sin diálogo | Media | Componente M04 | PRD RN-83 · MAPA M04, U15, F25 | — (corrección documental) | Resuelto | No |
| **P-12** Foto de perfil sin pantalla | Media | Se documenta como pendiente; el MVP usa inicial o avatar simple | PRD §6.8 · MAPA U01 | DEC-56 | Abierto | Sí |
| **P-13** Fecha del último cálculo en P04 | Baja | Añadida a P04 | PRD RN-42 · MAPA P04 | — | Resuelto | No |
| **P-14** Plazo de cambio de modalidad en U02 | Baja | En el MVP la modalidad no limita funciones; el límite pasa a E10 | PRD RN-35 | DEC-01 | Resuelto | Sí, si E10 adopta el límite (DEC-62) |

## 3. IDs e inventario (I)

| Hallazgo | Sev. | Resolución propuesta | Dónde se refleja | Decisión | Estado | ¿Revisión posterior? |
|---|---|---|---|---|---|---|
| **I-01** "P" con dos significados | Media | Premium se marca con ★ | MAPA §1.2 | — | Resuelto | No |
| **I-02** Panel del tutor contado como pantalla de la app | Media | Inventario separado para páginas web (T01–T04) | MAPA §3.2, §3.4 | DEC-07 | Resuelto | No |
| **I-03** Falta N09 | Baja | N09 = Alternativas | MAPA §1.3, N09 | — | Resuelto | No |
| **I-04** N03b y N01d fuera del inventario | Baja | N03b pasa a N09; N01d es una vista de N01 | MAPA §1.3 | — | Resuelto | No |
| **I-05** T00 y E00 | Baja | Tutor numerado T01–T04; E00 pasa a ser un nodo de decisión sin ID | MAPA §1.1, §1.3 | — | Resuelto | No |
| **I-06** S10 fuera del diagrama de Comunidad | Baja | S10 en el inventario con su acceso (U05); el diagrama de Comunidad se sustituye por la tabla de inventario y el flujo F24 | MAPA §3.1, F24 | — | Resuelto | No |
| **I-07** Inventario desactualizado | Baja | Inventario rehecho: 102 pantallas de la app + 4 web + 4 componentes | MAPA §3.4 | — | Resuelto | No |

## 4. Reglas sin reflejo en la navegación (R)

| Hallazgo | Sev. | Resolución propuesta | Dónde se refleja | Decisión | Estado | ¿Revisión posterior? |
|---|---|---|---|---|---|---|
| **R-01** Bloqueo de menores de 13 en el dispositivo | Alta | Comportamiento de A11 y de A01 descrito, condicionado a validación | PRD RN-02 · MAPA A11, §4.3 | DEC-18, DEC-31 | Requiere validación | Sí |
| **R-02** Restricciones de entrenamiento por edad | Alta | La regla v0.1 queda suspendida; E01 remite a la decisión; entretanto, DEC-64 (propuesta) | PRD RN-36, §9.3, §9.4 · MAPA E01, §8 | DEC-32, DEC-33 | Requiere validación | Sí |
| **R-03** Fecha límite en A10 | Media | A10 muestra la fecha de caducidad | MAPA A10 | DEC-60 (14 días) | Parcial | Sí: aprobar y validar el plazo |
| **R-04** Estado de demasiados intentos | Media | Estado definido en A05, A06, A07 y en §6 | PRD RN-07 · MAPA A05–A07, §6 | — | Resuelto | No |
| **R-05** Advertencias de seguridad en rutinas y sesión | Media | Advertencias en E03, E05 y E06 (con consentimiento); precauciones generales siempre | PRD RN-34 · MAPA E03, E05 | DEC-08 | Resuelto | No |
| **R-06** Mínimos de seguridad en P03 | Media | P03 explica y propone un ritmo seguro si la meta incumple los límites | PRD RN-22 · MAPA P03 | DEC-50 | Requiere validación | Sí: valores por un profesional |
| **R-07** Ubicación de la sugerencia de descanso | Media | En H01 (recomendaciones) y E09 | PRD RN-15, RN-33 · MAPA H01, E09 | DEC-16 | Parcial | Sí: umbrales con validación profesional |
| **R-08** Modalidad principal en Gratis | Media | En el MVP no limita funciones; el caso sin métricas propias pasa a DEC-55 | PRD RN-35 · MAPA O04 | DEC-01, DEC-55 | Parcial | Sí |
| **R-09** Herramienta de moderación | Media | Documentada como necesidad de E9 | PRD §3.3, §6.9 | DEC-40 | Abierto | Sí, antes de E9 |
| **R-10** Derechos ARCO incompletos | Media | Acceso desde U05, U18 y U14 con flujo F10 | PRD RN-90 · MAPA U14, U18, F10 | — | Requiere validación | Sí: procedimiento legal |
| **R-11** Ofertas de compra a menores | Media | En el MVP no hay compras (DEC-01); en E10 depende de DEC-38/44 | PRD RN-97 · MAPA U09 | DEC-01, DEC-38, DEC-44 | Parcial | Sí, en E10 |
| **R-12** Espera y aviso de doble pago en U10 | Media | U10 muestra la espera; U17 muestra el aviso de doble pago | MAPA U10, U17 | DEC-49 | Parcial | Sí, en E10 |
| **R-13** Eventos de XP desde E6 | Baja | Registro de eventos desde E6.2 como servicio transversal | PRD §4.2, RN-56 | — | Resuelto | Sí, en E5 (modelo de datos) |
| **R-14** Indicador de IA por mensaje | Baja | Cada respuesta se identifica como IA | PRD RN-76 · MAPA I01 | — | Resuelto | No |
| **R-15** Notificaciones sin datos sensibles | Baja | Documentado como comportamiento | PRD RN-84 | — | Resuelto | No |

## 5. Edad y privacidad (E)

| Hallazgo | Sev. | Resolución propuesta | Dónde se refleja | Decisión | Estado | ¿Revisión posterior? |
|---|---|---|---|---|---|---|
| **E-01** No se determina el país | Alta | México como primer país y reglas configurables por país; el mecanismo de detección queda pendiente | PRD §8.4, RN-124 | DEC-06 (aprobada), DEC-43 | Parcial | Sí, antes de E6.1 |
| **E-02** Autenticación social sin edad | Alta | Igual que P-02 | PRD RN-128 · MAPA F02 | DEC-09 | Resuelto | No |
| **E-03** Menores en plan Familiar | Alta | Flujo F19 llega hasta la decisión y se detiene; alternativas documentadas | PRD RN-108, §9.3 · MAPA U17, F19 | DEC-38 | Abierto | Sí, antes de E10 |
| **E-04** Datos recogidos antes del consentimiento parental | Alta | Documentado para la consulta legal; A10 permite cancelar y eliminar | PRD RN-04 · MAPA A10 | DEC-30 | Requiere validación | Sí |
| **E-05** Consentimiento de salud atado al registro | Alta | Registro separado del consentimiento de salud; pantalla A14, U18 y M01 | PRD RN-129–RN-132 · MAPA A04, A14, U18, M01, F05 | DEC-08 (aprobada), DEC-42 | Parcial | Sí: clasificación legal de los datos |
| **E-06** Detección de adultos en amistades de menores | Alta | Documentado dentro de la decisión de moderación | PRD §9.3 | DEC-40, DEC-32, DEC-33 | Abierto | Sí, antes de E9 |
| **E-07** Redundancia en amistades de 13–15 | Media | Pasa a la decisión sobre 13–15 | PRD §9.3 | DEC-32 | Abierto | Sí |
| **E-08** Fotos de perfil | Media | Igual que P-12 | PRD §6.8 | DEC-56 | Abierto | Sí |
| **E-09** Analítica sin consentimiento inicial | Media | Analítica desactivada hasta su consentimiento en A14 | PRD RN-133 · MAPA A14 | DEC-65 | Parcial | Sí: aprobar la propuesta |
| **E-10** Alimentos propios de 16–17 | Media | Pasa a la decisión sobre nutrición para menores | PRD §9.3 | DEC-36 | Requiere validación | Sí |
| **E-11** IA en modo restringido para 13–15 | Media | Pasa a la decisión sobre IA para menores | PRD §9.3 | DEC-41 | Requiere validación | Sí, antes de E8 |
| **E-12** Marca de bloqueo de menores de 13 | Media | Documentado para la consulta legal | PRD RN-02 · MAPA §4.3 | DEC-18, DEC-31 | Requiere validación | Sí |
| **E-13** Aviso al tutor al cumplir 16 | Baja | Flujo F16 con aviso por correo; alcance del tutor pendiente | MAPA A15, F16 | DEC-39 | Abierto | Sí |

---

## 6. Resumen

| Estado | Altos | Medios | Bajos | Total |
|---|---|---|---|---|
| Resuelto | 4 | 7 | 11 | **22** |
| Parcial | 4 | 10 | 1 | **15** |
| Abierto | 2 | 7 | 1 | **10** |
| Requiere validación | 4 | 8 | 0 | **12** |
| **Total** | **14** | **32** | **13** | **59** |

Conteo verificado automáticamente contra las tablas anteriores y contra las severidades de la auditoría original.

**Hallazgos altos resueltos:** X-01, P-01, P-02, E-02.
**Hallazgos altos no resueltos (10 de 14):**
- Parciales: X-02, P-03, E-01, E-05.
- Abiertos: E-03, E-06.
- Requieren validación: X-03, R-01, R-02, E-04.

Todos dependen de decisiones sobre menores, datos de salud, país o plazos legales.

### 6.1 Recorridos señalados en la auditoría sin código propio

La auditoría (§2) indicó tres recorridos incompletos que no recibieron código de hallazgo:

| Recorrido | Resolución | Dónde |
|---|---|---|
| F2 v0.1: tutor rechaza la solicitud | Estados "rechazado" y "caducado" en A10 | MAPA A10, F03 |
| F9 v0.1: persona invitada sin cuenta | Flujo completo con verificación de edad | MAPA F19 (menores: DEC-38) |
| Falta el recorrido de recuperación | Flujo F04 | MAPA F04 |
