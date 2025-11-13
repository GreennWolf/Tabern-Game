# 📋 RESUMEN EJECUTIVO - Sistema de Razas

## ✅ Estado: COMPLETO Y DEFINIDO

Fecha: 2025-11-13

---

## 📦 Contenido del Sistema

### Razas Implementadas: 8

1. ✅ **Humano** - Raza base estándar
2. ✅ **Enano** - Bebedores legendarios
3. ✅ **Elfo del Bosque** - Longevos con glamour
4. ✅ **Elfo de la Noche** - Mentirosos peligrosos
5. ✅ **Duende** - Maestros falsificadores
6. ✅ **Minotauro** - Fuerza destructiva
7. ✅ **Dracónido** - Peligro elemental
8. ✅ **Centauro** - Sabios pero logísticamente complejos

---

## 📁 Estructura de Archivos

```
docs/game-design/razas/
├── README.md                    # Índice y sistema de aparición
├── comparacion-razas.md         # Tablas comparativas y análisis
├── RESUMEN-EJECUTIVO.md         # Este archivo
├── humano.md                    # Especificación completa
├── enano.md                     # Especificación completa
├── elfo-del-bosque.md          # Especificación completa
├── elfo-de-la-noche.md         # Especificación completa
├── duende.md                    # Especificación completa
├── minotauro.md                # Especificación completa
├── draconido.md                # Especificación completa
└── centauro.md                 # Especificación completa
```

---

## 🎯 Plantilla Completada para Cada Raza

Cada archivo de raza incluye:

- ✅ **Edad Legal:** Edad mínima para consumir alcohol
- ✅ **Esperanza de Vida:** Longevidad de la raza
- ✅ **Etapas de Vida:** Rangos de edad con descripción física
- ✅ **Tolerancia al Alcohol:** Escala 1-10
- ✅ **Comportamiento Borracho:** 3 niveles progresivos
- ✅ **Bebidas Favoritas:** Preferencias culturales
- ✅ **Bebidas Prohibidas:** Tabúes y restricciones
- ✅ **Habilidades Especiales:** Capacidades únicas con efecto en gameplay
- ✅ **Actitud hacia otras razas:** Relaciones interraciales detalladas
- ✅ **Rasgos Físicos:** Descripción visual completa
- ✅ **Propensión a Mentir:** Escala 1-10 con explicación cultural
- ✅ **Notas de Juego:** Dificultad, comportamiento, riesgos, estrategias
- ✅ **Señales de Alerta:** Banderas rojas para el jugador
- ✅ **Verificación Recomendada:** Pasos sugeridos
- ✅ **Eventos Especiales:** Ideas de eventos narrativos
- ✅ **Mecánicas Especiales:** Sistemas únicos (si aplica)
- ✅ **Balanceo:** Consideraciones de diseño
- ✅ **Notas Culturales:** Lore y contexto del mundo

---

## 📊 Datos Clave del Sistema

### Distribución de Dificultad

| Nivel | Cantidad | Razas |
|-------|----------|-------|
| Baja | 1 | Humano |
| Media | 3 | Elfo del Bosque, Enano, Duende* |
| Alta | 3 | Elfo de la Noche, Dracónido, Centauro |
| Muy Alta | 1 | Minotauro |

*Duende es "media" en verificación pero "muy alta" en frecuencia de engaño

### Distribución de Peligrosidad

| Nivel | Razas |
|-------|-------|
| 🟢 Bajo | Humano, Elfo del Bosque |
| 🟡 Medio | Enano, Duende |
| 🟠 Alto | Elfo de la Noche, Dracónido, Centauro |
| 🔴 Crítico | Minotauro |

### Honestidad Promedio

- **Muy Honestos (1-3):** 3 razas
- **Moderados (4-5):** 2 razas
- **Mentirosos (6-9):** 3 razas
- **Promedio general:** 4.75/10

### Tolerancia Promedio

- **Muy Baja (1-3):** 2 razas
- **Media (4-6):** 3 razas
- **Alta (7-8):** 2 razas
- **Legendaria (9-10):** 1 raza
- **Promedio general:** 5.6/10

---

## 🎮 Integración con Gameplay

### Progresión Temporal

**Early Game (Días 1-10):**
- 3 razas: Humano (70%), Duende (20%), Elfo del Bosque (10%)
- Foco: Aprender mecánicas básicas
- Dificultad: Baja-Media

**Mid Game (Días 11-20):**
- +3 razas: Elfo de la Noche, Enano, Dracónido
- Foco: Complejidad, peligros reales
- Dificultad: Media-Alta

**Late Game (Días 21+):**
- +2 razas: Minotauro, Centauro
- Foco: Maestría, máximo desafío
- Dificultad: Alta-Muy Alta

### Mecánicas Introducidas

1. **Verificación de Edad** (Día 1 - Humano)
2. **Detección de Falsificación** (Día 3 - Duende)
3. **Glamour/Ilusiones** (Día 6 - Elfo del Bosque)
4. **Mentiras Complejas** (Día 11 - Elfo de la Noche)
5. **Conflictos Interraciales** (Día 11 - Enano vs Elfo)
6. **Peligros Elementales** (Día 16 - Dracónido)
7. **Gestión de Violencia** (Día 21 - Minotauro)
8. **Logística de Espacio** (Día 21 - Centauro)

### Sistemas Afectados

- ✅ **Sistema de Documentos:** Falsificación, verificación
- ✅ **Sistema de Diálogo IA:** Mentiras por raza
- ✅ **Sistema de Reputación:** Por raza y facción
- ✅ **Sistema de Daños:** Destrucción, costos
- ✅ **Sistema de Espacio:** Ocupación física
- ✅ **Sistema de Bebidas:** Preferencias y efectos
- ✅ **Sistema de Eventos:** Específicos por raza
- ✅ **Sistema de Upgrades:** Seguridad, espacio, etc.

---

## 🔗 Relaciones Interraciales

### Conflictos Críticos (Pueden causar peleas)

1. **Enano ↔ Elfo del Bosque** (Rivalidad histórica)
2. **Elfo del Bosque ↔ Elfo de la Noche** (Enemigos ancestrales)
3. **Minotauro + Cualquier raza borracha** (Violencia)

### Alianzas Positivas

1. **Humano ↔ Enano** (Comercio)
2. **Elfo del Bosque ↔ Centauro** (Naturaleza)
3. **Elfo de la Noche ↔ Minotauro** (Pragmática)

---

## 💰 Impacto Económico

### Alto Valor (Pagan Bien)
- Dracónido
- Enano (+ propinas)
- Centauro
- Minotauro (si no destruyen)

### Valor Medio
- Humano
- Elfo del Bosque (sin propinas)
- Elfo de la Noche

### Bajo Valor / Riesgo de Estafa
- Duende (pueden intentar estafar)

### Costos Potenciales
- Minotauro: -200+ monedas (destrucción)
- Dracónido: -100+ monedas (aliento elemental)
- Centauro: -50+ monedas (daño estructural)
- Duende: -5 a -20 monedas (robo pequeño)

---

## 🎨 Consideraciones de Diseño Visual

### Tamaños Relativos

| Raza | Altura Aproximada | Consideraciones Visuales |
|------|------------------|-------------------------|
| Duende | 0.8-1.1m | Pequeño, cámara debe ajustar |
| Enano | 1.2-1.5m | Bajo pero robusto |
| Humano | 1.6-1.9m | Estándar de referencia |
| Elfo del Bosque | 1.7-2.0m | Grácil, elegante |
| Elfo de la Noche | 1.75-2.05m | Similar pero más intimidante |
| Dracónido | 1.8-2.3m | Imponente, reptiliano |
| Minotauro | 2.2-2.8m | ENORME, muy intimidante |
| Centauro | 2.1-2.4m (altura) | Cuerpo de caballo, vista especial |

### Desafíos Visuales Especiales

- **Centauro:** Cuerpo completo no cabe en encuadre estándar
- **Minotauro:** Efecto de intimidación por tamaño
- **Dracónido:** Efectos elementales (fuego, hielo, etc.)
- **Elfo (ambos):** Glamour visual (efecto de ilusión)
- **Duende:** Animaciones de robo/prestidigitación

---

## 🧪 Testing y Balanceo

### Puntos Críticos a Testear

1. **Curva de Dificultad:**
   - ¿Es el salto de early a mid game manejable?
   - ¿Late game es desafiante pero no frustrante?

2. **Frecuencia de Mentiras:**
   - ¿60% de duendes tramposos es demasiado?
   - ¿Jugador puede aprender a detectar patrones?

3. **Eventos de Desastre:**
   - ¿Minotauro destructor es recuperable?
   - ¿Aliento dracónido tiene contramedidas?

4. **Economía:**
   - ¿Balance entre riesgo y recompensa?
   - ¿Upgrades son accesibles pero no triviales?

5. **Relaciones Interraciales:**
   - ¿Frecuencia de conflictos está balanceada?
   - ¿Jugador puede prevenir peleas?

### Métricas Sugeridas

- **Tasa de éxito del jugador:** 60-70% (difícil pero justo)
- **Tasa de desastres:** <10% (raros pero memorables)
- **Tiempo promedio por cliente:** 1-3 minutos
- **Clientes por día:** 10-15 (early), 20-30 (late)

---

## ✏️ Próximos Pasos Sugeridos

Ahora que las razas están completamente definidas, los siguientes sistemas a trabajar serían:

1. **Sistema de Clases** (Paladín, Guerrero, Mago, etc.)
2. **Sistema de Bebidas** (Catálogo completo con efectos)
3. **Sistema de Reglas del Libro** (Leyes por día/evento)
4. **Sistema de Documentos** (Tipos, falsificación, verificación)
5. **Sistema de Facciones** (Organizaciones, conflictos, reputación)
6. **Sistema de Eventos** (Narrativos, inspecciones, crisis)
7. **Sistema de Economía** (Precios, costos, upgrades)
8. **Progresión Narrativa** (Arco principal, finales)

---

## 📝 Notas Finales

### Fortalezas del Sistema

✅ **Diversidad:** 8 razas únicas con personalidades distintas
✅ **Progresión Clara:** Early → Mid → Late bien definida
✅ **Complejidad Escalable:** De simple (Humano) a complejo (Minotauro)
✅ **Relaciones Dinámicas:** Conflictos y alianzas interraciales
✅ **Balance Riesgo/Recompensa:** Razas peligrosas pagan mejor
✅ **Tutorialización Integrada:** Cada raza enseña una mecánica
✅ **Coherencia de Lore:** Cada raza tiene cultura y motivaciones
✅ **Flexibilidad de Diseño:** Fácil agregar razas futuras

### Consideraciones Técnicas

- Cada raza es un objeto/perfil claramente definido
- Sistema modular: fácil de editar/expandir
- Atributos numéricos permiten balanceo preciso
- Habilidades especiales están bien definidas para programación
- Relaciones interraciales son matriz clara

### Modificaciones Futuras

El sistema está diseñado para permitir:
- Agregar nuevas razas sin romper balance
- Ajustar porcentajes de aparición
- Modificar atributos individuales
- Añadir subespecies o variantes
- Eventos especiales por combinaciones de razas

---

## 🎉 SISTEMA COMPLETO Y LISTO PARA IMPLEMENTACIÓN

**Total de Páginas de Documentación:** 10 archivos MD
**Total de Razas Especificadas:** 8/8 (100%)
**Nivel de Detalle:** Alto (cada raza >2000 palabras)
**Estado:** ✅ APROBADO PARA CONTINUAR AL SIGUIENTE SISTEMA

---

*Documento generado: 2025-11-13*
*Próxima revisión: Después de implementar Sistema de Clases*
