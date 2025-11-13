# 🎭 Sistema de Falsificaciones

Este documento define los tipos de falsificaciones, cómo se crean, cómo detectarlas y quién las usa.

---

## 📊 NIVELES DE FALSIFICACIÓN

### Nivel 1: BURDA (10% de falsificaciones)

**Creador:** Criminales amateur, pobres desesperados

**Características:**
- Obviamente falsa
- Papel de mala calidad (manchado, arrugado)
- Sello borroso o dibujado a mano
- Errores de ortografía
- Retrato claramente diferente

**Detectable con:**
- ✓ Inspección visual básica (sin herramientas)
- ✓ Jugador principiante puede detectar

**Ejemplo visual:**
```
╔══════════════════════════════════════════╗
║  REENO DE CRUZE - IDENTIFICASION        ║  ← Errores ortográficos
║                                          ║
║  ┌──────────┐                            ║
║  │  RETRATO │  NOMBRE: Juan Peres        ║  ← Nombre mal escrito
║  │ BORROSO  │  RASA: Umano               ║  ← "Rasa" en vez de "Raza"
║  └──────────┘  EDAD: 17 años (MENOR!)   ║
║                                          ║
║  FECHA: 32/15/1225 ← Fecha imposible    ║
║                                          ║
║  [SELLO MAL DIBUJADO]  Sin firma        ║  ← Sello obviamente falso
╚══════════════════════════════════════════╝
```

**Razones de uso:**
- No tienen dinero para falsificación mejor
- Urgencia (necesitan documento YA)
- Esperan que tabernero no revise

---

### Nivel 2: MEDIANA (40% de falsificaciones)

**Creador:** Artífices, falsificadores profesionales básicos

**Características:**
- Visualmente aceptable
- Papel de calidad media
- Sello impreso (no dibujado) pero incorrecto
- Sin errores ortográficos
- Retrato coincide (documento robado o foto correcta)

**Detectable con:**
- ⚠️ Inspección cuidadosa
- ✓ Comparación con catálogo de sellos
- ✓ Verificación cruzada entre documentos

**Errores comunes:**

**Error 1: Sello incorrecto**
```
Documento dice: "Guardia Real de Cruce"
Sello muestra: Símbolo de "Guardia Real de Ciudad Vecina"
→ ❌ Autoridad y sello no coinciden
```

**Error 2: Fechas inconsistentes**
```
ID: Edad 25 años, nacimiento 15/3/1200
Permiso de Armas: Emitido 10/1/1220, edad del portador 20 años
Fecha actual: 15/6/1225

Matemática:
Si nació en 1200, en 1220 tendría 20 años ✓
Si nació en 1200, en 1225 tendría 25 años ✓
→ PERO si revisas bien...

Permiso dice emitido hace 5 años (1220)
Cliente tenía 20 años entonces
Ahora debería tener 25
→ ✓ Parece correcto

PERO documento falso olvidó actualizar foto
Retrato en Permiso: Cliente de 20 años (joven)
Retrato en ID: Cliente de 25 años (más maduro)
→ ❌ Retratos no coinciden en edad
```

**Error 3: Número de serie incorrecto**
```
Autoridad emisora: "Consejo de Bosque Verde" (élfico)
Número de serie: CR-1225-0543
→ CR = Cruce (humano)
→ ❌ Debería ser BV-1225-XXXX
```

---

### Nivel 3: AVANZADA (35% de falsificaciones)

**Creador:** Duendes con habilidad de falsificación, magos renegados

**Características:**
- Visualmente casi perfecta
- Papel de calidad alta
- Sello correcto (copiado perfectamente)
- Toda la información coherente
- Marca UV ausente o incorrecta

**Detectable con:**
- ❌ Inspección visual NO detecta
- ✓ Luz UV revela ausencia de marca de seguridad
- ✓ Verificación lógica profunda (restricciones raza-clase)
- ✓ Escáner de magia (detecta aura de ilusión)

**Errores sutiles:**

**Error 1: Falta marca UV**
```
Visualmente: Documento perfecto ✓
Luz UV: No brilla
Documento real: Debería brillar con marca de seguridad
→ ❌ Falsificación avanzada
```

**Error 2: Restricción raza-clase imposible**
```
ID perfecta: "Thorin, Enano, 50 años, Clérigo"
Visualmente: Todo perfecto ✓
Sello: Correcto ✓
Fechas: Coherentes ✓

PERO:
Enano + Clérigo = ❌ IMPOSIBLE (Enanos no creen en deidades)
→ Falsificador no conocía restricciones de lore
```

**Error 3: Información demasiado perfecta**
```
Pícaro presenta documentos
Todo es perfecto: Sellos ✓ Fechas ✓ Marcas UV ✓

Pero...
Pícaros tienen 50% probabilidad de documentos falsos
Documentos "perfectos" son sospechosos en Pícaro
→ ⚠️ Paradoja: ¿Demasiado perfecto para ser real?
```

---

### Nivel 4: MAESTRA (15% de falsificaciones)

**Creador:** Duendes maestros, magos ilusionistas expertos

**Características:**
- PERFECTA en todos los aspectos visuales
- Papel idéntico al original
- Sello perfecto
- Marca UV correcta (falsificada mágicamente)
- Toda información coherente

**Detectable con:**
- ❌ Inspección visual NO detecta
- ❌ Luz UV NO detecta (marca falsificada)
- ⚠️ Escáner de magia detecta (aura mágica residual)
- ✓ Solo detectable por: comportamiento del cliente, contexto narrativo

**Detección por comportamiento:**

**Señales del cliente:**
- Nerviosismo al ser interrogado
- Propensión a mentir activada (Duende 9/10)
- Historia no cuadra con documentos

**Ejemplo:**
```
Duende Pícaro presenta ID perfecta:
- Visual: Perfecto ✓
- Sello: Perfecto ✓
- UV: Marca presente ✓
- Escáner magia: Aura de ilusión detectada ❌

Cliente interrogado:
Jugador: "¿Dónde naciste?"
Cliente (Propensión mentir 9/10): "Eh... en Cruce... no, en Bosque Verde... espera..."
→ Historia inconsistente, nervioso
→ FALSIFICACIÓN CONFIRMADA
```

---

## 🎭 TIPOS DE FALSIFICACIÓN

### Tipo A: Documento Completamente Falso

**Descripción:** Creado desde cero, 100% falso

**Creación:**
- Artífice imprime documento en papel falso
- Duende usa magia de ilusión para crear
- Mago copía documento existente con magia

**Uso común:** Menores de edad, criminales sin identidad

**Detección:**
- Sello incorrecto (más común)
- Número de serie falso
- Autoridad emisora inexistente

---

### Tipo B: Documento Robado

**Descripción:** Documento real, pero pertenece a otra persona

**Creación:**
- Pícaro roba ID de víctima
- Bárbaro toma documento de persona muerta
- Comprado en mercado negro

**Uso común:** Criminales, refugiados

**Detección:**
- **Retrato no coincide con cliente** ← Más obvio
- Edad no coincide con apariencia
- Cliente no puede responder preguntas sobre información en documento

**Ejemplo:**
```
Documento (robado):
Retrato: Humano rubio, ojos azules
Nombre: "Carlos Montero"
Edad: 30 años

Cliente actual:
Humano moreno, ojos marrones, ~25 años

→ ❌ Retrato NO coincide → Documento robado
```

---

### Tipo C: Documento Alterado

**Descripción:** Documento real, pero información alterada

**Creación:**
- Edad cambiada (17 → 27 con edición)
- Nombre alterado
- Clase modificada
- Fecha de vencimiento extendida

**Uso común:** Menores intentando parecer mayores

**Detección:**
- Inspección con lupa revela edición
- Tinta diferente en número alterado
- Papel raspado donde se borró información

**Ejemplo:**
```
ID muestra edad: "27 años"
Lupa revela: Tinta diferente en el "2", papel raspado
Edad original era: "17 años" (menor)
→ ❌ Documento alterado
```

---

### Tipo D: Documento Legítimo pero Obtenido Ilegalmente

**Descripción:** Documento 100% real, emitido por autoridad legítima, pero mediante soborno/corrupción

**Creación:**
- Soborno a oficial del gobierno
- Documentos "perdidos" vendidos en mercado negro
- Autoridad corrupta emite IDs falsas

**Uso común:** Criminales con recursos, espías

**Detección:**
- ❌ IMPOSIBLE de detectar técnicamente (es documento real)
- ✓ Solo detectable por: cliente en orden de detención, comportamiento sospechoso

**Ejemplo:**
```
Criminal peligroso con orden de detención
→ Tiene ID REAL con alias (nombre falso)
→ Documento técnicamente perfecto porque ES real
→ Solo detectas si: comparas con orden de detención y reconoces la cara
```

---

## 🕵️ MÉTODOS DE DETECCIÓN AVANZADOS

### Método 1: Análisis de Consistencia Temporal

**Revisar timeline completa:**

```
ID: Nacimiento 1/1/1200 (Humano)
ID: Emisión 5/6/1220 (cliente tenía 20 años)
Permiso de Armas: Emisión 10/3/1222 (cliente tenía 22 años)
Fecha actual: 15/6/1225 (cliente tiene 25 años)

Verificar matemática:
1200 → 1220: 20 años ✓
1200 → 1222: 22 años ✓
1200 → 1225: 25 años ✓

TODO coherente ✓
```

**Ejemplo con error:**
```
ID: Nacimiento 1/1/1200
ID: Emisión 5/6/1220 (dice que cliente tenía 25 años)
Fecha actual: 1225 (cliente dice tener 25 años)

Matemática:
Si nació en 1200, en 1220 tenía 20 años (no 25) ❌
Si en 1225 tiene 25 años, nació en 1200 ✓
→ INCONSISTENCIA TEMPORAL
→ Documento falso (emisión tiene edad incorrecta)
```

---

### Método 2: Análisis de Probabilidad

**Usar estadísticas de falsificación:**

```
Cliente: Duende Pícaro
Probabilidad base de documento falso:
- Raza Duende: 40%
- Clase Pícaro: 50%
- Combinado: ~70% probabilidad falso

→ Escrutinio EXTRA requerido
→ Usar todas las herramientas disponibles
```

**Cliente: Centauro Paladín**
```
Probabilidad base:
- Raza Centauro: 2%
- Clase Paladín: 1%
- Combinado: ~1.5% probabilidad falso

→ Casi seguro que es real
→ Pero NO confiar ciegamente (1.5% no es 0%)
```

---

### Método 3: Interrogación Estratégica

**Preguntas trampa:**

**Pregunta 1: Detalles específicos**
```
Jugador: "¿Cómo se llama el Capitán de la Guardia que firmó tu permiso?"
Cliente con documento real: "Capitán Roderick" ✓
Cliente con documento falso: "Eh... no recuerdo..." ❌
```

**Pregunta 2: Conocimiento local**
```
Documento dice: "Nacido en Cruce, Distrito Norte"
Jugador: "¿Cuál es la taberna más famosa del Distrito Norte?"
Cliente real: "La Espada Rota" ✓
Cliente con documento robado: "No sé..." ❌
```

**Pregunta 3: Timing**
```
Jugador: "Tu permiso fue emitido el 10/3/1222, ¿qué hacías ese día?"
Cliente nervioso: "Eh... no recuerdo exactamente..."
→ ⚠️ Sospechoso (nadie recuerda día específico, pero nerviosismo indica culpa)
```

---

### Método 4: Uso de Bebidas Especiales

**Poción de Verdad (Tier 5):**

```
Sospechas de cliente
    ↓
Sirves Poción de Verdad (150 cobre)
    ↓
Cliente borracho Nivel 2 → Efecto "Forzar Verdad"
    ↓
Cliente NO PUEDE mentir por 10 minutos
    ↓
Preguntas: "¿Este documento es tuyo?"
    ↓
Cliente forzado: "No, lo robé..." ❌
```

**Inversión vs Beneficio:**
- Costo Poción: 150 cobre
- Recompensa por detectar criminal: 300 cobre
- Ganancia neta: 150 cobre
- Pero arriesgas si cliente era inocente (pérdida 150c)

---

## 📈 PROGRESIÓN DE FALSIFICACIONES

### Early Game (Días 1-14)

**Frecuencia:** 10% clientes tienen documento falso

**Tipos:** Solo Nivel 1 (Burdas)

**Ejemplos:**
- Humano menor (16 años) con ID que dice 18
- Retrato obviamente diferente
- Fecha futura (emitida "mañana")

**Dificultad:** MUY FÁCIL (tutorial)

---

### Mid Game (Días 15-60)

**Frecuencia:** 20-30% clientes tienen documento falso

**Tipos:** Nivel 1-2 (Burdas y Medianas)

**Ejemplos:**
- Sello incorrecto
- Nombres con variaciones entre documentos
- Número de serie incorrecto
- Restricciones raza-clase imposibles (comenzando)

**Dificultad:** MEDIA (requiere atención)

---

### Late Game (Día 61+)

**Frecuencia:** 40-50% clientes tienen documento falso

**Tipos:** Nivel 2-4 (Medianas, Avanzadas, Maestras)

**Ejemplos:**
- Falsificaciones maestras de Duendes
- Documentos robados con retrato casi coincidente
- Restricciones imposibles sutiles
- Documentos legítimos obtenidos ilegalmente

**Dificultad:** ALTA (maestría requerida)

---

## 🎭 FALSIFICADORES POR RAZA/CLASE

### Duende Pícaro

**Probabilidad de falsificación:** 70% (MÁS ALTO)

**Tipo común:** Nivel 3-4 (Avanzada/Maestra)

**Habilidad especial racial:** "Falsificación Maestra"
- Puede crear documentos visualmente perfectos
- Marca UV falsificada con magia
- Solo detectable con Escáner de Magia o inconsistencias lógicas

**Comportamiento:**
- Extremadamente confiado (falsificación es perfecta)
- Propensión a mentir: 9/10 (puede engañar en interrogatorio)
- Si acorralado → Puede admitir y ofrecer soborno

**Estrategia de detección:**
- SIEMPRE usar Escáner de Magia
- Verificar restricciones raza-clase cuidadosamente
- Interrogar con preguntas trampa

---

### Bárbaro (cualquier raza)

**Probabilidad de falsificación:** 15%

**Tipo común:** Nivel 1 (Burda) o Tipo B (Robado)

**Razón:**
- No entienden burocracia
- Prefieren robar documento a falsificar
- Documentos robados de enemigos caídos

**Comportamiento:**
- Directo, no trata de engañar
- Si le señalas error → Puede admitir honestamente
- O puede enfurecer y amenazar (10% probabilidad)

**Estrategia de detección:**
- Verificación visual crítica (retrato vs cliente)
- Documentos robados son obvios (retrato no coincide)

---

### Hechicero

**Probabilidad de falsificación:** 20%

**Tipo común:** Nivel 3 (Avanzada)

**Razón:**
- Muchos no tienen Licencia de Magia legal (magia innata)
- Usan magia para crear ilusiones en documentos

**Comportamiento:**
- Confiado en sus habilidades mágicas
- Si detectado → Puede usar magia defensiva (crear distracción)

**Estrategia de detección:**
- Escáner de Magia esencial
- Verificar que Licencia de Magia sea legítima

---

### Paladín

**Probabilidad de falsificación:** 1% (MÁS BAJO)

**Tipo común:** Ninguno (casi nunca falsifican)

**Razón:**
- Código sagrado prohíbe mentir
- Propensión a mentir: 1/10

**Comportamiento:**
- Si presenta documento falso → Probablemente NO ES PALADÍN
- Impostor usando documentos robados de Paladín real

**Estrategia de detección:**
- Si detectas falsificación en "Paladín" → Llamar Guardia inmediatamente
- Es criminal peligroso haciéndose pasar

---

## 🚨 CASOS ESPECIALES

### Caso 1: Refugiado con Documentos Falsos (Dilema Moral)

**Situación:**
```
Cliente: Familia élfica (madre + hijo)
Documentos: Falsos (Nivel 2, detectables)
Historia: Huyendo de guerra en Bosque Oscuro
Razón falsificación: No tenían tiempo de obtener documentos legales
```

**Opciones:**

**A) Rechazar (siguiendo la ley):**
- Cumples tu deber ✓
- Familia no puede entrar, posiblemente mueran ❌
- Sin consecuencias legales ✓

**B) Servir (ignorando falsificación):**
- Salvas a familia ✓
- Violas la ley ❌
- Riesgo de multa si te descubren (100 monedas) ❌
- +Reputación con facción élfica ✓

**C) Llamar a la Guardia:**
- Cumples protocolo ✓
- Familia arrestada ❌
- Recompensa pequeña (50 monedas) ✓
- -Reputación con facción élfica ❌

**Jugador debe decidir:** ¿Ley vs Moralidad?

---

### Caso 2: Noble con Pase VIP Sospechoso

**Situación:**
```
Cliente: "Duque Alaric"
Documento: Pase VIP (exime de todas las reglas)
Visual: Documento perfecto ✓
Sello Real: Parece legítimo ✓
Comportamiento: Arrogante, exige servicio inmediato
```

**Problema:**
- Si es real → Rechazar = TRAICIÓN (multa 1000 monedas + cierre)
- Si es falso → Servir = TRAICIÓN (multa 1000 monedas + cierre)

**Verificación:**
```
1. ¿Conoces al Duque Alaric de fama/rumor?
   → Consultar "Libro de Nobles" (si lo tienes)

2. Sello Real debe ser PERFECTO
   → Usar Lupa + UV + Escáner

3. Comportamiento:
   → Noble real: Arrogante pero educado
   → Impostor: Nervioso bajo presión

4. Pregunta trampa:
   "Su Excelencia, ¿cómo está Su Majestad el Rey?"
   → Noble real: Conoce estado del Rey
   → Impostor: "Eh... bien, supongo"
```

**Decisión final requiere certeza 99%+**

---

### Caso 3: Guardia Corrupto Extorsiona

**Situación:**
```
Guardabosques presenta documentos con error menor (sello ligeramente borroso)
Rechazas servicio
Cliente se va

Al día siguiente:
Guardia llega: "Ese era mi informante. Lo rechazaste. Multa: 200 monedas"

Pero...
Documento SÍ era sospechoso. ¿Guardia corrupto extorsionando?
```

**Opciones:**

**A) Pagar multa:**
- Evitas confrontación ✓
- Pierdes 200 monedas ❌
- Guardia corrupto seguirá extorsionando ❌

**B) Rechazar pago:**
- Defiendes tu decisión ✓
- Guardia puede cerrar taberna temporalmente ❌
- Posible escalación a conflicto con facción Guardia ❌

**C) Reportar a superior:**
- Expones corrupción ✓
- Riesgo si no tienes pruebas ❌
- Posible recompensa si tenías razón ✓

**Sistema de corrupción:** Algunos NPCs pueden abusar del sistema

---

## 📊 TABLA RESUMEN: Falsificaciones

| Nivel | % de Total | Detectable con | Creador Típico |
|-------|------------|----------------|----------------|
| Burda | 10% | Visual básica | Criminal amateur |
| Mediana | 40% | Catálogo sellos | Artífice |
| Avanzada | 35% | UV + Lógica | Duende hábil |
| Maestra | 15% | Escáner Magia | Duende maestro |

| Raza-Clase | % Falsos | Tipo Común |
|------------|----------|------------|
| Duende Pícaro | 70% | Maestra |
| Pícaro (otro) | 50% | Avanzada |
| Bárbaro | 15% | Burda/Robada |
| Hechicero | 20% | Avanzada |
| Paladín | 1% | Ninguno |
| Humano Plebeyo | 8% | Mediana |

---

## 🎯 OBJETIVOS DE DISEÑO

1. **Variedad:** 4 niveles de dificultad mantienen desafío
2. **Progresión:** Dificultad aumenta con experiencia del jugador
3. **Estrategia:** Múltiples métodos de detección
4. **Dilemas morales:** No siempre blanco/negro
5. **Maestría:** Jugador experto puede detectar 90%+ falsificaciones

---

**Sistema completo de falsificaciones listo para implementación.**
