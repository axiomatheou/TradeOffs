# HISTORIAS DE VIDA ^•ﻌ•^

Simulador simple de trade-offs en ecología evolutiva  
Por Santiago Caballero Rosas

---

## Qué es

Una página interactiva donde construyes un organismo con recursos limitados  
y lo enfrentas a un ambiente que no conoces de antemano.

La idea es mostrar algo muy intuitivo: no se puede optimizar todo al mismo tiempo.

---

## Cómo funciona

- Tienes 10 puntos.
- Cada carácter cuesta puntos.
- Los caracteres están en pares que compiten entre sí.
- Eliges una combinación y envías.

Después:

- Se selecciona un ambiente al azar.
- Se calcula un fitness entre 0 y 100.
- Se muestra qué aportó cada carácter.

---

## Ambientes

- Alta densidad / sequía  
- Alta depredación  
- Ambiente estable  

Cada uno favorece estrategias distintas.

---

## Modelo

El cálculo es intencionalmente simple.

Se suma el aporte de cada carácter según el ambiente:

\[
fitness = \sum w_i
\]

y se normaliza:

\[
fitness = \frac{fitness}{fitness_{max}} \cdot 100
\]

---

## Leaderboard

Se guarda en el navegador usando `localStorage`.

- No es global
- No se comparte entre dispositivos
- Se puede borrar manualmente

---

## ✝

Christos anesti! Alithos anesti!

---
