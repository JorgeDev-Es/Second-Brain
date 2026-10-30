# Canvas
## Seleccionar el canvas
`canvas` es un elemento HTML.
`canvas.getContext()` es el contexto.
## Redimensionar el canvas usando HTML vs CSS
Las dimensiones mostradas del canvas pueden ser cambiadas usando CSS, pero al hacerlo la imagen es escalada durante el renderizado para encajar el tamaño ...., lo que puede hacer que el renderizado de gráficos final termine distorsionado.

La mejor manera de especificar las dimensiones del canvas es cambiando los atributos `width` y `height` directamente en los elementos `<canvas>` usando directamente HTML o JavaScript.
```JavaScript
const canvas = getElementByID("canvas")

canvas.width = 1080
canvas.height = 720
```
## Ejemplos
```TypeScript
function loop() {  
    tick++  
	
    ctx!.fillStyle = "red"  
    ctx!.fillRect(tick, tick , 2, 2)  
	 
    window.requestAnimationFrame(loop)  
}
```
![[Archivos Adjuntos/Recording 2025-08-28 131558.gif]]
```JavaScript
function render() {

      if (isPlaying) {

        ctx!.clearRect(0, 0, cw, ch)

        ctx!.beginPath()

        ctx!.strokeStyle = "white"

        ctx!.moveTo(0, ch / 2)

        ctx!.lineTo(cw, ch / 2)

        ctx!.strokeStyle = "white"

        ctx!.moveTo(cw / 2, 0)

        ctx!.lineTo(cw / 2, ch)

        ctx!.stroke()

  

        tick++

  

        for (let i = 0; i < cw; i += 0.2) {

          ctx!.fillStyle = "rgb(255, 255, 255)"

          ctx!.fillRect(

            i,

            ch / 2 + Math.sin(i + tick) * 9,

            1,

            1

          )

        }

      }

      requestAnimationFrame(render)

    }
```
![[Archivos Adjuntos/Recording 2025-10-23 154105.gif]]
## Referencias
https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/canvas