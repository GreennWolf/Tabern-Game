# 📊 Sistema de Reputación Detallado

Este documento define cómo funciona el sistema de reputación con cada facción, incluyendo mecánicas precisas, fórmulas y efectos.

---

## 🎯 ESCALA DE REPUTACIÓN

### Valores y Rangos

**Escala numérica:** -100 a +100

```
+80 a +100:  ★★★★★ HÉROE LEGENDARIO
+50 a +79:   ★★★★  ALIADO DE CONFIANZA
+20 a +49:   ★★★   AMISTOSO
 -19 a +19:  ★★    NEUTRAL
-20 a -49:   ★     HOSTIL
-50 a -79:          ENEMIGO
-80 a -100:         ENEMIGO MORTAL
```

### Punto de Partida

**Al inicio del juego:**
- Todas las facciones comienzan en **0 (Neutral)**
- Excepciones por trasfondo (futuro):
  - Si eres ex-guardia → Guardia Real: +10
  - Si tienes pasado criminal → Gremio de Ladrones: +5

---

## 💫 EFECTOS POR NIVEL DE REPUTACIÓN

### Nivel: ENEMIGO MORTAL (-80 a -100)

**Acciones de la Facción:**
- Ataques activos contra ti
- Intentan destruirte por completo
- Sin diálogo, sin redención

**Efectos Específicos:**

**Guardia Real:**
- Arresto inmediato al ser visto
- Embargo de bienes
- Cierre permanente de taberna
- Bounty en tu cabeza (otros jugadores/NPCs te cazan)

**Gremio de Ladrones:**
- Contrato de asesinato contra ti
- Incendio provocado
- Muerte de empleados
- Sabotaje total

**Templo de la Luz:**
- Excomunión pública
- Cruzada menor
- Maldición divina
- Destierro social

**Círculo Arcano:**
- Contramagia permanente en tu zona
- Maldición arcana potente
- Boicot total de magos

**Consecuencia General:**
- **GAME OVER probable** si no corriges rápido
- Requiere acción dramática para recuperar (-50 puntos mínimo)

---

### Nivel: ENEMIGO (-50 a -79)

**Acciones de la Facción:**
- Hostilidad activa
- Sabotaje regular
- Presión para cerrarte

**Efectos Específicos:**

**Guardia Real:**
- Inspecciones diarias agresivas
- Multas aumentadas +200%
- Acoso constante
- Clientes son intimidados (pierdes -20% clientela)

**Gremio de Ladrones:**
- Robos semanales (100-300 monedas)
- Sabotaje (veneno en stock, daño estructural)
- Falsificaciones abundantes (80% de pícaros tienen docs falsos)

**Templo de la Luz:**
- Boicot religioso masivo (-40% clientela buena)
- Sermones públicos contra ti
- Paladines inspectores constantes

**Círculo Arcano:**
- Pérdida de licencias mágicas
- Precio inflado pociones (+200%)
- Maldiciones menores (molestias diarias)

**Hermandad del Bosque:**
- Plagas serias (ratas, insectos)
- Hongos venenosos en almacén
- Boicot de razas naturales (-25% clientela)

**Consecuencia General:**
- Muy difícil operar normalmente
- Pérdidas económicas graves (-30 a -50% ganancia)
- Requiere esfuerzo activo para mejorar

---

### Nivel: HOSTIL (-20 a -49)

**Acciones de la Facción:**
- Frialdad, desconfianza
- Penalizaciones económicas
- Sabotaje ocasional

**Efectos Específicos:**

**Guardia Real:**
- Inspecciones cada 2-3 días
- Multas +50%
- Desconfianza (escrutinio extra en documentos)

**Gremio de Ladrones:**
- Robos menores cada 3-5 días (20-80 monedas)
- Falsificaciones aumentan +40%
- Sin protección (otros criminales pueden atacarte)

**Templo de la Luz:**
- Boicot parcial (-15% clientela devota)
- Pérdida de bendiciones
- Presión moral

**Círculo Arcano:**
- Revocación licencias menores
- Precio alto en pociones (+50%)
- Inspecciones mágicas

**Gremio de Comerciantes:**
- Precios aumentados +30%
- Sin descuentos
- Retraso en entregas

**Consecuencia General:**
- Operación posible pero incómoda
- Pérdidas moderadas (-10 a -20% ganancia)
- Recuperación factible con esfuerzo

---

### Nivel: NEUTRAL (-19 a +19)

**Acciones de la Facción:**
- Relación estándar de negocio
- Sin bonos ni penalizaciones

**Efectos:**
- Precios normales
- Sin beneficios especiales
- Sin persecución

**Notas:**
- Estado default del juego
- La mayoría de jugadores permanecen aquí con varias facciones
- Zona "segura" pero sin ventajas

---

### Nivel: AMISTOSO (+20 a +49)

**Acciones de la Facción:**
- Relación positiva
- Descuentos y favores menores
- Protección leve

**Efectos Específicos:**

**Guardia Real:**
- Inspecciones cada 7 días (reducidas)
- Multas reducidas -20%
- Guardias responden rápido a llamadas
- Información sobre órdenes de detención

**Gremio de Ladrones:**
- Protección básica (-50% robos de terceros)
- Algunos clientes VIP del gremio
- Precio normal en mercado negro

**Templo de la Luz:**
- Bendición semanal (+5% ganancia 1 día)
- Clientes devotos frecuentes (+10% clientela buena)
- Sanación ocasional gratis

**Círculo Arcano:**
- Descuento pociones -10%
- Licencia para pociones básicas
- Consejo mágico ocasional

**Gremio de Comerciantes:**
- Descuento suministros -15%
- Acceso prioritario a productos raros
- Información de mercado

**Hermandad del Bosque:**
- Descuento ingredientes naturales -20%
- Advertencias sobre clima
- Clientes pacíficos frecuentes

**Consecuencia General:**
- Bonificación leve (+5 a +10% ganancia)
- Acceso a recursos exclusivos
- Ambiente más seguro

---

### Nivel: ALIADO DE CONFIANZA (+50 a +79)

**Acciones de la Facción:**
- Relación estrecha
- Beneficios significativos
- Protección activa

**Efectos Específicos:**

**Guardia Real:**
- Inspecciones cada 15 días (mínimas)
- Multas reducidas -50%
- Guardia patrulla tu zona regularmente
- Acceso a órdenes de detención con recompensas
- Aviso previo de inspecciones

**Gremio de Ladrones:**
- Protección total contra crimen organizado
- Acceso completo a mercado negro
- Información valiosa (inspecciones, competidores)
- Ayuda para "eliminar problemas"
- Clientes VIP frecuentes (+20% ganancia en esos clientes)

**Templo de la Luz:**
- Bendiciones permanentes (+10% ganancia)
- Sanación gratis siempre
- Exorcismos gratuitos
- Reputación de "Taberna Santa" (+15% clientela buena)
- Paladines protegen activamente

**Círculo Arcano:**
- Descuento pociones -30%
- Enchantments gratuitos (protección fuego, anti-robo)
- Detección mágica semanal gratis
- Acceso a ingredientes arcanos raros
- Licencias completas

**Gremio de Comerciantes:**
- Descuento suministros -35%
- Préstamos sin interés (hasta 500 monedas)
- Acceso exclusivo a suministros raros
- Información privilegiada de mercado
- Prioridad absoluta en entregas

**Hermandad del Bosque:**
- Descuento ingredientes -40%
- Alarma natural (animales avisan de peligros)
- Bendición del bosque (plantas decorativas, +ambiente)
- Compañero animal ocasional
- Antídotos gratuitos

**Consecuencia General:**
- Bonificación significativa (+15 a +25% ganancia)
- Protección activa contra enemigos de la facción
- Acceso a misiones exclusivas
- Ventajas estratégicas importantes

---

### Nivel: HÉROE LEGENDARIO (+80 a +100)

**Acciones de la Facción:**
- Máximo honor y respeto
- Beneficios excepcionales
- Protección total

**Efectos Específicos:**

**Guardia Real:**
- Sin inspecciones (confianza absoluta)
- Inmunidad a multas menores
- Guardia personal permanente (2 guardias siempre presentes)
- Acceso a arsenal (upgrades militares)
- Voz en decisiones del Consejo
- Recompensas dobles en criminales

**Gremio de Ladrones:**
- "Bajo Protección del Maestro"
- Inmunidad total a crimen (nadie te toca)
- El Maestro "elimina" cualquier problema que reportes
- Acceso a red de espionaje (información sobre TODO)
- Clientes ultra-VIP (nobles corruptos, señores criminales)
- Ganancia +40% en mercado negro

**Templo de la Luz:**
- "Campeón de la Luz"
- Bendiciones divinas permanentes (+20% ganancia)
- Intervención divina en crisis (auto-resurreción 1 vez)
- Paladines como guardia permanente
- Milagros menores bajo demanda
- Inmunidad a maldiciones

**Círculo Arcano:**
- "Taberna del Círculo" (sede oficial)
- Todos los enchantments gratis y permanentes
- Teleportación de emergencia disponible
- Acceso a biblioteca arcana
- Mago residente permanente
- Descuento pociones -50%

**Gremio de Comerciantes:**
- "Socio de Honor"
- Descuento suministros -50%
- Préstamos ilimitados (hasta 2000 monedas, sin interés)
- Insider trading (conoces precios futuros)
- Monopolio local (sin competencia)
- Dividendos pasivos (+50 monedas/día)

**Hermandad del Bosque:**
- "Guardián del Bosque"
- Guardián animal permanente (lobo, oso, etc.)
- Inmunidad a venenos y enfermedades
- Control menor de plantas (decoración automática)
- Ingredientes infinitos gratis
- Druida residente (sanación, consejo)

**Los Sombríos:**
- "Sombra Honoraria"
- Inmunidad total a asesinato (nadie se atreve)
- Red de espías a tu servicio
- Contratos de asesinato gratis (1/mes)
- Invisibilidad social (puedes "desaparecer" 1 día/semana)

**Orden del Escudo:**
- "Héroe de la Orden"
- Protección paladinesca 24/7
- Bendiciones de combate
- Acceso a armería sagrada
- Inmunidad a mal y corrupción
- Cruzados personales

**Consecuencia General:**
- Bonificación masiva (+30 a +50% ganancia)
- Protección casi absoluta
- Acceso a contenido único
- Posición de poder en la sociedad
- **Casi imposible de alcanzar** (requiere campaña dedicada)

**Nota:** Solo es realista alcanzar +80 con 1-2 facciones máximo, debido a conflictos entre facciones.

---

## ⚡ GANANCIA Y PÉRDIDA DE REPUTACIÓN

### Tabla de Acciones y Valores

| Acción | Facción Afectada | Cambio | Notas |
|--------|------------------|--------|-------|
| Servir a miembro | Esa facción | +1 a +3 | Según rango del miembro |
| Servir a miembro VIP | Esa facción | +5 a +10 | Líderes, héroes |
| Servir a enemigo de facción | Facción enemiga | -5 a -15 | Según intensidad de enemistad |
| Rechazar a miembro | Esa facción | -3 a -8 | Sin razón válida |
| Rechazar a miembro con razón | Esa facción | -1 a -3 | Si documento falso, menor impacto |
| Rechazar a enemigo | Facción contraria | +5 a +10 | Demuestras lealtad |
| Entregar criminal a Guardia | Guardia Real | +10 a +30 | Según gravedad del crimen |
| Entregar criminal a Guardia | Facción del criminal | -20 a -60 | Traición grave |
| Esconder criminal | Facción del criminal | +15 a +30 | Alto riesgo |
| Esconder criminal | Guardia Real | -30 a -80 | Si descubren |
| Completar misión | Facción | +15 a +50 | Según dificultad |
| Fallar misión | Facción | -10 a -30 | Según importancia |
| Donación grande (200+ monedas) | Facción | +10 a +25 | Solo algunas facciones |
| Traición | Facción traicionada | -50 a -90 | Casi irrecuperable |
| Acto heroico | Facción beneficiada | +30 a +60 | Salvar miembros, eventos especiales |

### Fórmulas de Cálculo

**Servir a Cliente:**
```
Reputación ganada = Base + (Rango del cliente) + (Calidad del servicio)

Base = +1
Rango: Plebeyo +0, Miembro regular +1, Oficial +2, Líder +4
Calidad: Bebida favorita +1, Servicio rápido +1
```

**Ejemplo:**
- Cliente: Guardia regular (rango +1)
- Servicio: Bebida favorita (+1)
- Total: +1 (base) +1 (rango) +1 (calidad) = **+3 Guardia Real**

**Entregar Criminal:**
```
Reputación perdida con facción del criminal = -20 × (1 + Rango/10)
Reputación ganada con Guardia = +10 × (1 + Gravedad crimen)

Gravedad: Menor (robo) = 0.5, Media (falsificación) = 1, Alta (asesinato) = 2
```

**Ejemplo:**
- Criminal: Pícaro del Gremio de Ladrones, crimen de falsificación (gravedad 1)
- Pérdida: -20 × (1 + 0.3) = **-26 Gremio de Ladrones**
- Ganancia: +10 × (1 + 1) = **+20 Guardia Real**

---

## 🔄 DECAIMIENTO DE REPUTACIÓN

### Decay Natural (Olvido)

**Reputaciones extremas decaen lentamente hacia neutral:**

```
Si Reputación > +20: -0.1 puntos/día (hacia +20)
Si Reputación < -20: +0.1 puntos/día (hacia -20)
Si -20 ≤ Reputación ≤ +20: Sin decay
```

**Razón de diseño:**
- Evita que jugadores alcancen +100 y se queden ahí sin esfuerzo
- Requiere mantenimiento activo de relaciones
- Permite recuperación gradual de errores antiguos

**Ejemplo:**
- Tienes +85 con Guardia Real
- Cada día sin interacción: +85 → +84.9 → +84.8...
- En 650 días sin interacción llegaría a +20 (pero es muy lento)

### Excepciones al Decay

**NO decae:**
- Reputación ganada por "actos permanentes" (donaciones de edificios, heroísmo excepcional)
- Marcada como "Lazo permanente"

---

## 🎯 RECUPERACIÓN DE REPUTACIÓN

### Desde Enemigo Mortal (-80+)

**Requiere:**
1. **Acto Dramático** (+50 puntos mínimo)
   - Salvar la vida del líder de la facción
   - Evitar desastre catastrófico
   - Misión suicida exitosa

2. **Intermediario** (NPC que negocie por ti)
   - Requiere +60 con facción neutral respecto a tu enemigo
   - Costo: 500-1000 monedas de soborno

3. **Tiempo** (castigo temporal)
   - Mínimo 30 días in-game sin interacción negativa adicional
   - Durante este tiempo, facción te ignora (ni positivo ni negativo)

**Ejemplo Narrativo:**
```
Jugador tiene -85 con Templo de la Luz (Enemigo Mortal)

Opción 1: Acto Heroico
- Durante ataque del Culto de Sangre, jugador protege el templo
- Salva la vida de 3 sacerdotes
- Resultado: +60 reputación (de -85 a -25, ahora Hostil)

Opción 2: Intermediario
- Jugador tiene +70 con Círculo Arcano (Aliado)
- Archimago Zarathos negocia con Templo
- Costo: 800 monedas + misión para Templo
- Resultado: +40 reputación (de -85 a -45, ahora Enemigo leve)
```

### Desde Enemigo (-50 a -79)

**Requiere:**
- Misiones de "Penitencia" (3-5 misiones seguidas)
- Cada misión: +10 a +15 reputación
- Total: +30 a +75 puntos posibles

**O:**
- Donación masiva (500-1000 monedas según facción)
- +30 a +50 puntos inmediatos

### Desde Hostil (-20 a -49)

**Requiere:**
- Misiones estándar (2-3 misiones)
- Servir consistentemente a miembros (20-30 clientes)
- Tiempo: ~10-15 días in-game

**Recuperación natural:**
- Si evitas acciones negativas, +1 punto cada 2 días (gradual)

---

## 📈 PROGRESIÓN RECOMENDADA

### Early Game (Días 1-30)

**Objetivo:** Mantenerse neutral con todos, explorar facciones

**Estrategia:**
- Servir a todos por igual
- No tomar partido en conflictos
- Evitar rechazar clientes sin razón

**Resultado esperado:** -10 a +15 con la mayoría de facciones

### Mid Game (Días 31-60)

**Objetivo:** Elegir 2-3 facciones aliadas

**Estrategia:**
- Completar misiones de facciones elegidas
- Empezar a rechazar enemigos de tus aliados
- Aceptar que algunas facciones se volverán hostiles

**Resultado esperado:**
- 2-3 facciones: +30 a +50 (Aliados)
- 2-3 facciones: -20 a -40 (Hostiles)
- Resto: Neutral

### Late Game (Días 61+)

**Objetivo:** Maximizar con facción principal, gestionar enemistades

**Estrategia:**
- Dedicación completa a 1 facción (+70+)
- Gestión activa de facciones hostiles (evitar -80)
- Aprovechar alianzas para beneficios

**Resultado esperado:**
- 1 facción: +70 a +90 (Héroe)
- 2 facciones: +40 a +60 (Aliados)
- 3-4 facciones: -30 a -60 (Enemigos controlados)
- Resto: Neutral o leve

---

## 🎮 UI Y FEEDBACK AL JUGADOR

### Panel de Reputación

**Información mostrada:**

```
╔═══════════════════════════════════════════════╗
║           REPUTACIÓN CON FACCIONES            ║
╠═══════════════════════════════════════════════╣
║                                               ║
║ Guardia Real             [████████░░] +78     ║
║ Estado: ★★★★ ALIADO DE CONFIANZA              ║
║ Cambio reciente: +3 (serviste a Capitán)     ║
║                                               ║
║ Gremio de Ladrones       [░░░░░░░░░░] -42    ║
║ Estado: ★ HOSTIL                              ║
║ Cambio reciente: -10 (entregaste a Pícaro)   ║
║                                               ║
║ Templo de la Luz         [███████░░░] +65     ║
║ Estado: ★★★★ ALIADO DE CONFIANZA              ║
║ Cambio reciente: +5 (serviste a Clérigo)     ║
║                                               ║
║ [Ver todas las facciones...]                  ║
╚═══════════════════════════════════════════════╝
```

### Notificaciones en Tiempo Real

**Cuando sirves a un cliente:**
```
┌─────────────────────────────────────┐
│ Serviste a Guardia Elena            │
│ Guardia Real: +3 (+78 total)        │
│ Gremio de Ladrones: -5 (-42 total)  │
└─────────────────────────────────────┘
```

**Cuando alcanzas nuevo nivel:**
```
┌─────────────────────────────────────────────┐
│ ★★★★ NUEVO NIVEL DE REPUTACIÓN              │
│                                             │
│ Guardia Real: ALIADO DE CONFIANZA (+78)     │
│                                             │
│ Beneficios desbloqueados:                   │
│ • Guardia patrulla tu zona                  │
│ • Acceso a órdenes de detención             │
│ • Aviso previo de inspecciones              │
│                                             │
│ Nuevas misiones disponibles (ver tablón)    │
└─────────────────────────────────────────────┘
```

### Advertencias de Consecuencias

**Antes de tomar decisión crítica:**
```
┌─────────────────────────────────────────────┐
│ ⚠️  ADVERTENCIA DE REPUTACIÓN                │
│                                             │
│ Si entregas a este cliente:                 │
│                                             │
│ Gremio de Ladrones: -25 (-67 total)         │
│ → Alcanzarías ENEMIGO (-50)                 │
│                                             │
│ Consecuencias:                              │
│ • Robos semanales (100-300 monedas)         │
│ • Sabotaje estructural                      │
│ • Falsificaciones abundantes                │
│                                             │
│ ¿Estás seguro? [Sí] [No]                    │
└─────────────────────────────────────────────┘
```

---

## 📊 STATS RECOMENDADOS PARA TRACKING

**Para cada facción, trackear:**

1. **Reputación actual** (número -100 a +100)
2. **Nivel de reputación** (texto: Enemigo Mortal, Enemigo, etc.)
3. **Cambios últimos 7 días** (historial)
4. **Acciones significativas** (log de eventos que afectaron +10 o más)
5. **Misiones activas** (relacionadas con esa facción)
6. **Tiempo hasta próximo decay** (si aplica)
7. **Beneficios activos** (lista de buffs por esa reputación)
8. **Consecuencias activas** (lista de debuffs)

**Estadística global:**
- **Promedio de reputación** (suma de todas / número de facciones)
- **Facciones aliadas** (cuántas están en +20 o más)
- **Facciones enemigas** (cuántas están en -20 o menos)
- **Facción más alta**
- **Facción más baja**

---

## 🎯 ACHIEVEMENTS RELACIONADOS

**Diplomático:** Alcanza +50 con 5 facciones simultáneamente (muy difícil por conflictos)

**Héroe Universal:** Alcanza +80 con 1 facción

**Leyenda Viviente:** Alcanza +100 con 1 facción (casi imposible)

**Enemigo Público:** Alcanza -80 con 3 facciones (difícil sobrevivir)

**Equilibrista:** Mantén todas las facciones entre -10 y +10 durante 30 días (neutralidad perfecta)

**Cambio de Corazón:** Recupera desde -80 a +50 con una facción (redención épica)

**Maestro del Caos:** Ten simultáneamente +80 con una facción y -80 con su enemigo

---

## 💡 TIPS DE DISEÑO

**1. Hacer que cada punto importe:**
- No inflar valores (no dar +50 por servir 1 cliente)
- Progresión lenta y significativa

**2. Consecuencias visibles:**
- Jugador debe VER el impacto de sus decisiones
- Feedback inmediato en UI

**3. Recuperación posible pero costosa:**
- Nunca "punto de no retorno" absoluto
- Pero recuperar debe ser difícil y caro

**4. Balance de poder:**
- Imposible estar bien con todos
- Forzar decisiones difíciles

**5. Recompensa a largo plazo:**
- Beneficios de +80 deben sentirse ÉPICOS
- Justificar 60+ días de campaña dedicada

---

**Sistema de Reputación:** Núcleo numérico que controla TODAS las interacciones con facciones.
