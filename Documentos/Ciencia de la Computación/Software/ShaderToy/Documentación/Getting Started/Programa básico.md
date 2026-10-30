## Programa Básico
```GLSL
void mainImage( out vec4 fragColor, in vec2 fragCoord )
{
    // Normalized pixel coordinates (from 0 to 1)
    vec2 uv = fragCoord/iResolution.xy;

    // Time varying pixel color
    vec3 col = 0.5 + 0.5*cos(iTime+uv.xyx+vec3(0,2,4));

    // Output to screen
    fragColor = vec4(col,1.0);
}
```
## 
`void mainImage(out vec4 fragColor, in vec2 fragCoord)`
Esta es la función principal que ShaderToy llama para cada píxel.
- `fragCoord`: coordenadas del píxel en pantalla, en píxeles (por ejemplo, (100, 200)).
- `fragColor`: es la salida, el color final que tendrá ese píxel (RGBA).
**`vec2 uv = fragCoord / iResolution.xy;`**  
Divide las coordenadas del píxel por la resolución de la pantalla (`iResolution.xy`), para obtener coordenadas normalizadas de 0 a 1, independientemente del tamaño de la ventana.  
Esto es importante para que los cálculos funcionen igual en cualquier resolución.
**`vec3 col = 0.5 + 0.5 * cos(iTime + uv.xyx + vec3(0, 2, 4));`**  
Esta línea genera el color del píxel:

- Usa una función coseno para hacer una animación que cambia con el tiempo (`iTime`).
    
- `uv.xyx` crea un vector de 3 componentes usando la coordenada X, Y y luego otra X para variar cada canal RGB.
    
- `vec3(0, 2, 4)` desplaza cada componente para darle variación.
    
- Multiplicamos y sumamos para mantener los valores entre 0 y 1 (colores válidos).
**`fragColor = vec4(col, 1.0);`**  
Finalmente, asigna el color calculado al fragmento, con alfa 1 (totalmente opaco).