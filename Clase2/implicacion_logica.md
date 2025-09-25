# Lógica Proposicional: La Implicación p → q

## Introducción

En lógica proposicional, la **implicación** se expresa con el símbolo →
y se lee como **"si p entonces q"**. Esta relación es fundamental para
el razonamiento lógico, pero también la podemos entender
fácilmente con ejemplos cotidianos.

La forma general es:

p → q

-   p: antecedente (la condición)
-   q: consecuente (lo que sucede si se cumple la condición)

Se interpreta así: **"si ocurre p, entonces ocurrirá q"**.

------------------------------------------------------------------------

## Primer ejemplo cotidiano

**Proposición 1 (p):** Si llueve\
**Proposición 2 (q):** La carretera se moja

La implicación completa sería:

"Si llueve (p), entonces la carretera se moja (q)."

Esto significa que cada vez que se cumple la condición p (llueve),
podemos concluir que q (la carretera se moja) también será verdadero.

**Atención**: Lo contrario no necesariamente es cierto. Que la carretera
esté mojada **no garantiza** que haya llovido (puede que alguien la haya
lavado, o que un tubo se haya roto).\
Es decir: q → p **no equivale** a p → q.

------------------------------------------------------------------------

## Ejemplo 2: Vida escolar

**Proposición 1 (p):** Si estudias para el examen\
**Proposición 2 (q):** Entonces aprobarás el examen

"Si estudias (p), entonces aprobarás (q)."

Interpretación:
- Si p es verdadero (sí estudias), entonces se cumple q (apruebas).
- Si no estudias, no podemos concluir nada con certeza a partir de esta
proposición. Podrías aprobar por suerte, o reprobar.

------------------------------------------------------------------------

## Ejemplo 3: Tecnología

**Proposición 1 (p):** Si presiono el botón de encendido de mi
computadora\
**Proposición 2 (q):** Entonces la computadora se enciende

"Si presiono el botón (p), entonces la computadora se enciende (q)."

Interpretación:
- Si p se cumple (presionar el botón), normalmente q se cumple (la
computadora se enciende).
- Pero que la computadora esté encendida (q verdadero) no significa
necesariamente que presionaste el botón (p). Quizá se encendió sola
después de un reinicio automático.

------------------------------------------------------------------------

## Nota recordatorio

1.  p → q significa **si ocurre p, entonces ocurre q**.
2.  Es una **relación de dependencia**: el antecedente p es la condición
    que, de cumplirse, asegura el consecuente q.
3.  **No funciona al revés**: que ocurra q no significa que
    necesariamente ocurrió p.

------------------------------------------------------------------------

## Aclaración

La implicación **solo es falsa en un caso**: cuando p es verdadero y q
es falso.
En todos los demás casos, p → q se considera verdadera.

Esto puede parecer extraño al inicio, así que lo aclaramos con un
ejemplo práctico en programación.

------------------------------------------------------------------------

## Mini ejemplo aplicado a la programación

Supongamos que estamos programando un sistema muy simple para encender
una luz:

**Proposición p:** El usuario presiona el botón.\
**Proposición q:** La luz se enciende.

La regla es: **Si el usuario presiona el botón (p), entonces la luz se
enciende (q).**

Veamos cada caso de la tabla:

1.  **p = V, q = V → p → q = V**\
    El usuario presionó el botón y la luz se encendió.\
    La condición se cumplió y todo funcionó bien.

2.  **p = V, q = F → p → q = F**\
    El usuario presionó el botón, pero la luz **no** se encendió.\
    Aquí la implicación es **falsa**, porque se esperaba que al
    cumplirse p, q también fuera verdadero.\
    (En programación, esto podría señalar un **error lógico o de
    hardware**).

3.  **p = F, q = V → p → q = V**\
    El usuario **no** presionó el botón, pero la luz está encendida.\
    La implicación sigue siendo **verdadera**, porque no se incumplió la
    regla: nunca dijimos que la luz solo podía encenderse si el botón
    era presionado, solo dijimos que "si se presiona, se enciende".\
    (En programación, esto puede ser que la luz se encendió por otro
    evento, como un temporizador automático).

4.  **p = F, q = F → p → q = V**\
    El usuario no presionó el botón y la luz tampoco se encendió.\
    La implicación es **verdadera** porque no se violó la regla. No se
    presionó el botón, por lo tanto no había obligación de que la luz se
    encendiera.

------------------------------------------------------------------------

## Resumen de cierre

-   La implicación solo falla cuando se **promete algo** (si p,
    entonces q) y esa promesa se rompe (se cumple p, pero q no).
-   En programación, esto se interpreta como una condición que no se
    cumple: el antecedente ocurre, pero el consecuente no.
