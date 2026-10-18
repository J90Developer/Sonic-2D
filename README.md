# ⚡ Sonic 2D Web3 Platformer (40 Niveles)

Videojuego completo de plataformas 2D inspirado en la jugabilidad clásica de Sonic (momentum, loopings 360°, spin-dash, muelles, anillos dorados y badniks), integrado con un ecosistema **Web3 Play-to-Earn (Proof-of-Gameplay)** y arquitectura políglota con **HTML5, Python, C++, Java y Ruby**.

---

## 🎮 Cómo Jugar (Inicio Inmediato en Windows)

1. Haz doble clic en **`jugar-sonic-windows.bat`** (en la raíz) o en **`sonic_game/jugar-sonic.bat`**.
2. Se abrirá de inmediato en tu navegador web predeterminado (Edge, Chrome, Firefox, Brave, etc.).
3. **No requiere instalar servidores, paquetes ni compiladores** para disfrutar del juego al 100%.

### 🕹️ Controles del Juego
| Teclas | Acción |
| :--- | :--- |
| **←** / **→** o **A** / **D** | Acelerar con inercia (alcanza velocidad supersónica / Mach) |
| **ESPACIO** o **Z** | Saltar con Spin-Attack (destruye badniks enemigos) |
| **↓** (en carrera) | **Rodar (Roll)**: Se convierte en bola, gana inercia en pendientes y destruye enemigos |
| **↓** + **ESPACIO** (parado) | **Spin-Dash**: Carga energía y suelta **↓** para salir disparado a máxima velocidad |
| **↑** / **↓** (parado) | Mirar hacia arriba / agacharse |
| **P** | Pausar / Reanudar el juego |
| **Táctil (Móvil)** | D-Pad virtual y botón de salto táctil en pantalla |

---

## 🌐 Ecosistema Web3 y Minería Play-to-Earn (Proof-of-Gameplay)

- **Fases 1 a 5 (Fases de Prueba / Sandbox Testnet)**:
  - Entorno de prueba sin coste de gas para calibrar físicas, saltos, recolección de anillos y simulación de transacciones blockchain.
- **Tasa de Minado por Velocidad (Hashrate)**:
  - Mientras Sonic corre a alta velocidad y recoge anillos, el motor calcula en tiempo real un flujo de hashes criptográficos basados en el desplazamiento y la aceleración.
- **Reclamo de Tokens $RING**:
  - Al cruzar el poste de meta de cada nivel, se valida un voucher criptográfico de *Proof of Gameplay (PoG)* que acredita tokens `$RING` en tu monedero (compatible con MetaMask o monedero local Sandbox).

---

## 🏗️ Arquitectura Políglota de los Componentes

| Tecnología | Archivo / Directorio | Rol en el Proyecto |
| :--- | :--- | :--- |
| **HTML5 / JS / Canvas** | [`index.html`](index.html), [`js/`](js/) | **Cliente de Juego Principal**: Motor de físicas 60 FPS, animaciones procedurales, loopings 360°, audio Web Audio API y UI Web3. |
| **Python** | [`backend/server.py`](backend/server.py) | **Servidor Anti-Cheat & Oráculo Web3**: Valida métricas de niveles completados y firma vouchers criptográficos PoG. |
| **C++** | [`physics_core/sonic_physics.cpp`](physics_core/sonic_physics.cpp) | **Núcleo de Físicas de Alta Velocidad**: Implementación determinista de las ecuaciones de inercia, rampas y loopings. |
| **Java** | [`blockchain_service/RewardDistributor.java`](blockchain_service/RewardDistributor.java) | **Microservicio de Recompensas Blockchain**: Simula el contrato inteligente ERC-20, pool de liquidez y recibos de bloque. |
| **Ruby** | [`tools/generate_levels.rb`](tools/generate_levels.rb) | **Generador de Niveles**: Script de generación procedural y exportación de los 40 niveles en formato JSON. |

---

## 🗺️ Los 40 Niveles y Zonas Temáticas

- **Fases 1 a 5**: *Fases de Prueba (Testnet Sandbox: Aceleración, Economía de Anillos, Loopings, Pinchos y Mini-Jefe).*
- **Actos 6 a 10**: *Emerald Plains (Verdes praderas, loopings, cascadas).*
- **Actos 11 a 15**: *Lava Caverns (Cavernas volcánicas y plataformas sobre magma).*
- **Actos 16 a 20**: *Cyber Grid (Circuitos digitales, barreras láser y estética tron).*
- **Actos 21 a 25**: *Casino Metropolis (Rebotadores de pinball, luces de neón y super muelles).*
- **Actos 26 a 30**: *Sky Fortress (Fortalezas voladoras y corrientes de aire).*
- **Actos 31 a 35**: *Quantum Core (Zonas de gravedad alterada y túneles cuánticos).*
- **Actos 36 a 40**: *Genesis Citadel (Ciudadela mecánica final y confrontaciones culminantes).*
