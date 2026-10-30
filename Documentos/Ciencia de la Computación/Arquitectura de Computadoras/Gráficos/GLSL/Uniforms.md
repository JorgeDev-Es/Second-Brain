### Uniforms
Los parametros


1. **`uniform vec3 iResolution;`**  
    Resolución de la pantalla o ventana donde se renderiza (x = ancho en píxeles, y = alto en píxeles, z = profundidad — a menudo 1).
    
2. **`uniform float iTime;`**  
    Tiempo transcurrido en segundos desde que comenzó a ejecutarse el shader. Muy útil para animaciones.
    
3. **`uniform float iTimeDelta;`**  
    Tiempo en segundos entre el frame anterior y el actual.
    
4. **`uniform int iFrame;`**  
    Número del frame actual (0, 1, 2, 3, ...). Útil para animaciones o efectos que dependan de la cantidad de frames.
    
5. **`uniform float iChannelTime[4];`**  
    Tiempo transcurrido para cada uno de los 4 canales de textura (iChannel0, iChannel1, etc.).
    
6. **`uniform vec4 iMouse;`**  
    Posición del ratón en píxeles (x, y) y estado de clic (z, w).
    
7. **`uniform sampler2D iChannel0;` ... `iChannel3;`**  
    Texturas o imágenes que el shader puede usar como entrada para muestrear colores o datos.
    
8. **`uniform vec4 iDate;`**  
    Fecha y hora actuales (año, mes, día, tiempo en segundos desde medianoche).
    
9. **`uniform float iSampleRate;`**  
    Frecuencia de muestreo de audio.
    
10. **`uniform vec3 iCameraPos;`** (en algunos contextos)  
    Posición de la cámara.