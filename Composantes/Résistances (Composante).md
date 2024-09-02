Une résistance est une composante qui limite la quantité de courant qui peut passer en fonction d'un voltage donné selon la relation $V = R * I$.

La valeur d'une résistance est illustrée sur la composante à l'aide d'un code de couleurs.

![[resistor-color-chart.avif]]

Pour les résistances à 6 bandes, on ajoute un coefficient de température en ppm/°C.
Pour connaître la variation, on se fie à la formule suivante:
$$TCR = \frac{(R - R_a)}{R_a} + (T - T_a) \times 1000000 $$
Où:
- $R_a$ : Résistance à la température de référence $T_a$
- $R$ : Résistance à la température $T$

![[ppmChart.png]]

Pour calculer rapidement les propriétés d'une résistance [la calculatrice en ligne de Digikey](https://www.digikey.ca/en/resources/conversion-calculators/conversion-calculator-resistor-color-code) est un outil utile.