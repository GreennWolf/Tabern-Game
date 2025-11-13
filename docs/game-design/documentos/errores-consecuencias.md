# ⚠️ Sistema de Errores y Consecuencias

Este documento define qué sucede cuando el jugador comete errores al verificar documentos.

---

## 🎯 FILOSOFÍA DEL SISTEMA

### Papers Please Inspiration

**Tensión constante:**
- Cada decisión tiene peso
- Errores tienen consecuencias reales
- Balance entre rapidez (ganancia) y precisión (evitar multas)

**Perdón temprano, castigo tarde:**
- Early game: Sistema perdona errores (tutorial)
- Mid game: Penalizaciones moderadas
- Late game: Errores cuestan caro

---

## 📊 TIPOS DE ERRORES

### Error Tipo 1: FALSO POSITIVO

**Definición:** Rechazas a cliente con documentos LEGÍTIMOS

**Causas:**
- Malinterpretas sello auténtico como falso
- Calculas mal las fechas
- No conoces restricción raza-clase (y crees que es imposible cuando sí es posible)
- Paranoia (todo te parece sospechoso)

**Ejemplo:**
```
Cliente: Elfo del Bosque Druida (100% legítimo)
Documentos: ID + Licencia de Magia (ambos reales)

Jugador piensa: "Elfos + Magia = Sospechoso"
Jugador rechaza servicio

Resultado: ❌ ERROR - Cliente era legítimo
```

---

### Error Tipo 2: FALSO NEGATIVO

**Definición:** Sirves a cliente con documentos FALSOS

**Causas:**
- No revisas cuidadosamente (prisa)
- Falsificación maestra engaña
- No usas herramientas disponibles (UV, Escáner)
- Ignoras inconsistencias por pereza

**Ejemplo:**
```
Cliente: Duende Pícaro con ID falsa (Nivel 3 - Avanzada)
Documentos: Visualmente perfectos, pero sin marca UV

Jugador NO usa Luz UV (pereza o prisa)
Jugador sirve

Resultado: ❌ ERROR - Serviste a falsificador
```

---

### Error Tipo 3: VIOLACIÓN DE REGLAS

**Definición:** Sirves a cliente que viola Libro de Reglas del día

**Causas:**
- No consultaste Libro de Reglas
- Olvidaste regla específica
- Malinterpretas regla

**Ejemplo:**
```
Libro de Reglas HOY:
"Prohibido servir a Minotauros"

Cliente: Minotauro con documentos 100% legítimos

Jugador sirve (olvidó consultar reglas)

Resultado: ❌ ERROR - Violaste regla del día
```

---

### Error Tipo 4: SERVIR A CRIMINAL BUSCADO

**Definición:** Sirves a cliente en Orden de Detención

**Causas:**
- No comparaste con órdenes en la pared
- No reconociste el retrato
- Ignoraste orden conscientemente (dilema moral)

**Ejemplo:**
```
Orden de Detención:
"Vex la Sombra" - Elfo Noche Pícaro - Recompensa 300c

Cliente entra: Elfo Noche Pícaro con documentos legítimos

Jugador NO compara con órdenes
Jugador sirve

Resultado: ❌ ERROR - Serviste a criminal buscado
```

---

## 💰 SISTEMA DE MULTAS

### Early Game (Días 1-14)

**Política:** Perdón y educación

**Primer error:**
- Advertencia verbal (sin multa)
- Inspector explica error
- "Esta vez pase, pero tenga más cuidado"

**Segundo error:**
- Multa: 20 monedas (simbólica)
- Advertencia escrita

**Tercer error en adelante:**
- Multa: 50 monedas

**Razón:** Tutorial, jugador está aprendiendo

---

### Mid Game (Días 15-60)

**Política:** Penalización moderada

**Por error:**

| Tipo Error | Multa | Pérdida Reputación |
|------------|-------|---------------------|
| Falso Positivo | 50c | -5 (con facción del cliente) |
| Falso Negativo | 100c | -10 (con Guardia) |
| Violación Reglas | 150c | -15 (con Consejo) |
| Servir Criminal | 200c | -20 (con Guardia) |

**Acumulación:**
- 5+ errores en 1 semana: Inspección sorpresa
- 10+ errores en 1 mes: Suspensión de licencia (2 días cerrado)

---

### Late Game (Día 61+)

**Política:** Penalización severa

**Por error:**

| Tipo Error | Multa | Pérdida Reputación | Extra |
|------------|-------|---------------------|-------|
| Falso Positivo | 100c | -10 | Cliente demanda posible |
| Falso Negativo | 300c | -25 | Inspección forzada |
| Violación Reglas | 500c | -30 | Suspensión 1 día |
| Servir Criminal | 800c | -50 | Suspensión 3 días |

**Errores críticos:**

**Servir a criminal de alta peligrosidad (⚠️⚠️⚠️):**
- Multa: 1000 monedas
- Suspensión: 7 días
- -100 Reputación con Guardia
- Posible cierre permanente si reincidente

**Servir a menor (menor de edad):**
- Multa: 500 monedas
- Suspensión: 3 días
- -50 Reputación con Consejo
- Escándalo público (clientes reducidos 20% por 1 semana)

---

## 🚨 SISTEMA DE INSPECCIONES

### Inspección Rutinaria

**Frecuencia:** 1 vez por semana (aleatorio)

**Proceso:**
```
Inspector de la Guardia entra
    ↓
Revisa tus registros de últimos 7 días
    ↓
Compara con base de datos oficial
    ↓
Detecta errores que cometiste
    ↓
Aplica multas retroactivas
```

**Ejemplo:**
```
Inspector: "El día 10/6, serviste a un Minotauro"
Inspector: "Ese día, Libro de Reglas prohibía Minotauros"
Inspector: "Multa: 150 monedas"

Jugador: "No revisé el Libro de Reglas ese día..."
Inspector: "Esa es su responsabilidad. Aquí está su multa."
```

**Resultado positivo:**
```
Inspector: "Registros impecables esta semana"
Inspector: "Bonificación por buen desempeño: 100 monedas"
```

---

### Inspección Sorpresa (por acumulación de errores)

**Trigger:** 5+ errores en 1 semana

**Proceso:**
```
Inspector llega sin aviso
    ↓
Auditoría completa (revisa TODO)
    ↓
Detecta TODOS los errores cometidos
    ↓
Multas masivas + posible suspensión
```

**Severidad:**

**5-7 errores:**
- Multa total: 500-800 monedas
- Advertencia final

**8-10 errores:**
- Multa total: 1000-1500 monedas
- Suspensión: 2-3 días

**11+ errores:**
- Multa total: 2000+ monedas
- Suspensión: 1 semana
- Evaluación para cierre permanente

---

### Inspección por Denuncia

**Trigger:** Cliente que rechazaste presenta queja oficial

**Proceso:**
```
Cliente con documentos legítimos es rechazado
    ↓
Cliente enojado va a Consejo Municipal
    ↓
Presenta queja formal
    ↓
Inspector llega al día siguiente
    ↓
Revisa caso específico
```

**Si tenías razón (documentos eran falsos):**
- Sin consecuencias ✓
- +10 Reputación con Guardia
- Posible recompensa pequeña (50c)

**Si estabas equivocado (documentos eran legítimos):**
- Multa: 200 monedas (falsa acusación)
- Cliente puede demandar (daño a reputación)
- -20 Reputación con facción del cliente

---

## ⚖️ SISTEMA DE DEMANDAS

### Cliente Demanda por Falso Positivo

**Condiciones:**
- Rechazaste cliente con documentos legítimos
- Cliente es miembro de facción poderosa
- O cliente es noble/VIP

**Proceso:**
```
Recibes notificación: "Ha sido demandado por [Cliente]"
    ↓
Juicio en 3 días (in-game)
    ↓
Debes presentar evidencia de por qué rechazaste
```

**Resultado si pierdes juicio:**
- Multa: 500-1000 monedas (compensación al cliente)
- -50 Reputación con facción del cliente
- Anuncio público (vergüenza)

**Resultado si ganas juicio:**
- Sin consecuencias ✓
- +20 Reputación con Consejo (defendiste tu caso)

**Cómo ganar juicio:**
- Demuestra que tenías razón en sospechar
- Muestra que seguiste protocolo correctamente
- Argumenta que error fue razonable (falsificación maestra)

---

## 📉 SISTEMA DE REPUTACIÓN

### Pérdida de Reputación por Errores

**Con Guardia Real:**
- Cada Falso Negativo: -10 reputación
- Servir criminal: -50 reputación

**Efectos:**
- < 50 reputación: Inspecciones más frecuentes
- < 25 reputación: Amenaza de cierre
- 0 reputación: Cierre permanente

---

**Con Facciones Específicas:**

**Ejemplo: Facción Élfica**
```
Rechazas Elfo con documentos legítimos
→ -10 reputación con Facción Élfica

Efectos:
- Elfos vienen menos a tu taberna (-20% clientes élficos)
- Precios de Vino Élfico suben (+30%)
- Acceso a eventos élficos bloqueado
```

---

**Con Consejo Municipal:**
- Cada violación de reglas: -15 reputación

**Efectos:**
- < 50: Multas aumentan 50%
- < 25: Licencias más caras
- 0: Revocación de licencia (cierre permanente)

---

### Recuperación de Reputación

**Métodos:**

**1. Desempeño impecable:**
- 1 semana sin errores: +10 reputación (con Guardia)
- 1 mes sin errores: +50 reputación (con Consejo)

**2. Capturar criminales:**
- Cada criminal entregado: +20 reputación (con Guardia)
- Criminal peligroso (⚠️⚠️⚠️): +50 reputación

**3. Quests de facción:**
- Completar misión para facción: +30-100 reputación

**4. Donaciones:**
- Donar al Consejo: 500 monedas = +25 reputación
- Donar a Guardia: 300 monedas = +15 reputación

---

## 🔒 SISTEMA DE SUSPENSIONES

### Suspensión Temporal

**Duración:** 1-7 días (in-game)

**Efectos durante suspensión:**
- Taberna cerrada (0 ingresos)
- Gastos fijos continúan (alquiler, servicios)
- Clientes regulares pueden irse a competencia
- -5 reputación global por día cerrado

**Pérdidas estimadas:**

**1 día suspensión:**
- Ingresos perdidos: ~500 monedas (promedio diario)
- Gastos fijos: ~100 monedas
- Pérdida total: ~600 monedas

**7 días suspensión:**
- Ingresos perdidos: ~3500 monedas
- Gastos fijos: ~700 monedas
- Pérdida clientela: -20% clientes regulares
- Pérdida total: ~4500 monedas + clientela

---

### Cierre Permanente (Game Over)

**Condiciones para cierre:**

**1. Reputación 0 con Consejo Municipal:**
- Acumulación de violaciones graves
- Sin recuperación posible

**2. Reputación 0 con Guardia Real:**
- Servir criminales reiteradamente
- Colaboración con organizaciones ilegales

**3. Bancarrota:**
- No puedes pagar multa de 1000+ monedas
- Deudas acumuladas > 2000 monedas
- Sin ingresos para operar

**4. Evento catastrófico:**
- Servir a Pase VIP falso = TRAICIÓN
- Colaborar con Culto de la Sombra (ilegal absoluto)
- Causar muerte de inspector (negligencia extrema)

**Pantalla de Game Over:**
```
╔══════════════════════════════════════════╗
║         TABERNA CERRADA PERMANENTEMENTE  ║
║                                          ║
║  El Consejo Municipal ha revocado su    ║
║  licencia de operación.                  ║
║                                          ║
║  Razón: [Reputación 0 con Guardia]      ║
║                                          ║
║  Días operados: 87                       ║
║  Clientes servidos: 523                  ║
║  Criminales capturados: 12               ║
║  Errores cometidos: 45 (demasiados)     ║
║                                          ║
║  [Reintentar]  [Menú Principal]          ║
╚══════════════════════════════════════════╝
```

---

## 💡 BALANCEO: Riesgo vs Recompensa

### Escenario 1: Cliente Sospechoso

**Situación:**
```
Duende Pícaro con documentos Nivel 3 (Avanzados)
Visual: Perfecto ✓
UV: Sin marca ❌
Escáner Magia: No tienes (cuesta 200c)
```

**Opciones:**

**A) Servir (asumir riesgo):**
- Si es falso: Multa 300c, -25 reputación
- Si es real: Ganancia 30c

**B) Rechazar:**
- Si es falso: ✓ Decisión correcta, +10 reputación
- Si es real: Demanda posible 500c, -50 reputación

**C) Comprar Escáner de Magia (200c):**
- Inversión: -200c ahora
- Detecta falsificaciones futuras
- ROI: ~10 clientes sospechosos

**Análisis:**
```
Probabilidad falso (Duende Pícaro): 70%
Valor esperado SERVIR: 0.7 × (-300c) + 0.3 × (30c) = -201c
Valor esperado RECHAZAR: 0.7 × (10c equiv.) + 0.3 × (-500c) = -143c
Valor esperado ESCÁNER: -200c inicial, pero +300c por cada falsificación detectada

→ Mejor decisión: COMPRAR ESCÁNER (inversión a largo plazo)
```

---

### Escenario 2: Refugiado (Dilema Moral)

**Situación:**
```
Familia élfica huyendo de guerra
Documentos: Nivel 2 (Medianos), claramente falsos
Historia: Trágica, niños hambrientos
```

**Opciones:**

**A) Servir (compasión):**
- Riesgo multa: 300c (si te descubren)
- Probabilidad descubrimiento: 30% (Inspección rutinaria)
- Valor esperado: -90c
- +Satisfacción moral ✓
- +Reputación Facción Élfica

**B) Rechazar (ley):**
- Sin riesgo ✓
- -Satisfacción moral ❌
- Familia probablemente muere (narrativa)

**C) Reportar a Guardia:**
- Recompensa: 50c
- -Reputación Facción Élfica (-30)
- -Satisfacción moral extrema ❌

**No hay respuesta correcta:** Jugador decide valores

---

## 📈 CURVA DE APRENDIZAJE

### Días 1-7: Tutorial

**Errores esperados:** 3-5 (perdonados)
**Objetivo:** Aprender mecánicas básicas
**Multas:** 0-50c total

---

### Días 8-30: Aprendizaje

**Errores esperados:** 10-15
**Objetivo:** Dominar verificación cruzada
**Multas:** 500-1000c total

---

### Días 31-60: Maestría

**Errores esperados:** 5-8
**Objetivo:** Detectar falsificaciones avanzadas
**Multas:** 500-800c total

---

### Día 61+: Experto

**Errores esperados:** 2-4
**Objetivo:** Perfección casi absoluta
**Multas:** 200-400c total

**Jugador experto:**
- Detecta 95%+ falsificaciones
- Balance perfecto rapidez/precisión
- Intuición desarrollada
- Ganancias máximas (~700c/día neto)

---

## 🎯 OBJETIVOS DE DISEÑO

1. **Consecuencias reales:** Errores duelen, decisiones importan
2. **Perdón temprano:** Tutorial generoso para aprender
3. **Castigo escalado:** Complejidad y penalización aumentan juntas
4. **Dilemas morales:** No siempre hay respuesta "correcta"
5. **Recuperación posible:** Siempre hay camino de vuelta (excepto Game Over)
6. **Tensión constante:** "¿Será real o falso?" en cada cliente
7. **Maestría recompensada:** Jugador experto prospera

---

## 📊 TABLA RESUMEN: Consecuencias

| Error | Multa (Early) | Multa (Mid) | Multa (Late) | Reputación |
|-------|---------------|-------------|--------------|------------|
| Falso Positivo | 20c | 50c | 100c | -5/-10 |
| Falso Negativo | 50c | 100c | 300c | -10/-25 |
| Violación Reglas | 50c | 150c | 500c | -15/-30 |
| Servir Criminal | 100c | 200c | 800c | -20/-50 |
| Servir Menor | 200c | 500c | 500c | -50 |
| Traición (VIP falso) | 1000c | 1000c | 1000c | Game Over |

---

**Sistema completo de consecuencias definido. Balance entre dificultad y justicia.**
