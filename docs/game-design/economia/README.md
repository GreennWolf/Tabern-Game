# 💰 Sistema de Economía - El Tabernero del Cruce

## Filosofía de Diseño

**"Papers, Please pero con economía de supervivencia"**

Tu taberna es un negocio. Debes:
- Generar ingresos suficientes para sobrevivir
- Gestionar gastos fijos y variables
- Invertir en mejoras para crecer
- Balancear riesgo vs recompensa
- Tomar decisiones económicas difíciles

**La economía es el corazón del loop de juego.**

---

## 🎯 LOOP ECONÓMICO BÁSICO

```
DÍA N:
1. GASTOS FIJOS (pagos obligatorios)
   - Alquiler: -50 monedas
   - Empleados: -30 monedas (si tienes)
   - Impuestos: -10% ganancia del día anterior
   - Deudas: Variable

2. APERTURA (8:00 - 22:00)
   - Atender clientes
   - Vender bebidas
   - Ingresos: +Variable

3. EVENTOS ALEATORIOS
   - Robos: -50 a -300 monedas
   - Destrucción: -100 a -500 monedas
   - Multas: -50 a -500 monedas
   - Bonificaciones: +50 a +300 monedas

4. CIERRE (22:00)
   - Calcular ganancia neta del día
   - Comprar stock para mañana
   - (Opcional) Invertir en upgrades

5. BALANCE FINAL
   - Si balance positivo: +dinero
   - Si balance negativo: -dinero (peligro)
   - Si llegas a 0 monedas: GAME OVER
```

---

## 💵 MONEDA Y VALORES

### Sistema Monetario

**Moneda:** Monedas de cobre (c)

**Conversión:**
- 1 moneda de cobre (c) = 1 unidad básica
- 100c = 1 moneda de plata (p)
- 100p = 1 moneda de oro (o)

**Para simplicidad del juego:**
- Todo se mide en monedas de cobre (c)
- Valores típicos: 1c a 10,000c

### Escala de Valores

```
1-10c:    Muy barato (agua, pan)
11-50c:   Barato (cerveza común, comida simple)
51-100c:  Normal (vino común, comida buena)
101-300c: Caro (bebidas especiales, comida de calidad)
301-1000c: Muy caro (bebidas raras, lujos)
1000c+:   Legendario (bebidas únicas, artefactos)
```

---

## 📊 INGRESOS

### Venta de Bebidas

**Precio = Costo Base + Modificadores**

**Fórmula:**
```
Precio Final = (Costo Base × Modificador Rareza × Modificador Demanda) + Propina

Costo Base: Según tipo de bebida
Modificador Rareza: 1.0 (común) a 3.0 (legendaria)
Modificador Demanda: 0.8 (baja) a 1.5 (alta)
Propina: 0% a 20% (según raza/clase/reputación)
```

**Ejemplos:**

**Cerveza Común:**
- Costo base: 10c
- Rareza: 1.0 (común)
- Demanda: 1.0 (normal)
- Propina: 10% (cliente estándar)
- **Precio final: 11c**

**Vino Élfico Raro:**
- Costo base: 200c
- Rareza: 2.0 (raro)
- Demanda: 1.2 (alta, Festival Élfico)
- Propina: 15% (elfo agradecido)
- **Precio final: 552c**

### Propinas por Raza/Clase

| Raza/Clase | Propina Base | Notas |
|------------|--------------|-------|
| Humano | 10% | Estándar |
| Enano | 15-20% | Generosos si felices |
| Elfo del Bosque | 0% | No dan propina (vulgar) |
| Elfo de la Noche | 5% | Calculadores |
| Duende | 0-5% | Tacaños, pueden robar |
| Minotauro | 10% | Directos |
| Dracónido | 15-25% | Ricos, nobles |
| Centauro | 15% | Honorables |
| Guerrero | +5% | Respetan servicio |
| Paladín | +10% | Generosidad divina |
| Pícaro | -5% | Tacaños |
| Plebeyo | +0% | Pobres |

### Ingresos por Cliente

**Promedio por cliente:**
- Early Game: 15-30c
- Mid Game: 30-80c
- Late Game: 80-200c

**Clientes por día:**
- Early Game: 8-12 clientes
- Mid Game: 15-25 clientes
- Late Game: 25-40 clientes

**Ingreso bruto diario promedio:**
- Early Game: 120-360c/día
- Mid Game: 450-2000c/día
- Late Game: 2000-8000c/día

---

## 💸 GASTOS

### Gastos Fijos Diarios

**Obligatorios todos los días:**

| Concepto | Costo | Frecuencia | Notas |
|----------|-------|------------|-------|
| **Alquiler** | 50c | Diario | Dueño del edificio |
| **Servicios** | 10c | Diario | Agua, luz (magia) |
| **Limpieza** | 5c | Diario | Básica |
| **Seguro** | 20c | Diario | Protección básica |
| **Licencia** | 15c | Diario | Permiso de operación |
| **TOTAL BÁSICO** | **100c/día** | Diario | **Mínimo para abrir** |

**Con empleados:**

| Empleado | Salario | Beneficio |
|----------|---------|-----------|
| Camarero | 30c/día | +5 clientes/día, +10% velocidad |
| Cocinero | 25c/día | Vende comida (+50c/día promedio) |
| Guardia | 50c/día | -50% robos, +seguridad |
| Músico | 20c/día | +ambiente, +10% propinas |

### Gastos Variables

**Stock de Bebidas:**
- Debes comprar stock para el día siguiente
- Costo: 40-60% del precio de venta
- Si no tienes stock → No puedes vender

**Ejemplo:**
- Vendes cerveza a 10c
- Compras cerveza a 4-6c
- Margen: 40-60%

**Reparaciones:**
- Daño por cliente borracho: 20-100c
- Daño por Minotauro: 200-500c
- Daño por Dracónido: 100-300c
- Daño estructural: 500-2000c

**Multas:**
- Violación menor: 50-150c
- Violación grave: 200-500c
- Servir a criminal: 300-1000c
- Documento falso no detectado: 100-400c

### Impuestos

**Impuesto Diario:**
- 10% de ganancia bruta del día anterior
- Calculado al abrir (6:00)
- No puedes evitarlo (legal)

**Ejemplo:**
- Día 1: Ganaste 500c
- Día 2: Pagas 50c de impuesto al abrir

**Con alta reputación Gremio Comerciantes (+60):**
- Impuesto reducido a 7%

---

## 🏗️ SISTEMA DE UPGRADES

### Categorías de Upgrades

**1. CAPACIDAD**
- Más mesas/sillas
- Más clientes simultáneos
- Más almacenamiento

**2. SEGURIDAD**
- Protección contra robos
- Guardias contratados
- Sistemas de alarma

**3. CALIDAD**
- Mejor decoración (+propinas)
- Mejor equipo (+velocidad)
- Mejor ambiente (+reputación)

**4. EFICIENCIA**
- Herramientas mejores (-tiempo servicio)
- Stock automático
- Automatización

**5. ESPECIALES**
- Enchantments mágicos
- Licencias especiales
- Membresías de facciones

---

## 🛠️ UPGRADES DETALLADOS

### Tier 1 - Early Game (Días 1-30)

**Mesa Extra (+2 clientes simultáneos)**
- Costo: 200c
- Beneficio: +2 clientes al mismo tiempo
- ROI: ~10 días (20c extra/día)

**Barril de Cerveza Mejorado (+20% stock)**
- Costo: 150c
- Beneficio: Almacenas más cerveza, menos viajes
- ROI: Conveniencia

**Decoración Básica (+5% propinas)**
- Costo: 100c
- Beneficio: +5% propinas
- ROI: ~20 días (5c extra/día)

**Cerradura Reforzada (-30% robos)**
- Costo: 250c
- Beneficio: -30% probabilidad de robo
- ROI: Variable (ahorra 30-100c por robo evitado)

---

### Tier 2 - Mid Game (Días 31-60)

**Ampliación del Local (+5 clientes)**
- Costo: 800c
- Beneficio: +5 clientes simultáneos
- ROI: ~15 días (50c extra/día)

**Cocina Profesional (habilita comida)**
- Costo: 600c
- Beneficio: Vende comida (+100-200c/día)
- ROI: 3-6 días

**Sistema de Alarma Mágico (-60% robos)**
- Costo: 700c
- Beneficio: -60% robos, alerta temprana
- ROI: 5-10 días (según frecuencia de robos)

**Escenario para Músicos (+15% propinas)**
- Costo: 400c
- Beneficio: +15% propinas, +ambiente
- Requiere: Contratar músico (20c/día)
- ROI: ~15 días

**Catálogo de Sellos Oficiales (anti-falsificación)**
- Costo: 500c
- Beneficio: +30% detección de falsificaciones
- ROI: Evita multas (100-400c)

---

### Tier 3 - Late Game (Días 61+)

**Segunda Planta (+10 clientes, +VIP room)**
- Costo: 2500c
- Beneficio: +10 clientes, zona VIP (clientes ricos pagan +50%)
- ROI: ~20 días (125c extra/día)

**Enchantment Anti-Robo (inmunidad robos)**
- Costo: 2000c
- Beneficio: Inmunidad total a robos mundanos
- Requiere: Reputación +40 con Círculo Arcano
- ROI: 10-15 días

**Licencia de Mercado Negro (bebidas ilegales)**
- Costo: 1500c
- Beneficio: Vende bebidas ilegales (+200% precio)
- Requiere: Reputación +60 con Gremio de Ladrones
- ROI: ~8 días (200c extra/día)

**Bodega de Vinos de Lujo (almacén premium)**
- Costo: 1800c
- Beneficio: Almacena vinos raros, +control temperatura
- ROI: Acceso a clientes nobles

**Guardia Personal Permanente (protección total)**
- Costo inicial: 1000c
- Costo mensual: 300c/mes (10c/día)
- Beneficio: -80% violencia, -90% robos, +intimidación

---

### Tier 4 - End Game (Día 90+)

**Franquicia (segunda taberna)**
- Costo: 5000c
- Beneficio: +50% ingreso pasivo/día (gestionada por IA)
- Requiere: Reputación +70 con Gremio Comerciantes
- ROI: ~25 días

**Taberna Legendaria (reconocimiento total)**
- Costo: 10000c
- Beneficio: Clientes VIP exclusivos, +100% propinas, inmunidad inspecciones
- Requiere: Reputación +80 con 3 facciones
- ROI: Prestigio (no económico directo)

**Portal Mágico (teletransporte de suministros)**
- Costo: 8000c
- Beneficio: Stock infinito, sin esperar entregas
- Requiere: Reputación +80 con Círculo Arcano
- ROI: Conveniencia extrema

---

## 📈 PROGRESIÓN ECONÓMICA

### Fases del Juego

**Fase 1: SUPERVIVENCIA (Días 1-15)**

**Objetivo:** No morir
- Ingresos: 120-360c/día
- Gastos: 100c/día (fijos)
- Balance: +20 a +260c/día
- Estrategia: Minimalismo, evitar riesgos, aceptar casi todos los clientes

**Upgrades recomendados:**
- Mesa Extra (200c) - Prioridad 1
- Decoración Básica (100c) - Prioridad 2
- Cerradura (250c) - Si hay robos

**Objetivo de ahorro:** 500c (buffer de emergencia)

---

**Fase 2: CRECIMIENTO (Días 16-45)**

**Objetivo:** Expandir e invertir
- Ingresos: 450-2000c/día
- Gastos: 150-250c/día (fijos + empleados)
- Balance: +200 a +1750c/día
- Estrategia: Inversión agresiva, contratar empleados, aumentar capacidad

**Upgrades recomendados:**
- Ampliación Local (800c) - Prioridad 1
- Cocina (600c) - Prioridad 2
- Sistema Alarma (700c) - Prioridad 3
- Contratar Camarero (30c/día)

**Objetivo de ahorro:** 2000c (para tier 3)

---

**Fase 3: CONSOLIDACIÓN (Días 46-75)**

**Objetivo:** Estabilizar y optimizar
- Ingresos: 2000-5000c/día
- Gastos: 300-500c/día (todo incluido)
- Balance: +1500 a +4700c/día
- Estrategia: Alta selectividad de clientes, especializarse en nicho

**Upgrades recomendados:**
- Segunda Planta (2500c) - Prioridad 1
- Enchantment Anti-Robo (2000c) - Prioridad 2
- Bodega Vinos (1800c) - Prioridad 3
- Contratar Guardia (50c/día)

**Objetivo de ahorro:** 5000c+ (para tier 4)

---

**Fase 4: DOMINIO (Día 76+)**

**Objetivo:** Maximizar y dominar mercado
- Ingresos: 5000-15000c/día
- Gastos: 500-800c/día (operación completa)
- Balance: +4200 a +14200c/día
- Estrategia: Clientes VIP exclusivos, múltiples ingresos pasivos

**Upgrades recomendados:**
- Franquicia (5000c)
- Portal Mágico (8000c)
- Taberna Legendaria (10000c)

**Objetivo de ahorro:** Infinito (eres rico)

---

## ⚖️ BALANCE Y DIFICULTAD

### Curva de Dificultad Económica

**Días 1-7: TUTORIAL (Muy Fácil)**
- Gastos bajos (50c/día)
- Clientes honestos (90%)
- Sin eventos catastróficos
- Objetivo: Aprender sin morir

**Días 8-30: NORMAL (Moderado)**
- Gastos normales (100c/día)
- Clientes mixtos (70% honestos)
- Eventos menores (robos 10-50c)
- Objetivo: Crecer establemente

**Días 31-60: DIFÍCIL (Alto)**
- Gastos altos (200c/día con empleados)
- Clientes sospechosos (50% honestos)
- Eventos mayores (destrucción 100-300c)
- Objetivo: Sobrevivir y expandir

**Días 61+: MAESTRÍA (Muy Alto)**
- Gastos muy altos (400c/día)
- Clientes extremos (30% honestos)
- Eventos catastróficos (500-2000c)
- Objetivo: Dominar

---

## 🎯 ESTRATEGIAS ECONÓMICAS

### Estrategia 1: CONSERVADORA (Bajo Riesgo)

**Filosofía:** Seguridad primero
- Acepta solo clientes con documentos perfectos
- Invierte en seguridad temprano
- Mantiene buffer de 500c siempre
- No toma préstamos

**Pro:** Muy difícil quebrar
**Con:** Crecimiento lento, ingresos bajos

---

### Estrategia 2: AGRESIVA (Alto Riesgo)

**Filosofía:** Crecer rápido o morir
- Acepta clientes sospechosos (más volumen)
- Invierte todo en capacidad
- Opera con buffer mínimo (100c)
- Toma préstamos para upgrades

**Pro:** Crecimiento explosivo
**Con:** Un desastre = game over

---

### Estrategia 3: ESPECIALIZADA (Nicho)

**Filosofía:** Maestro de un nicho
- Enfoque en facción específica (ej: solo nobles)
- Invierte en calidad, no cantidad
- Precios premium
- Reputación como ventaja

**Pro:** Altos márgenes, clientes leales
**Con:** Vulnerable a cambios en facción

---

### Estrategia 4: VOLUMEN (Eficiencia)

**Filosofía:** Vende mucho, margen bajo
- Máxima capacidad (muchos clientes)
- Precios competitivos
- Velocidad optimizada
- Automatización

**Pro:** Ingresos estables, predecibles
**Con:** Margen bajo, requiere mucho trabajo

---

## 💡 SISTEMAS ESPECIALES

### Préstamos

**Gremio de Comerciantes ofrece préstamos:**

| Cantidad | Interés | Plazo | Requisito |
|----------|---------|-------|-----------|
| 500c | 10% | 15 días | Rep +20 |
| 1000c | 15% | 30 días | Rep +40 |
| 2000c | 20% | 45 días | Rep +60 |
| 5000c | 0% | 60 días | Rep +80 |

**Si no pagas:**
- -50 reputación Gremio
- Embargo de bienes
- Posible game over

---

### Seguros

**Compra de Gremio de Comerciantes:**

| Tipo | Costo | Cobertura |
|------|-------|-----------|
| Robo | 50c/mes | 80% de pérdidas por robo |
| Incendio | 80c/mes | 90% de daño por fuego |
| Violencia | 100c/mes | 70% de daño por peleas |
| Completo | 200c/mes | 80% de todo |

**ROI:** Solo vale la pena si experimentas eventos frecuentes

---

### Inversiones Pasivas

**Disponibles late game:**

| Inversión | Costo | Retorno |
|-----------|-------|---------|
| Acciones Gremio | 2000c | +50c/día |
| Caravana Comercial | 3000c | +80c/día (riesgo 20% pérdida) |
| Mina Enana | 5000c | +150c/día |
| Viñedo Élfico | 8000c | +300c/día (requiere 60 días) |

---

## 📊 TABLA DE PRECIOS DE REFERENCIA

### Bebidas Comunes

| Bebida | Costo | Venta | Margen |
|--------|-------|-------|--------|
| Agua | 0c | 1c | 100% |
| Cerveza Común | 4c | 10c | 60% |
| Vino Común | 8c | 20c | 60% |
| Ron | 12c | 30c | 60% |
| Whisky | 20c | 50c | 60% |

### Bebidas Especiales

| Bebida | Costo | Venta | Margen |
|--------|-------|-------|--------|
| Cerveza Enana | 30c | 80c | 62% |
| Vino Élfico | 100c | 250c | 60% |
| Hidromiel Centauro | 80c | 200c | 60% |
| Aguardiente Dracónido | 150c | 400c | 62% |

### Bebidas Raras/Legendarias

| Bebida | Costo | Venta | Margen |
|--------|-------|-------|--------|
| Vino Élfico 100 años | 400c | 1000c | 60% |
| Poción Mágica | 200c | 600c | 67% |
| Licor Prohibido | 300c | 1200c | 75% (ilegal) |
| Bebida Legendaria | 1000c | 5000c | 80% |

**Nota:** Margen consistente ~60% permite cálculos fáciles

---

## 🎮 BALANCE RECOMENDADO

### Objetivos de Ahorro por Fase

| Día | Ahorro Objetivo | Propósito |
|-----|----------------|-----------|
| 7 | 200c | Buffer mínimo |
| 15 | 500c | Primera expansión |
| 30 | 1500c | Empleados + upgrades |
| 45 | 3000c | Tier 3 upgrades |
| 60 | 5000c | Segunda planta o franquicia |
| 90+ | 10000c+ | Dominio total |

### Ingresos Mínimos para Sobrevivir

| Fase | Ingreso Mínimo/Día | Gastos/Día | Margen |
|------|-------------------|-----------|--------|
| Early | 150c | 100c | 50c |
| Mid | 400c | 250c | 150c |
| Late | 800c | 500c | 300c |
| End | 1500c | 800c | 700c |

**Si caes bajo mínimo por 3 días consecutivos → Entra en DEUDA**

---

## ⚠️ SISTEMAS DE EMERGENCIA

### Deuda y Bancarrota

**Si llegas a 0 monedas:**

1. **Día 1 de Deuda:**
   - Advertencia
   - Gremio ofrece préstamo de emergencia (200c, 50% interés)

2. **Día 2-3 de Deuda:**
   - No puedes comprar stock
   - Solo vendes lo que tienes
   - Clientes disminuyen -50%

3. **Día 4+ de Deuda:**
   - Embargo de bienes
   - Pierdes upgrades (vendidos)
   - Si no recuperas → GAME OVER Día 7

**Cómo salir:**
- Acepta préstamo
- Vende upgrades manualmente
- Pide ayuda a facción aliada (+60 rep)

---

## 📂 ARCHIVOS DEL SISTEMA

- `README.md` ← Estás aquí (overview)
- `precios-dinamicos.md` - Sistema de precios variable
- `upgrades-completos.md` - Catálogo completo de mejoras
- `balance-economico.md` - Números, fórmulas, balance
- `RESUMEN-EJECUTIVO.md` - Estado del sistema

---

**Sistema de Economía:** Núcleo de supervivencia y progresión del jugador.
