# 📋 RESUMEN EJECUTIVO - Sistema de Clases

## ✅ Estado: COMPLETO Y DEFINIDO

Fecha: 2025-11-13

---

## 📦 Contenido del Sistema

### Clases Implementadas: 13

#### Clases Marciales (4)
1. ✅ **Guerrero** - Disciplinado, maestro del combate
2. ✅ **Paladín** - Caballero sagrado, código absoluto
3. ✅ **Bárbaro** - Furia salvaje, destructivo
4. ✅ **Monje** - Disciplina interior, letal sin armas

#### Clases Mágicas (4)
5. ✅ **Mago** - Erudito arcano, magia estudiada
6. ✅ **Hechicero** - Magia innata caótica
7. ✅ **Clérigo** - Servidor divino
8. ✅ **Druida** - Guardián natural, forma salvaje

#### Clases Expertas (3)
9. ✅ **Pícaro** - Maestro del engaño, MÁXIMA mentira
10. ✅ **Bardo** - Artista carismático, encantador
11. ✅ **Guardabosques** - Explorador, compañero animal

#### Clases Especiales (2)
12. ✅ **Artífice** - Inventor mágico-mecánico
13. ✅ **Plebeyo** - Sin clase, gente común

---

## 📁 Estructura de Archivos

```
docs/game-design/clases/
├── README.md                    # Índice, sistema de aparición, reglas
├── comparacion-clases.md        # Tablas comparativas completas
├── RESUMEN-EJECUTIVO.md         # Este archivo
│
├── guerrero.md                  # Especificación completa
├── paladin.md                   # Especificación completa
├── barbaro.md                   # Especificación completa
├── monje.md                     # Especificación completa
│
├── mago.md                      # Especificación completa
├── hechicero.md                 # Especificación completa
├── clerigo.md                   # Especificación completa
├── druida.md                    # Especificación completa
│
├── picaro.md                    # Especificación completa
├── bardo.md                     # Especificación completa
├── guardabosques.md             # Especificación completa
│
├── artifice.md                  # Especificación completa
└── plebeyo.md                   # Especificación completa
```

---

## 🎯 Especificación Completa por Clase

Cada archivo incluye:

- ✅ **Descripción y Rol Social**
- ✅ **Razas Comunes** (probabilidades)
- ✅ **Comportamiento General**
- ✅ **Propensión a Mentir** (modificador)
- ✅ **Restricciones de Bebida** (por código/cultura)
- ✅ **Comportamiento Borracho** (3 niveles + efecto especial)
- ✅ **Actitud hacia Armas** (resistencia al desarme)
- ✅ **Lealtades y Facciones**
- ✅ **Habilidades Especiales**
- ✅ **Verificación** (multicapa: documentos, apariencia, comportamiento, diálogo)
- ✅ **Eventos Especiales**
- ✅ **Rangos por Edad**
- ✅ **Riesgos y Beneficios**
- ✅ **Notas de Juego**
- ✅ **Combinaciones Raza-Clase**

---

## 📊 Datos Clave del Sistema

### Distribución de Dificultad

| Nivel | Cantidad | Clases |
|-------|----------|--------|
| Muy Baja | 1 | Plebeyo |
| Baja | 2 | Monje, Guardabosques |
| Media | 5 | Guerrero, Bardo, Clérigo, Druida, Artífice |
| Alta | 2 | Mago, Paladín, Bárbaro |
| Muy Alta | 3 | Pícaro, Hechicero |

### Distribución de Honestidad

| Honestidad | Clases |
|------------|--------|
| Casi Imposible Mentir (1-2) | Paladín, Monje, Clérigo |
| Muy Honestos (3-4) | Guerrero, Druida, Guardabosques, Bárbaro, Artífice |
| Moderados (5-6) | Mago, Hechicero |
| Mentirosos (7-9) | Bardo, Pícaro |

### Peligro Borracho (Nivel 3)

| Peligro | Clases |
|---------|--------|
| 🔴 Catastrófico | Hechicero, Bárbaro (Minotauro) |
| 🔴 Crítico | Mago, Paladín, Clérigo, Monje |
| 🟠 Alto | Guerrero, Druida, Artífice |
| 🟡 Moderado | Pícaro, Bardo, Guardabosques |
| 🟢 Bajo | Plebeyo |

---

## 🎮 Progresión Temporal

### Early Game (Días 1-10)
- **80% Plebeyos** (tutorial)
- **15% Guerreros** (introducción a clases)
- **5% Artesanos**

**Objetivo:** Aprender mecánicas básicas sin complejidad de clase

### Mid Game (Días 11-20)
- **40% Plebeyos**
- **20% Guerreros**
- **10% Pícaros** (introducen engaño maestro)
- **10% Bardos**
- **5% cada:** Mago, Clérigo, Guardabosques, Bárbaro

**Objetivo:** Complejidad, engaño, magia, conflictos

### Late Game (Días 21+)
- **20% Plebeyos** (descanso)
- Distribución equilibrada del resto
- Aparecen clases raras: Paladín (3%), Monje (2%), Druida (3%), Hechicero (4%), Artífice (3%)

**Objetivo:** Máxima complejidad, todas las mecánicas

---

## ⚔️ Sistema de Armas

### Regla Variable
- Algunos días: Armas PROHIBIDAS
- Otros días: Armas PERMITIDAS
- El jugador verifica en el Libro del día

### Resistencia al Desarme (Clase + Raza combinadas)

**Fórmula de Resistencia:**
- Clase base (ninguna/baja/media/alta/extrema)
- + Modificador racial
- = Resistencia final

**Ejemplo:**
- Enano Guerrero: Alta (clase) + 1 (raza) = MUY ALTA
- Minotauro Bárbaro: Extrema (clase) + 2 (raza) = **IMPOSIBLE**

### Excepciones
- **Paladines con licencia:** Pueden portar armas legalmente
- **Guardias locales:** Exentos
- **Magos:** Argumentan que "báculo no es arma"

---

## 🚫 Restricciones Raza-Clase

### ENANOS - NO MAGIA/DEIDADES

**Regla fundamental:** Enanos NO creen en magia ni deidades

❌ **Prohibido:**
- Mago (0%)
- Hechicero (0%)
- Clérigo (0%)
- Druida (0%)

⚠️ **Excepción única:**
- **Artífice:** Aceptable porque es "ingeniería arcana" NO "magia"
- Enanos lo ven como artesanía mejorada, no hechicería

✅ **Común:**
- Guerrero (40%)
- Artífice (25%)
- Bárbaro, Pícaro, Monje (resto)

### Otras Restricciones Culturales

**Elfos del Bosque:**
- ❌ Bárbaro (1% - opuesto a refinamiento)
- ✅✅✅ Druida, Guardabosques, Mago

**Elfos de la Noche:**
- ❌ Clérigo de luz, Paladín (0%)
- ✅✅✅ Pícaro, Monje, Guardabosques

**Minotauros:**
- ❌ Clases mágicas (1-2%)
- ✅✅✅ Guerrero, Bárbaro (80%)

**Centauros:**
- ❌ Pícaro (0% - deshonroso)
- ✅✅✅ Druida, Guardabosques, Monje

**Duendes:**
- ❌ Guerrero, Paladín (1-2%)
- ✅✅✅ Pícaro (60%), Bardo (20%)

**Dracónidos:**
- ✅ Cualquier clase (más versátiles)
- ✅✅✅ Hechicero (30% - magia innata dracónica)

**Humanos:**
- ✅ Cualquier clase sin restricción (más versátiles)

---

## 💥 Efectos Especiales por Clase (Borracho Nivel 3)

| Clase | Efecto | Daño Estimado |
|-------|--------|---------------|
| **Hechicero** | Oleada mágica masiva | 200-500 monedas |
| **Bárbaro** | Furia destructiva | 200-400 monedas |
| **Mago** | Magia salvaje | 100-300 monedas |
| **Guerrero** | Instinto marcial | 100-200 monedas |
| **Monje** | Técnicas letales | 100-200 monedas |
| **Artífice** | Invento explota | 50-200 monedas |
| **Druida** | Transformación animal | 50-150 monedas |
| **Guardabosques** | Animal companion | 50-100 monedas |
| **Pícaro** | Robo compulsivo | 20-100 monedas |
| **Clérigo** | Invocación divina | Variable |
| **Paladín** | Crisis de fe | Psicológico |
| **Bardo** | Canción ofensiva | Indirecto |

---

## 🎭 Verificación Multicapa

El jugador debe usar **TODOS** estos métodos:

### 1. Documentos de Gremio
- Guerrero: Sello militar
- Mago: Círculo arcano
- Paladín: Orden sagrada
- **Pícaro: NO TIENEN** (o son FALSOS)

### 2. Apariencia Visual
- Armadura, túnicas, símbolos
- Herramientas, armas, instrumentos
- Estado físico (cicatrices, músculos, etc.)

### 3. Armas que Porta
- Guerrero: Espada, escudo
- Mago: Báculo
- Pícaro: Dagas ocultas
- Paladín: Arma sagrada

### 4. Diálogo (IA)
- Vocabulario específico
- Conocimiento de oficio
- Consistencia en historia

### 5. Comportamiento
- Postura, movimientos
- Reacciones
- Interacción con entorno

**Si hay contradicciones = MENTIRA**

---

## 🎲 Eventos Especiales por Clase

### Inspecciones (Late Game)
- **Paladín Inspector** (Día 15+) - Inspección moral CRÍTICA
- **Círculo de Magos** (Día 18+) - Magia ilegal
- **Clérigo Inquisidor** (Día 18+) - Caza herejes

### Caos/Violencia
- **Bárbaro en Furia** (Día 20+) - Destrucción masiva
- **Magia Salvaje** (Día 16+) - Mago borracho
- **Oleada Mágica** (Día 22+) - Hechicero borracho
- **Duelo** (Variable) - Combate entre clientes

### Gremios/Organizaciones
- **Gremio de Ladrones** (Día 14+) - Pícaros reclutan
- **Duelo de Bardos** (Día 12+) - Competencia
- **Círculo Druídico** (Día 19+) - Reunión

### Beneficios
- **Monje Zen** (Día 22+) - Enseña técnica (+habilidad permanente)
- **Clérigo Sanador** (Día 13+) - Cura gratis
- **Artífice** (Día 17+) - Vende upgrades

---

## 🎯 Top 5 Combinaciones Más Difíciles

### 1. Duende Pícaro
- **PESADILLA ABSOLUTA**
- Mentira (9+9), falsificación maestra, sigilo
- Probabilidad detección: 10%

### 2. Elfo de la Noche Pícaro
- Sigilo + glamour + mentiras
- Asesino perfecto
- Extremadamente peligroso

### 3. Minotauro Bárbaro
- Fuerza + furia = catástrofe
- Imposible desarmar
- Daño: 500+ monedas

### 4. Dracónido Hechicero (Cromático)
- Aliento + oleada mágica
- Doble peligro
- Daño: 300-700 monedas

### 5. Paladín Inspector
- Detecta TODO ilegal
- Puede cerrar taberna
- Imposible engañar

---

## 🔧 Sistemas Afectados

### Integración con Otros Sistemas

✅ **Sistema de Razas:**
- Restricciones (Enanos NO magia)
- Probabilidades combinadas
- Stats aditivos/multiplicativos

✅ **Sistema de Documentos:**
- Cada clase tiene tipo de documento
- Pícaros falsifican todo
- Verificación específica

✅ **Sistema de Armas:**
- Actitud por clase
- Resistencia combinada raza+clase
- Negociación según clase

✅ **Sistema de Diálogo IA:**
- Propensión a mentir por clase
- Vocabulario específico
- Personalidad base

✅ **Sistema de Eventos:**
- Eventos específicos por clase
- Inspecciones por gremios
- Conflictos entre clases

✅ **Sistema de Facciones:**
- Cada clase tiene lealtades
- Órdenes, gremios, círculos
- Conflictos inter-clase

✅ **Sistema de Economía:**
- Clases raras pagan más
- Daño por clase (borracho)
- Upgrades específicos

---

## 📈 Curva de Aprendizaje

### Fase 1: Tutorial (Días 1-5)
- Solo Plebeyos + Guerreros
- Mecánicas básicas
- Sin complejidad de clase

### Fase 2: Introducción (Días 6-10)
- Primeros Pícaros
- Aprender detección de mentiras
- Introducción a falsificación

### Fase 3: Complejidad (Días 11-15)
- Clases mágicas
- Nuevos peligros (magia)
- Múltiples clases simultáneas

### Fase 4: Maestría (Días 16-20)
- Clases expertas
- Combinaciones difíciles
- Eventos complejos

### Fase 5: Dominio (Días 21+)
- Todas las clases posibles
- Combinaciones extremas
- Máximo desafío

---

## 🎲 Balanceo

### Frecuencia de Clases

**Early:** 95% sin clase o simple → Tutorial sin frustración
**Mid:** 60% simple → Desafío moderado pero manejable
**Late:** 40% simple → Alto desafío, requiere maestría

### Eventos Especiales

NO todos los días son caos:
- Días tranquilos (solo plebeyos)
- Días moderados (mezcla)
- Días caóticos (evento especial)
- **Boss Days:** Paladín Inspector, Minotauro Bárbaro, etc.

### Recompensa vs Riesgo

Clases difíciles/raras:
- Pagan MÁS (oro, propinas, información)
- Riesgo ALTO (destrucción, cierres, multas)
- Reputación si manejas bien

---

## 🔍 Estrategias Recomendadas

### Para el Jugador

**Detección:**
1. Verificar TODOS los documentos
2. Preguntas cruzadas (buscar contradicciones)
3. Observar comportamiento
4. Consultar libro sobre clase
5. No confiar en apariencia sola

**Manejo de Riesgo:**
1. Cortar alcohol a clases peligrosas (magos, bárbaros)
2. Si hay Paladín, asegura que TODOS sean legales
3. Pícaros: asumir mentira hasta probar honestidad
4. Minotauro Bárbaro: extrema precaución

**Económico:**
1. Clases raras = riesgo pero recompensa
2. Invertir en seguridad (guardias, trampas)
3. Seguro contra destrucción
4. Artífices venden upgrades valiosos

---

## ✏️ Próximos Sistemas a Definir

Con Razas y Clases completos, los siguientes son:

1. **Sistema de Bebidas** (tipos, efectos, restricciones)
2. **Sistema del Libro de Reglas** (leyes diarias/semanales)
3. **Sistema de Documentos** (IDs, falsificación, verificación)
4. **Sistema de Facciones** (organizaciones, conflictos, reputación)
5. **Sistema de Eventos** (narrativos, inspecciones, crisis)
6. **Sistema de Economía** (precios, costos, upgrades, progresión)
7. **Narrativa Principal** (arco de historia, finales múltiples)

---

## 📝 Notas Finales

### Fortalezas del Sistema

✅ **13 clases únicas** con personalidades distintas
✅ **Progresión clara:** Early → Mid → Late bien definida
✅ **Complejidad escalable:** De Plebeyo (simple) a Duende Pícaro (imposible)
✅ **Integración Raza+Clase:** Restricciones culturales, stats combinados
✅ **Verificación multicapa:** Documentos + Apariencia + Diálogo + Comportamiento
✅ **Efectos especiales únicos:** Cada clase tiene mecánica distinta borracho
✅ **Balanceo Riesgo/Recompensa:** Clases difíciles pagan mejor
✅ **Eventos específicos:** Cada clase desbloquea narrativas únicas
✅ **Dilemas morales:** Pícaros, Paladines Caídos, Gremios

### Consideraciones Técnicas

- Sistema modular: fácil editar/expandir
- Atributos numéricos claros para balanceo
- Probabilidades raza-clase definidas
- Efectos especiales programables
- IA puede generar diálogos específicos por clase
- Sistema de rangos por edad (escalado por longevidad racial)

### Modificaciones Futuras

El sistema permite:
- Agregar nuevas clases
- Subclases o especializaciones
- Variantes (Paladín Caído, Monje Borracho, etc.)
- Multiclase (futuro DLC?)
- Prestigio/rangos avanzados

---

## 🎉 SISTEMA COMPLETO Y LISTO

**Total de Archivos:** 16 archivos MD
**Total de Clases Especificadas:** 13/13 (100%)
**Nivel de Detalle:** Alto (cada clase >1500 palabras)
**Estado:** ✅ APROBADO PARA CONTINUAR

---

*Documento generado: 2025-11-13*
*Complementa: Sistema de Razas (completado)*
*Próxima revisión: Después de implementar Sistema de Bebidas*

---

## 🔗 Integración Razas + Clases

**Sistema de Razas:** 8 razas × ~2000 palabras = 16,000 palabras
**Sistema de Clases:** 13 clases × ~1500 palabras = 19,500 palabras
**Comparaciones y Matrices:** ~5,000 palabras

**TOTAL DOCUMENTACIÓN:** ~40,500 palabras
**Combinaciones posibles:** 8 razas × 13 clases = **104 arquetipos únicos**

Cada combinación Raza+Clase tiene:
- Stats únicos
- Comportamiento único
- Dificultad específica
- Eventos especiales potenciales

**El juego tiene profundidad masiva antes de tocar una línea de código.** 🚀
