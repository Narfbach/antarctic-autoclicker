╔══════════════════════════════════════════════════════════════════════════╗
║                  A N T A R C T I C   -   README FINAL                    ║
║                     Sistema de Autoclicker con Licencias                 ║
╚══════════════════════════════════════════════════════════════════════════╝


📦 EJECUTABLE COMPILADO
═══════════════════════════════════════════════════════════════════════════
Ubicación:    dist/Antarctic.exe
Tamaño:       ~10.15 MB
Icono:        Incluido (icon.ico)
Dependencias: Ninguna (standalone)


🔑 TU LICENSE KEY PERSONAL
═══════════════════════════════════════════════════════════════════════════
Ver archivo: MI_KEY_PRIVADA.txt

Key: ANTARCTIC-L6UN-0RFD-45OJ

Esta es tu key personal como propietario. Úsala para activar el programa.


✨ CARACTERÍSTICAS IMPLEMENTADAS
═══════════════════════════════════════════════════════════════════════════
✓ Sistema de autoclicker avanzado con burst mode
✓ Sistema de perfiles (guardar/cargar hasta 5 configuraciones)
✓ Sistema de autenticación con license keys únicas
✓ Humanización de clicks (anti-detección)
✓ Ultra mode (velocidad máxima)
✓ Auto-burst on click (activación automática)
✓ Múltiples botones del mouse (izquierdo/derecho/medio)
✓ Clicks simples/dobles/triples
✓ Interfaz temática Matrix (verde/negro)
✓ Persistencia automática de configuración y licencia


🎮 CÓMO USAR EL PROGRAMA
═══════════════════════════════════════════════════════════════════════════
1. Ejecutar dist/Antarctic.exe
2. Primera vez: Ingresar license key
3. F3: Capturar coordenadas del mouse
4. F2: Ejecutar burst manual
5. F5: Toggle auto-burst (burst al hacer click)
6. Configurar clicks/interval/duration según necesites
7. Usar perfiles para guardar configuraciones


🔧 CONTROLES DEL PROGRAMA
═══════════════════════════════════════════════════════════════════════════
[F3]  → Capturar coordenadas actuales del mouse
[F2]  → Ejecutar burst manualmente
[F5]  → Activar/desactivar auto-burst mode

Sección de Perfiles:
• Dropdown: Seleccionar perfil existente
• LOAD:   Cargar perfil seleccionado
• SAVE:   Guardar configuración actual (pide nombre)
• DEL:    Eliminar perfil seleccionado

Configuración:
• CLICKS:      Número de clicks por burst (1-100)
• INTERVAL:    Tiempo entre clicks en ms (1-200ms)
• DURATION:    Duración del burst en segundos (0.01-2.0s)
• AUTO DELAY:  Delay antes de auto-burst (0-1s)

Opciones:
• TYPE:        Single/Double/Triple click
• BUTTON:      Left/Right/Middle mouse button
• HUMANIZATION: Randomiza clicks (5-15) e interval (10-30ms)
• ULTRA MODE:   Velocidad máxima (sin delays)
• AUTO-BURST:   Activa burst automático al hacer click


💼 PARA DISTRIBUIR A COMPRADORES
═══════════════════════════════════════════════════════════════════════════

Paso 1: Generar nuevas license keys
────────────────────────────────────────────────────────────────────────
python key_generator.py

• Ingresa cuántas keys necesitas (ejemplo: 10)
• El script generará keys únicas con formato: ANTARCTIC-XXXX-XXXX-XXXX
• Guarda AMBOS: la key Y el hash


Paso 2: Agregar keys al código
────────────────────────────────────────────────────────────────────────
1. Abre antarctic.py
2. Busca la clase KeyManager (línea ~217)
3. Encuentra la lista valid_keys_hashed
4. Agrega los HASHES (no las keys) a la lista:

   self.valid_keys_hashed = [
       "31406357c4ad44e8726ba6956710afc2be3c3566003c06191aa2942e1d9409e5",
       "TU_NUEVO_HASH_AQUI_1",
       "TU_NUEVO_HASH_AQUI_2",
       # ... más hashes
   ]

5. Guarda el archivo


Paso 3: Recompilar el ejecutable
────────────────────────────────────────────────────────────────────────
pyinstaller --onefile --windowed --icon=icon.ico --name=Antarctic antarctic.py

• El nuevo .exe estará en: dist/Antarctic.exe
• Incluirá todas las keys agregadas


Paso 4: Distribuir
────────────────────────────────────────────────────────────────────────
• Envía el Antarctic.exe a tus compradores
• Envía UNA LICENSE KEY ÚNICA a cada comprador (NO el hash)
• Cada comprador ingresa su key al abrir el programa por primera vez
• Una vez activado, no volverá a pedir la key


🔒 SEGURIDAD DEL SISTEMA
═══════════════════════════════════════════════════════════════════════════
✓ Keys hasheadas con SHA256 (imposible revertir)
✓ Las keys originales NO están en el código
✓ Solo los hashes están embebidos en el .exe
✓ Licencia activada se guarda encriptada en antarctic.lic
✓ Archivo .lic usa base64 + validación de hash
✓ Si borran antarctic.lic, deben reactivar con su key
✓ Una key puede usarse múltiples veces (sin límite de activaciones)


📁 ARCHIVOS GENERADOS POR EL USUARIO
═══════════════════════════════════════════════════════════════════════════
antarctic.lic            → Licencia activada (no compartir)
antarctic_profiles.json  → Perfiles de configuración guardados

NOTA: Estos archivos se crean en la misma carpeta que Antarctic.exe


🗂️ ESTRUCTURA DEL PROYECTO
═══════════════════════════════════════════════════════════════════════════
Antarctic/
├── dist/
│   └── Antarctic.exe          ← EJECUTABLE FINAL
├── build/                     ← Archivos temporales de compilación
├── antarctic.py               ← Código fuente principal
├── key_generator.py           ← Generador de license keys
├── icon.ico                   ← Icono del programa
├── MI_KEY_PRIVADA.txt         ← Tu key personal (privada)
├── README_FINAL.txt           ← Este archivo
└── Antarctic.spec             ← Configuración de PyInstaller


⚙️ REQUISITOS PARA DESARROLLO
═══════════════════════════════════════════════════════════════════════════
Python 3.13.3 (o superior)
Librerías:
  - tkinter (incluida en Python)
  - pyinstaller (pip install pyinstaller)

Comando para instalar dependencias:
  pip install pyinstaller


🎯 CASOS DE USO
═══════════════════════════════════════════════════════════════════════════
• Gaming: BoomBang, Minecraft, juegos de clicks
• Testing: Automatización de pruebas de UI
• Productividad: Automatizar tareas repetitivas
• Stress testing: Pruebas de carga en aplicaciones


⚠️ NOTAS IMPORTANTES
═══════════════════════════════════════════════════════════════════════════
• El programa requiere Windows (usa ctypes y win32 API)
• Compatible con Windows 7, 8, 10, 11
• NO funciona en Linux/Mac (requiere reescritura)
• Los clicks se envían via SendMessage (compatibilidad máxima)
• Auto-burst detecta clicks del mouse nativamente (hook de sistema)


🐛 TROUBLESHOOTING
═══════════════════════════════════════════════════════════════════════════
Problema: "Invalid license key"
  → Verifica que la key esté correctamente escrita
  → Verifica que el hash de la key esté en valid_keys_hashed
  → Recompila el .exe si agregaste la key después

Problema: "No se activa el burst"
  → Presiona F3 para capturar coordenadas primero
  → Verifica que esté conectado a la ventana BoomBang (o cualquier otra)
  → Verifica que no haya otro programa bloqueando los clicks

Problema: El .exe no abre
  → Verifica que no esté bloqueado por antivirus
  → Ejecuta como administrador si es necesario
  → Verifica que icon.ico exista al compilar


📞 SOPORTE
═══════════════════════════════════════════════════════════════════════════
Para agregar más funcionalidades o reportar bugs, contacta al desarrollador.


═══════════════════════════════════════════════════════════════════════════
             ¡Disfruta de Antarctic! 🐧
═══════════════════════════════════════════════════════════════════════════
