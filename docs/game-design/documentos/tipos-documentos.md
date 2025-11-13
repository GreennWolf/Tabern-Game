# 📋 Tipos de Documentos - Plantillas Detalladas

Este documento define la estructura exacta de cada tipo de documento en el juego.

---

## 🪪 1. IDENTIFICACIÓN PERSONAL (ID)

**Obligatorio para:** TODOS los clientes

### Plantilla Visual

```
╔══════════════════════════════════════════╗
║  REINO DE CRUCE - IDENTIFICACIÓN        ║
║                                          ║
║  ┌──────────┐                            ║
║  │          │  NOMBRE: Juan Pérez        ║
║  │  RETRATO │  RAZA: Humano              ║
║  │          │  EDAD: 25 años             ║
║  └──────────┘  SEXO: Masculino           ║
║                                          ║
║  FECHA NACIMIENTO: 15/3/1200            ║
║  LUGAR NACIMIENTO: Cruce, Distrito Norte║
║                                          ║
║  FECHA EMISIÓN: 10/1/1225               ║
║  VÁLIDO HASTA: 10/1/1235                ║
║                                          ║
║  AUTORIDAD: Consejo Municipal de Cruce  ║
║  Nº SERIE: CR-1225-0543                 ║
║                                          ║
║  ┌────────┐                              ║
║  │ SELLO  │  Firma: [Firma manuscrita]  ║
║  │OFICIAL │                              ║
║  └────────┘                              ║
╚══════════════════════════════════════════╝
```

### Elementos Clave

**Retrato:**
- Sprite del cliente (debe coincidir visualmente)
- Tamaño: 64x64 pixels
- Elfos con glamour: retrato muestra versión "glamurosa" (más vieja)

**Nombre:**
- Formato: Nombre + Apellido(s)
- Variaciones culturales:
  - Humanos: 1-2 apellidos
  - Enanos: Nombre + "hijo de [Padre]" (ej: Thorin hijo de Thrain)
  - Elfos: Nombre + "de [Lugar]" (ej: Legolas de Bosque Verde)
  - Minotauros: Nombre único (ej: Asterion)

**Raza:**
- Debe ser una de las 8 razas jugables
- Escrito completo (no abreviado)

**Edad:**
- En años
- Debe ser legal según raza (ver docs/game-design/razas/)

**Fecha Emisión:**
- Formato: DD/MM/AAAA
- No puede ser futura
- No puede ser más de 10 años atrás (IDs expiran)

**Autoridad Emisora:**
- Lista de autoridades legítimas (ver abajo)
- Debe coincidir con lugar de nacimiento/residencia

**Número de Serie:**
- Formato: [CÓDIGO]-[AÑO]-[NÚMERO]
  - CR = Cruce
  - BV = Bosque Verde (Élfico)
  - MH = Montaña de Hierro (Enano)
- Único para cada ID

**Sello Oficial:**
- Imagen del sello de la autoridad emisora
- Debe coincidir con catálogo de sellos (en tu taberna)

**Firma:**
- Manuscrita (visual)
- No necesita ser legible pero debe existir

---

## ⚔️ 2. PERMISO DE PORTE DE ARMAS

**Obligatorio para:** Clientes que portan arma visible

### Plantilla Visual

```
╔══════════════════════════════════════════╗
║  GUARDIA REAL - PERMISO DE ARMAS        ║
║                                          ║
║  PORTADOR: Juan Pérez                   ║
║  CLASE: Guerrero                         ║
║  RAZA: Humano                            ║
║                                          ║
║  ARMAS AUTORIZADAS:                     ║
║  [✓] Espada Larga                       ║
║  [✓] Daga                                ║
║  [ ] Arco                                ║
║  [ ] Hacha de Guerra                     ║
║                                          ║
║  RESTRICCIONES:                          ║
║  - No desenvainar en lugares públicos   ║
║  - No portar en templos                  ║
║                                          ║
║  EMITIDO: 5/6/1225                      ║
║  VENCE: 5/6/1226                         ║
║                                          ║
║  AUTORIDAD: Capitán de la Guardia       ║
║  ┌────────┐                              ║
║  │ SELLO  │  Firma: [Firma del Capitán] ║
║  │ GUARDIA│                              ║
║  └────────┘                              ║
╚══════════════════════════════════════════╝
```

### Verificaciones Clave

**Clase compatible con arma:**
- Guerrero + Espada: ✓ OK
- Mago + Espada: ❌ Sospechoso
- Bárbaro + Hacha: ✓ OK
- Pícaro + Arco: ✓ OK

**Fecha vencimiento:**
- No puede estar vencido
- Si vencido → Cliente no puede portar armas legalmente

**Arma visible coincide con autorizada:**
- Cliente porta Espada Larga → Debe tener [✓] Espada Larga
- Cliente porta Arco → Debe tener [✓] Arco

---

## 🔮 3. LICENCIA DE USO DE MAGIA

**Obligatorio para:** Clases mágicas (Mago, Hechicero, Clérigo, Druida)

### Plantilla Visual

```
╔══════════════════════════════════════════╗
║  CONSEJO DE MAGOS - LICENCIA ARCANA     ║
║                                          ║
║  MAGO: Elena de la Torre                ║
║  CLASE: Mago                             ║
║  ESPECIALIZACIÓN: Evocación              ║
║                                          ║
║  NIVEL MÁGICO AUTORIZADO: 3              ║
║  (Hechizos hasta Nivel 3)                ║
║                                          ║
║  ESCUELAS PERMITIDAS:                    ║
║  [✓] Evocación                           ║
║  [✓] Abjuración                          ║
║  [ ] Nigromancia (PROHIBIDA)             ║
║                                          ║
║  RESTRICCIONES:                          ║
║  - No lanzar hechizos ofensivos en ciudad║
║  - No convocar criaturas extraplanares   ║
║                                          ║
║  EMITIDO: 12/2/1224                     ║
║  VENCE: 12/2/1229 (5 años)              ║
║                                          ║
║  AUTORIDAD: Gran Archimago Aldric       ║
║  ┌────────┐        ┌──────────┐         ║
║  │ SELLO  │        │  MARCA   │         ║
║  │CONSEJO │        │MÁGICA UV │         ║
║  └────────┘        └──────────┘         ║
║                                          ║
║  Firma: [Firma del Archimago]           ║
╚══════════════════════════════════════════╝
```

### Verificaciones Clave

**Clase debe ser mágica:**
- Mago, Hechicero, Clérigo, Druida: ✓ Requiere licencia
- Guerrero, Bárbaro, Pícaro: ❌ NO necesita licencia (no usan magia)

**Restricciones raciales:**
- Enano + Licencia de Magia: ❌ IMPOSIBLE (Enanos no creen en magia)
- Elfo + Licencia de Magia: ✓ Común

**Marca Mágica UV:**
- Solo visible con Luz UV (upgrade de taberna)
- Documentos reales: Símbolo arcano brilla
- Falsificaciones: No brilla o brilla incorrectamente

**Escuelas Prohibidas:**
- Nigromancia: Generalmente prohibida
- Si cliente tiene [✓] Nigromancia → Documento ilegal o facción oscura

---

## 🛡️ 4. CERTIFICADO DE AFILIACIÓN A FACCIÓN

**Obligatorio para:** Clientes que representan una facción oficial

### Plantilla Visual

```
╔══════════════════════════════════════════╗
║  GREMIO DE COMERCIANTES - CERTIFICADO   ║
║                                          ║
║  ┌──────────┐                            ║
║  │  SELLO   │  MIEMBRO: Carlos Montero  ║
║  │ GREMIO   │  RANGO: Mercader Junior   ║
║  └──────────┘                            ║
║                                          ║
║  FACCIÓN: Gremio de Comerciantes        ║
║  CÓDIGO MIEMBRO: GM-1225-0892           ║
║                                          ║
║  PRIVILEGIOS:                            ║
║  [✓] Descuento 10% en tabernas          ║
║  [✓] Acceso a Distrito Comercial 24/7   ║
║  [ ] Exención de impuestos               ║
║                                          ║
║  RESPONSABILIDADES:                      ║
║  - Pagar cuota mensual (50 monedas)     ║
║  - Representar al Gremio honorablemente ║
║                                          ║
║  EMITIDO: 1/1/1225                      ║
║  VÁLIDO HASTA: 31/12/1225               ║
║                                          ║
║  AUTORIDAD: Maestro del Gremio          ║
║  Firma: [Firma del Maestro]             ║
╚══════════════════════════════════════════╝
```

### Facciones Principales

**Legales/Neutrales:**
1. Gremio de Comerciantes
2. Guardia Real
3. Templo de la Luz
4. Consejo de Magos
5. Orden de Paladines
6. Gremio de Artesanos

**Sospechosas/Ilegales:**
7. Gremio de Ladrones (ilegal pero tolerado)
8. Culto de la Sombra (completamente ilegal)
9. Hermandad Sangrienta (organización criminal)

### Verificaciones Clave

**Privilegios deben respetarse:**
- Cliente con "Descuento 10%" → Debes aplicar descuento
- Cliente con "Exención de Reglas Menores" → Puede violar reglas menores sin consecuencia

**Conflictos de facción:**
- Templo de la Luz + Culto de la Sombra: ❌ IMPOSIBLE (facciones enemigas)
- Guardia Real + Gremio de Ladrones: ❌ IMPOSIBLE

**Fecha vencimiento:**
- Certificados de facción vencen anualmente
- Si vencido → Privilegios no aplican

---

## 🏛️ 5. PERMISO DE ENTRADA A LA CIUDAD

**Obligatorio para:** Razas "exóticas" según reglas del día (Minotauro, Dracónido)

### Plantilla Visual

```
╔══════════════════════════════════════════╗
║  GUARDIA FRONTERIZA - PERMISO ENTRADA   ║
║                                          ║
║  VISITANTE: Asterion                    ║
║  RAZA: Minotauro                         ║
║  ORIGEN: Llanuras del Sur                ║
║                                          ║
║  PROPÓSITO DE VISITA:                    ║
║  Comercio - Venta de pieles              ║
║                                          ║
║  DURACIÓN AUTORIZADA:                    ║
║  Del 1/6/1225 al 7/6/1225 (7 días)      ║
║                                          ║
║  RESTRICCIONES:                          ║
║  - Solo Distrito Comercial y Tabernas   ║
║  - Toque de queda: 22:00                 ║
║  - Supervisión requerida en Distrito Noble║
║                                          ║
║  FIANZA DEPOSITADA: 100 monedas         ║
║  (Devuelta al salir si no hay incidentes)║
║                                          ║
║  EMITIDO: 1/6/1225                      ║
║  FRONTERA: Puerta Sur                    ║
║                                          ║
║  AUTORIDAD: Guardia Fronterizo Marcus   ║
║  ┌────────┐                              ║
║  │ SELLO  │  Firma: [Firma del Guardia] ║
║  │FRONTERA│                              ║
║  └────────┘                              ║
╚══════════════════════════════════════════╝
```

### Verificaciones Clave

**Duración:**
- Hoy es 5/6/1225 → Permiso válido (dentro de rango)
- Hoy es 10/6/1225 → Permiso VENCIDO → Cliente ilegal

**Restricciones de tiempo:**
- Si es 23:00 y permiso dice "Toque de queda 22:00" → Cliente violando regla
- Debes rechazar o reportar

**Reglas cambiantes:**
- Libro de Reglas dice "Hoy prohibido Minotauros"
- Cliente tiene permiso válido
- → Regla del día ANULA permiso → Debes rechazar

---

## ✨ 6. CERTIFICADO DE PUREZA DIVINA

**Obligatorio para:** Paladines, Clérigos (en ciertas fases del juego)

### Plantilla Visual

```
╔══════════════════════════════════════════╗
║  TEMPLO DE LA LUZ - CERTIFICADO DIVINO  ║
║                                          ║
║      ✦ ✦ ✦                              ║
║                                          ║
║  SIERVO: Seraphina del Alba             ║
║  CLASE: Paladín                          ║
║  DEIDAD: Lumina, Diosa de la Luz        ║
║                                          ║
║  Este certificado confirma que el       ║
║  portador ha sido BENDECIDO por la      ║
║  Diosa Lumina y mantiene pureza         ║
║  espiritual sin corrupción.             ║
║                                          ║
║  ÚLTIMA PRUEBA: 20/5/1225               ║
║  (Ritual de Purificación superado)      ║
║                                          ║
║  PRÓXIMA RENOVACIÓN: 20/11/1225         ║
║  (Cada 6 meses)                          ║
║                                          ║
║  ALINEACIÓN CONFIRMADA: Legal Buena     ║
║                                          ║
║  ┌────────┐                              ║
║  │ SELLO  │  Firma: [Alto Sacerdote]    ║
║  │SAGRADO │                              ║
║  └────────┘  [Símbolo de Lumina]        ║
║                                          ║
║  "Que la Luz guíe tu camino"            ║
╚══════════════════════════════════════════╝
```

### Verificaciones Clave

**Solo para clases divinas:**
- Paladín: ✓ Debe tener
- Clérigo: ✓ Debe tener
- Mago: ❌ No necesita

**Renovación:**
- Si hace más de 6 meses desde última prueba → Certificado vencido
- Paladín con certificado vencido → Sospechoso (¿perdió la bendición?)

**Alineación:**
- Paladín DEBE ser Legal Bueno
- Si detectas comportamiento malvado → Contradicción

**Uso estratégico:**
- Si cliente dice ser Paladín pero no tiene certificado → Impostor
- Pícaro disfrazado de Paladín → Detectado

---

## 🚨 7. ORDEN DE DETENCIÓN

**Recibido por:** TÚ (el tabernero), emitido por la Guardia

### Plantilla Visual

```
╔══════════════════════════════════════════╗
║  ⚠️  GUARDIA REAL - ORDEN DE DETENCIÓN  ║
║                                          ║
║  ┌──────────┐                            ║
║  │          │  CRIMINAL: Vex la Sombra  ║
║  │  RETRATO │  ALIAS: "El Fantasma"     ║
║  │          │  RAZA: Elfo de la Noche   ║
║  └──────────┘  CLASE: Pícaro             ║
║                                          ║
║  CRÍMENES:                               ║
║  - Robo a la Corona (3 cargos)          ║
║  - Falsificación de documentos          ║
║  - Evasión de la justicia                ║
║                                          ║
║  PELIGROSIDAD: ⚠️⚠️⚠️ ALTA              ║
║                                          ║
║  RECOMPENSA: 300 monedas                ║
║                                          ║
║  INSTRUCCIONES:                          ║
║  Si este individuo entra en su          ║
║  establecimiento, NO lo confronte.      ║
║  Notifique inmediatamente a la Guardia. ║
║                                          ║
║  VÁLIDO: Del 1/6/1225 al 30/6/1225      ║
║                                          ║
║  ┌────────┐                              ║
║  │ SELLO  │  Capitán Roderick            ║
║  │ GUARDIA│  Guardia Real de Cruce      ║
║  └────────┘                              ║
╚══════════════════════════════════════════╝
```

### Mecánica

**TÚ recibes esto:**
- Cada semana, Guardia te entrega 2-5 órdenes de detención
- Las cuelgas en tu pared (visible para jugador)
- Debes memorizar caras

**Si el criminal entra:**
1. Comparas cliente con órdenes en pared
2. Si coincide → Puedes:
   - **Opción A:** Llamar discretamente a Guardia (recompensa 300c)
   - **Opción B:** Servir normalmente, ignorar orden (riesgo)
   - **Opción C:** Advertir al criminal (pierdes reputación con Guardia, ganas con Gremio Ladrones)

**Peligrosidad:**
- ⚠️ BAJA: No reacciona violentamente
- ⚠️⚠️ MEDIA: Puede amenazarte si lo confrontas
- ⚠️⚠️⚠️ ALTA: Puede atacarte (daño a taberna, posible muerte)

---

## 📖 8. LIBRO DE REGLAS DEL DÍA

**Recibido por:** TÚ (el tabernero), emitido por el Consejo

### Plantilla Visual

```
╔══════════════════════════════════════════╗
║  CONSEJO MUNICIPAL - REGLAS DEL DÍA     ║
║                                          ║
║  FECHA: 15/6/1225                       ║
║                                          ║
║  REGLAS ACTIVAS HOY:                     ║
║                                          ║
║  1. PROHIBIDO servir a Minotauros       ║
║     Razón: Tensión con Gremio Comercio  ║
║     Multa por violación: 200 monedas    ║
║                                          ║
║  2. OBLIGATORIO verificar Licencia      ║
║     de Magia para todos los magos       ║
║     Multa por violación: 100 monedas    ║
║                                          ║
║  3. Toque de queda ADELANTADO a 21:00   ║
║     (aplicable a razas exóticas)        ║
║                                          ║
║  4. BONIFICACIÓN: +20% precio en        ║
║     bebidas importadas (Festival élfico)║
║                                          ║
║  VÁLIDO: Solo hoy (15/6/1225)           ║
║  Nuevas reglas mañana a las 6:00        ║
║                                          ║
║  ┌────────┐                              ║
║  │ SELLO  │  Secretario del Consejo     ║
║  │CONSEJO │                              ║
║  └────────┘                              ║
╚══════════════════════════════════════════╝
```

### Mecánica

**Papers Please mechanic:**
- Cada día (in-game), TÚ recibes nuevo Libro de Reglas
- Reglas CAMBIAN diariamente/semanalmente
- Debes MEMORIZAR y APLICAR reglas actuales

**Ejemplo de progresión:**

**Día 1 (Tutorial):**
```
1. Verificar edad legal (18+ para humanos)
```

**Día 15:**
```
1. Verificar edad legal
2. Verificar que ID no esté vencida
3. Prohibido servir a menores élficos (80+ años)
```

**Día 45:**
```
1. Todo lo anterior
2. Prohibido Minotauros hoy
3. Obligatorio Licencia de Magia para magos
4. Solo Guerreros pueden portar armas hoy
5. Clérigos deben mostrar Certificado de Pureza
```

**Complejidad aumenta progresivamente.**

---

## 🎖️ 9. PASE VIP

**Obligatorio para:** Clientes de élite (rarísimo)

### Plantilla Visual

```
╔══════════════════════════════════════════╗
║     👑 DECRETO REAL - PASE VIP 👑       ║
║                                          ║
║  ┌──────────┐                            ║
║  │          │  PORTADOR: Duque Alaric   ║
║  │ RETRATO  │  TÍTULO: Duque del Norte  ║
║  │  REAL    │  FAMILIA: Casa Valorian   ║
║  └──────────┘                            ║
║                                          ║
║  Por decreto de Su Majestad el Rey      ║
║  Aldric III, el portador tiene          ║
║  INMUNIDAD DIPLOMÁTICA.                 ║
║                                          ║
║  PRIVILEGIOS:                            ║
║  [✓] Exento de TODAS las reglas locales ║
║  [✓] Prioridad de servicio               ║
║  [✓] Descuento Real (50% en todo)       ║
║  [✓] Protección de la Guardia Real       ║
║                                          ║
║  Este pase NO PUEDE ser rechazado       ║
║  bajo pena de traición.                  ║
║                                          ║
║  EMITIDO: 1/1/1225                      ║
║  VÁLIDO: Indefinidamente                ║
║                                          ║
║  ┌────────┐                              ║
║  │ SELLO  │  Su Majestad Rey Aldric III ║
║  │  REAL  │                              ║
║  └────────┘  [Corona dorada grabada]    ║
╚══════════════════════════════════════════╝
```

### Mecánica

**Rarísimo:** Solo 2-3 en TODO el juego

**Poder absoluto:**
- Cliente con Pase VIP puede violar CUALQUIER regla
- Tú DEBES servir sin cuestionar
- Exento de verificaciones

**Falsificación ultra-peligrosa:**
- Duendes maestros pueden falsificar Pase VIP
- Si lo haces mal y sirves a falsificador → **TREASON** (traición)
- Multa: 1000 monedas + posible cierre permanente

**Detección:**
- Sello Real debe ser PERFECTO (requiere Lupa + UV)
- Papel real tiene textura única (dorada, brillante)
- Solo nobles conocidos pueden tener Pase VIP
  - Si un Plebeyo presenta Pase VIP → 99% falso

**Dilema moral:**
- Rechazar = Posible error catastrófico
- Aceptar = Posible trampa catastrófica
- Debes ser EXPERTO para decidir

---

## 📊 TABLA RESUMEN: Documentos por Situación

| Situación Cliente | Documentos Requeridos |
|-------------------|-----------------------|
| Cliente básico (Humano Plebeyo) | ID |
| Cliente con espada (Guerrero) | ID + Permiso de Armas |
| Mago con bastón | ID + Licencia de Magia |
| Paladín armado (Late Game) | ID + Permiso de Armas + Certificado Pureza |
| Minotauro (Mid/Late Game) | ID + Permiso de Entrada |
| Miembro de Gremio Comercio | ID + Certificado de Afiliación |
| Elfo Hechicero | ID + Licencia de Magia |
| Duende Pícaro con daga | ID + Permiso de Armas (alta sospecha) |
| Noble con Pase VIP | Solo Pase VIP (exento de todo) |

---

## 🎨 CONSIDERACIONES VISUALES

### Colores por Tipo

- **ID Personal:** Azul
- **Permisos de Armas:** Rojo
- **Licencias de Magia:** Púrpura
- **Certificados de Facción:** Verde/Amarillo (según facción)
- **Permisos de Entrada:** Gris
- **Certificados Divinos:** Dorado/Blanco
- **Órdenes de Detención:** Rojo oscuro con ⚠️
- **Pases VIP:** Dorado brillante con corona

### Estilo Visual

**Documentos legítimos:**
- Papel limpio, nítido
- Sellos bien definidos
- Texto alineado
- Bordes rectos

**Falsificaciones:**
- Papel manchado, doblado
- Sellos borrosos o incorrectos
- Texto desalineado, errores de ortografía
- Bordes irregulares

---

## 🔗 INTEGRACIÓN CON SISTEMAS

**Con Razas:** Edades legales varían, glamour élfico complica verificación

**Con Clases:** Clases determinan qué documentos necesitan

**Con Facciones:** Certificados de facción otorgan privilegios/restricciones

**Con Bebidas:** Algunos clientes usan documentos para acceder a bebidas exclusivas

**Con Eventos:** Reglas del día cambian requisitos documentales

---

**Plantillas completas definidas para implementación técnica.**
