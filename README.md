# Solve Laberinth

El sensor IR que uso es [este](http://es.aliexpress.com/item/5x-TCRT5000-Infrared-Reflectance-Sensor-Obstacle-Avoidance-Track-Module-IR-TE364/32493457475.html?spm=2114.13010608.0.96.FsjovU)

![a](./images/5x-TCRT5000-Infrared-Reflectance-Sensor-Obstacle-Avoidance-Track-Module-IR-TE364.jpg)

Usa sensores de tipo TCRT5000 Módulo IR TE364

Aprovechando el pin A0 (que es el analógico) se pueden medir perfectamente distancias entre 1 y 6cm (alguno más si lo haces con cuidado).

Podemos ver en una gráfica donde se ve que se puede usar todo el rango 0-1023

![1](./images/medidaSensorIR.png)

Si tenemos luz ambiente, lo que necesitamos es calibrar el nivel de luz ambiental. En esta imagen he usado el monitor encendido para medir las distancias, con el mismo resultado de distancias, pero a partir del 600
![1](./images/medidaSensorIRconLuz.png)

Podemos ver el rersultado con algo tan sencillo como este programa y el Serial Plotter

    void setup() {
    Serial.begin(9600);

    }

    void loop() {
    Serial.println(analogRead(A0));

    }

Podemos complicarlo más  usando varios sensores y definiendo umbrales
