# 🎖️ Sistema de Progresión del Jugador - El Tabernero del Cruce

## Filosofía de Diseño

**"Maestría a través de la experiencia, no niveles arbitrarios"**

A diferencia de RPGs tradicionales, tu progresión no es numérica (Level 1, 2, 3...) sino **basada en habilidades aprendidas** y **maestría demostrada**.

**Principios:**
1. **Aprender haciendo** - Practicas → Mejoras
2. **Elecciones permanentes** - Habilidades desbloqueadas no se pierden
3. **Especialización** - Imposible dominar todo, debes elegir camino
4. **Recompensas significativas** - Cada habilidad impacta gameplay

---

## 🎯 SISTEMAS DE PROGRESIÓN

### 1. Experiencia y Maestría

**No hay "niveles" tradicionales. Hay MAESTRÍA en categorías:**

```
CATEGORÍAS DE MAESTRÍA:
├── Verificación de Documentos
├── Detección de Mentiras
├── Gestión de Conflictos
├── Conocimiento de Bebidas
├── Negociación
├── Intimidación
└── Diplomacia
```

**Cada categoría tiene 5 rangos:**

```
★☆☆☆☆ Novato (0-100 XP)
★★☆☆☆ Aprendiz (101-300 XP)
★★★☆☆ Competente (301-600 XP)
★★★★☆ Experto (601-1000 XP)
★★★★★ Maestro (1001+ XP)
```

---

### 2. Ganancia de Experiencia

**XP se gana por ACCIONES, no por tiempo:**

| Acción | XP Ganado | Categoría |
|--------|-----------|-----------|
| Detectar documento falso | +5 XP | Verificación |
| Detectar mentira (diálogo) | +3 XP | Detección Mentiras |
| Resolver pelea sin violencia | +10 XP | Gestión Conflictos |
| Servir bebida perfecta (favorita del cliente) | +2 XP | Conocimiento Bebidas |
| Negociar descuento en compra | +4 XP | Negociación |
| Intimidar a criminal para que confiese | +8 XP | Intimidación |
| Mejorar reputación con facción | +Variable | Diplomacia |

**Multiplicadores:**
- Primera vez: ×2 XP
- Racha perfecta (5+ aciertos seguidos): ×1.5 XP
- Bajo presión (fila larga): ×1.2 XP

---

### 3. Habilidades Desbloqueables

**Cada rango de maestría desbloquea 1-2 habilidades:**

---

## 📜 ÁRBOL DE HABILIDADES: VERIFICACIÓN

### ★☆☆☆☆ Novato (0 XP) - Habilidades Básicas

**"Ojo Básico"** (Pasiva)
- Efecto: Documentos obviamente falsos se marcan automáticamente
- Detección: Retrato no coincide, fecha futura, sin firma

**"Consulta del Libro"** (Activa)
- Efecto: Puedes consultar Libro de Reglas sin penalización de tiempo
- Cooldown: Ninguno

---

### ★★☆☆☆ Aprendiz (100 XP)

**"Memoria de Sellos"** (Pasiva)
- Efecto: Recuerdas sellos oficiales vistos previamente
- Detección: +20% detección de sellos falsos

**"Comparación Rápida"** (Activa)
- Efecto: Compara 2 documentos lado a lado en 2 segundos (normalmente 5)
- Cooldown: Ninguno

---

### ★★★☆☆ Competente (300 XP)

**"Ojo de Halcón"** (Pasiva)
- Efecto: Documentos con errores medianos se resaltan levemente
- Detección: Fechas inconsistentes, nombres con variación menor

**"Verificación Instantánea"** (Activa)
- Efecto: Verifica documento completo en 1 segundo
- Cooldown: 30 segundos
- Precisión: 80%

---

### ★★★★☆ Experto (600 XP)

**"Maestro de Documentos"** (Pasiva)
- Efecto: +40% velocidad de verificación
- Detalle: Detectas inconsistencias sutiles (numeración fuera de secuencia)

**"Sexto Sentido"** (Pasiva)
- Efecto: Documentos falsificados por Duendes maestros tienen brillo rojo leve
- Detección: 60% de falsificaciones maestras

---

### ★★★★★ Maestro (1000 XP)

**"Verificador Legendario"** (Pasiva - PERMANENTE)
- Efecto: Detección automática del 95% de falsificaciones
- Solo falla con falsificaciones perfectas (1% de duendes)
- Velocidad: +60% verificación

**"Visión del Inspector"** (Activa)
- Efecto: Revela TODOS los errores en documento instantáneamente
- Cooldown: 1 minuto
- Precisión: 100%

---

## 🗣️ ÁRBOL DE HABILIDADES: DETECCIÓN DE MENTIRAS

### ★☆☆☆☆ Novato (0 XP)

**"Interrogatorio Básico"** (Activa)
- Efecto: Puedes hacer 1 pregunta al cliente
- Respuesta: Basada en propensión a mentir de raza/clase

---

### ★★☆☆☆ Aprendiz (100 XP)

**"Lenguaje Corporal"** (Pasiva)
- Efecto: Clientes muy nerviosos muestran icono de sudor
- Detección: Solo clientes con propensión mentir >7/10

---

### ★★★☆☆ Competente (300 XP)

**"Interrogatorio Cruzado"** (Activa)
- Efecto: Puedes hacer 3 preguntas relacionadas
- Si contradicción → Cliente revelado como mentiroso
- Cooldown: Por cliente

---

### ★★★★☆ Experto (600 XP)

**"Psicología Avanzada"** (Pasiva)
- Efecto: Ves "nivel de confianza" del cliente (0-100%)
- <50% = Probablemente mintiendo

**"Presión Psicológica"** (Activa)
- Efecto: Fuerzas a cliente a confesar si miente
- Éxito: 70% (depende de intimidación)
- Cooldown: 2 minutos

---

### ★★★★★ Maestro (1000 XP)

**"Mente Abierta"** (Pasiva - PERMANENTE)
- Efecto: Detección automática de mentiras (85% precisión)
- Clientes mentirosos tienen aura roja leve

**"Verdad Absoluta"** (Activa)
- Efecto: Cliente NO PUEDE mentir por 30 segundos
- Funciona incluso en Pícaros/Elfos oscuros
- Cooldown: 5 minutos
- Requiere: +60 reputación con Templo de la Luz (bendición)

---

## ⚔️ ÁRBOL DE HABILIDADES: GESTIÓN DE CONFLICTOS

### ★☆☆☆☆ Novato (0 XP)

**"Llamar a la Guardia"** (Activa)
- Efecto: Guardia llega en 30 segundos
- Arresta a agresores
- Cooldown: 10 minutos

---

### ★★☆☆☆ Aprendiz (100 XP)

**"Voz Firme"** (Activa)
- Efecto: 40% chance de detener pelea verbal
- No funciona con bárbaros borrachos

---

### ★★★☆☆ Competente (300 XP)

**"Mediación"** (Activa)
- Efecto: 60% chance de resolver conflicto pacíficamente
- Funciona con clases diplomáticas (Bardo, Clérigo)

**"Separación Preventiva"** (Pasiva)
- Efecto: Puedes asignar mesas a clientes (evitar razas enemigas juntas)

---

### ★★★★☆ Experto (600 XP)

**"Presencia Intimidante"** (Pasiva)
- Efecto: -30% probabilidad de violencia en tu presencia
- No funciona con Minotauros/Bárbaros nivel 3 borracho

**"Intervención Heroica"** (Activa)
- Efecto: Detienes pelea física instantáneamente
- Éxito: 70% (falla si clientes muy fuertes)
- Cooldown: 5 minutos

---

### ★★★★★ Maestro (1000 XP)

**"Pacificador Legendario"** (Pasiva - PERMANENTE)
- Efecto: -60% violencia total en taberna
- Aura de paz

**"Palabra de Comando"** (Activa)
- Efecto: CONGELA a todos los clientes por 10 segundos
- Termina cualquier conflicto instantáneamente
- Cooldown: 30 minutos
- Requiere: +70 reputación con Orden del Escudo (bendición divina)

---

## 🍺 ÁRBOL DE HABILIDADES: CONOCIMIENTO DE BEBIDAS

### ★☆☆☆☆ Novato (0 XP)

**"Catálogo Básico"** (Pasiva)
- Efecto: Conoces 10 bebidas comunes

---

### ★★☆☆☆ Aprendiz (100 XP)

**"Memoria de Preferencias"** (Pasiva)
- Efecto: Recuerdas bebida favorita de clientes regulares
- +5% propina si sirves favorita

---

### ★★★☆☆ Competente (300 XP)

**"Sommelier"** (Pasiva)
- Efecto: Recomiendas bebida perfecta para raza/clase
- +10% propina

**"Mezcla Rápida"** (Activa)
- Efecto: Preparas bebida en mitad de tiempo
- Cooldown: 1 minuto

---

### ★★★★☆ Experto (600 XP)

**"Maestro Cervecero"** (Pasiva)
- Efecto: Puedes fabricar bebidas básicas (50% costo)
- Requiere: Upgrade de cocina

**"Cata Experta"** (Activa)
- Efecto: Identificas TODOS los ingredientes de bebida
- Detectas venenos/adulteraciones (100%)
- Cooldown: Ninguno

---

### ★★★★★ Maestro (1000 XP)

**"Sommelier Legendario"** (Pasiva - PERMANENTE)
- Efecto: +20% propinas en todas las bebidas
- Clientes SIEMPRE satisfechos con elección

**"Alquimia de Bebidas"** (Activa)
- Efecto: Creas bebida mágica única (efecto aleatorio)
- Cooldown: 1 día
- Requiere: +60 reputación con Círculo Arcano

---

## 💰 ÁRBOL DE HABILIDADES: NEGOCIACIÓN

### ★☆☆☆☆ Novato (0 XP)

**"Regateo Básico"** (Activa)
- Efecto: -5% precio en compras
- Éxito: 50%

---

### ★★☆☆☆ Aprendiz (100 XP)

**"Ojo para Gangas"** (Pasiva)
- Efecto: Mercado negro te ofrece descuentos espontáneos (aleatorio)

---

### ★★★☆☆ Competente (300 XP)

**"Negociador Astuto"** (Activa)
- Efecto: -15% precio en compras
- Éxito: 70%

**"Venta Persuasiva"** (Activa)
- Efecto: +20% precio de venta (cliente paga más)
- Éxito: 60%
- Cooldown: Por cliente

---

### ★★★★☆ Experto (600 XP)

**"Maestro del Trato"** (Pasiva)
- Efecto: -25% precio en TODAS las compras (permanente)

**"Encanto Mercantil"** (Activa)
- Efecto: Cliente paga +50% y está feliz
- Éxito: 80%
- Cooldown: 5 minutos

---

### ★★★★★ Maestro (1000 XP)

**"Magnate Comercial"** (Pasiva - PERMANENTE)
- Efecto: -40% precio compras, +30% precio ventas
- Acceso a contratos exclusivos

**"Palabra de Oro"** (Activa)
- Efecto: Cliente acepta CUALQUIER precio que pongas
- Éxito: 100%
- Cooldown: 1 hora
- Límite: No funciona en facción enemiga (-50 rep)

---

## 👊 ÁRBOL DE HABILIDADES: INTIMIDACIÓN

### ★☆☆☆☆ Novato (0 XP)

**"Amenaza Verbal"** (Activa)
- Efecto: 30% chance de asustar a cliente débil
- Funciona solo con Plebeyos/Pícaros de bajo nivel

---

### ★★☆☆☆ Aprendiz (100 XP)

**"Postura Amenazante"** (Pasiva)
- Efecto: Criminales de bajo nivel evitan problemas (+10% honestidad)

---

### ★★★☆☆ Competente (300 XP)

**"Mirada Penetrante"** (Activa)
- Efecto: 60% chance de que cliente confiese
- No funciona con clases de alta voluntad (Paladín, Monje)

---

### ★★★★☆ Experto (600 XP)

**"Aura de Terror"** (Pasiva)
- Efecto: -40% probabilidad de engaño en tu presencia
- Criminales nerviosos

**"Interrogatorio Agresivo"** (Activa)
- Efecto: 80% chance de confesar
- Funciona en casi todas las clases (excepto Paladines)
- Riesgo: -5 reputación si cliente era inocente

---

### ★★★★★ Maestro (1000 XP)

**"Señor del Miedo"** (Pasiva - PERMANENTE)
- Efecto: Criminales te temen (80% no intentan engañarte)
- Solo pícaros maestros se atreven

**"Juicio Final"** (Activa)
- Efecto: Cliente confiesa TODO (crímenes, afiliaciones, secretos)
- Éxito: 95%
- Cooldown: 1 hora
- Requiere: +60 reputación con Guardia Real o Los Sombríos

---

## 🕊️ ÁRBOL DE HABILIDADES: DIPLOMACIA

### ★☆☆☆☆ Novato (0 XP)

**"Cortesía Básica"** (Pasiva)
- Efecto: +1 reputación con facciones por servir a miembros

---

### ★★☆☆☆ Aprendiz (100 XP)

**"Charla Amistosa"** (Activa)
- Efecto: Cliente comparte rumores/información
- Cooldown: Por cliente

---

### ★★★☆☆ Competente (300 XP)

**"Mediador Natural"** (Pasiva)
- Efecto: +50% ganancia de reputación con todas las facciones

**"Favor Solicitado"** (Activa)
- Efecto: Pides descuento/información a facción aliada (+40 rep)
- Cooldown: 1 día

---

### ★★★★☆ Experto (600 XP)

**"Diplomático Experto"** (Pasiva)
- Efecto: +100% ganancia de reputación, -50% pérdida de reputación

**"Reconciliación"** (Activa)
- Efecto: Recuperas +20 reputación con facción hostil (-20 a -49)
- Cooldown: 1 semana
- Costo: 300 monedas (regalo)

---

### ★★★★★ Maestro (1000 XP)

**"Embajador Universal"** (Pasiva - PERMANENTE)
- Efecto: +200% ganancia de reputación
- Puedes mantener 5+ facciones como aliados (normalmente 2-3)

**"Alianza Imposible"** (Activa)
- Efecto: Mejoras temporalmente relación entre 2 facciones enemigas
- Duración: 7 días
- Cooldown: 1 mes
- Requiere: +70 con AMBAS facciones (casi imposible)

---

## 🎓 MAESTRÍAS ESPECIALES (LATE GAME)

### Desbloqueables solo con requisitos extremos

**"Ojo de Dios"** (Requiere: Maestro en Verificación + Detección Mentiras)
- Efecto: SABES instantáneamente si cliente es honesto o no
- Precisión: 100%
- Pasiva permanente

**"Señor de la Taberna"** (Requiere: Maestro en Gestión Conflictos + Intimidación)
- Efecto: CERO violencia en tu taberna. Imposible.
- Clientes violentos se calman automáticamente

**"Maestro del Comercio"** (Requiere: Maestro en Negociación + Conocimiento Bebidas)
- Efecto: +50% ganancia en TODAS las transacciones
- Monopolio local

**"Líder de Facciones"** (Requiere: Maestro en Diplomacia + Rep +80 con 5 facciones)
- Efecto: Puedes comandar acciones de facciones aliadas
- Ejemplo: Pedir a Guardia que haga raid, Gremio que elimine competencia

---

## 📊 PROGRESIÓN DE XP REQUERIDO

### Tabla de XP Total Necesario

| Categoría | Novato | Aprendiz | Competente | Experto | Maestro | Total |
|-----------|--------|----------|------------|---------|---------|-------|
| Verificación | 0 | 100 | 300 | 600 | 1000 | 2000 XP |
| Detección Mentiras | 0 | 100 | 300 | 600 | 1000 | 2000 XP |
| Gestión Conflictos | 0 | 100 | 300 | 600 | 1000 | 2000 XP |
| Conocimiento Bebidas | 0 | 100 | 300 | 600 | 1000 | 2000 XP |
| Negociación | 0 | 100 | 300 | 600 | 1000 | 2000 XP |
| Intimidación | 0 | 100 | 300 | 600 | 1000 | 2000 XP |
| Diplomacia | 0 | 100 | 300 | 600 | 1000 | 2000 XP |

**Total para Maestro en TODO:** 14,000 XP (prácticamente imposible en 1 playthrough)

**Realista en 1 playthrough (90 días):**
- 2-3 Maestros (6000-9000 XP)
- 2-3 Expertos
- Resto Competente

---

## ⏱️ TIEMPO PARA MAESTRÍA

**Estimación de XP/Día:**

| Fase | XP/Día Promedio | Notas |
|------|----------------|-------|
| Early (1-30) | 20-40 XP | Pocas acciones complejas |
| Mid (31-60) | 50-100 XP | Más falsificaciones, conflictos |
| Late (61-90) | 100-200 XP | Máxima complejidad |

**Tiempo para primera Maestría:**
- Enfoque dedicado: ~30-40 días
- Juego normal: ~50-60 días
- Sin enfoque: ~70+ días

**Imposible dominar todo en 90 días** (solo 6000-12000 XP disponible)

---

## 🎯 RUTAS DE ESPECIALIZACIÓN RECOMENDADAS

### Ruta del Inspector (Papers Please Puro)

**Prioriza:**
1. Verificación → Maestro (prioridad 1)
2. Detección Mentiras → Maestro (prioridad 2)
3. Negociación → Competente (ahorro)

**Playstyle:** Preciso, meticuloso, burocrático
**Fortaleza:** Casi imposible engañarte
**Debilidad:** Conflictos son difíciles

---

### Ruta del Diplomático

**Prioriza:**
1. Diplomacia → Maestro (prioridad 1)
2. Gestión Conflictos → Experto (prioridad 2)
3. Negociación → Experto (economía)

**Playstyle:** Político, alianzas múltiples
**Fortaleza:** +5 facciones como aliados
**Debilidad:** Vulnerable a engaños

---

### Ruta del Señor del Crimen

**Prioriza:**
1. Intimidación → Maestro (prioridad 1)
2. Detección Mentiras → Experto (prioridad 2)
3. Gestión Conflictos → Experto (violencia)

**Playstyle:** Autoritario, temido
**Fortaleza:** Criminales te temen, confesan fácil
**Debilidad:** Facción legal te odia

---

### Ruta del Mercader

**Prioriza:**
1. Negociación → Maestro (prioridad 1)
2. Conocimiento Bebidas → Maestro (prioridad 2)
3. Diplomacia → Competente (facciones comerciales)

**Playstyle:** Capitalista puro
**Fortaleza:** Máxima ganancia económica
**Debilidad:** No especializado en detección

---

### Ruta Balanceada

**Prioriza:**
- Todas las categorías → Competente (300 XP cada una)
- 1-2 → Experto (favoritas)

**Playstyle:** Versátil, adaptable
**Fortaleza:** Sin debilidades críticas
**Debilidad:** No domina nada

---

## 🏆 ACHIEVEMENTS RELACIONADOS

**"Primera Maestría"** - Alcanza Maestro en cualquier categoría

**"Doble Maestro"** - Alcanza Maestro en 2 categorías

**"Trinidad Perfecta"** - Alcanza Maestro en 3 categorías (muy difícil)

**"Verificador Perfecto"** - 100 documentos falsos detectados consecutivos

**"Pacificador"** - Resuelve 50 conflictos sin violencia

**"Magnate"** - Acumula 20,000 monedas

**"Diplomático Universal"** - +60 con 7+ facciones simultáneamente

**"Señor del Miedo"** - Haz confesar a 100 criminales

**"Sommelier Maestro"** - Sirve bebida perfecta 200 veces

**"Leyenda"** - Completa el juego con 3 Maestrías

---

## 📂 ARCHIVOS DEL SISTEMA

- `README.md` ← Estás aquí (overview)
- `arboles-habilidades.md` - Detalles de cada habilidad
- `balance-xp.md` - Números, balanceo, progresión
- `especializaciones.md` - Guías de builds recomendados
- `RESUMEN-EJECUTIVO.md` - Estado del sistema

---

**Sistema de Progresión:** Recompensa maestría y especialización, no grinding.
