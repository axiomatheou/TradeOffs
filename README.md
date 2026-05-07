# HISTORIAS DE VIDA ^•ﻌ•^
Simulador de trade-offs en ecología evolutiva  
Por Santiago Caballero Rosas

---

## Qué es

Una página interactiva donde construyes un organismo con recursos limitados y lo enfrentas a un ambiente que no conoces de antemano. La idea central es sencilla: no se puede optimizar todo al mismo tiempo.

---

## Cómo funciona

Tienes **10 puntos** para distribuir entre caracteres biológicos antes de que el ambiente sea revelado. Cada carácter tiene un costo, y los caracteres están organizados en pares que compiten por los mismos recursos. Algunos pares son **mutuamente excluyentes**, no pueden coexistir en el mismo organismo, igual que en la naturaleza.

Una vez que envías tu organismo, se sortea un ambiente al azar, se calcula tu fitness y se muestra un desglose de qué aportó (o costó) cada carácter en ese contexto.

---

## Caracteres

Los rasgos están agrupados en cinco trade-offs, cada uno con justificación biológica real:

| Par | Dimensión |
|---|---|
| Alas grandes / Gónadas grandes | Dispersión vs. reproducción |
| Coraza / Tamaño corporal | Defensa vs. dominancia competitiva |
| Camuflaje / Coloración llamativa | Supervivencia vs. éxito reproductivo |
| Agilidad / Reservas de grasa | Escape vs. resistencia a la escasez |
| Madurez temprana / Longevidad | Presente vs. futuro |

---

## Ambientes

- 🌵 **Alta densidad / Sequía** — favorece dispersión, reservas y reproducción rápida
- 🦅 **Alta depredación** — favorece defensa, camuflaje y escape
- 🌱 **Ambiente estable** — favorece inversión reproductiva y longevidad

Cada ambiente penaliza activamente algunos rasgos, no solo los ignora.

---

## Modelo

El fitness se calcula en dos términos.

El primero es la suma de las contribuciones individuales de cada carácter según el ambiente, donde los valores pueden ser negativos (un rasgo activamente maladaptativo en ese contexto):

$$fitness_{bruto} = \sum_{i} w_{i}(env)$$
 
El segundo agrega las interacciones entre pares de rasgos que comparten sustrato fisiológico. Algunos pares se frenan mutuamente (covarianza negativa), otros son coherentes entre sí (covarianza positiva):
 
$$fitness_{bruto} = \sum_{i} w_{i}(env) + \sum_{i < j} cov_{ij}(env)$$
 
Finalmente se normaliza sobre el máximo alcanzable por ambiente:
 
$$fitness = \frac{fitness_{bruto}}{fitness_{max}(env)} \cdot 100$$

El resultado es un índice entre 0 y 100. El máximo varía por ambiente porque cada uno tiene una combinación óptima distinta.

---

## Leaderboard

Las partidas se guardan localmente en el navegador con `localStorage`. Está pensado para uso en clase, donde varios estudiantes juegan desde el mismo navegador y comparan estrategias en tiempo real.

La tabla no es solo un ranking. Es evidencia de que organismos con estrategias completamente distintas pueden tener fitness similar dependiendo del ambiente que les tocó.

---

## Uso en clase

El simulador funciona mejor como punto de partida para discusión. La secuencia natural es: jugar una vez sin pensar demasiado → ver el resultado → entender qué costó cada decisión → volver a intentar con otra estrategia → comparar en el leaderboard.

No hay una respuesta correcta.

---

## Licencia

Se puede usar con fines educativos dando crédito al autor. No modificar sin preguntar.

---

✝ Christos anesti! Alithos anesti!
