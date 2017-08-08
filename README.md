# Tarea
lty (argumentos)

Función lines:
Esta función permite graficar segmentos de líneas rectas en un gráfico previo: 
lines(x, ...) lines.default(x, y=NULL, type="l", 
col=par("col"), lty=par("lty"), ...)
Argumentos: 
•	x, y: Vectores de coordenadas de los puntos a unir.
•	type: Carácter que indica el tipo de grafico; pueden especificarse los tipos plausibles en el argumento ’type’ de la función  ’plot(...)’. 
•	col: Color a usar. 
•	lty: Tipo de linea a usar. 
•	...: Pueden especificarse otros parámetros gráficos (ver ’par’), tales como ’lwd’. Detalles: Las coordenadas pueden suministrarse a ’lines’ en una estructura de graficación (una lista con componentes x e y), etc. Ver ’xy.coords’.
Las coordenadas pueden contener valores ’NA’. Cuando esto sucede el punto correspondiente es omitido del gráfico, y ninguna línea es dibujada hasta o desde tal punto. Por tanto, pueden usarse valores faltantes para obtener discontinuidades en las líneas.

Ejemplo 1:
y<-rnorm(12) 
x<-1:12
plot(x,y,xaxt="n",cex.axis=0.8,pch=23,bg="gray", 
col="black",cex=1.1,main="Uso de ’lines’ 
para dibujar una serie",cex.main=0.9) 
axis(1,at=1:12,lab=month.abb,las=2,cex.axis=0.8)
lines(x,y,lwd=1.5) 
Ejemplo 2: 
x<-rnorm(50) 
y<-2*x+rnorm(50) 
library(modreg) 
plot(x,y,main="Ejemplo de la función  
’lines’\ndibujando una curva suavizada") 
lines(loess.smooth(x,y))
