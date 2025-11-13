# 🎲 Generación Dinámica de Reglas

Este documento define cómo el sistema genera el Libro de Reglas cada día de manera procedural.

---

## 🎯 OBJETIVOS DEL SISTEMA

1. **Variedadsin repetición:** Evitar que dos partidas sean idénticas
2. **Coherencia narrativa:** Reglas deben tener sentido en contexto
3. **Progresión natural:** Complejidad aumenta suavemente
4. **Balance:** No abrumar ni aburrir al jugador
5. **Dilemas interesantes:** Crear situaciones moralmente ambiguas

---

## 📊 ALGORITMO DE GENERACIÓN

### Fase 1: Determinar Número de Reglas

**Fórmula base:**
```
Número de Reglas = MIN(Piso((Día / 7) + 1), 10)
```

**Ejemplos:**
```
Día 1: (1 / 7) + 1 = 1.14 → 1 regla
Día 7: (7 / 7) + 1 = 2 reglas
Día 14: (14 / 7) + 1 = 3 reglas
Día 30: (30 / 7) + 1 = 5.28 → 5 reglas
Día 70: (70 / 7) + 1 = 11 → 10 reglas (máximo)
```

**Modificadores:**
- Evento especial activo: +1-3 reglas
- Alta reputación con Consejo: -1 regla (menos estrictos)
- Baja reputación con Consejo: +2 reglas (más estrictos)
- Emergencia: +3-5 reglas específicas

---

### Fase 2: Seleccionar Tipos de Reglas

**Distribución por fase:**

#### Early Game (Días 1-14)

```
Probabilidades:
- Obligaciones: 80%
- Prohibiciones: 20%
- Restricciones: 0%
- Bonificaciones: 0%
- Exenciones: 0%
- Emergencias: 0%
```

**Razón:** Enseñar mecánicas básicas sin abrumar

**Ejemplo Día 5:**
```
1. ✅ OBLIGATORIO verificar edad legal (80% probabilidad)
```

---

#### Mid Game (Días 15-60)

```
Probabilidades:
- Obligaciones: 40%
- Prohibiciones: 30%
- Restricciones: 20%
- Bonificaciones: 8%
- Exenciones: 2% (aparece con prohibiciones)
- Emergencias: 0%
```

**Razón:** Introducir complejidad y contradicciones

**Ejemplo Día 30:**
```
1. ✅ OBLIGATORIO verificar edad legal (Obligación - permanente)
2. ⛔ PROHIBIDO servir a Minotauros (Prohibición - 30%)
3. 🕐 TOQUE DE QUEDA 21:00 razas exóticas (Restricción - 20%)
4. ⭐ EXENCIÓN Guerreros de toque de queda (2% - aparece porque hay restricción)
5. 💰 BONIFICACIÓN +20% bebidas élficas (8% - Festival)
```

---

#### Late Game (Día 61+)

```
Probabilidades:
- Obligaciones: 30%
- Prohibiciones: 25%
- Restricciones: 20%
- Bonificaciones: 10%
- Exenciones: 10%
- Emergencias: 5%
```

**Razón:** Máxima complejidad, todos los tipos activos

**Ejemplo Día 80:**
```
1. ✅ OBLIGATORIO verificar edad
2. ✅ OBLIGATORIO Licencia Magia para magos
3. ✅ OBLIGATORIO Certificado Pureza para Paladines
4. ⛔ PROHIBIDO servir a Minotauros
5. ⛔ PROHIBIDO Gremio de Ladrones
6. 🕐 TOQUE QUEDA 21:00 razas exóticas
7. 🕐 LÍMITE 2 bebidas alcohólicas por cliente
8. ⭐ EXENCIÓN Guerreros de toque de queda
9. 💰 BONIFICACIÓN +30% bebidas enanas
10. 🚨 EMERGENCIA: Búsqueda activa - Reportar Elfos Noche (5% - aleatorio)
```

---

### Fase 3: Seleccionar Reglas Específicas

**Sistema de pesos:**

Cada regla del catálogo tiene:
1. **Peso base** (1-10)
2. **Modificadores contextuales**
3. **Cooldown** (no puede repetirse inmediatamente)

---

#### Pesos por Contexto

**Eventos activos:**

```
IF Festival Élfico activo:
    Peso("BONIFICACIÓN +20% bebidas élficas") = 100 (garantizado)
    Peso("PROHIBIDO bebidas élficas") = 0 (imposible)
    Peso("OBLIGATORIO verificar Certificado Facción élfica") = 50 (muy probable)

IF Guerra con Minotauros activa:
    Peso("PROHIBIDO Minotauros") = 100 (garantizado)
    Peso("EXENCIÓN Minotauros") = 0 (imposible)
```

---

**Reputación con facciones:**

```
IF Reputación Guardia > 75:
    Peso("OBLIGATORIO cooperar con Guardia") = 2 (menos común)
    Peso("BONIFICACIÓN por criminal capturado") = 10 (más común)

IF Reputación Guardia < 25:
    Peso("OBLIGATORIO cooperar con Guardia") = 20 (muy común)
    Peso("Inspecciones diarias") = 15 (más frecuentes)
```

---

**Aleatoriedad controlada:**

```
30% de las reglas son completamente aleatorias (variedad)
70% de las reglas siguen lógica narrativa
```

**Ejemplo:**
```
Día 45:
- 3 reglas narrativas (Festival Élfico → bebidas élficas, Certificados)
- 2 reglas aleatorias (Prohibido Bárbaros, Límite 2 bebidas)
→ Total: 5 reglas coherentes pero variadas
```

---

#### Sistema de Cooldown

**Reglas no pueden repetirse inmediatamente:**

```
IF "PROHIBIDO Minotauros" activa hoy:
    Cooldown = 3 días
    → No puede volver a aparecer hasta Día+4
```

**Cooldowns por tipo:**
- Prohibiciones específicas: 3-7 días
- Obligaciones: 1-3 días (pueden ser permanentes)
- Restricciones: 2-5 días
- Bonificaciones: 7-14 días (eventos)
- Emergencias: 14-30 días (raro)

**Excepción:**
- Reglas permanentes (verificar edad) no tienen cooldown

---

### Fase 4: Determinar Duración

**Fórmula:**
```
Duración = Random(Duración Mínima, Duración Máxima) × Modificador Evento
```

**Ejemplo:**
```
Regla: "PROHIBIDO Minotauros"
Duración base: 1-7 días
Random: 4 días

IF Guerra con Minotauros activa:
    Modificador = 3x
    Duración final = 4 × 3 = 12 días
```

---

**Tipos de duración:**

**Efímera (1 día):**
- Reglas menores
- Pruebas temporales
- 20% de reglas

**Corta (3-7 días):**
- Mayoría de prohibiciones
- Eventos menores
- 40% de reglas

**Mediana (7-30 días):**
- Obligaciones importantes
- Campañas de seguridad
- 30% de reglas

**Larga (30+ días o permanente):**
- Reglas fundamentales
- Tratados importantes
- 10% de reglas

---

### Fase 5: Añadir Exenciones

**Lógica:**
```
IF regla es Prohibición o Restricción:
    Probabilidad Exención = 15%
    IF Exención generada:
        Seleccionar grupo lógico para eximir
```

**Ejemplo:**
```
Regla: "PROHIBIDO armas en el local"
→ 15% probabilidad de exención
→ Random: Sí
→ Grupo lógico: Guerreros (necesitan armas profesionalmente)
→ Regla adicional: "EXENCIÓN Guerreros de prohibición de armas"
```

**Grupos típicos para exenciones:**
- Guerreros (armas)
- Guardia Real (todo)
- Nobles (privilegios)
- Diplomáticos (inmunidad)
- Paladines (confianza moral)

---

### Fase 6: Añadir Emergencias

**Probabilidad:**
```
Early Game: 0%
Mid Game: 1%
Late Game: 5%
```

**Trigger:**
```
IF Random(1-100) <= Probabilidad:
    Generar Emergencia
    → ANULA 50% de reglas normales
    → Añade 3-5 reglas de emergencia específicas
```

**Ejemplo:**
```
Día 85:
Reglas normales generadas: 10 reglas
Random emergencia: 3 (< 5%)
→ EMERGENCIA: Estado de Sitio

Efecto:
→ 5 reglas normales ANULADAS
→ 3 reglas de emergencia AÑADIDAS:
   1. 🚨 TODOS fuera a las 18:00
   2. 🚨 Prohibidas reuniones +3 personas
   3. 🚨 Reportar comportamiento sospechoso obligatorio

→ Total final: 5 normales + 3 emergencia = 8 reglas activas
```

---

## 🔄 PERSISTENCIA Y CAMBIOS

### Reglas Permanentes

**Lista de reglas que SIEMPRE están activas:**

```
1. OBLIGATORIO verificar edad legal según raza
2. OBLIGATORIO permitir inspecciones sin aviso
3. OBLIGATORIO pagar impuestos semanales
4. PROHIBIDO servir Vino de Sangre (ilegal absoluto)
5. PROHIBIDO servir Bebida Corrupta (ilegal absoluto)
6. PROHIBIDO servir a miembros del Culto de la Sombra
```

**Estas NO se generan, están hardcoded en el sistema.**

---

### Reglas que Expiran

**Cada día a las 6:00 AM:**

```
FOR cada regla activa:
    IF regla.duración_restante > 0:
        regla.duración_restante -= 1
    ELSE:
        Eliminar regla de lista activa
        Añadir regla a cooldown (no puede repetirse aún)
```

---

### Generación de Nuevas Reglas

**Cada día a las 6:00 AM:**

```
1. Eliminar reglas expiradas
2. Contar reglas activas restantes
3. Calcular cuántas reglas nuevas generar:
   Nuevas = (Reglas Objetivo - Reglas Actuales)
4. Generar nuevas reglas siguiendo Fases 1-6
5. Consolidar Libro de Reglas final
6. Presentar al jugador
```

**Ejemplo:**

```
Día 30 (fin):
Reglas activas: 5
- OBLIGATORIO verificar edad (permanente)
- PROHIBIDO Minotauros (expira mañana)
- TOQUE QUEDA 21:00 (3 días restantes)
- BONIFICACIÓN +20% bebidas élficas (expira mañana)
- OBLIGATORIO Licencia Magia (14 días restantes)

Día 31 (6:00 AM):
→ Eliminar "PROHIBIDO Minotauros" (expiró)
→ Eliminar "BONIFICACIÓN +20% bebidas élficas" (expiró)
→ Reglas activas: 3

Objetivo para Día 31: (31/7) + 1 = 5.42 → 5 reglas
Generar: 5 - 3 = 2 reglas nuevas

→ Genera "PROHIBIDO Hechiceros" (7 días)
→ Genera "OBLIGATORIO Certificado Pureza Paladines" (14 días)

Libro de Reglas Día 31:
1. OBLIGATORIO verificar edad (permanente)
2. TOQUE QUEDA 21:00 (2 días restantes)
3. OBLIGATORIO Licencia Magia (13 días restantes)
4. PROHIBIDO Hechiceros (7 días nuevos) ← NUEVA
5. OBLIGATORIO Certificado Pureza Paladines (14 días nuevos) ← NUEVA
```

---

## 🎭 INTEGRACIÓN CON EVENTOS

### Eventos Generan Reglas Específicas

**Tipos de eventos y reglas asociadas:**

**Festival Élfico:**
```
Reglas generadas automáticamente:
1. BONIFICACIÓN +20% precio bebidas élficas (garantizado)
2. OBLIGATORIO verificar Certificado Facción élfica (50% probabilidad)
3. PROHIBIDO discriminación contra Elfos (80% probabilidad)
4. Mayor frecuencia de clientes élficos (+200%)

Duración: 7-14 días
```

---

**Guerra con Minotauros:**
```
Reglas generadas automáticamente:
1. PROHIBIDO servir a Minotauros (garantizado, duración guerra completa)
2. OBLIGATORIO reportar avistamientos de Minotauros (100%)
3. BONIFICACIÓN +100c por Minotauro capturado (80%)
4. EMERGENCIA posible si guerra escala (10% por día)

Duración: 14-60 días (hasta fin de guerra)
```

---

**Pandemia en la Ciudad:**
```
Reglas generadas automáticamente:
1. EMERGENCIA: Cuarentena - Solo residentes (garantizado)
2. OBLIGATORIO distancia 2m entre clientes (100%)
3. OBLIGATORIO mascarillas para todos (100%)
4. RESTRICCIÓN: Máximo 5 clientes simultáneos (80%)
5. PROHIBIDO bebidas importadas (50% - si brote externo)

Duración: 14-90 días (hasta cura/control)
```

---

**Operación Limpieza (Guardia):**
```
Reglas generadas automáticamente:
1. BONIFICACIÓN +50c por criminal entregado (garantizado)
2. OBLIGATORIO revisar Órdenes Detención diariamente (100%)
3. PROHIBIDO Gremio de Ladrones (80%)
4. Inspecciones más frecuentes (+100%)

Duración: 14-30 días
```

---

**Celebración Real:**
```
Reglas generadas automáticamente:
1. DESCUENTO -20% impuestos (garantizado)
2. BONIFICACIÓN +50% propinas (80%)
3. PROHIBIDO rechazar nobles (100%)
4. BONIFICACIÓN capacidad +50% (50%)

Duración: 1-3 días
```

---

### Eventos Modifican Reglas Existentes

**Ejemplos:**

**Si "PROHIBIDO Minotauros" está activa Y Festival de Paz comienza:**
```
→ Regla SE ANULA automáticamente
→ Reemplazada por "EXENCIÓN Minotauros temporalmente"
→ Duración: Durante festival (3-7 días)
```

**Si "TOQUE QUEDA 22:00" está activa Y Ataque Terrorista ocurre:**
```
→ Regla SE MODIFICA a "EMERGENCIA: TOQUE QUEDA 18:00"
→ Más estricta, ANULA exenciones previas
→ Duración: Hasta fin de emergencia
```

---

## 📈 PROGRESIÓN DE COMPLEJIDAD

### Complejidad Medida

**Fórmula de Complejidad:**
```
Complejidad = (Nº Reglas × 10) + (Nº Exenciones × 20) + (Nº Contradicciones × 30)
```

**Ejemplos:**

**Día 5:**
```
1 regla + 0 exenciones + 0 contradicciones
= (1 × 10) + (0 × 20) + (0 × 30)
= 10 puntos de complejidad
```

**Día 30:**
```
5 reglas + 1 exención + 0 contradicciones
= (5 × 10) + (1 × 20) + (0 × 30)
= 70 puntos de complejidad
```

**Día 80:**
```
10 reglas + 3 exenciones + 2 contradicciones
= (10 × 10) + (3 × 20) + (2 × 30)
= 220 puntos de complejidad
```

---

### Curva de Complejidad Objetivo

```
Día 1-14: 10-50 puntos (Tutorial)
Día 15-30: 50-100 puntos (Aprendizaje)
Día 31-60: 100-150 puntos (Competencia)
Día 61-90: 150-250 puntos (Maestría)
Día 91+: 200-300+ puntos (Experto)
```

**Sistema ajusta automáticamente:**
- Si complejidad < objetivo: Genera reglas adicionales
- Si complejidad > objetivo: Reduce generación siguiente día

---

## 🎯 CALIDAD DE REGLAS

### Evitar Reglas Aburridas

**Reglas NO DEBEN:**
1. Ser idénticas a día anterior (cooldown)
2. Ser imposibles de cumplir (contradicción total)
3. No afectar gameplay significativamente
4. Ser tan comunes que jugador las ignora

**Filtros de calidad:**

```
IF regla_generada == regla_ayer:
    Rechazar, generar otra

IF regla_generada hace imposible jugar:
    Rechazar (ej: "PROHIBIDO servir a TODOS")

IF regla_generada afecta <5% de clientes:
    Reducir peso para próxima vez

IF regla se repite >5 veces en 14 días:
    Cooldown extendido a 14 días
```

---

### Fomentar Dilemas Interesantes

**Sistema busca activamente crear situaciones morales:**

**Generación de contradicciones:**
```
IF regla "PROHIBIDO Minotauros" activa:
    Aumentar peso de evento "Refugiado Minotauro"
    → Cliente Minotauro con historia trágica aparece
    → Jugador decide: ¿Ley o compasión?
```

**Generación de tentaciones:**
```
IF regla "PROHIBIDO Gremio Ladrones" activa:
    Aumentar peso de cliente "Ladrón con soborno"
    → Cliente ofrece 500c para ignorar regla
    → Jugador decide: ¿Dinero o legalidad?
```

**Generación de presión:**
```
IF reglas activas >= 8:
    Aumentar velocidad de llegada de clientes
    → Fila larga, clientes impacientes
    → Jugador decide: ¿Rapidez o precisión?
```

---

## 🛠️ PARÁMETROS DE TUNNING

**Variables ajustables para balance:**

```
MAX_REGLAS_SIMULTANEAS = 10
COMPLEJIDAD_MULTIPLIER = 1.0 (ajustar dificultad global)
PROBABILIDAD_EMERGENCIA_LATE = 5%
COOLDOWN_REGLAS_COMUNES = 3 días
COOLDOWN_REGLAS_RARAS = 7 días
PESO_NARRATIVA = 70% (vs 30% aleatorio)
DURACION_PROMEDIO_REGLA = 7 días
PROBABILIDAD_EXENCION = 15%
PROBABILIDAD_CONTRADICCION_INTENCIONAL = 10%
```

**Estas pueden ajustarse post-testeo para mejorar experiencia.**

---

## 📊 TABLA RESUMEN: Generación

| Fase Juego | Nº Reglas | Tipos Activos | Complejidad | Emergencias |
|------------|-----------|---------------|-------------|-------------|
| Early (1-14) | 1-3 | Obligaciones | 10-50 | 0% |
| Mid (15-60) | 3-5 | Oblig + Prohib + Restr | 50-150 | 1% |
| Late (61+) | 7-10+ | TODOS | 150-300+ | 5% |

| Tipo Regla | Peso Early | Peso Mid | Peso Late |
|------------|-----------|----------|-----------|
| Obligación | 80% | 40% | 30% |
| Prohibición | 20% | 30% | 25% |
| Restricción | 0% | 20% | 20% |
| Bonificación | 0% | 8% | 10% |
| Exención | 0% | 2% | 10% |
| Emergencia | 0% | 1% | 5% |

---

## 🎯 OBJETIVOS DE DISEÑO CUMPLIDOS

1. ✅ **Variedad:** 180 reglas × combinaciones = miles de configuraciones únicas
2. ✅ **Coherencia:** 70% reglas narrativas, 30% aleatorias
3. ✅ **Progresión:** Complejidad aumenta suavemente de 10 a 300 puntos
4. ✅ **Balance:** Cooldowns y pesos previenen repetición
5. ✅ **Dilemas:** Sistema genera contradicciones y tentaciones intencionalmente

---

**Sistema de generación dinámico completo, listo para implementación procedural.**
