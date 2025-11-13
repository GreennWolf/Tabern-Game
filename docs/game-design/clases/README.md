# ⚔️ Sistema de Clases - El Tabernero del Cruce

## Índice de Clases

Este directorio contiene las especificaciones completas de todas las clases del juego.

### Clases Disponibles (13)

#### Clases Marciales
1. [Guerrero](./guerrero.md) - Maestro del combate, disciplinado
2. [Paladín](./paladin.md) - Caballero sagrado, código de honor
3. [Bárbaro](./barbaro.md) - Furia salvaje, instintivo
4. [Monje](./monje.md) - Disciplina interior, abstinencia

#### Clases Mágicas
5. [Mago](./mago.md) - Erudito arcano, estudiado
6. [Hechicero](./hechicero.md) - Magia innata, caótico
7. [Clérigo](./clerigo.md) - Servidor divino, devoto
8. [Druida](./druida.md) - Guardián natural, primitivo

#### Clases Expertas
9. [Pícaro](./picaro.md) - Maestro del engaño, oportunista
10. [Bardo](./bardo.md) - Artista carismático, manipulador social
11. [Guardabosques](./guardabosques.md) - Explorador salvaje, solitario

#### Clases Especiales
12. [Artífice](./artifice.md) - Maestro de objetos mágicos, inventor
13. [Plebeyo](./plebeyo.md) - Sin entrenamiento formal, gente común

---

## Progresión de Aparición

### Early Game (Días 1-10)
- **80% SIN CLASE** (Plebeyos - granjeros, mercaderes, viajeros)
- **15% Guerrero** (guardias, soldados)
- **5% Artesano** (comerciantes, herreros)

### Mid Game (Días 11-20)
- **40% SIN CLASE**
- **20% Guerrero**
- **10% Pícaro**
- **10% Bardo**
- **5% Bárbaro**
- **5% Guardabosques**
- **5% Mago**
- **5% Clérigo**

### Late Game (Días 21+)
- **20% SIN CLASE**
- Distribución más equilibrada entre todas las clases
- Aparecen clases raras: Paladín (3%), Monje (2%), Druida (3%), Hechicero (4%), Artífice (3%)

---

## Restricciones Raza-Clase

Cada raza tiene restricciones lógicas basadas en su cultura, fisiología y lore.

---

### 👤 HUMANO

✅ **SIN RESTRICCIONES** - La raza más versátil
- Pueden ser cualquier clase sin penalización
- Adaptabilidad es su fortaleza racial

---

### ⚒️ ENANO (NO CREEN EN MAGIA/DEIDADES)

❌ **PROHIBIDO (0%):**
- Mago, Hechicero, Clérigo, Druida (NO creen en magia/deidades)
- Bardo (cultura seria, no son artistas refinados)

⚠️ **MUY RARO (1%):**
- Paladín (honor cultural extremo, NO magia divina)
- Monje (disciplina posible pero contra cultura)

✅ **COMÚN:**
- Guerrero (40%)
- Artífice (25%) - "ingeniería arcana" aceptable, NO magia
- Pícaro (15%)
- Bárbaro (10%) - enanos renegados
- Monje (5%)
- Guardabosques (4%)

**LORE:** Cultura de forja, artesanía, honor. Desprecian magia "débil". El arte es funcional, no decorativo.

---

### 🌲 ELFO DEL BOSQUE

❌ **PROHIBIDO (0-1%):**
- Bárbaro (opuesto a refinamiento élfico)
- Artífice (tecnología vs naturaleza)

⚠️ **RARO (3-5%):**
- Pícaro (considerado deshonroso)
- Clérigo (prefieren druidas, conexión directa con naturaleza)
- Guerrero (prefieren guardabosques)

✅ **MUY COMÚN:**
- Druida (40%)
- Mago (30%)
- Guardabosques (25%)

**LORE:** Refinados, longevos, conectados con naturaleza. Rechazan tecnología y comportamiento "bajo".

---

### 🌙 ELFO DE LA NOCHE

❌ **PROHIBIDO (0%):**
- Paladín (opuesto a cultura oscura)
- Clérigo de Luz (religión opuesta)
- Bardo (sigilo vs llamar atención)

⚠️ **RARO (2-5%):**
- Druida (solo círculos oscuros/lunares)
- Guerrero (prefieren sigilo)
- Hechicero (posible pero raro)
- Bárbaro (contra cultura disciplinada)

✅ **MUY COMÚN:**
- Pícaro (40%)
- Monje (25%)
- Guardabosques (15%)

**LORE:** Cultura de sombras, sigilo, pragmatismo. Rechazan atención y luz.

---

### 🎭 DUENDE

❌ **PROHIBIDO (0-1%):**
- Guerrero (demasiado pequeños para combate frontal)
- Paladín (imposible mantener código sagrado)
- Bárbaro (físicamente imposible)
- Monje (disciplina vs naturaleza traviesa)

⚠️ **MUY RARO (2-5%):**
- Clérigo (no son devotos, demasiado traviesos)
- Guardabosques (posible pero raro)
- Druida (prefieren trucos a naturaleza seria)

✅ **MUY COMÚN:**
- Pícaro (60%)
- Bardo (20%)
- Mago (10%)
- Hechicero (5%)
- Artífice (4%)

**LORE:** Pequeños, traviesos, ágiles. Viven del engaño y travesuras. Disciplina y honor no son lo suyo.

---

### 🐂 MINOTAURO

❌ **PROHIBIDO (0-1%):**
- Mago (cultura anti-intelectual)
- Hechicero (rechazan magia débil)
- Druida (separados de naturaleza, viven en laberintos)
- Bardo (no son artistas)
- Pícaro (demasiado grandes para sigilo, honor guerrero)

⚠️ **RARO (2-5%):**
- Clérigo (solo deidades de guerra/fuerza)
- Monje (disciplina posible pero raro)
- Guardabosques (más guerreros que exploradores)
- Artífice (algunos forjan armas)

✅ **MUY COMÚN:**
- Guerrero (45%)
- Bárbaro (40%)

**LORE:** Cultura de fuerza, honor de batalla, territorialidad. Desprecian astucia y magia. El combate directo es todo.

---

### 🐉 DRACÓNIDO

✅ **SIN RESTRICCIONES GENERALES** (versátiles por linaje)

**PERO depende del LINAJE:**

**Metálicos (Oro, Plata, Bronce):**
- ✅✅✅ Paladín, Guerrero, Clérigo de bien
- ❌ Pícaro asesino (deshonroso)
- ⚠️ Bárbaro (contra honor)

**Cromáticos (Rojo, Negro, Verde, Azul, Blanco):**
- ✅✅✅ Hechicero, Guerrero, Bárbaro
- ❌ Paladín (opuesto a naturaleza malvada)
- ⚠️ Clérigo (solo deidades oscuras)

**Distribución General:**
- Hechicero (30%) - magia innata dracónica
- Guerrero (25%)
- Paladín (15%) - metálicos
- Resto: distribuido

**LORE:** Linaje dracónico define todo. Honor vs poder, bien vs mal.

---

### 🐴 CENTAURO

❌ **PROHIBIDO (0%):**
- Pícaro (deshonroso, imposible sigilo por tamaño)
- Artífice (nómadas, rechazan tecnología)

⚠️ **RARO (2-5%):**
- Bárbaro (son sabios, no salvajes - pero tribus guerreras existen)
- Clérigo (prefieren druidas)
- Mago (algunos sabios pero raro)
- Hechicero (muy raro)
- Bardo (posible pero poco común)

✅ **MUY COMÚN:**
- Druida (30%)
- Guardabosques (25%)
- Monje (15%)
- Guerrero (10%) - guerreros tribales

**LORE:** Nómadas sabios, conexión con naturaleza, honor tribal. Rechazan tecnología y deshonra.

---

## Sistema de Rangos por Edad

Cada clase tiene rangos que dependen de la edad del personaje:

| Rango | Descripción | Edad (relativa a raza) | Comportamiento |
|-------|-------------|----------------------|----------------|
| Novato | Recién entrenado | 0-20% de vida adulta | Inseguro, cumple reglas |
| Experimentado | Veterano competente | 21-50% | Confiado, flexible |
| Veterano | Maestro del oficio | 51-80% | Sabio, respetado |
| Legendario | Héroe/leyenda | 81-100% | Poderoso, excepciones a reglas |

**Ejemplo para Humano Guerrero:**
- Novato: 18-25 años
- Experimentado: 26-45 años
- Veterano: 46-65 años
- Legendario: 66-80 años

**Ejemplo para Elfo Mago:**
- Novato: 120-200 años
- Experimentado: 201-450 años
- Veterano: 451-650 años
- Legendario: 651-750 años

---

## Sistema de Armas

### Regla Variable
Algunos días la taberna PROHÍBE armas, otros días NO.

**El jugador debe:**
1. Verificar regla del día (en el Libro)
2. Inspeccionar si el cliente porta armas
3. Negociar el desarme
4. Lidiar con resistencia según clase+raza

### Actitud por Clase hacia Desarme

| Clase | Actitud General | Resistencia |
|-------|----------------|-------------|
| Guerrero | "Mi arma es mi identidad" | Alta |
| Paladín | Cumple reglas (pero pide permiso especial) | Baja |
| Bárbaro | "Nunca me separo de mi arma" | Muy Alta |
| Monje | Sin armas (o no les importa) | Ninguna |
| Mago | "Mi báculo no cuenta como arma" | Media |
| Hechicero | Pocas armas, no les importa | Baja |
| Clérigo | Símbolo sagrado (¿es arma?) | Media |
| Druida | Armas naturales (bastón) | Media |
| Pícaro | Oculta armas fácilmente | Alta (engaño) |
| Bardo | Pocas armas | Baja |
| Guardabosques | Arco vital para identidad | Alta |
| Artífice | "Es una herramienta, no arma" | Media |
| Plebeyo | Generalmente sin armas | Ninguna |

### Actitud por Raza hacia Desarme

| Raza | Actitud | Modificador |
|------|---------|-------------|
| Humano | Variable | Neutral |
| Enano | "Es artesanía ancestral" | +1 Resistencia |
| Elfo del Bosque | Respetan reglas | -1 Resistencia |
| Elfo de la Noche | Desconfían, ocultan | +2 Resistencia |
| Duende | Ocultan fácilmente | +1 Engaño |
| Minotauro | "Es parte de mí" | +2 Resistencia |
| Dracónido | Depende de honor (linaje) | Variable |
| Centauro | Respetan, pero portan siempre | +1 Resistencia |

### Ejemplo de Combinaciones

**Enano Guerrero:**
- Resistencia: Alta (clase) + 1 (raza) = **MUY ALTA**
- Diálogo: "Este hacha la forjó mi abuelo. No se separa de mí."
- Probabilidad de dejar arma: 20%

**Elfo del Bosque Druida:**
- Resistencia: Media (clase) - 1 (raza) = **BAJA**
- Diálogo: "Entiendo las reglas. Dejaré mi bastón."
- Probabilidad de dejar arma: 80%

**Minotauro Bárbaro:**
- Resistencia: Muy Alta (clase) + 2 (raza) = **EXTREMA**
- Diálogo: "¿Quieres mi hacha? VEN Y TÓMALA."
- Probabilidad de dejar arma: 5%
- Consecuencia: Posible pelea si insistes

**Pícaro Duende:**
- Resistencia: Alta (engaño) + 1 (raza) = **ENGAÑO MAESTRO**
- Diálogo: "¡Claro! No tengo armas." (MIENTE, tiene 3 dagas ocultas)
- Probabilidad de detectar armas: 30%

---

## Verificación Multicapa de Clase

El jugador debe combinar TODOS estos métodos:

### 1. Documento de Gremio
- Guerrero: Sello de regimiento/ejército
- Mago: Licencia de círculo arcano
- Paladín: Orden sagrada
- Pícaro: ¡NO tienen documentos legales! (señal de alerta)
- Clérigo: Documentos de templo
- Druida: Círculo druídico
- Bardo: Licencia de artista
- Etc.

### 2. Apariencia Visual
- Guerrero: Armadura, cicatrices, postura militar
- Mago: Túnica, tinta en dedos, fatiga mental
- Bárbaro: Pieles, tatuajes tribales, salvaje
- Clérigo: Símbolo sagrado visible, túnica religiosa
- Pícaro: Ropa oscura, capucha, oculta rostro
- Bardo: Ropas coloridas, instrumento

### 3. Armas que Porta
- Guerrero: Espada, escudo
- Bárbaro: Hacha de guerra
- Guardabosques: Arco, flechas
- Mago: Báculo arcano
- Pícaro: Dagas (ocultas)
- Paladín: Espada sagrada

### 4. Diálogo (IA)
- Guerrero: Habla de batallas, disciplina
- Mago: Vocabulario académico, teorías
- Pícaro: Evasivo, dobles sentidos
- Bárbaro: Directo, agresivo
- Bardo: Carismático, cuentacuentos

### 5. Comportamiento
- Paladín: Honesto, rígido moralmente
- Pícaro: Toca cosas, observa salidas
- Mago: Lee, analiza
- Bárbaro: Impaciente, físicamente amenazante

**Si todo coincide = Probablemente honesto**
**Si hay contradicciones = Está mintiendo sobre su clase**

---

## Efectos Especiales por Clase (Borracho)

Cuando un cliente de cierta clase se emborracha, pueden ocurrir efectos únicos:

| Clase | Efecto Especial (Nivel 3 borracho) |
|-------|-----------------------------------|
| Mago | **Magia Salvaje** - Hechizos accidentales (fuego, transformación) |
| Hechicero | **Oleada Mágica** - Explosión caótica de magia |
| Bárbaro | **Furia Borracha** - Entra en frenesi, destroza todo |
| Clérigo | **Bendición/Maldición** - Invoca a su deidad sin control |
| Druida | **Forma Animal** - Se transforma parcialmente |
| Bardo | **Canción Ofensiva** - Insulta a todos con música |
| Paladín | **Crisis de Fe** - Rompe su código, consecuencias graves |
| Pícaro | **Robo Compulsivo** - Roba todo sin control |
| Monje | **Pierde Disciplina** - Pelea con técnicas letales |
| Guardabosques | **Animal Companion Aparece** - Invoca bestia |
| Artífice | **Invento Explota** - Dispositivo mágico falla |

---

## Eventos Especiales por Clase (Mid-Late Game)

### Aleatorios

**Inspector Paladín** (Día 15+)
- Orden sagrada inspecciona taberna
- Verifica MORALIDAD de clientes
- Penalización si serviste "corruptos"

**Duelo de Bardos** (Día 12+)
- Dos bardos rivales en taberna
- Competencia de insultos/música
- Puedes mediar o dejar que escale

**Círculo de Magos** (Día 18+)
- Investigación de magia ilegal
- Verifican si serviste hechiceros renegados
- Pueden detectar magia residual

**Gremio de Ladrones** (Día 14+)
- Pícaros reclutan en tu taberna
- Puedes cooperar (ilegal) o reportar
- Consecuencias en ambos casos

**Bárbaro en Furia** (Día 20+)
- Cliente bárbaro borracho destroza taberna
- Daño masivo
- Otros clientes huyen

**Monje Zen** (Día 22+)
- Monje anciano ofrece sabiduría
- Puede enseñarte técnica de detección
- Mejora permanente

---

## Plantilla de Clase

Cada clase incluye:

- **Descripción y Rol Social**
- **Razas Comunes** (probabilidades)
- **Comportamiento General**
- **Propensión a Mentir** (modificador)
- **Restricciones de Bebida**
- **Comportamiento Borracho** (efectos especiales)
- **Actitud hacia Armas**
- **Lealtades y Facciones**
- **Habilidades Especiales**
- **Verificación** (cómo identificar)
- **Eventos Especiales**
- **Rangos por Edad**
- **Notas de Juego**

---

## Notas de Diseño

### Complejidad Progresiva
- Early: Mayoría sin clase (simple)
- Mid: Clases comunes (Guerrero, Pícaro, Bardo)
- Late: Clases raras y peligrosas (Paladín, Monje, Hechicero)

### Balanceo
- Clases mágicas = Mayor peligro potencial
- Clases marciales = Mayor resistencia física
- Clases expertas = Mayor engaño

### Combinación Raza + Clase
- Stats se combinan (aditivos o multiplicativos según caso)
- Pueden crear contradicciones interesantes
- Ejemplo: Elfo Bárbaro (refinado vs salvaje)
