# Canvas 2D
## Código base
`<canvas>`
```HTML
<canvas id="canvas"></canvas>
```

```TypeScript
const canvas = document.getElementById("canvas")
const ctx = canvas.getContext("2d")

if (!ctx) return

loop()
```

```TypeScript
function loop() {

	window.requestAnimationFrame(loop)
}
```
## Linea diagonal
```TypeScript
function loop() {  
    tick++  
    
    ctx!.shadowBlur = 2  
    ctx!.fillStyle = "red"  
    ctx!.fillRect(tick, tick , 2, 2)  
    
    window.requestAnimationFrame(loop)  
}
```
![[Archivos Adjuntos/Recording 2025-08-28 131558 1.gif|400x400]]
## Linea diagonal arcoiris
```TypeScript
function loop() {  
    tick++
    
    ctx!.shadowBlur = 2  
    ctx!.fillStyle = `hsl(${tick * 0.1}, 100%, 50%)`  
    ctx!.fillRect(tick, tick , 2, 2)  
    
    window.requestAnimationFrame(loop)  
}
```
![[Archivos Adjuntos/Recording 2025-08-28 134649.gif|400x400]]

## Y Center
`ctx!.fillRect(tick, canvas.height / 2, 2, 2)`
![[Archivos Adjuntos/y center.gif|400x400]]
## 
`ctx!.fillRect(tick, canvas.height / 2 + Math.sin(tick), 2, 2)`
![[Archivos Adjuntos/20250828-2212-54.3514056.gif]]

## Bouncing Circle
## Basic
```TypeScript
let tick = 0  
  
let circleX = cw / 2  
let circleY = ch / 2  
let circleXMovement = 5  
let circleYMovement = 5  
let radius = 10
```

```TypeScript
function render() {  
	ctx!.clearRect(0, 0, canvas.value!.width, canvas.value!.height)  
	
	tick++  
	
	ctx!.beginPath()  
	ctx!.strokeStyle = '#fff'  
	
	circleX - radius <= 0 || circleX + radius >= cw ? circleXMovement = -circleXMovement : null  
	circleY - radius <= 0 || circleY + radius >= ch ? circleYMovement = -circleYMovement : null
	
	circleX += circleXMovement  
	circleY += circleYMovement  
	
	ctx!.arc(circleX, circleY, radius, 0, Math.PI * 2, false)  
	ctx!.stroke()  
	  
	window.requestAnimationFrame(render)  
}
```

![[Archivos Adjuntos/Recording 2025-08-28 211509.gif]]