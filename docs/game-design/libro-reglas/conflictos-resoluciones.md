# ⚖️ Conflictos y Resoluciones entre Reglas

Este documento define cómo resolver contradicciones cuando múltiples reglas aplican al mismo cliente.

---

## 🎯 FILOSOFÍA DE RESOLUCIÓN

### Jerarquía de Prioridades

**Orden de precedencia (mayor a menor):**

```
1. EMERGENCIAS (máxima prioridad)
2. Pase VIP
3. PROHIBICIONES
4. OBLIGACIONES
5. RESTRICCIONES
6. EXENCIONES
7. BONIFICACIONES
```

**Regla general:**
> Cuando dos reglas contradicen, la de MAYOR prioridad gana.

---

## 🚨 CASOS DE CONFLICTO

### Tipo 1: Emergencia vs Todas las Demás

**Principio:** Emergencia ANULA todo lo demás

**Ejemplo 1:**
```
Regla Normal: "EXENCIÓN Guerreros de toque de queda 22:00"
EMERGENCIA: "TODOS fuera a las 18:00"

Cliente: Guerrero a las 19:00

Resolución:
EMERGENCIA > EXENCIÓN
→ Guerrero DEBE ser rechazado ❌
```

**Ejemplo 2:**
```
Regla Normal: "BONIFICACIÓN +20% bebidas élficas"
EMERGENCIA: "Prohibidas TODAS las bebidas importadas"

Cliente: Elfo pide Vino Élfico (importado)

Resolución:
EMERGENCIA > BONIFICACIÓN
→ NO puedes servir Vino Élfico ❌
```

**Ejemplo 3:**
```
Regla Normal: "OBLIGATORIO verificar Licencia de Magia"
EMERGENCIA: "Prohibido uso de magia - NO servir a clases mágicas"

Cliente: Mago con Licencia perfecta

Resolución:
EMERGENCIA > OBLIGACIÓN
→ NO puedes servir al Mago (incluso con licencia perfecta) ❌
```

---

### Tipo 2: Pase VIP vs Reglas Normales

**Principio:** Pase VIP exime de TODO (excepto Emergencias)

**Ejemplo 1:**
```
Regla: "PROHIBIDO Minotauros"
Cliente: Minotauro con Pase VIP

Resolución:
Pase VIP > PROHIBICIÓN
→ Minotauro PUEDE ser servido ✓
```

**Ejemplo 2:**
```
Regla 1: "PROHIBIDO armas"
Regla 2: "TOQUE QUEDA 21:00"
Regla 3: "OBLIGATORIO Licencia de Magia"
Cliente: Mago con espada, 22:00, SIN Licencia de Magia, PERO con Pase VIP

Resolución:
Pase VIP exime de TODO
→ Cliente PUEDE ser servido ✓
```

**PERO:**
```
EMERGENCIA: "TODOS fuera a las 18:00"
Cliente: Noble con Pase VIP a las 19:00

Resolución:
EMERGENCIA > Pase VIP
→ Cliente DEBE ser rechazado ❌
```

---

### Tipo 3: Prohibición vs Obligación

**Principio:** Prohibición gana (seguridad > proceso)

**Ejemplo 1:**
```
Regla A: "PROHIBIDO Minotauros"
Regla B: "OBLIGATORIO servir a miembros del Gremio de Comerciantes"
Cliente: Minotauro miembro del Gremio de Comerciantes

Resolución:
PROHIBICIÓN > OBLIGACIÓN
→ Cliente DEBE ser rechazado ❌
(Prohibición racial anula obligación de facción)
```

**Ejemplo 2:**
```
Regla A: "PROHIBIDO bebidas alcohólicas a Clérigos"
Regla B: "OBLIGATORIO servir a miembros del Templo"
Cliente: Clérigo del Templo pide cerveza

Resolución:
PROHIBICIÓN aplica al TIPO de bebida
OBLIGACIÓN aplica a ENTRADA/SERVICIO general
→ Solución: Sirve bebida NO alcohólica ✓
(No es contradicción real, son compatibles)
```

---

### Tipo 4: Prohibición vs Exención

**Principio:** Exención ANULA prohibición para grupo específico

**Ejemplo 1:**
```
Regla A: "PROHIBIDO armas en el local"
Regla B: "EXENCIÓN Guerreros de prohibición de armas"
Cliente: Guerrero con espada

Resolución:
EXENCIÓN > PROHIBICIÓN (para Guerreros)
→ Guerrero PUEDE entrar con arma ✓
```

**Ejemplo 2:**
```
Regla A: "PROHIBIDO armas en el local"
Regla B: "EXENCIÓN Guerreros de prohibición de armas"
Cliente: Bárbaro con hacha

Resolución:
Bárbaro NO es Guerrero
PROHIBICIÓN aplica a Bárbaro
→ Bárbaro NO puede entrar con hacha ❌
(O debe dejar hacha afuera)
```

**Ejemplo 3:**
```
Regla A: "TOQUE QUEDA 21:00 para razas exóticas"
Regla B: "EXENCIÓN Guardia Real de toque de queda"
Cliente: Minotauro (raza exótica) miembro Guardia Real, 22:00

Resolución:
EXENCIÓN > RESTRICCIÓN (para Guardia)
→ Minotauro de la Guardia PUEDE ser servido ✓
```

---

### Tipo 5: Exención vs Obligación

**Principio:** Obligación sigue aplicando (exención solo afecta prohibiciones/restricciones)

**Ejemplo 1:**
```
Regla A: "OBLIGATORIO Licencia de Magia para magos"
Regla B: "EXENCIÓN Paladines de inspecciones rutinarias"
Cliente: Paladín (NO mago)

Resolución:
No hay conflicto real
Paladín no es mago → No necesita Licencia de Magia
→ Servir ✓
```

**Ejemplo 2:**
```
Regla A: "OBLIGATORIO verificar edad legal"
Regla B: "EXENCIÓN nobles de verificación de edad"
Cliente: Noble Humano de 16 años (menor)

Resolución:
EXENCIÓN permite NO verificar, PERO ley fundamental (edad legal) sigue aplicando
→ SI verificas: Es menor, debes rechazar ❌
→ SI NO verificas: Violás ley, posible multa si Inspector detecta ❌

Dilema: ¿Confías en que noble es mayor o verificas?
(Mayoría de nobles son adultos, pero hay riesgo)
```

---

### Tipo 6: Restricción vs Exención

**Principio:** Exención ANULA restricción para grupo específico

**Ejemplo 1:**
```
Regla A: "LÍMITE 2 bebidas alcohólicas por cliente"
Regla B: "EXENCIÓN Enanos de límite de bebidas"
Cliente: Enano pide 5 cervezas

Resolución:
EXENCIÓN > RESTRICCIÓN
→ Enano PUEDE beber 5 cervezas ✓
```

**Ejemplo 2:**
```
Regla A: "MÁXIMO 10 clientes simultáneos"
Regla B: "EXENCIÓN miembros de la Guardia no cuentan para límite"
Situación: 10 clientes actuales, llega Guardia

Resolución:
EXENCIÓN > RESTRICCIÓN
→ Guardia PUEDE entrar (no cuenta para límite) ✓
→ Total real: 11 personas, pero solo 10 cuentan
```

---

### Tipo 7: Bonificación vs Prohibición

**Principio:** Prohibición gana (seguridad > beneficio económico)

**Ejemplo 1:**
```
Regla A: "PROHIBIDO bebidas élficas"
Regla B: "BONIFICACIÓN +20% precio bebidas élficas"
Cliente: Elfo pide Vino Élfico

Resolución:
PROHIBICIÓN > BONIFICACIÓN
→ NO puedes servir Vino Élfico ❌
(Bonificación queda inútil esta combinación)
```

**Ejemplo 2:**
```
Regla A: "PROHIBIDO Minotauros"
Regla B: "BONIFICACIÓN +50c por servir a miembros Gremio Comerciantes"
Cliente: Minotauro miembro Gremio Comerciantes

Resolución:
PROHIBICIÓN > BONIFICACIÓN
→ Cliente DEBE ser rechazado ❌
(Pierdes bonificación, pero evitas multa)
```

---

### Tipo 8: Obligación vs Obligación (Contradicción Total)

**Principio:** ERROR DE GENERACIÓN (no debería pasar)

**Ejemplo hipotético:**
```
Regla A: "OBLIGATORIO servir a TODOS los Elfos"
Regla B: "OBLIGATORIO rechazar a TODOS los Elfos"
Cliente: Elfo

Resolución:
→ CONTRADICCIÓN TOTAL (bug del sistema)
→ Si pasa: Aplicar regla más reciente
→ O permitir al jugador elegir (sin penalización)
```

**Sistema debe prevenir esto en generación.**

---

### Tipo 9: Exención vs Exención (Múltiples Exenciones)

**Principio:** Aplicar TODAS las exenciones acumulativamente

**Ejemplo 1:**
```
Regla A: "EXENCIÓN Guerreros de toque de queda"
Regla B: "EXENCIÓN Guardia Real de toque de queda"
Cliente: Guerrero miembro Guardia Real, 23:00

Resolución:
Ambas exenciones aplican
→ Cliente PUEDE ser servido ✓
```

**Ejemplo 2:**
```
Regla A: "EXENCIÓN nobles de verificación de edad"
Regla B: "EXENCIÓN diplomáticos de verificación de documentos"
Cliente: Noble diplomático

Resolución:
Ambas exenciones aplican
→ NO necesitas verificar edad NI documentos ✓
(Pero arriesgas si es menor o criminal)
```

---

## 🧩 CASOS COMPLEJOS

### Caso Complejo 1: Triple Contradicción

**Situación:**
```
Regla 1: "PROHIBIDO Minotauros"
Regla 2: "EXENCIÓN Guerreros de toque de queda"
Regla 3: "OBLIGATORIO servir a Guardia Real"
Cliente: Minotauro Guerrero de la Guardia Real

Análisis:
- Regla 1 dice: NO servir (Prohibición raza)
- Regla 2: No aplica directamente (solo afecta toque de queda)
- Regla 3 dice: SÍ servir (Obligación facción)

Jerarquía:
PROHIBICIÓN (raza) > OBLIGACIÓN (facción)

Resolución:
→ Cliente DEBE ser rechazado ❌
(Prohibición racial tiene prioridad)

PERO:
Si cliente tiene Pase VIP:
Pase VIP > PROHIBICIÓN
→ Cliente PUEDE ser servido ✓
```

---

### Caso Complejo 2: Emergencia Parcial

**Situación:**
```
Regla Normal: "PROHIBIDO Minotauros"
EMERGENCIA: "Levantamiento de prohibición racial por 1 día (Día de la Paz)"
Cliente: Minotauro

Análisis:
- Emergencia especial ANULA prohibición
- Es tipo raro de emergencia "permisiva" (vs restrictiva)

Resolución:
EMERGENCIA > PROHIBICIÓN
→ Cliente PUEDE ser servido ✓
(Solo por hoy)
```

---

### Caso Complejo 3: Exención con Condición

**Situación:**
```
Regla A: "PROHIBIDO armas"
Regla B: "EXENCIÓN Guerreros de prohibición de armas SI tienen Permiso vigente"
Cliente: Guerrero con espada, Permiso vencido

Análisis:
- Exención existe PERO tiene condición
- Condición NO cumplida (permiso vencido)
- Por lo tanto, exención NO aplica

Resolución:
PROHIBICIÓN aplica
→ Guerrero NO puede entrar con arma ❌
(O debe dejar arma afuera)
```

---

### Caso Complejo 4: Reglas en Cascada

**Situación:**
```
Regla 1: "PROHIBIDO bebidas alcohólicas a Clérigos"
Regla 2: "OBLIGATORIO servir a miembros del Templo"
Regla 3: "BONIFICACIÓN +10c por servir a Templo"
Cliente: Clérigo del Templo pide cerveza

Análisis paso a paso:
1. Cliente pide cerveza (alcohólica)
2. Regla 1: PROHIBIDO alcohol a Clérigos → NO puedes servir cerveza
3. Regla 2: OBLIGATORIO servir a Templo → Debes servir algo
4. Regla 3: BONIFICACIÓN si sirves → Incentivo económico

Resolución:
→ Rechaza cerveza ❌
→ Ofrece bebida NO alcohólica ✓
→ Recibes bonificación ✓
(Cumples todas las reglas)
```

---

### Caso Complejo 5: Dilema del Refugiado

**Situación:**
```
Regla 1: "PROHIBIDO Minotauros"
Regla 2: "OBLIGATORIO reportar comportamiento sospechoso"
Cliente: Minotauro refugiado con historia trágica, documentos perfectos

Análisis moral:
- Técnicamente debe ser rechazado (Regla 1)
- Pero historia es legítima, no es criminal
- Reportar sería inhumano

Resolución LEGAL:
PROHIBICIÓN > compasión
→ Cliente DEBE ser rechazado ❌

Resolución MORAL:
Jugador decide romper regla
→ Sirve al refugiado
→ Riesgo de multa 200c (30% probabilidad Inspector detecta)
→ +Reputación con facción Minotauro
→ -Reputación con Guardia si te descubren

No hay respuesta "correcta" → Dilema del jugador
```

---

## 🎓 GUÍA RÁPIDA DE RESOLUCIÓN

### Algoritmo de Decisión

```
1. ¿Hay EMERGENCIA activa que aplica?
   SÍ → Seguir emergencia, ignorar resto
   NO → Continuar

2. ¿Cliente tiene Pase VIP válido?
   SÍ → Servir (excepto si hay emergencia)
   NO → Continuar

3. ¿Hay PROHIBICIÓN que aplica al cliente?
   SÍ → ¿Hay EXENCIÓN que lo exime?
      SÍ → Continuar verificación
      NO → RECHAZAR cliente
   NO → Continuar

4. ¿Todas las OBLIGACIONES cumplidas?
   SÍ → Continuar
   NO → Pedir documentos faltantes o rechazar

5. ¿Cliente viola RESTRICCIÓN?
   SÍ → ¿Hay EXENCIÓN?
      SÍ → Servir
      NO → Rechazar o limitar servicio
   NO → Continuar

6. ¿Hay BONIFICACIÓN aplicable?
   SÍ → Aplicar beneficio
   NO → Servicio normal

7. SERVIR AL CLIENTE ✓
```

---

### Tabla de Precedencia

| Regla A | vs | Regla B | Ganador | Notas |
|---------|----|---------| --------|-------|
| Emergencia | vs | Pase VIP | Emergencia | Emergencia anula todo |
| Emergencia | vs | Cualquiera | Emergencia | Máxima prioridad |
| Pase VIP | vs | Prohibición | Pase VIP | Excepto emergencia |
| Pase VIP | vs | Obligación | Pase VIP | Exime de verificaciones |
| Prohibición | vs | Obligación | Prohibición | Seguridad > proceso |
| Prohibición | vs | Exención | Exención | Si aplica a grupo |
| Prohibición | vs | Bonificación | Prohibición | Seguridad > ganancia |
| Obligación | vs | Exención | Obligación | Exención solo afecta prohib/restr |
| Restricción | vs | Exención | Exención | Si aplica a grupo |
| Bonificación | vs | Restricción | Restricción | Límite > beneficio |

---

## 💡 EJEMPLOS PRÁCTICOS COMPLETOS

### Ejemplo 1: Día Normal (Día 35)

**Libro de Reglas:**
```
1. OBLIGATORIO verificar edad
2. PROHIBIDO Minotauros
3. OBLIGATORIO Licencia de Magia para magos
4. TOQUE QUEDA 21:00 razas exóticas
5. EXENCIÓN Guerreros de toque de queda
```

**Cliente 1: Humano Mago, 19:00, con Licencia**
```
✓ Edad: OK
✓ Raza: No prohibida
✓ Licencia: Presente
✓ Hora: OK
→ SERVIR ✓
```

**Cliente 2: Minotauro Guerrero, 20:00, documentos perfectos**
```
✓ Edad: OK
❌ Raza: Minotauro → PROHIBIDO (Regla 2)
✓ Clase: Guerrero (exento de toque queda, pero eso no ayuda)
→ RECHAZAR ❌
```

**Cliente 3: Dracónido Guerrero, 22:00**
```
✓ Edad: OK
✓ Raza: No prohibida
❌ Hora: 22:00 > 21:00 → TOQUE QUEDA
✓ PERO Guerrero → EXENCIÓN (Regla 5)
→ SERVIR ✓
```

---

### Ejemplo 2: Día con Emergencia (Día 75)

**Libro de Reglas:**
```
1-5. (Reglas normales del ejemplo anterior)
6. 🚨 EMERGENCIA: Estado de sitio - TODOS fuera a las 18:00
```

**Cliente 1: Humano Plebeyo, 19:00**
```
❌ Hora: 19:00 > 18:00 → EMERGENCIA
→ RECHAZAR ❌ (Emergencia anula todo)
```

**Cliente 2: Noble con Pase VIP, 19:00**
```
✓ Pase VIP: Presente
❌ PERO EMERGENCIA > Pase VIP
→ RECHAZAR ❌
```

**Cliente 3: Miembro Guardia Real, 20:00**
```
✓ Guardia Real tiene EXENCIÓN implícita de emergencias (autoridad)
→ SERVIR ✓
(Pero verificar que es realmente Guardia)
```

---

### Ejemplo 3: Festival (Día 50)

**Libro de Reglas:**
```
1. OBLIGATORIO verificar edad
2. PROHIBIDO discriminación contra Elfos (evento)
3. BONIFICACIÓN +20% bebidas élficas
4. OBLIGATORIO servir a delegación élfica
5. EXENCIÓN Elfos de toque de queda esta semana
```

**Cliente 1: Elfo pide Vino Élfico, 19:00**
```
✓ Edad: OK
✓ Raza: Protegida (Regla 2)
✓ Bebida: Bonificación +20% (Regla 3)
→ SERVIR ✓
→ Cobrar 45c × 1.2 = 54c
```

**Cliente 2: Humano rechaza servir a Elfo previo**
```
❌ Regla 2: Prohibido discriminar Elfos
→ Si rechazas Elfo sin razón válida: Multa 300c
```

---

## 🎯 OBJETIVO FINAL

**Sistema de resolución debe:**
1. ✅ Ser consistente (misma situación = misma resolución)
2. ✅ Ser predecible (jugador puede anticipar resultado)
3. ✅ Crear dilemas (situaciones sin respuesta clara)
4. ✅ Recompensar conocimiento (jugador experto navega mejor)
5. ✅ Ser justo (jugador no penalizado por ambigüedad del sistema)

**Documentación completa de resolución de conflictos lista.**
