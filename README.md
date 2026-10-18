# ⚔️ Ajedrez Medieval 3D: Guerra de Tronos

Un videojuego completo de ajedrez tridimensional ambientado en las batallas de la Edad Media, con modelos 3D detallados de ejércitos medievales (lanceros, corceles de justa, inquisidores, baluartes de asedio, reyes y reinas guerreros), motor de Inteligencia Artificial con 4 rangos de dificultad, efectos sonoros bélicos procedurales y soporte multiplataforma garantizado para **Windows 10** y **Linux**.

---

## 🚀 Cómo Jugar

No requiere instalación de software adicional, servidores pesados ni compiladores. Funciona de inmediato al 100% de forma local y offline.

### En Windows 10
1. Haz doble clic en el archivo **`jugar-windows.bat`** (o directamente en **`index.html`**).
2. Se abrirá en tu navegador web predeterminado (Microsoft Edge, Google Chrome, Mozilla Firefox, Opera, Brave, etc.).

### En Linux (Ubuntu, Debian, Fedora, Arch, etc.)
1. Abre una terminal en la carpeta del juego y dale permisos de ejecución si es necesario:
   ```bash
   chmod +x jugar-linux.sh
   ./jugar-linux.sh
   ```
2. O simplemente haz doble clic en **`index.html`** y ábrelo con cualquier navegador web.

---

## 🛡️ Tropas y Modelos 3D de la Edad Media

Cada pieza tradicional de ajedrez ha sido esculpida proceduralmente en 3D con materiales PBR y armas representativas de la época:

- **Peón (Infantería / Lancero Medieval):** Soldado con yelmo cónico normando, cota de malla, peto heráldico, escudo de lágrima (*kite shield*) y lanza de combate.
- **Torre (Torreón de Asedio Fortificado):** Baluarte de piedra de castillo con matacanes, aspilleras para arqueros, almenas góticas y estandarte flameante.
- **Caballo (Caballero de Élite / Corcel de Batalla):** Corcel de guerra acorazado con jinete de torneo, yelmo con cimera emplumada y lanza de justa.
- **Alfil (Inquisidor / Paladín Clérigo):** Figura sagrada con armadura ceremonial, mitra episcopal de doble pico y báculo pastoral de cruz.
- **Dama (Reina Guerrera Soberana):** Soberana con coraza de placas esculpida, hombreras curvas, capa ondeante, corona floreada y cetro real con orbe.
- **Rey (Monarca Imperial de Batalla):** Gran señor en armadura imperial completa de placas con blasones de oro, manto con caída real, Corona Imperial con cruz y Espada Magna (mandoble) ceremonial clavada en la peana.

---

## 🧠 Motor de Inteligencia Artificial y Dificultades

El motor de IA utiliza el algoritmo **Minimax con Poda Alfa-Beta**, búsqueda quiescente en capturas y tablas de valores posicionales (*Piece-Square Tables*):

1. **🥉 Nivel 1: Recluta (Fácil):** Búsqueda a profundidad 1-2 con movimientos dinámicos ideales para novatos o partidas relajadas.
2. **🥈 Nivel 2: Escudero (Medio):** Búsqueda a profundidad 2-3 con evaluación material y protección posicional básica.
3. **🥇 Nivel 3: Caballero (Difícil):** Búsqueda a profundidad 3-4 con ordenamiento óptimo de capturas (MVV-LVA) y control del centro.
4. **👑 Nivel 4: Gran Mariscal (Experto):** Búsqueda profunda y defensiva con evaluación estratégica avanzada y cálculo posicional.

---

## 🎮 Controles y Funcionalidades

- **Cámara 3D Orbital:**
  - *Rotación libre:* Clic izquierdo y arrastrar el ratón.
  - *Zoom:* Rueda del ratón o gesto de pellizco en pantalla táctil.
  - *Paneo / Desplazamiento:* Clic derecho y arrastrar el ratón.
- **Alternar Vista 2D/3D:** Botón *Vista Cenital* para pasar a una vista táctica cenital perfecta desde arriba.
- **Modos de Juego:**
  - *Comandante vs IA:* Juega con Blancas o Negras contra la máquina.
  - *Duelo 1 vs 1 (Local):* Modo pase y juegue para dos comandantes en el mismo equipo.
- **Reglas FIDE Oficiales Completas:**
  - Enroque corto (O-O) y largo (O-O-O).
  - Captura al paso (*en passant*).
  - Coronación / Promoción de peones con menú interactivo (Dama, Torre, Alfil, Caballo).
  - Detección estricta de Jaque, Jaque Mate, Tablas por Rey Ahogado, Material Insuficiente y 50 Movimientos.
  - Historial de movimientos en Notación Algebraica Estándar (SAN).
  - Bajas de Guerra (piezas capturadas) con cálculo en vivo de ventaja de material.
  - Reloj de tiempo de batalla para ambos bandos.
  - Función de Deshacer jugada (*Undo*).
  - Efectos de sonido procedurales generados por la tarjeta de audio mediante Web Audio API (cero riesgo de archivos perdidos).

---

## 📁 Estructura del Proyecto

```
Ajedrez/
├── index.html                  # Interfaz principal, HUD y modales
├── css/
│   └── style.css               # Estilos medievales, bordes dorados y marcos góticos
├── js/
│   ├── vendor/
│   │   ├── three.min.js        # Librería Three.js (local para juego offline)
│   │   └── OrbitControls.js    # Controlador de cámara orbital
│   ├── chess/
│   │   ├── rules.js            # Motor de reglas oficiales FIDE
│   │   └── ai.js               # Motor de IA Minimax Alfa-Beta (4 niveles)
│   ├── graphics/
│   │   ├── models.js           # Modelos 3D de soldados medievales
│   │   ├── scene.js            # Escena 3D, luces, sombras y animaciones
│   │   └── board.js            # Tablero tallado en madera y mármol
│   ├── audio/
│   │   └── soundEffects.js     # Sonidos procedurales (Web Audio API)
│   └── app.js                  # Controlador central del juego
├── jugar-windows.bat           # Lanzador de 1 clic para Windows 10
├── jugar-linux.sh              # Lanzador de 1 clic para Linux
└── README.md                   # Manual y documentación técnica
```

---

## 🛠️ Portabilidad a Otros Lenguajes (C#, C++, Java)

Dado que toda la lógica de reglas (`rules.js`) y el motor de IA (`ai.js`) se diseñaron con orientación a objetos limpia y desacoplada:
- **C# / .NET / Godot:** Se puede incrustar con WebView2 / Blazor Desktop, o portar la clase `ChessGame` y `ChessAI` a C# en Godot Engine usando nodos `MeshInstance3D`.
- **C++:** Se puede utilizar con wrappers ligeros como Ultralight / WebKit o portar la lógica a Raylib 3D / OpenGL.
- **Java:** Se puede envolver en una ventana JavaFX con componente `WebView` o portar a libGDX.
