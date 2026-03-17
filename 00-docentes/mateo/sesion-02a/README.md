# sesion-02a

martes 17 marzo, 2026

## Tratado de los objetos musicales — Pierre Schaeffer (1966)

El *Traité des objets musicaux* es la obra teórica central de Pierre Schaeffer, compositor y teórico francés fundador de la música concreta. En este libro Schaeffer propone un marco conceptual para escuchar y clasificar los sonidos con independencia de su origen o causa, una postura que denomina **escucha reducida** (*écoute réduite*), tomada del concepto fenomenológico de reducción de Husserl.

El núcleo del tratado es la noción de **objeto sonoro**: cualquier fenómeno acústico que pueda percibirse como una unidad coherente de escucha. A partir de ahí, Schaeffer construye una tipología y morfología detallada de los objetos sonoros, describiendo sus cualidades en términos de masa, grano, allure, perfil dinámico, entre otros.

El libro sentó las bases de la **electroacústica** y la **musicología experimental**, e influyó profundamente en compositores, diseñadores de sonido y teóricos del audio durante la segunda mitad del siglo XX.

## Componentes

### CD4017BE

Contador/divisor decimal CMOS de 10 salidas. Recibe pulsos de reloj en su pin CLK y activa de forma secuencial las salidas Q0–Q9, una a la vez. Se usa frecuentemente para secuenciadores de pasos, control de LEDs y generación de patrones rítmicos. Opera entre 3V y 15V.

### Resistencia

Una resistencia frena el paso de la corriente eléctrica, igual que una manguera más angosta reduce el flujo de agua. Al poner más resistencia, llega menos corriente a un componente. Esto sirve para proteger LEDs de quemarse, dividir voltajes, o ajustar cuánta señal pasa por un punto del circuito. Su valor se mide en ohms (Ω).

#### Código de colores

Las resistencias tienen bandas de colores pintadas que indican su valor. Las más comunes tienen **4 bandas**:

```
 ┌────────────────────────────┐
 │  B1  │  B2  │  B3  │  B4   │
 │ 1er  │ 2do  │ mult │ toler │
 │dígito│dígito│ ×10ⁿ │  ±%   │
 └────────────────────────────┘
```

| Color            | 1er dígito | 2do dígito | Multiplicador | Tolerancia |
|------------------|------------|-----------|---------------|------------|
| ⬛ Negro          | 0         | 0         | ×1            | —          |
| 🟫 Café           | 1         | 1         | ×10           | ±1%        |
| 🟥 Rojo           | 2         | 2         | ×100          | ±2%        |
| 🟧 Naranja        | 3         | 3         | ×1 000        | —          |
| 🟨 Amarillo       | 4         | 4         | ×10 000       | —          |
| 🟩 Verde          | 5         | 5         | ×100 000      | ±0.5%      |
| 🟦 Azul           | 6         | 6         | ×1 000 000    | ±0.25%     |
| 🟪 Violeta        | 7         | 7         | ×10 000 000   | ±0.1%      |
| 🩶 Gris           | 8         | 8         | —             | ±0.05%     |
| ⬜ Blanco         | 9         | 9         | —             | —          |
| 🔶 Dorado         | —         | —         | ×0.1          | ±5%        |
| 🔘 Plateado       | —         | —         | ×0.01         | ±10%       |

**Ejemplo:** Café · Negro · Rojo · Dorado → 1, 0, ×100, ±5% → **1 000 Ω (1kΩ) ±5%**

> La banda de tolerancia suele estar más separada del resto, o ser dorada/plateada.

#### Esquemático: batería 9V → resistencia 1kΩ → LED

```
                1kΩ          LED
      ┌───────/\/\/────────►|────┐
      │                    anode │
      │                         │
     (+)                        │
     ─┤  9V                     │
     (-)                        │
      │                         │
      └─────────────────────────┘

  (+) positivo de la batería
   │  cable
  /\/\/  resistencia 1kΩ  (limita la corriente para no quemar el LED)
   │  cable
  ►|  LED  (la punta del triángulo es el ánodo +, la rayita es el cátodo -)
   │  cable
  (-) negativo de la batería  →  GND
```

> La corriente siempre fluye de (+) a (−). Sin la resistencia, el LED recibiría demasiada corriente y se quemaría en segundos.

## Referencias

- Schaeffer, P. (1966). *Traité des objets musicaux: essai interdisciplines*. Éditions du Seuil.
  - Traducción al español: Schaeffer, P. (1988). *Tratado de los objetos musicales*. Alianza Editorial.
