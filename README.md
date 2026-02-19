# Núcleo de Interacción XR Pro

Proyecto integrador de Realidad Extendida (XR) que implementa módulos de interacción avanzada, accesibilidad universal y optimización de rendimiento para entornos virtuales web.

## Descripción

Este proyecto demuestra la implementación de un sistema de realidad virtual accesible que responde a la interacción del usuario mediante detección de mirada (gaze detection), proporciona alternativas de accesibilidad según estándares WCAG 2.1, y mantiene un rendimiento óptimo en navegadores web.

## Objetivos Cumplidos

### Módulo A: Narrativa Dinámica e Interacción por Presencia
- Detección de mirada mediante Raycasting
- Temporizador de interacción (10 segundos)
- Cambio dinámico de iluminación ambiental
- Activación de paneles informativos contextuales

### Módulo B: Accesibilidad Universal
- **WCAG 1.4.3** - Modo de alto contraste para usuarios con baja visión
- **WCAG 1.2.1** - Subtítulos espaciales para contenido auditivo
- Interfaz adaptable a necesidades del usuario

### Módulo C: Optimización y Rendimiento
- Geometrías optimizadas (baja carga poligonal)
- Renderizado a 60 FPS estables
- Sin dependencias externas pesadas

## Tecnologías Utilizadas

- **A-Frame 1.4.0** - Framework de realidad virtual para web
- **Three.js r147** - Motor de renderizado 3D
- **HTML5/CSS3/JavaScript** - Estándares web modernos
- **WebGL** - Aceleración gráfica hardware

## Instalación y Uso

### Requisitos previos
- Navegador web moderno (Chrome, Firefox, Edge)
- Servidor local (recomendado: VS Code Live Server)

### Pasos de instalación

1. Clonar el repositorio:
```bash
git clone https://github.com/MarjorieLis/Actividad-_2.14.git
cd Actividad-_2.14
```

2. Abrir con servidor local:
- Si usas VS Code: Instalar extensión "Live Server" → Clic derecho en index.html → "Open with Live Server"
- O usar Python: python -m http.server 8000
3. Acceder a: http://localhost:8000 (o el puerto que indique tu servidor)

### Controles
- Navegación: Click y arrastrar para rotar la cámara
- Interacción: Mantener la vista en el objeto rojo durante 10 segundos
- Accesibilidad: Usar el panel "Preferencias de Accesibilidad" en la esquina superior derecha

### Características de Accesibilidad
Criterios WCAG Implementados
1. 1.4.3 Contraste (Mínimo) - Nivel AA
- Modo alto contraste que incrementa la relación de contraste a 4.5:1
- Activación mediante botón en menú de preferencias
2. 1.2.1 Solo Audio y Solo Video (Pregrabado) - Nivel A
- Subtítulos espaciales que indican fuentes de audio
- Texto descriptivo posicionado en la escena
3. 1.4.1 Uso del Color - Nivel A
- Información no transmitida exclusivamente por color
- Uso de iconos, texto y formas para indicar estados

### Demostración
Video demostrativo del sistema de accesibilidad:

### Detalles Técnicos
Sistema de Raycasting
El proyecto implementa un sistema de detección de mirada utilizando THREE.Raycaster que emite un rayo desde el centro de la cámara para detectar intersecciones con objetos marcados como interactivos.

Transición de Iluminación
Las transiciones de luz utilizan interpolación lineal (lerp) para evitar cambios bruscos que rompan la inmersión del usuario.

Optimización
- Geometrías básicas sin texturas pesadas
- Iluminación optimizada con sombras desactivadas
- Renderizado eficiente a 60 FPS

Rendimiento
- FPS: 60 estables en navegadores modernos
- Carga inicial: < 2 segundos
- Tamaño total: < 100 KB (sin dependencias externas)

Compatibilidad
- Google Chrome 90+
- Mozilla Firefox 88+
- Microsoft Edge 90+
- Safari 14+
- Dispositivos móviles (iOS/Android)

Referencias
- A-Frame Documentation: https://aframe.io/docs/1.7.0/introduction/
- WCAG 2.1 Guidelines: https://www.w3.org/WAI/WCAG22/quickref/?versions=2.1
- Three.js Documentation: https://threejs.org/docs/?spm=a2ty_o01.29997173.0.0.4e025171aDmfVZ
- WebXR API: https://www.w3.org/TR/webxr/?spm=a2ty_o01.29997173.0.0.4e025171aDmfVZ
