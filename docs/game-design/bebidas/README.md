# 🍺 Sistema de Bebidas - El Tabernero del Cruce

## Índice

Este directorio contiene las especificaciones completas del sistema de bebidas del juego.

### Estructura

1. [Categorías de Bebidas](./categorias.md) - Clasificación general
2. [Catálogo Completo](./catalogo.md) - Todas las bebidas disponibles
3. [Efectos Especiales](./efectos-especiales.md) - Mecánicas únicas
4. [Restricciones](./restricciones.md) - Por raza y clase
5. [Precios y Rareza](./economia.md) - Sistema económico

---

## 📊 Categorías Principales

### 1. **Bebidas Alcohólicas Comunes**
Cerveza, vino, ron, aguardiente - Lo básico de cualquier taberna

### 2. **Bebidas Raciales**
Específicas de cada raza (cerveza enana, vino élfico, hidromiel de centauro)

### 3. **Bebidas Mágicas**
Pociones, vinos encantados, bebidas con efectos sobrenaturales

### 4. **Bebidas Naturales/No Alcohólicas**
Té, agua, jugos, bebidas de druidas

### 5. **Bebidas Prohibidas/Ilegales**
Bebidas con sangre, pociones oscuras, sustancias controladas

### 6. **Bebidas Especiales/Raras**
Eventos, estaciones, muy caras o difíciles de conseguir

---

## 🎯 Propiedades de Bebidas

Cada bebida tiene:

### Básico
- **Nombre**
- **Categoría**
- **Nivel de alcohol** (0-10)
- **Precio** (monedas de cobre)
- **Rareza** (común, poco común, rara, muy rara, legendaria)

### Efectos
- **Sabor/Descripción**
- **Efecto en embriaguez** (cuánto contribuye al nivel borracho)
- **Efectos especiales** (romper glamour, forzar verdad, etc.)
- **Duración del efecto**

### Restricciones
- **Razas que lo prefieren**
- **Razas que lo rechazan**
- **Clases prohibidas** (por código/religión)
- **Legal/Ilegal** (en ciertos reinos)

### Disponibilidad
- **Cuándo aparece** (Early/Mid/Late game)
- **Costo de reabastecimiento**
- **Stock** (cantidad disponible por día)

---

## 🔢 Nivel de Alcohol (Escala 1-10)

| Nivel | Tipo | Ejemplos |
|-------|------|----------|
| 0 | Sin alcohol | Agua, té, jugos |
| 1-2 | Muy ligero | Cerveza ligera, hidromiel suave |
| 3-4 | Ligero | Cerveza común, vino ligero |
| 5-6 | Medio | Vino común, ron, sake |
| 7-8 | Fuerte | Aguardiente, whisky, cerveza enana |
| 9-10 | Muy fuerte | Destilados puros, bebidas legendarias |

**Interacción con Tolerancia Racial:**
- Enano (10/10 tolerancia) + Cerveza enana (8/10 alcohol) = Apenas se emborracha
- Elfo (3/10 tolerancia) + Vino común (5/10 alcohol) = Se emborracha rápido
- Duende (2/10 tolerancia) + Aguardiente (8/10 alcohol) = Inconsciente

---

## 💰 Sistema de Precios

### Precio Base por Nivel de Alcohol

| Nivel Alcohol | Precio Base (cobre) |
|---------------|-------------------|
| 0 (sin alcohol) | 1-2 |
| 1-2 (muy ligero) | 3-5 |
| 3-4 (ligero) | 5-8 |
| 5-6 (medio) | 10-15 |
| 7-8 (fuerte) | 20-30 |
| 9-10 (muy fuerte) | 40-60 |

### Modificadores de Precio

**Rareza:**
- Común: x1
- Poco común: x1.5
- Rara: x2
- Muy rara: x3
- Legendaria: x5-10

**Racial:**
- Bebida racial específica: +50% si no es de esa raza

**Mágica:**
- Efectos mágicos: +100% a +500%

**Ilegal:**
- Bebidas prohibidas: x2 (mercado negro)

---

## 🎲 Efectos Especiales

### Mecánicos

**Romper Glamour:**
- Algunas bebidas revelan la edad/apariencia real de elfos

**Forzar Verdad:**
- Cliente borracho es más honesto (reduce propensión a mentir temporalmente)

**Amplificar Magia:**
- Magos/Hechiceros: efectos mágicos más fuertes (peligroso)

**Calmar/Enfurecer:**
- Modifican comportamiento borracho

**Curación Menor:**
- Algunas bebidas clericales curan heridas leves

**Visiones:**
- Bebidas druídicas causan visiones proféticas

### Narrativos

**Desbloquear Diálogo:**
- Ciertos clientes solo hablan si les das su bebida favorita

**Afectar Reputación:**
- Servir bebida correcta = +reputación con facción

**Eventos Especiales:**
- Bebidas raras activan eventos únicos

---

## 🚫 Bebidas Prohibidas

### Por Raza

**Enanos:**
- Vinos élficos (orgullo cultural, no prohibición legal)

**Elfos del Bosque:**
- Destilados industriales
- Bebidas con sangre animal

**Elfos de la Noche:**
- Bebidas benditas por luz/sol

**Druidas (clase):**
- Bebidas antinaturales/químicas

**Clérigos (clase):**
- Varía por deidad (bebidas oscuras, alcohol fuerte, etc.)

**Paladines (clase):**
- Alcohol corrupto
- Bebidas asociadas con mal

### Por Ley

**Reino:**
- Pociones sin licencia
- Bebidas con ingredientes ilegales
- Alcohol excesivamente fuerte (controlado)

---

## 🔄 Sistema de Embriaguez

**Fórmula:**
```
Nivel Borracho = (Alcohol de Bebida × Cantidad) ÷ Tolerancia Racial
```

**Ejemplo:**
- Elfo (Tolerancia 3/10) + 2 copas de Vino (5/10) = (5 × 2) ÷ 3 = 3.3 → Nivel 3 Borracho
- Enano (Tolerancia 10/10) + 2 copas de Vino (5/10) = (5 × 2) ÷ 10 = 1 → Nivel 1 Borracho

**Niveles de Embriaguez:**
- **Nivel 1 (1-3 puntos):** Alegre, relajado
- **Nivel 2 (4-6 puntos):** Torpe, habla de más
- **Nivel 3 (7+ puntos):** Efectos especiales por clase (magia salvaje, furia, etc.)

---

## 📅 Disponibilidad Temporal

### Early Game (Días 1-10)
- Solo bebidas comunes
- Cerveza, vino común, agua, té
- Precios bajos

### Mid Game (Días 11-20)
- Bebidas raciales aparecen
- Algunas bebidas mágicas básicas
- Mayor variedad

### Late Game (Días 21+)
- Bebidas raras y legendarias
- Bebidas prohibidas (mercado negro)
- Eventos con bebidas únicas

---

## 🎨 Integración con Gameplay

### Verificación
- Jugador debe verificar si cliente PUEDE beber ciertas bebidas (restricciones raza/clase)
- Servir bebida prohibida = consecuencias

### Estrategia
- Usar bebidas para manipular clientes (verdad, glamour, calmar)
- Bebidas caras = más ganancia pero más riesgo
- Bebidas raras = eventos especiales

### Progresión
- Desbloquear bebidas mejores
- Ampliar menú = más clientes
- Bebidas especiales = reputación con facciones

---

## 📝 Notas de Diseño

### Balance
- Bebidas fuertes = más ganancia pero más riesgo de nivel 3 borracho
- Bebidas mágicas = efectos interesantes pero caras/raras
- No todas las bebidas disponibles siempre (stock limitado)

### Economía
- Jugador debe comprar stock
- Bebidas caras requieren inversión inicial
- Algunas bebidas se estropean (urgencia)

### Narrativa
- Bebidas cuentan historias (cerveza de batalla enana, vino élfico de 300 años)
- Eventos especiales ligados a bebidas (festival del vino, escasez de cerveza)
