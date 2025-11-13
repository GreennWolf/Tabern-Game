# 💰 Economía del Sistema de Bebidas

Este documento define precios, costos, rareza, stock y mecánicas económicas del sistema de bebidas.

---

## 📊 TIERS DE PRECIOS

### Tier 1: BÁSICAS (1-5 cobre)

**Ejemplos:**
- Agua (0 cobre - gratis si solicitan)
- Té de Hierbas (2 cobre)
- Jugo de Frutas (3 cobre)
- Leche (2 cobre)

**Características:**
- Disponibilidad: Infinita (siempre en stock)
- Margen: 50% (compras a 1c, vendes a 2c)
- Riesgo: Ninguno
- Uso: Tutorial, clientes pobres, non-alcoholic

---

### Tier 2: COMUNES (10-20 cobre)

**Ejemplos:**
- Cerveza Común (10 cobre)
- Cerveza Ligera (8 cobre)
- Vino Común (12 cobre)
- Hidromiel Suave (15 cobre)

**Características:**
- Disponibilidad: Muy alta (stock 50+ unidades)
- Restocking: Diario automático
- Margen: 60% (compras a 6c, vendes a 10c)
- Riesgo: Ninguno
- Uso: Pan de cada día, 80% de ventas early game

---

### Tier 3: PREMIUM (25-50 cobre)

**Ejemplos:**
- Cerveza Enana "Martillo de Hierro" (25 cobre)
- Vino Élfico "Lágrima de Estrella" (45 cobre)
- Whisky Enano (30 cobre)
- Hidromiel de Guerrero (35 cobre)

**Características:**
- Disponibilidad: Media (stock 10-20 unidades)
- Restocking: Semanal
- Margen: 70% (compras a 15c, vendes a 25c)
- Riesgo: Bajo
- Uso: Clientes específicos (razas/clases preferidas)

---

### Tier 4: RARAS (60-100 cobre)

**Ejemplos:**
- Cerveza de Glamour (60 cobre)
- Vino de Runa (80 cobre)
- Aguardiente "Aliento de Dragón" (70 cobre)
- Hidromiel Encantada (50 cobre)

**Características:**
- Disponibilidad: Baja (stock 2-5 unidades)
- Restocking: Semanal, requiere comerciante especial
- Margen: 80% (compras a 35c, vendes a 60c)
- Riesgo: Medio (efectos especiales potentes)
- Uso: Clientes ricos, situaciones especiales

---

### Tier 5: LEGENDARIAS (100-200 cobre)

**Ejemplos:**
- Elixir de Visiones (100 cobre)
- Poción de Verdad (150 cobre)
- Elixir del Dragón Ancestral (800 cobre)

**Características:**
- Disponibilidad: Muy baja (stock 0-1 unidades)
- Restocking: Evento especial, misión, comerciante raro
- Margen: 100%+ (compras a 50c, vendes a 100c+)
- Riesgo: Alto (requiere licencias especiales)
- Uso: Late game, eventos narrativos clave

---

### Tier 6: ILEGALES (mercado negro)

**Ejemplos:**
- Vino de Sangre (200 cobre)
- Bebida Corrupta "Sombra Líquida" (180 cobre)
- Licor de Olvido (120 cobre)

**Características:**
- Disponibilidad: Mercado negro SOLAMENTE
- Restocking: Contacto criminal (evento)
- Margen: 150%+ (compras a 80c, vendes a 200c)
- Riesgo: EXTREMO (cierre, arresto, multa)
- Uso: Late game, ruta moral oscura

---

## 🏪 SISTEMA DE STOCK

### Stock Inicial (Early Game)

Al empezar el juego, tu inventario:

```
TIER 1 (Básicas): ∞ (infinito)
- Agua: ∞
- Té: ∞
- Jugos: ∞

TIER 2 (Comunes): 30 unidades cada una
- Cerveza Común: 30
- Vino Común: 30
- Hidromiel Suave: 30

TIER 3 (Premium): 0 unidades
(Desbloqueadas en Mid Game)

TIER 4+: 0 unidades
(Desbloqueadas en Late Game)
```

**Total inversión inicial:** ~350 cobre

---

### Sistema de Restocking

#### Restocking Automático (Tier 1-2)

**Frecuencia:** Cada día (in-game)
**Costo:** Automático, deducido de caja
**Condición:** Si stock < 20 unidades, restock a 50

**Ejemplo:**
```
Día 1: Tienes 50 Cervezas Comunes
Día 2: Vendiste 35, quedan 15
Día 3: Sistema auto-restock a 50 (costo: 210 cobre)
```

---

#### Restocking Manual (Tier 3+)

**Frecuencia:** Semanal, visita de comerciante
**Costo:** Pago manual por unidad
**Condición:** Debes COMPRAR activamente del comerciante

**Mecánica:**
1. Cada semana, comerciante visita tu taberna
2. Ofrece catálogo de bebidas premium/raras
3. Tú decides cuántas comprar
4. Stock limitado (ej: solo 10 Cervezas Enanas disponibles)

**Ejemplo:**
```
Comerciante Enano llega:
"Tengo 10 Cervezas Enanas 'Martillo de Hierro' (15c cada una)"

Jugador compra: 8 unidades (costo 120 cobre)
Stock actualizado: Cerveza Enana = 8
```

---

#### Restocking Evento Especial (Tier 4-5)

**Frecuencia:** Aleatorio, 1-2 veces por mes
**Costo:** Alto, negociable
**Condición:** Evento narrativo específico

**Ejemplos:**
- Mago itinerante ofrece Vino de Runa (solo 2 unidades)
- Clérigo vende Agua Bendita en bulk (20 unidades)
- Druida trae Elixir de Visiones (1 unidad única)

---

#### Mercado Negro (Tier 6)

**Frecuencia:** Raro, requiere contacto criminal
**Costo:** Muy alto, peligroso
**Condición:** Ruta narrativa oscura

**Mecánica:**
1. Pícaro/Criminal ofrece bebidas ilegales
2. Precio inflado (x2-3 normal)
3. Riesgo de trampa/Inspector
4. Dilema moral

---

## 💸 FÓRMULA DE PRECIOS

### Precio Base

```
Precio Venta = (Alcohol Nivel × 5) + Rareza + Efecto Especial
```

**Ejemplo:**
```
Cerveza Común:
- Alcohol: 4/10
- Rareza: 0 (común)
- Efecto: 0 (ninguno)
- Precio: (4 × 5) + 0 + 0 = 20 cobre

Cerveza de Glamour:
- Alcohol: 5/10
- Rareza: +15 (rara)
- Efecto: +20 (rompe glamour)
- Precio: (5 × 5) + 15 + 20 = 60 cobre
```

---

### Modificadores de Precio

#### Por Raza (Cliente paga más/menos)

**Enano + Cerveza Enana:**
- Precio base: 25 cobre
- Modificador: +20% (orgullo racial)
- Precio final: 30 cobre

**Elfo + Vino Élfico:**
- Precio base: 45 cobre
- Modificador: +15% (nostalgia cultural)
- Precio final: 52 cobre

**Minotauro + Vino Élfico:**
- Precio base: 45 cobre
- Modificador: -30% (desprecio)
- Precio final: 32 cobre (o lo rechaza)

---

#### Por Temporada/Evento

**Invierno:** Hidromiel de Invierno +30%
**Festival Enano:** Cerveza Enana +50% demanda
**Luna Llena:** Bebidas nocturnas +20%

---

#### Por Reputación

**Reputación Alta con Enanos:**
- Puedes comprar Cerveza Enana más barata (-10%)
- Enanos pagan más en tu taberna (+5%)

**Reputación Baja con Elfos:**
- Vino Élfico más caro (+20% costo)
- Elfos no vienen a tu taberna

---

## 📈 PROGRESIÓN ECONÓMICA

### Early Game (Días 1-30)

**Bebidas disponibles:**
- Tier 1: Todas
- Tier 2: Todas
- Tier 3+: Ninguna

**Ingresos promedio/día:** 150-300 cobre
**Gastos promedio/día:** 100 cobre (restocking + operación)
**Ganancia neta:** 50-200 cobre/día

**Estrategia:**
- Vende principalmente Tier 2
- Aprende mecánicas sin riesgo
- Ahorra para upgrades

---

### Mid Game (Días 31-90)

**Bebidas disponibles:**
- Tier 1-2: Todas
- Tier 3: Desbloqueadas (comerciante semanal)
- Tier 4: Algunas (eventos especiales)

**Ingresos promedio/día:** 400-700 cobre
**Gastos promedio/día:** 200-300 cobre
**Ganancia neta:** 100-400 cobre/día

**Estrategia:**
- Identifica clientes premium (Enanos, Elfos, Dracónidos)
- Invierte en bebidas Tier 3 específicas
- Comienza a usar efectos especiales

---

### Late Game (Día 91+)

**Bebidas disponibles:**
- Tier 1-5: Todas (con licencias)
- Tier 6: Mercado negro (opcional)

**Ingresos promedio/día:** 800-1500 cobre
**Gastos promedio/día:** 400-600 cobre
**Ganancia neta:** 400-900 cobre/día

**Estrategia:**
- Servir bebidas legendarias a clientes VIP
- Usar efectos especiales estratégicamente
- Maximizar reputación con facciones clave
- Dilema moral: ¿mercado negro?

---

## 🔓 SISTEMA DE DESBLOQUEO

### Licencias Requeridas

Ciertas bebidas requieren licencias especiales:

#### Licencia de Bebidas Mágicas (100 monedas)

**Desbloquea:**
- Vino de Runa
- Elixir de Visiones
- Cerveza de Glamour
- Hidromiel Encantada

**Requisito:** Reputación Media + Inspección aprobada

---

#### Licencia de Bebidas Sagradas (50 monedas)

**Desbloquea:**
- Agua Bendita (venta legal)
- Vino Sagrado
- Hidromiel de Luz

**Requisito:** Aprobación de templo local

---

#### Licencia de Alquimia (200 monedas)

**Desbloquea:**
- Poción de Verdad (LEGAL con licencia)
- Licor de Olvido (LEGAL con licencia)
- Elixir del Dragón Ancestral

**Requisito:** Late game + Reputación Alta + Quest

---

### Upgrades de Taberna

#### Bodega Mejorada (300 monedas)

**Efecto:**
- +50% capacidad stock (75 unidades comunes)
- Bebidas raras duran +1 semana
- -10% costo de restocking

---

#### Barril Enano Auténtico (500 monedas)

**Efecto:**
- Cerveza Enana siempre fresca
- Enanos pagan +30% más
- +Reputación con facción enana

---

#### Vinoteca Élfica (600 monedas)

**Efecto:**
- Vinos permanecen perfectos
- Elfos visitan más frecuentemente
- Acceso a vinos ultra-raros

---

## 💡 ESTRATEGIAS ECONÓMICAS

### Maximizar Ganancias

**Identifica clientes premium:**
- Enano → Sirve Cerveza Enana (25c, él paga 30c)
- Elfo → Sirve Vino Élfico (45c, él paga 52c)
- Dracónido → Sirve bebidas específicas de linaje

**No desperdicies bebidas raras:**
- NO sirvas Cerveza de Glamour a Humano (no la necesita)
- SÍ guárdala para Elfo sospechoso (verificación)

**Ajusta precios por temporada:**
- Invierno: Sube precio de Hidromiel de Invierno
- Festival: Sube precio de bebidas culturales

---

### Minimizar Costos

**Evita sobre-stock Tier 3+:**
- Solo compra lo necesario
- Bebidas premium no venden diario
- Stock parado = dinero perdido

**Negocia con comerciantes:**
- Alta reputación = descuentos
- Compra bulk = -10% costo

**Evita multas:**
- NO vendas ilegales si no vale la pena
- Multa de 500c > ganancia de 200c

---

### Balance Riesgo/Recompensa

#### Bajo Riesgo, Baja Ganancia
- Vende solo Tier 1-2
- Ganancia: 50-200c/día
- Riesgo: Ninguno
- Aburrido pero seguro

#### Medio Riesgo, Media Ganancia
- Vende Tier 3, algunas Tier 4
- Ganancia: 200-500c/día
- Riesgo: Bajo (licencias legales)
- Balance ideal

#### Alto Riesgo, Alta Ganancia
- Vende Tier 5-6 (mercado negro)
- Ganancia: 500-1000c/día
- Riesgo: Extremo (cierre, arresto)
- Solo late game con estrategia

---

## 📋 TABLA RESUMEN: COSTO vs VENTA

| Bebida | Tier | Costo Compra | Precio Venta | Margen | Disponibilidad |
|--------|------|--------------|--------------|--------|----------------|
| Agua | 1 | 0c | 0c | - | ∞ |
| Té Hierbas | 1 | 1c | 2c | 50% | ∞ |
| Cerveza Común | 2 | 6c | 10c | 40% | Alta |
| Vino Común | 2 | 7c | 12c | 42% | Alta |
| Cerveza Enana | 3 | 15c | 25c | 40% | Media |
| Vino Élfico | 3 | 25c | 45c | 44% | Media |
| Cerveza Glamour | 4 | 35c | 60c | 42% | Baja |
| Vino de Runa | 4 | 45c | 80c | 44% | Baja |
| Elixir Visiones | 5 | 50c | 100c | 50% | Muy baja |
| Poción Verdad | 5 | 80c | 150c | 47% | Muy baja |
| Elixir Dragón | 5 | 400c | 800c | 50% | Evento |
| Vino de Sangre | 6 | 80c | 200c | 60% | Negro |

---

## ⚖️ BALANCE ECONÓMICO

### Objetivos de Diseño

1. **Early game:** Jugador aprende sin presión económica
2. **Mid game:** Decisiones económicas importan
3. **Late game:** Jugador prospera pero con dilemas morales

---

### Prevención de Explotación

**Anti-farming:**
- Bebidas raras no spawn infinito
- Comerciante tiene stock limitado
- Precio sube si compras demasiado

**Anti-spam:**
- Cliente solo bebe 1-3 copas máximo
- No puedes vender 50 Elixires en 1 día
- Sistema de satisfacción previene sobre-servicio

---

### Economía Realista

**Contexto de precios:**
- Cerveza Común (10c) = comida básica
- Cerveza Enana (25c) = comida en restaurant
- Vino Élfico (45c) = comida premium
- Elixir Visiones (100c) = 10 días de comida

**Sistema coherente:**
- Jugador gana ~200c/día promedio
- Upgrade taberna cuesta 300-600c (1-3 semanas ahorro)
- Bebida legendaria (800c) = lujo extremo

---

## 🎯 METAS ECONÓMICAS DEL JUGADOR

### Corto Plazo (Semana 1-2)
- [ ] Gana 500 cobre total
- [ ] Compra primer upgrade (Bodega Mejorada)
- [ ] Desbloquea comerciante semanal

### Mediano Plazo (Mes 1)
- [ ] Gana 2000 cobre total
- [ ] Obtén Licencia de Bebidas Mágicas
- [ ] Sirve primera bebida Tier 4 con éxito

### Largo Plazo (Mes 2-3)
- [ ] Gana 5000+ cobre total
- [ ] Desbloquea todas las licencias legales
- [ ] Decisión: ¿Mercado negro o ruta legal?

---

**Sistema económico completo:** Precios, costos, stock, restocking, progresión, balance.

**Filosofía:** Recompensa estrategia y conocimiento del cliente, NO farming mecánico.
