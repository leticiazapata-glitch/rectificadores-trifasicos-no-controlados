# Rectificadores Trifásicos no Controlados
# Caracterización Experimental y Comparativa de Rectificadores Trifásicos No Controlados

Estudio experimental y análisis comparativo del desempeño de rectificadores trifásicos de media onda (3 pulsos) y puente completo de Graetz (6 pulsos) operando sobre cargas pasivas ($R, RC, RL, RLC$).

## Objetivo
Evaluar el impacto de la topología de conversión y el filtrado pasivo sobre el voltaje medio ($V_{\text{medio}}$), el nivel de rizado ($V_{pp}$), las corrientes de carga y el voltaje inverso máximo ($V_{\text{inv,máx}}$) soportado por los diodos.

---

##  Resultados Principales y Oscilogramas

### 1. Comparación de Topologías (Carga Resistiva $R$)
* **Media Onda (3 pulsos):** Entrega un voltaje medio de $29,5\text{ V}$ con un rizado pico a pico de $18,8\text{ V}$.
* **Puente Completo / Graetz (6 pulsos):** Duplica la tensión media de salida a $59,2\text{ V}$ y reduce el rizado a $12,8\text{ V}$, operando a una frecuencia de pulsos doble ($300\text{ Hz}$).

#### Oscilograma Media Onda (3 pulsos)
![Media Onda - 3 pulsos](3pulsos.jpg)

#### Oscilograma Puente Completo (6 pulsos)
![Onda Completa - 6 pulsos](6pulsos.jpg)

---

### 2. Dinámica Trifásica y Filtrado Capacitivo ($RC$)
* **Entrelazado Trifásico:** Muestra cómo las 3 fases conducen sucesivamente para generar la tensión de salida rectificada en el puente de Graetz.
* **Filtro Capacitivo ($C$):** Eleva la tensión continua media ($62,1\text{ V}$ en onda completa) y reduce drásticamente el rizado pico a pico a niveles de $1,2\text{ V}$, entregando una señal continua prácticamente plana.

#### Contribución de las 3 Fases en Puente Completo
![Contribución de 3 Fases](graf12.jpg)

#### Tensión de Salida con Filtro Capacitivo ($RC$)
![Onda Completa con Filtro RC](graf14.jpg)

---

### 3. Tabla Comparativa de Resultados Experimentales

| Topología | Tipo de Carga | $V_{\text{medio}}$ [V] | $V_{pp}$ [V] | $V_{\text{RMS}}$ [V] | $I_{\text{medio}}$ [A] | $V_{\text{inv,máx}}$ [V] |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: |
| **Media Onda** | Resistiva ($R$) | 29,5 | 18,8 | 29,9 | 0,027 | 65,6 |
| **Media Onda** | Capacitiva ($RC$) | 34,8 | 1,6 | 34,8 | 0,036 | 66,5 |
| **Puente Completo** | Resistiva ($R$) | 59,2 | 12,8 | 59,3 | 0,054 | 65,2 |
| **Puente Completo** | Capacitiva ($RC$) | 62,1 | 1,2 | 62,1 | 0,061 | 63,2 |



---

##  Conclusiones Técnicas
1. **Eficiencia de la Topología:** El puente de Graetz aprovecha ambos semiciclos de la red trifásica, entregando un voltaje promedio $2\times$ mayor sin inyectar componentes continuas a la fuente, lo que evita la saturación de transformadores.
2. **Dimensionamiento de Componentes:** El diodo $D_1$ se ve expuesto a tensiones inversas máximas equivalentes al voltaje entre líneas del sistema ($\approx 63\text{ V} - 66\text{ V}$), parámetro crítico para la selección de semiconductores de potencia.
3. **Optimización de Filtrado:** La combinación con filtro capacitivo ($RC$) entrega la señal de salida más limpia y continua, reduciendo el rizado $V_{pp}$ de $12,8\text{ V}$ a solo $1,2\text{ V}$.

---

## Equipamiento e Instrumentación
* Osciloscopio Digital (adquisición de formas de onda)
* Módulo de Diodos de Potencia y Cargas Pasivas ($R, L, C$)
* Fuente Trifásica Variable

---

## Autora
**Leticia Zapata Acevedo**  
Estudiante de Ingeniería Civil Eléctrica  
Facultad de Ciencias Físicas y Matemáticas (FCFM) – Universidad de Chile  
*Informe desarrollado para el curso EL3003 – Laboratorio de Ingeniería Eléctrica.*
