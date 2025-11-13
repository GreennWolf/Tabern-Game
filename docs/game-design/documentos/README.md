# 📜 Sistema de Documentos

Este sistema define todos los documentos que los clientes deben presentar, cómo verificarlos, detectar falsificaciones y las consecuencias de errores.

**Inspiración:** Papers, Please - verificación detallada de documentos es CORE MECHANIC del juego.

---

## 🎯 FILOSOFÍA DE DISEÑO

### Core Loop

```
1. Cliente llega → Presenta documentos
2. Jugador examina → Verifica datos
3. Jugador compara → Busca inconsistencias
4. Jugador decide → Servir / Rechazar / Llamar Guardia
5. Consecuencias → Ganancia / Pérdida / Reputación
```

### Complejidad Progresiva

**Early Game (Días 1-14):**
- Solo ID Básica (raza, edad, nombre)
- Verificación simple: edad legal, raza coincide
- Falsificaciones obvias (foto no coincide)

**Mid Game (Días 15-60):**
- Múltiples documentos (ID + Permiso de Armas + Afiliación Facción)
- Verificación cruzada: datos deben coincidir entre documentos
- Falsificaciones medianas (sellos incorrectos, fechas inconsistentes)

**Late Game (Día 61+):**
- 3-5 documentos simultáneos
- Reglas cambiantes diarias (Libro de Reglas)
- Falsificaciones maestras (duendes expertos)
- Dilemas morales (documento falso pero razón válida)

---

## 📋 TIPOS DE DOCUMENTOS

### 1. Documentos Obligatorios (Todos los clientes)

**Identificación Personal (ID):**
- Nombre completo
- Raza
- Edad
- Retrato (sprite del cliente)
- Firma
- Fecha de emisión
- Autoridad emisora

---

### 2. Documentos Condicionales

**Permiso de Porte de Armas:**
- Requerido si cliente porta arma visible
- Especifica: tipo de arma, clase del portador, fecha de vencimiento

**Licencia de Uso de Magia:**
- Requerido para clases mágicas (Mago, Hechicero, Clérigo, Druida)
- Especifica: escuela de magia, nivel permitido, restricciones

**Certificado de Afiliación a Facción:**
- Requerido si cliente representa una facción oficial
- Especifica: facción, rango, privilegios

**Permiso de Entrada a la Ciudad:**
- Requerido para razas "exóticas" (Minotauro, Dracónido) según reglas
- Especifica: duración de estancia, propósito de visita

**Certificado de Pureza Divina:**
- Requerido para Paladines/Clérigos en ciertas fases del juego
- Emitido por templo, demuestra alineación

---

### 3. Documentos Especiales

**Orden de Detención:**
- TÚ recibes esto de la guardia
- Lista de criminales buscados (foto, nombre, recompensa)
- Si sirves a un criminal buscado → multa/arresto

**Libro de Reglas del Día:**
- TÚ recibes esto cada mañana
- Lista de restricciones actuales (ej: "Prohibido servir a Minotauros hoy")
- Cambia diariamente/semanalmente

**Pase VIP:**
- Documento raro, emitido por el Rey/Gobernador
- Permite excepciones a las reglas
- Puede ser falsificado (alto riesgo)

---

## 🔍 ELEMENTOS A VERIFICAR

### Verificación Visual

**Comparar Retrato vs Cliente Real:**
- Sprite del documento debe coincidir con sprite del cliente
- Raza obvia (Enano vs Elfo vs Humano)
- Detalles físicos (color de piel, cuernos, alas)

**Glamour Élfico:**
- Elfos jóvenes pueden usar glamour para aparentar más edad
- Si sospechas → Sirve Cerveza de Glamour → Glamour se rompe → Revela edad real

---

### Verificación de Datos

**Nombre:**
- Debe coincidir en TODOS los documentos
- Variación sospechosa: "Juan Pérez" en ID, "J. Perez" en Permiso de Armas (puede ser legítimo o error)

**Raza:**
- ID dice "Elfo" → Cliente DEBE ser Elfo
- Si no coincide → Falsificación obvia o robo de identidad

**Edad:**
- Debe ser legal para beber (según raza):
  - Humano: 18+ años
  - Enano: 30+ años
  - Elfo: 80+ años (madurez élfica)
  - Minotauro: 15+ años
  - Centauro: 20+ años
- Debe coincidir con apariencia (con trampa de glamour élfico)

**Clase:**
- Si porta arma → Permiso debe especificar clase compatible
  - Guerrero con espada: ✓ OK
  - Mago con espada: ❌ Sospechoso (Magos no usan espadas normalmente)

**Fecha de Emisión:**
- No puede ser futura (documento emitido "mañana" → falsificación)
- No puede ser demasiado antigua (IDs vencen cada 10 años)

**Autoridad Emisora:**
- Debe ser legítima:
  - "Consejo de Ancianos de Bosque Verde" → ✓ Facción conocida
  - "Consejo de Ancianos de Bosque Oscuro Inexistente" → ❌ Falsificación

---

### Verificación de Autenticidad

**Sello Oficial:**
- Cada facción/autoridad tiene sello único
- Falsificaciones usan sellos incorrectos o borrosos
- Puedes comparar con "Catálogo de Sellos Oficiales" (en tu taberna)

**Firma:**
- Debe estar presente
- Puede ser ilegible pero debe existir
- Ausencia de firma → Documento incompleto

**Calidad del Papel:**
- Documentos oficiales: papel de calidad (visual "limpio")
- Falsificaciones baratas: papel deteriorado, manchas
- Falsificaciones maestras: indistinguibles (Duendes)

---

### Verificación Cruzada

**Múltiples Documentos:**

Ejemplo 1:
```
ID dice: "Juan, Humano, 25 años, Guerrero"
Permiso de Armas dice: "Juan, Elfo, 120 años, Mago"
→ ❌ INCONSISTENCIA CRÍTICA
```

Ejemplo 2:
```
ID dice: "Thorin, Enano, 45 años"
Licencia de Magia dice: "Thorin, Enano, 45 años, Mago"
→ ❌ IMPOSIBLE (Enanos no pueden ser Magos)
```

Ejemplo 3:
```
ID dice: "Legolas, Elfo Bosque, 120 años, Bárbaro"
→ ❌ IMPOSIBLE (Elfos del Bosque no pueden ser Bárbaros)
```

---

## 🎮 MECÁNICA DE VERIFICACIÓN

### Interfaz de Inspección

**Vista Expandida de Documento:**
1. Jugador hace clic en documento → Se expande en pantalla
2. Puede hacer zoom en detalles (sello, firma, retrato)
3. Puede comparar lado a lado con otros documentos
4. Puede consultar "Catálogo de Sellos" o "Libro de Reglas"

**Herramientas de Verificación:**

**Lupa (gratis):**
- Examina detalles pequeños
- Revela calidad del papel
- Muestra microimpresiones en sellos auténticos

**Luz UV (50 monedas, upgrade):**
- Revela marcas de seguridad invisibles
- Documentos reales tienen marca UV
- Falsificaciones no (excepto maestras)

**Escáner de Magia (200 monedas, upgrade):**
- Detecta magia residual en documentos
- Falsificaciones mágicas (Duendes) brillan diferente
- Solo funciona si TÚ tienes sensibilidad mágica (o contratas a Mago)

---

### Sistema de Sospecha

**Indicadores Visuales:**

**Sin Sospecha (Verde):**
- Todo parece correcto
- Peligro: Falsificación maestra puede parecer legítima

**Sospecha Leve (Amarillo):**
- Algo no cuadra (ej: edad en límite legal, sello ligeramente borroso)
- Puedes servir bajo tu propio riesgo
- O puedes investigar más (hacer preguntas, pedir más documentos)

**Sospecha Alta (Rojo):**
- Inconsistencia crítica detectada
- Recomendado: NO servir o llamar a guardia

**Certeza de Falsificación (Rojo parpadeante):**
- Error obvio (fecha futura, raza imposible con clase)
- Debes rechazar o arrestar

---

### Decisiones del Jugador

Cuando detectas problema:

**1. Servir de todos modos:**
- Riesgo: Si es criminal/menor → Multa, pérdida de reputación
- Beneficio: Cliente paga, evitas confrontación
- Moral: ¿Está bien ignorar reglas por dinero?

**2. Rechazar entrada:**
- Riesgo: Si documento era legítimo → Cliente enfadado, pérdida de ganancia
- Beneficio: Seguridad, cumples la ley
- Consecuencia: Algunos clientes con documentos raros legítimos se ofenden

**3. Llamar a la Guardia:**
- Riesgo: Si documento era legítimo → Demanda, multa por falsa acusación (100 monedas)
- Beneficio: Si era criminal → Recompensa (50-500 monedas)
- Consecuencia: Facción del cliente pierde reputación contigo

**4. Hacer preguntas al cliente:**
- "¿Por qué tu ID dice 150 años pero aparentas 25?"
  - Respuesta legítima: "Soy Elfo, usamos glamour"
  - Respuesta sospechosa: "Eh... olvida eso..."
- Basado en propensión a mentir (Raza + Clase)

**5. Pedir documento adicional:**
- "Muéstrame tu Certificado de Pureza Divina ya que eres Paladín"
- Si no lo tiene → Sospecha aumenta
- Si lo inventa en el momento → Falsificación confirmada

---

## 📊 PROGRESIÓN DEL SISTEMA

### Early Game: Tutorial de Verificación

**Días 1-7:**
- Solo ID Básica requerida
- Verificación simple: edad, raza
- Falsificaciones OBVIAS:
  - Retrato no coincide
  - Edad bajo mínimo legal
  - Sin firma
- 90% documentos legítimos
- Consecuencias leves por error

---

### Mid Game: Complejidad Aumenta

**Días 8-30:**
- 2-3 documentos por cliente
- Verificación cruzada requerida
- Reglas comienzan a cambiar (Libro de Reglas semanal)
- Falsificaciones MEDIANAS:
  - Sello incorrecto
  - Fechas inconsistentes entre documentos
  - Nombre con variación menor
- 70% documentos legítimos
- Consecuencias medianas por error (50-100 monedas multa)

---

### Late Game: Maestría Requerida

**Día 31+:**
- 3-5 documentos por cliente
- Reglas cambian DIARIAMENTE
- Órdenes de detención activas
- Falsificaciones MAESTRAS (Duendes):
  - Perfectas visualmente
  - Requieren herramientas avanzadas (UV, Escáner Magia)
  - Solo detectables por inconsistencias lógicas
- 50% documentos legítimos (tú decides en quién confiar)
- Consecuencias severas por error (200-500 monedas, cierre temporal)
- Dilemas morales:
  - Refugiado con documentos falsos pero historia trágica
  - Criminal con documentos perfectos
  - Orden de detención contra cliente regular bueno

---

## 🎭 INTEGRACIÓN CON OTROS SISTEMAS

### Con Razas

**Elfos y Glamour:**
- Documento dice 80 años (legal)
- Apariencia: 20 años humanos
- Sirves Cerveza de Glamour → Glamour cae → Aparenta 15 años humanos (60 años élficos reales)
- Conclusión: ¡Es menor! Documento falso

**Duendes y Falsificación:**
- Propensión a mentir: 9/10
- Habilidad especial: Falsificación maestra
- 40% de Duendes tienen documentos falsos (vs 5% otras razas)
- Requieren escrutinio extra

**Minotauros y Regulación:**
- Frecuentemente requieren "Permiso de Entrada" (regulación racial)
- Si regla del día dice "Prohibido Minotauros" → Debes rechazar INCLUSO con documentos perfectos

---

### Con Clases

**Paladín:**
- Siempre tiene documentos legítimos (propensión mentir: 1/10)
- Si detectas falsificación en Paladín → ERROR TUYO o impostor

**Pícaro:**
- Propensión a mentir: 9/10
- 50% de Pícaros tienen documentos falsos o robados
- Maestros del engaño (pueden tener 3 IDs diferentes)
- Algunos tienen documentos "demasiado perfectos" (robados de autoridades)

**Artífice:**
- Pueden fabricar documentos falsos tecnológicos (no mágicos)
- Falsificaciones difíciles de detectar sin herramientas

---

### Con Facciones

**Gremio de Ladrones:**
- Miembros frecuentemente usan alias
- Documentos pueden ser robados o falsificados
- Si tienes alta reputación con ellos → Toleran que los atrapes ocasionalmente

**Templo de la Luz:**
- Documentos siempre impecables
- Alta confianza (pero impostores usan sus sellos)

**Guardia Real:**
- Presenta órdenes de detención
- Tú DEBES cumplir o enfrenta consecuencias severas

---

### Con Bebidas

**Poción de Verdad:**
- Sirves a cliente sospechoso
- Cliente borracho nivel 2 → NO PUEDE mentir
- Pregunta: "¿Es este tu documento real?"
- Respuesta forzada: "No, es falso..."
- Confirma tu sospecha

---

### Con Eventos

**Inspección Sorpresa:**
- Inspector llega, revisa tus registros
- Si serviste a menores/criminales → Multa retroactiva
- Si rechazaste correctamente → Bonificación

**Festival de Facción:**
- Durante Festival Élfico: 200% Elfos
- Muchos usan glamour → Verificación difícil
- Oportunidad de usar Cerveza de Glamour estratégicamente

---

## 📈 ESTADÍSTICAS DE FALSIFICACIÓN

### Por Raza (% documentos falsos)

| Raza | % Falsos | Razón |
|------|----------|-------|
| Humano | 10% | Promedio, algunos criminales |
| Enano | 5% | Honorables, raramente falsifican |
| Elfo Bosque | 3% | Altamente honorables |
| Elfo Noche | 15% | Cultura de sigilo, algunos usan alias |
| Duende | 40% | Maestros falsificadores |
| Minotauro | 8% | Directos, pero algunos indocumentados |
| Dracónido | 12% | Algunos usan identidades falsas (linaje) |
| Centauro | 2% | Extremadamente honorables |

---

### Por Clase (% documentos falsos)

| Clase | % Falsos | Razón |
|-------|----------|-------|
| Guerrero | 5% | Disciplinados, legales |
| Paladín | 1% | Sagrados, NUNCA falsifican |
| Bárbaro | 15% | No entienden burocracia, usan documentos robados |
| Monje | 2% | Disciplinados, honestos |
| Mago | 8% | Algunos renegados sin licencia |
| Hechicero | 20% | Muchos no tienen licencia legal (magia innata) |
| Clérigo | 3% | Religiosos, honestos |
| Druida | 10% | Rechazan burocracia, algunos indocumentados |
| Pícaro | 50% | Maestros del engaño |
| Bardo | 25% | Viajeros, múltiples identidades |
| Guardabosques | 12% | Viven fuera de ciudades, algunos sin papeles |
| Artífice | 6% | Legales pero algunos falsifican tecnológicamente |
| Plebeyo | 8% | Promedio, algunos pobres sin acceso |

---

## 🎯 OBJETIVOS DE DISEÑO

1. **Tensión constante:** Cada cliente es un mini-puzzle
2. **Maestría progresiva:** Jugador mejora con experiencia
3. **Decisiones morales:** No siempre blanco/negro
4. **Integración profunda:** Documentos conectan con TODOS los sistemas
5. **Rejugabilidad:** Reglas cambiantes hacen cada partida única

---

## 📂 ESTRUCTURA DE ARCHIVOS

- `README.md` ← Estás aquí (overview general)
- `tipos-documentos.md` - Plantillas detalladas de cada documento
- `verificacion.md` - Guía paso a paso de verificación
- `falsificaciones.md` - Tipos de falsificaciones y cómo detectarlas
- `errores-consecuencias.md` - Sistema de multas, reputación, game over

---

**Sistema de documentos:** Core mechanic inspirado en Papers Please, integrado profundamente con todos los sistemas del juego.
