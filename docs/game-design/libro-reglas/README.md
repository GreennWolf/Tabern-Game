# 📖 Sistema de Libro de Reglas

Este sistema define las reglas cambiantes que el jugador debe seguir cada día, inspirado en la mecánica core de Papers, Please.

---

## 🎯 FILOSOFÍA DE DISEÑO

### Papers Please Core Mechanic

**"Las reglas cambian constantemente, debes adaptarte"**

**Características principales:**
1. **Reglas cambian diariamente/semanalmente**
2. **Debes consultar el Libro CADA día**
3. **Violar reglas = Multa inmediata**
4. **Complejidad aumenta progresivamente**
5. **Reglas pueden contradecirse entre sí (dilemas)**

### Tensión Constante

```
Día 1: "Verificar edad legal"
→ Simple, 1 regla

Día 15: "Verificar edad + Prohibido Minotauros + Obligatorio licencia de magia"
→ Moderado, 3 reglas

Día 60: "Verificar edad + Prohibido Minotauros EXCEPTO con Pase VIP +
         Obligatorio licencia magia + Solo Guerreros pueden portar armas +
         Clérigos deben tener Certificado Pureza + Toque queda 21:00 razas exóticas +
         Bonificación 20% bebidas importadas"
→ Complejo, 7+ reglas simultáneas
```

**Jugador debe:**
- Memorizar reglas activas
- Consultar constantemente el Libro
- Adaptarse a cambios repentinos
- Tomar decisiones bajo presión

---

## 📋 ESTRUCTURA DEL LIBRO DE REGLAS

### Documento Diario

Cada mañana (6:00 in-game), recibes el Libro de Reglas actualizado:

```
╔══════════════════════════════════════════╗
║  CONSEJO MUNICIPAL - LIBRO DE REGLAS    ║
║                                          ║
║  FECHA: 15 de Junio, 1225               ║
║  VÁLIDO: Solo hoy (15/6/1225)           ║
║                                          ║
║  ═══ REGLAS ACTIVAS ═══                 ║
║                                          ║
║  1. ⛔ PROHIBIDO servir a Minotauros    ║
║     Razón: Tensión diplomática          ║
║     Multa por violación: 200 monedas    ║
║                                          ║
║  2. ✅ OBLIGATORIO verificar Licencia   ║
║     de Magia para clases mágicas        ║
║     Multa por violación: 100 monedas    ║
║                                          ║
║  3. 🕐 TOQUE DE QUEDA 21:00             ║
║     Para razas exóticas solamente       ║
║     (Minotauro, Dracónido)              ║
║     Multa por violación: 150 monedas    ║
║                                          ║
║  4. 💰 BONIFICACIÓN +20% precio         ║
║     En bebidas élficas (Festival)       ║
║                                          ║
║  ═══ VIGENCIA ═══                       ║
║  Reglas 1-3: Solo hoy                   ║
║  Regla 4: Hasta 20/6/1225 (Festival)    ║
║                                          ║
║  Nuevas reglas mañana a las 6:00        ║
║                                          ║
║  ┌────────┐                              ║
║  │ SELLO  │  Secretario del Consejo     ║
║  │CONSEJO │  Marcus Aldric              ║
║  └────────┘                              ║
╚══════════════════════════════════════════╝
```

---

## 🏷️ TIPOS DE REGLAS

### 1. PROHIBICIONES (⛔)

**Formato:** "PROHIBIDO [acción] para [target]"

**Ejemplos:**
- "PROHIBIDO servir a Minotauros"
- "PROHIBIDO servir bebidas alcohólicas a Clérigos"
- "PROHIBIDO entrada a miembros del Gremio de Ladrones"
- "PROHIBIDO armas dentro del establecimiento"

**Efecto:**
- Si sirves a cliente que viola prohibición → Multa automática
- No hay excepciones (excepto Pase VIP)

**Razones típicas:**
- Tensión diplomática entre facciones
- Eventos religiosos (prohibiciones de alcohol)
- Crisis de seguridad (prohibición de armas)
- Órdenes del Rey

---

### 2. OBLIGACIONES (✅)

**Formato:** "OBLIGATORIO [verificación] para [target]"

**Ejemplos:**
- "OBLIGATORIO verificar Licencia de Magia para todos los magos"
- "OBLIGATORIO verificar Certificado de Pureza para Paladines"
- "OBLIGATORIO exigir Permiso de Entrada a razas exóticas"
- "OBLIGATORIO revisar Certificado de Facción si cliente representa organización"

**Efecto:**
- Si NO verificas documento requerido → Multa si Inspector detecta
- Debes pedir documento activamente

**Razones típicas:**
- Aumentar seguridad
- Cumplimiento de tratados
- Prevención de crímenes
- Control de fronteras

---

### 3. RESTRICCIONES (🕐)

**Formato:** "RESTRICCIÓN [condición] para [target]"

**Ejemplos:**
- "TOQUE DE QUEDA 21:00 para razas exóticas"
- "LÍMITE 2 bebidas alcohólicas por cliente"
- "MÁXIMO 10 clientes simultáneos en el local"
- "PROHIBIDO música en vivo después de 22:00"

**Efecto:**
- Si violas restricción → Multa
- Puede ser verificable por Inspector

**Razones típicas:**
- Control de orden público
- Regulaciones de salud
- Prevención de disturbios
- Leyes de ruido

---

### 4. BONIFICACIONES (💰)

**Formato:** "BONIFICACIÓN [beneficio] en [contexto]"

**Ejemplos:**
- "BONIFICACIÓN +20% precio en bebidas élficas (Festival Élfico)"
- "BONIFICACIÓN +50 monedas por cada criminal entregado (Operación Limpieza)"
- "DESCUENTO -30% en renovación de licencias (Celebración Real)"
- "IMPUESTO -10% esta semana (Generosidad del Rey)"

**Efecto:**
- Oportunidad de ganar más dinero
- Incentivo para comportamientos específicos

**Razones típicas:**
- Festivales culturales
- Celebraciones nacionales
- Campañas de seguridad
- Buena voluntad del gobierno

---

### 5. EXENCIONES (⭐)

**Formato:** "EXENCIÓN [grupo] de [regla normal]"

**Ejemplos:**
- "EXENCIÓN Guerreros de prohibición de armas"
- "EXENCIÓN miembros de la Guardia Real de toque de queda"
- "EXENCIÓN nobles de verificación de edad"
- "EXENCIÓN Paladines de inspecciones rutinarias"

**Efecto:**
- Grupo específico NO está sujeto a regla
- Debes verificar que cliente pertenece a grupo exento

**Razones típicas:**
- Privilegios de clase social
- Necesidades operativas (Guardia)
- Tratados diplomáticos
- Tradiciones históricas

---

### 6. EMERGENCIAS (🚨)

**Formato:** "EMERGENCIA: [situación excepcional]"

**Ejemplos:**
- "EMERGENCIA: Ciudad en cuarentena - Solo residentes locales"
- "EMERGENCIA: Estado de sitio - Cierre inmediato a las 18:00"
- "EMERGENCIA: Búsqueda activa - Reportar cualquier Elfo de la Noche"
- "EMERGENCIA: Envenenamiento masivo - Prohibida toda bebida importada"

**Efecto:**
- ANULA reglas normales
- Prioridad absoluta
- Duración variable (hasta que se levante)

**Razones típicas:**
- Crisis de seguridad
- Epidemias
- Ataques terroristas
- Desastres naturales

---

## 📈 PROGRESIÓN DE COMPLEJIDAD

### Early Game (Días 1-14)

**Objetivo:** Aprender mecánicas básicas

**Complejidad:**
- 1-2 reglas activas simultáneamente
- Solo tipo Obligación (verificar edad)
- Reglas cambian cada 3-5 días (lento)
- Sin contradicciones

**Ejemplo típico Día 3:**
```
1. ✅ OBLIGATORIO verificar edad legal según raza
```

**Ejemplo típico Día 10:**
```
1. ✅ OBLIGATORIO verificar edad legal según raza
2. ✅ OBLIGATORIO verificar ID no esté vencida
```

---

### Mid Game (Días 15-60)

**Objetivo:** Dominar verificación cruzada

**Complejidad:**
- 3-5 reglas activas simultáneamente
- Tipos: Prohibiciones + Obligaciones + Restricciones
- Reglas cambian cada 1-2 días (moderado)
- Algunas contradicciones menores (Exenciones)

**Ejemplo típico Día 30:**
```
1. ✅ OBLIGATORIO verificar edad legal
2. ⛔ PROHIBIDO servir a Minotauros
3. ✅ OBLIGATORIO Licencia de Magia para magos
4. 🕐 TOQUE DE QUEDA 22:00 para razas exóticas
5. ⭐ EXENCIÓN Guerreros de prohibición de armas
```

**Primer dilema:**
```
Cliente: Minotauro Guerrero (con Pase VIP)
Regla: Prohibido Minotauros
Pase VIP: Exime de TODAS las reglas
→ ¿Confías en el Pase VIP?
```

---

### Late Game (Día 61+)

**Objetivo:** Maestría bajo presión extrema

**Complejidad:**
- 7-10+ reglas activas simultáneamente
- TODOS los tipos de reglas
- Reglas cambian DIARIAMENTE
- Contradicciones frecuentes (dilemas morales)
- Emergencias aleatorias

**Ejemplo típico Día 80:**
```
1. ✅ OBLIGATORIO verificar edad
2. ⛔ PROHIBIDO servir a Minotauros
3. ✅ OBLIGATORIO Licencia Magia para magos
4. ✅ OBLIGATORIO Certificado Pureza para Paladines
5. ✅ OBLIGATORIO Permiso Entrada para razas exóticas
6. 🕐 TOQUE QUEDA 21:00 razas exóticas
7. 🕐 LÍMITE 2 bebidas alcohólicas por cliente
8. ⭐ EXENCIÓN Guerreros de toque de queda
9. 💰 BONIFICACIÓN +30% bebidas enanas (Festival)
10. ⛔ PROHIBIDO entrada a Gremio de Ladrones
```

**Dilema complejo:**
```
Cliente: Minotauro Guerrero, 22:30 (pasado toque de queda)
Regla 2: Prohibido Minotauros
Regla 6: Toque de queda 21:00 razas exóticas (Minotauro es exótico)
Regla 8: EXENCIÓN Guerreros de toque de queda

Interpretación:
- ¿Exención de toque de queda también exime prohibición general?
- ¿O solo exime el toque de queda pero prohibición sigue?

Correcto: Exención solo aplica a toque de queda
→ Minotauro SIGUE PROHIBIDO (Regla 2)
→ Debes rechazar
```

---

## 🔄 SISTEMA DE CAMBIOS

### Frecuencia de Cambios

**Early Game:**
- Nuevas reglas cada 3-5 días
- 1-2 reglas cambian, resto permanece

**Mid Game:**
- Nuevas reglas cada 1-2 días
- 2-3 reglas cambian

**Late Game:**
- Nuevas reglas CADA DÍA
- 3-5 reglas cambian diariamente
- Algunas reglas permanentes (semanas/meses)

---

### Tipos de Cambios

**Tipo A: Adición**
- Nueva regla se AÑADE a las existentes
- Complejidad aumenta

```
Día 20:
1. Verificar edad
2. Prohibido Minotauros

Día 21:
1. Verificar edad (permanece)
2. Prohibido Minotauros (permanece)
3. NUEVO: Obligatorio Licencia de Magia
```

---

**Tipo B: Sustitución**
- Regla antigua se REEMPLAZA por nueva
- Complejidad constante

```
Día 20:
1. Prohibido Minotauros

Día 21:
1. Prohibido Dracónidos (sustituye anterior)
```

---

**Tipo C: Eliminación**
- Regla antigua se ELIMINA
- Complejidad disminuye (raro)

```
Día 20:
1. Verificar edad
2. Prohibido Minotauros

Día 21:
1. Verificar edad (permanece)
(Prohibición Minotauros eliminada)
```

---

**Tipo D: Modificación**
- Regla existente se MODIFICA levemente
- Fácil de confundir con original

```
Día 20:
Toque de queda 22:00 para razas exóticas

Día 21:
Toque de queda 21:00 para razas exóticas
(⚠️ Cambió de 22:00 a 21:00 - fácil de perder)
```

---

### Duración de Reglas

**Efímeras (1 día):**
- Mayoría de prohibiciones temporales
- "Prohibido Minotauros hoy"

**Cortas (3-7 días):**
- Regulaciones menores
- "Toque de queda durante festival"

**Medianas (1-4 semanas):**
- Campañas de seguridad
- "Obligatorio Certificado Pureza este mes"

**Largas (permanentes):**
- Reglas básicas
- "Siempre verificar edad legal"

**Emergencias (hasta que se levante):**
- Crisis
- "Cuarentena hasta nuevo aviso"

---

## ⚖️ CONFLICTOS Y CONTRADICCIONES

### Tipo 1: Regla vs Exención

**Situación:**
```
Regla A: "PROHIBIDO armas en el local"
Regla B: "EXENCIÓN Guerreros pueden portar armas"
```

**Cliente:** Guerrero con espada

**Resolución:**
- Exención ANULA prohibición general para grupo específico
- Cliente PUEDE entrar con arma ✓

---

### Tipo 2: Prohibición vs Pase VIP

**Situación:**
```
Regla: "PROHIBIDO servir a Minotauros"
Cliente: Minotauro con Pase VIP
```

**Resolución:**
- Pase VIP exime de TODAS las reglas
- Cliente PUEDE ser servido ✓
- PERO si Pase VIP es falso → Traición (multa 1000c + cierre)

---

### Tipo 3: Reglas Contradictorias Aparentes

**Situación:**
```
Regla A: "PROHIBIDO bebidas alcohólicas a Clérigos"
Regla B: "OBLIGATORIO servir a miembros del Templo de la Luz"
Cliente: Clérigo del Templo de la Luz, pide cerveza
```

**Resolución:**
- Regla A aplica al TIPO de bebida
- Regla B aplica a ENTRADA/SERVICIO general
- Solución: Servir bebida NO alcohólica ✓
- Si cliente insiste en alcohol → Rechazar pedido específico

---

### Tipo 4: Emergencia vs Reglas Normales

**Situación:**
```
Regla normal: "Exención Guardia de toque de queda"
EMERGENCIA: "Estado de sitio - TODOS fuera a las 18:00"
Cliente: Guardia a las 19:00
```

**Resolución:**
- Emergencia ANULA todas las reglas normales (incluida Exención)
- Cliente debe ser rechazado ❌

---

## 🎲 GENERACIÓN DINÁMICA DE REGLAS

### Factores que Influyen

**1. Eventos Narrativos:**
- Guerra con Minotauros → "Prohibido Minotauros"
- Festival Élfico → "Bonificación +20% bebidas élficas"
- Ataque terrorista → "Emergencia: Toque de queda 18:00"

**2. Reputación con Facciones:**
- Alta reputación Guardia → Menos inspecciones, reglas más laxas
- Baja reputación Consejo → Reglas más estrictas, multas aumentadas

**3. Fase del Juego:**
- Early: Pocas reglas, simples
- Mid: Reglas moderadas, algunas contradicciones
- Late: Muchas reglas, contradicciones frecuentes

**4. Aleatoriedad Controlada:**
- 30% de reglas son aleatorias (variedad)
- 70% de reglas siguen narrativa lógica

---

### Pool de Reglas Posibles

**Prohibiciones (20 variantes):**
1. Prohibido [raza específica]
2. Prohibido [clase específica]
3. Prohibido [facción específica]
4. Prohibido armas
5. Prohibido bebidas alcohólicas
6. Prohibido bebidas mágicas
7. Prohibido entrada menores (edad aumentada)
8. Prohibido música en vivo
9. Prohibido más de X clientes simultáneos
10. Prohibido servicio después de [hora]
... (10 más)

**Obligaciones (15 variantes):**
1. Obligatorio Licencia de Magia
2. Obligatorio Certificado de Pureza
3. Obligatorio Permiso de Entrada
4. Obligatorio Certificado de Facción
5. Obligatorio Permiso de Armas
6. Obligatorio verificar ID no vencida
7. Obligatorio registrar nombre de cada cliente
8. Obligatorio reportar comportamiento sospechoso
9. Obligatorio usar Luz UV en todos los documentos
10. Obligatorio verificar Órdenes de Detención
... (5 más)

**Restricciones (10 variantes):**
1. Toque de queda [hora] para [grupo]
2. Límite bebidas alcohólicas por cliente
3. Límite clientes simultáneos
4. Prohibido música después de [hora]
5. Obligatorio espacio entre clientes (distanciamiento)
6. Máximo [tiempo] por cliente
7. Prohibido servicios para llevar
8. Obligatorio mascarillas (pandemia)
9. Prohibido reuniones de más de X personas
10. Horario reducido (cierre temprano)

**Bonificaciones (8 variantes):**
1. +X% precio en [bebida/categoría]
2. +X monedas por criminal capturado
3. -X% impuestos esta semana
4. -X% renovación licencias
5. +X reputación por comportamiento ejemplar
6. Subsidio gubernamental +X monedas/día
7. Descuento en compra de [bebida]
8. Recompensa por servir a [facción específica]

---

## 📊 IMPACTO EN GAMEPLAY

### Presión Cognitiva

**Jugador debe:**
1. **Leer** Libro de Reglas cada mañana (6:00)
2. **Memorizar** 1-10 reglas activas
3. **Consultar** constantemente durante el día
4. **Aplicar** reglas a cada cliente
5. **Detectar** excepciones y exenciones
6. **Resolver** contradicciones

**Tensión:**
- Fila de clientes esperando
- Algunos se impacientan si tardas mucho
- Presión por rapidez VS precisión

---

### Estrategias del Jugador

**Estrategia 1: Memorización**
- Leer Libro al inicio del día
- Memorizar reglas más importantes
- Solo consultar para confirmar

**Ventaja:** Rapidez
**Desventaja:** Puedes olvidar regla y cometer error

---

**Estrategia 2: Consulta Constante**
- Tener Libro siempre visible
- Consultar para CADA cliente
- Verificar reglas una por una

**Ventaja:** Precisión máxima
**Desventaja:** Lentitud, clientes impacientes, menos ganancia

---

**Estrategia 3: Balance**
- Memorizar reglas críticas (prohibiciones)
- Consultar reglas complejas (exenciones)
- Experiencia desarrolla intuición

**Ventaja:** Óptimo
**Desventaja:** Requiere experiencia

---

### Integración con Otros Sistemas

**Con Documentos:**
- Reglas determinan QUÉ documentos verificar
- "Obligatorio Licencia de Magia" → Debes pedir documento

**Con Bebidas:**
- Reglas pueden prohibir categorías de bebidas
- "Prohibido bebidas alcohólicas a Clérigos"
- Bonificaciones afectan precios

**Con Facciones:**
- Reglas reflejan tensiones entre facciones
- "Prohibido Gremio de Ladrones" = Conflicto con Guardia
- Exenciones favorecen facciones poderosas

**Con Eventos:**
- Eventos generan nuevas reglas
- "Festival Élfico" → "Bonificación bebidas élficas"
- "Guerra" → "Prohibido enemigos"

**Con Economía:**
- Bonificaciones aumentan ganancia
- Multas por violaciones reducen ganancia
- Reglas restrictivas reducen clientela

---

## 🎯 OBJETIVOS DE DISEÑO

1. **Tensión constante:** "¿Recordé todas las reglas?"
2. **Adaptabilidad:** Jugador debe ser flexible
3. **Complejidad progresiva:** Dificultad aumenta naturalmente
4. **Dilemas reales:** Contradicciones crean decisiones difíciles
5. **Integración profunda:** Afecta TODOS los sistemas
6. **Papers Please authenticity:** Sensación idéntica al original

---

## 📂 ESTRUCTURA DE ARCHIVOS

- `README.md` ← Estás aquí (overview general)
- `tipos-reglas.md` - Catálogo completo de 60+ reglas posibles
- `generacion-dinamica.md` - Sistema de generación procedural
- `conflictos-resoluciones.md` - Guía para resolver contradicciones
- `ejemplos-dias.md` - 90 días de ejemplo con reglas progresivas

---

**Sistema de Libro de Reglas:** Core mechanic que cambia el juego cada día, inspirado directamente en Papers, Please.
