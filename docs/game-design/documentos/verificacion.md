# 🔍 Guía de Verificación de Documentos

Este documento explica paso a paso cómo verificar documentos en el juego.

---

## 📋 PROTOCOLO DE VERIFICACIÓN (5 PASOS)

### Paso 1: VERIFICACIÓN VISUAL

**Comparar Retrato vs Cliente**

```
Mira el retrato en la ID
    ↓
Mira al cliente frente a ti
    ↓
¿Coinciden visualmente?
    ├─ SÍ → Continuar Paso 2
    └─ NO → FALSIFICACIÓN CONFIRMADA
```

**Elementos a comparar:**
- Raza (Humano vs Elfo vs Enano es obvio)
- Color de piel
- Rasgos distintivos (cuernos, alas, barba)
- Género

**⚠️ TRAMPA: Glamour Élfico**
- Elfos jóvenes usan glamour para aparentar más edad
- Retrato muestra versión glamurosa (más vieja)
- Cliente real aparenta más joven
- Solución: Cerveza de Glamour rompe ilusión

**Ejemplo:**
```
Retrato ID: Elfo adulto (~30 años apariencia humana)
Cliente real: Elfo adulto (~30 años apariencia humana)
ID dice: 150 años (legal)
→ ✓ Parece OK

PERO sirves Cerveza de Glamour
→ Glamour cae
→ Cliente real: Elfo adolescente (~18 años apariencia humana)
→ Edad real: ~75 años (menor de 80)
→ ❌ MENOR, ID FALSA
```

---

### Paso 2: VERIFICACIÓN DE DATOS BÁSICOS

**Checklist rápido:**

```
[ ] Nombre presente
[ ] Raza especificada
[ ] Edad especificada
[ ] Fecha de emisión presente
[ ] Autoridad emisora presente
[ ] Firma presente
[ ] Sello presente
```

**Si falta CUALQUIER elemento → Documento incompleto/falso**

---

#### 2.1 Verificar Edad Legal

**Tabla de Edades Mínimas:**

| Raza | Edad Mínima Legal | Razón |
|------|-------------------|-------|
| Humano | 18 años | Adultez humana |
| Enano | 30 años | Enanos maduran lento |
| Elfo Bosque | 80 años | Elfos viven siglos |
| Elfo Noche | 80 años | Elfos viven siglos |
| Duende | 25 años | Madurez duende |
| Minotauro | 15 años | Maduran rápido |
| Dracónido | 20 años | Madurez dracónica |
| Centauro | 20 años | Madurez centauro |

**Proceso:**
```
Leer raza en ID
    ↓
Leer edad en ID
    ↓
Comparar con tabla
    ├─ Edad >= Mínima → ✓ Legal
    └─ Edad < Mínima → ❌ MENOR
```

**Ejemplo:**
```
Raza: Elfo del Bosque
Edad: 75 años
Mínimo: 80 años
→ ❌ MENOR (5 años por debajo)
```

---

#### 2.2 Verificar Fechas

**Fecha de Emisión:**

```
Fecha emisión: 10/6/1225
Fecha actual: 15/6/1225
→ ✓ OK (emitida hace 5 días)

Fecha emisión: 20/6/1225
Fecha actual: 15/6/1225
→ ❌ FUTURA (¿emitida en 5 días?)
```

**Fecha de Vencimiento:**

```
ID emitida: 10/6/1215 (hace 10 años)
Vencimiento: 10/6/1225
Fecha actual: 15/6/1225
→ ❌ VENCIDA (5 días pasados)
```

**Antigüedad Máxima (ID):**
- IDs vencen cada 10 años
- Si emisión hace más de 10 años → Vencida

---

#### 2.3 Verificar Autoridad Emisora

**Autoridades Legítimas:**

**Para IDs:**
- Consejo Municipal de Cruce
- Consejo de Ancianos de Bosque Verde (Elfos)
- Montaña de Hierro - Registro Enano
- Clan Minotauro del Sur
- Conclave de Dracónidos

**Para Permisos de Armas:**
- Guardia Real
- Capitán de la Guardia
- Consejo Militar

**Para Licencias de Magia:**
- Consejo de Magos
- Gran Archimago
- Academia Arcana

**Verificación:**
```
ID dice emitida por: "Consejo Municipal de Cruce"
→ Buscar en tu "Catálogo de Autoridades"
→ ✓ Encontrado → Legítimo
→ ❌ No encontrado → Falso

ID dice emitida por: "Consejo de Ancianos de Ciudad Inexistente"
→ ❌ Autoridad falsa
```

---

### Paso 3: VERIFICACIÓN DE AUTENTICIDAD

#### 3.1 Verificar Sello Oficial

**Proceso:**

```
1. Identificar autoridad emisora en documento
2. Abrir "Catálogo de Sellos Oficiales" (en taberna)
3. Buscar sello de esa autoridad
4. Comparar visualmente
    ├─ Coincide perfectamente → ✓ Auténtico
    ├─ Similar pero diferencias → ⚠️ Sospechoso
    └─ Completamente diferente → ❌ Falso
```

**Detalles a comparar:**
- Forma del sello (circular, cuadrado, escudo)
- Símbolo central (corona, espada, libro)
- Texto alrededor del sello
- Detalles ornamentales

**Ejemplo:**

```
Documento: Sello "Guardia Real"
Catálogo muestra:
  - Forma: Circular
  - Centro: Espada cruzada con escudo
  - Texto: "GUARDIA REAL DE CRUCE"
  - Bordes: Ornamentos florales

Documento del cliente muestra:
  - Forma: Circular ✓
  - Centro: Espada cruzada con escudo ✓
  - Texto: "GUARDIA REAL DE CRUZE" ❌ (ortografía)
  - Bordes: Sin ornamentos ❌

→ FALSIFICACIÓN (detalles incorrectos)
```

---

#### 3.2 Verificar Calidad del Papel

**Documentos Auténticos:**
- Papel limpio, sin manchas
- Bordes rectos, bien cortados
- Texto nítido, bien impreso
- Sin arrugas o dobleces

**Falsificaciones Baratas:**
- Papel manchado, sucio
- Bordes irregulares
- Texto borroso, mal impreso
- Muchas arrugas

**Falsificaciones Maestras (Duendes):**
- Visualmente PERFECTAS
- Papel de calidad igual
- Indistinguibles visualmente
- Solo detectables por inconsistencias lógicas

**Indicador visual en juego:**
```
[Documento Auténtico] - Fondo blanco limpio
[Falsificación Barata] - Fondo amarillento con manchas
[Falsificación Maestra] - Fondo blanco limpio (requiere otros métodos)
```

---

#### 3.3 Usar Herramientas de Verificación

**LUPA (gratis, inicial):**

Uso:
```
Click derecho en documento → "Usar Lupa"
→ Zoom 4x en sello
→ Revela microimpresiones
```

Detecta:
- Detalles del sello
- Calidad de impresión
- Marcas de seguridad visibles

**LUZ UV (50 monedas, upgrade):**

Uso:
```
Click derecho en documento → "Luz UV"
→ Documento brilla bajo luz especial
```

Detecta:
- Marcas de seguridad UV en documentos reales
- Licencias de Magia tienen marca mágica que brilla púrpura
- Falsificaciones: no brillan o brillan color incorrecto

**Ejemplo:**
```
Licencia de Magia auténtica + UV = Brilla púrpura con símbolo arcano
Licencia de Magia falsa + UV = No brilla (o brilla azul incorrecto)
```

**ESCÁNER DE MAGIA (200 monedas, upgrade late game):**

Uso:
```
Click derecho en documento → "Escanear Magia"
→ Detecta rastros mágicos
```

Detecta:
- Falsificaciones mágicas (creadas por Duendes con magia)
- Documentos robados (tienen aura residual del dueño original)
- Glamours y ilusiones

**Ejemplo:**
```
ID falsa creada por Duende Hechicero
→ Escáner detecta: "Aura de Ilusión detectada"
→ ❌ Documento mágicamente alterado
```

---

### Paso 4: VERIFICACIÓN CRUZADA (Múltiples Documentos)

**Si cliente presenta 2+ documentos, TODOS deben coincidir**

#### 4.1 Verificar Consistencia de Datos

**Nombre debe coincidir:**

```
ID: "Juan Pérez"
Permiso de Armas: "Juan Pérez"
→ ✓ Coincide

ID: "Juan Pérez"
Permiso de Armas: "Juan Rodriguez"
→ ❌ Inconsistencia
```

**Variaciones menores (pueden ser legítimas):**
```
ID: "Carlos Alberto Montero"
Permiso: "C.A. Montero"
→ ⚠️ Sospechoso pero puede ser legítimo (iniciales)
→ Hacer pregunta al cliente para confirmar
```

---

**Raza debe coincidir:**

```
ID: "Elfo del Bosque"
Licencia de Magia: "Elfo del Bosque"
→ ✓ Coincide

ID: "Humano"
Licencia de Magia: "Elfo"
→ ❌ IMPOSIBLE (raza cambió?)
```

---

**Edad debe coincidir:**

```
ID: 25 años
Permiso de Armas emitido hace 2 años: 23 años en ese momento
Edad actual debería ser: 25 años
→ ✓ Matemática correcta

ID: 25 años
Permiso emitido hace 5 años: 25 años en ese momento
→ ❌ Inconsistencia (debería tener 30 ahora)
```

---

#### 4.2 Verificar Compatibilidad Raza-Clase

**Restricciones imposibles:**

```
ID: "Enano, Mago"
→ ❌ IMPOSIBLE (Enanos no pueden ser Magos)

Licencia de Magia: Portador "Enano"
→ ❌ IMPOSIBLE (Enanos no usan magia)

ID: "Elfo del Bosque, Bárbaro"
→ ❌ IMPOSIBLE (Elfos Bosque no pueden ser Bárbaros)
```

**Tabla de restricciones críticas:**

| Raza | Clases PROHIBIDAS |
|------|-------------------|
| Enano | Mago, Hechicero, Clérigo, Druida, Bardo |
| Elfo Bosque | Bárbaro, Artífice |
| Elfo Noche | Paladín, Clérigo (Luz), Bardo |
| Duende | Guerrero, Paladín, Bárbaro, Monje |
| Minotauro | Mago, Hechicero, Clérigo, Druida, Bardo, Pícaro |

**Si encuentras combinación prohibida → FALSIFICACIÓN CONFIRMADA**

---

#### 4.3 Verificar Clase Compatible con Equipamiento

**Armas visibles:**

```
Cliente porta: Espada Larga
Permiso de Armas dice: "Espada Larga autorizada"
Clase: Guerrero
→ ✓ Todo coincide

Cliente porta: Espada Larga
Permiso de Armas dice: "Arco autorizado"
→ ❌ Porta arma no autorizada

Cliente porta: Espada Larga
Clase: Mago
→ ⚠️ Sospechoso (Magos rara vez usan espadas)
```

**Clases y armas típicas:**

| Clase | Armas Comunes | Armas Raras |
|-------|---------------|-------------|
| Guerrero | Espada, Escudo | Cualquiera |
| Paladín | Espada, Maza | Lanza |
| Bárbaro | Hacha, Espada Grande | Cadenas |
| Monje | Ninguna (manos) | Bastón |
| Mago | Bastón, Varita | Ninguna física |
| Pícaro | Daga, Arco | Espada Corta |
| Guardabosques | Arco, Espada Corta | Hacha |

---

### Paso 5: VERIFICACIÓN CONTRA LIBRO DE REGLAS

**Consultar reglas activas del día**

```
Abrir "Libro de Reglas del Día"
    ↓
Leer reglas activas
    ↓
Verificar que cliente cumple TODAS las reglas
    ├─ Cumple todas → ✓ OK para servir
    └─ Viola alguna → ❌ Debes rechazar
```

**Ejemplo de verificación:**

```
LIBRO DE REGLAS HOY (15/6/1225):
1. Prohibido servir a Minotauros
2. Obligatorio Licencia de Magia para magos
3. Toque de queda 21:00 para razas exóticas

Cliente: Minotauro con ID perfecta
→ ❌ RECHAZAR (Regla 1)

Cliente: Mago sin Licencia de Magia
→ ❌ RECHAZAR (Regla 2)

Cliente: Dracónido a las 22:00
→ ❌ RECHAZAR (Regla 3, es raza exótica y pasó toque de queda)
```

---

#### Verificación contra Órdenes de Detención

```
Mirar órdenes de detención en tu pared
    ↓
Comparar retrato con cliente actual
    ├─ Coincide → Cliente es criminal buscado
    │   ├─ Llamar Guardia → Recompensa
    │   ├─ Servir → Riesgo de multa
    │   └─ Advertir → Pierde reputación Guardia, gana Ladrones
    └─ No coincide → Cliente limpio
```

---

## 🎮 FLUJO COMPLETO DE VERIFICACIÓN

### Ejemplo Práctico: Cliente Élfico

**SITUACIÓN:**
- Cliente: Elfo del Bosque, aparenta ~25 años (humano)
- Documentos presentados: ID + Licencia de Magia
- Hora: 19:00

---

**PASO 1: Visual**
```
Retrato ID: Elfo adulto ✓
Cliente real: Elfo adulto ✓
Raza coincide: Sí ✓
```

**PASO 2: Datos Básicos**
```
ID:
- Nombre: Legolas de Bosque Verde ✓
- Raza: Elfo del Bosque ✓
- Edad: 120 años ✓ (legal, mínimo 80)
- Emisión: 5/5/1220 (hace 5 años) ✓
- Autoridad: Consejo de Ancianos Bosque Verde ✓
- Firma: Presente ✓
- Sello: Presente ✓
```

**PASO 3: Autenticidad**
```
Sello: Comparar con catálogo
→ Coincide perfectamente ✓

Calidad papel: Limpio, nítido ✓

Usar UV en Licencia de Magia:
→ Brilla púrpura con símbolo arcano ✓
```

**PASO 4: Cruzada**
```
ID: "Legolas de Bosque Verde, Elfo Bosque, 120 años, Mago"
Licencia: "Legolas de Bosque Verde, Elfo Bosque, 120 años"
→ Nombres coinciden ✓
→ Razas coinciden ✓
→ Edades coinciden ✓

Restricciones raza-clase:
Elfo Bosque + Mago = ✓ Compatible

Clase Mago sin armas físicas = ✓ Coherente
```

**PASO 5: Reglas del Día**
```
Libro dice:
1. Obligatorio Licencia de Magia para magos
   → Cliente tiene Licencia ✓
2. No servir a Minotauros
   → Cliente es Elfo ✓
3. Toque de queda 21:00 para razas exóticas
   → Hora actual 19:00 ✓

Órdenes de detención:
→ Ninguna coincide con cliente ✓
```

**DECISIÓN:**
```
✅ TODOS LOS PASOS PASADOS
→ SERVIR AL CLIENTE
```

---

### Ejemplo Práctico: Cliente Sospechoso

**SITUACIÓN:**
- Cliente: Duende, aparenta adulto
- Documentos: ID + Permiso de Armas
- Arma visible: Espada Larga
- Clase declarada: Guerrero

---

**PASO 1: Visual**
```
Retrato: Duende ✓
Cliente: Duende ✓
Coincide ✓
```

**PASO 2: Datos**
```
ID:
- Raza: Duende
- Clase: Guerrero
- Edad: 30 años (legal, mínimo 25) ✓

Pero...
```

**PASO 4: Cruzada (detecta error)**
```
Restricciones raza-clase:
Duende + Guerrero = ❌ PROHIBIDO

Duendes NO pueden ser Guerreros (demasiado pequeños)
→ FALSIFICACIÓN CONFIRMADA
```

**DECISIÓN:**
```
❌ RECHAZAR o LLAMAR GUARDIA
```

---

## 📊 NIVELES DE SOSPECHA

### Sistema de Indicadores

**🟢 VERDE (Sin Sospecha):**
- Todos los chequeos pasados
- Sin inconsistencias
- Documentos auténticos

**Acción:** Servir con confianza

---

**🟡 AMARILLO (Sospecha Leve):**
- Algo no cuadra perfectamente
- Variaciones menores (iniciales en nombre)
- Sello ligeramente borroso
- Edad en límite exacto (ej: Elfo de 80 años)

**Acción:**
- Servir bajo tu propio riesgo
- O hacer pregunta al cliente
- O usar herramienta adicional (UV)

---

**🟠 NARANJA (Sospecha Alta):**
- Inconsistencias significativas
- Fechas extrañas
- Sello incorrecto
- Cliente nervioso al ser interrogado

**Acción:**
- No servir
- Pedir documento adicional
- Usar todas las herramientas disponibles

---

**🔴 ROJO (Falsificación Confirmada):**
- Error crítico (raza-clase imposible)
- Fecha futura
- Sello completamente incorrecto
- Cliente admite falsificación

**Acción:**
- Rechazar inmediatamente
- O llamar a Guardia (si hay recompensa)

---

## 🕐 PROGRESIÓN DE DIFICULTAD

### Early Game (Días 1-14)

**Documentos requeridos:** 1 (solo ID)

**Verificaciones:**
- ✓ Edad legal
- ✓ Retrato coincide

**Falsificaciones:** Obvias
- Retrato no coincide
- Edad claramente menor
- Sin firma

**Tiempo por cliente:** 30 segundos

---

### Mid Game (Días 15-60)

**Documentos requeridos:** 2-3

**Verificaciones:**
- ✓ Todo lo anterior
- ✓ Verificación cruzada
- ✓ Reglas del día (cambian semanalmente)
- ✓ Autenticidad de sellos

**Falsificaciones:** Medianas
- Sellos incorrectos
- Fechas inconsistentes
- Nombres con variaciones

**Tiempo por cliente:** 60-90 segundos

---

### Late Game (Día 61+)

**Documentos requeridos:** 3-5

**Verificaciones:**
- ✓ TODO lo anterior
- ✓ Reglas cambian DIARIAMENTE
- ✓ Órdenes de detención activas
- ✓ Herramientas avanzadas necesarias

**Falsificaciones:** Maestras
- Visualmente perfectas
- Solo detectables por lógica
- Requieren experiencia del jugador

**Tiempo por cliente:** 90-180 segundos

**Presión adicional:**
- Fila de clientes esperando
- Algunos se impacientan y se van (pérdida ganancia)

---

## 💡 CONSEJOS AVANZADOS

### Patrones de Falsificación por Raza

**Duendes:**
- 40% documentos falsos
- Falsificaciones maestras (visualmente perfectas)
- Error común: Se olvidan de actualizar edad entre documentos
- Tip: Siempre verifica matemática de fechas

**Pícaros:**
- 50% documentos falsos
- Múltiples IDs (nombres diferentes)
- Error común: Inconsistencias clase-arma
- Tip: Si es Pícaro, escrutinio extra

**Bárbaros:**
- 15% documentos falsos
- Generalmente usan documentos robados (no falsificados)
- Retrato no coincide (documento robado de otra persona)
- Tip: Verificación visual crítica

---

### Preguntas Inteligentes al Cliente

Si sospechas, puedes hacer preguntas:

**"¿Por qué tu ID dice 150 años pero aparentas 25?"**
- Elfo: "Uso glamour" ✓ Legítimo
- Humano: "Eh... soy elfo... creo" ❌ Sospechoso

**"¿Dónde obtuviste este Permiso de Armas?"**
- "De la Guardia Real en Cruce" ✓
- "Eh... lo encontré..." ❌

**"¿A qué facción representas?"**
- Si tiene Certificado de Facción, debe saberlo inmediatamente
- Si duda o se confunde → Documento robado/falso

---

### Uso Estratégico de Bebidas

**Poción de Verdad + Interrogación:**
```
Sospechas de cliente
    ↓
Sirves "Poción de Verdad"
    ↓
Cliente borracho nivel 2 → NO PUEDE mentir
    ↓
Preguntas: "¿Este es tu documento real?"
    ↓
Cliente forzado a responder verdad
    ↓
Confirmas falsificación
```

**Cerveza de Glamour + Elfos:**
```
Elfo dice tener 120 años (legal)
Aparenta edad adulta
    ↓
Sirves "Cerveza de Glamour"
    ↓
Glamour cae → Aparenta adolescente
    ↓
Edad real: 70 años (menor de 80)
    ↓
Falsificación confirmada
```

---

## 🎯 OBJETIVO FINAL

**Maestría del jugador:**
- Después de 100+ clientes, jugador reconoce patrones
- Puede detectar falsificaciones en 10-15 segundos
- Intuición desarrollada ("este Duende parece sospechoso...")
- Balance entre rapidez (ganancia) y precisión (evitar multas)

**Papers Please inspiration:**
- Sistema complejo pero justo
- Jugador mejora con práctica
- Satisfacción al detectar falsificación maestra
- Tensión constante ("¿será real o falso?")

---

**Guía completa de verificación para implementación del sistema.**
