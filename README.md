# DAFO — Estructura del proyecto

## Qué hay aquí

```
dafo_proyecto/
├── index.html          ← el juego entero (178 KB)
├── assets/
│   ├── apreton/        f1, f2, f3   → animación de trato cerrado
│   ├── sello/          s1, s2, s3   → animación de sello del banco
│   ├── firma/          g1, g2, g3   → animación de firma de préstamo
│   └── personajes/     18 retratos  → 6 personajes × 3 estados
└── README.md
```

## Cómo ejecutarlo

**En local**: abre `index.html` con doble clic. Funciona directamente, siempre que la carpeta `assets` esté al lado.

> ⚠️ Si mueves `index.html` sin llevarte `assets`, las imágenes no aparecerán.

**Publicado en internet**: sube toda la carpeta a un hosting estático (GitHub Pages, Netlify, Vercel). El juego quedará accesible desde cualquier móvil con la URL, que es lo que necesitas para el multijugador.

## Cómo añadir una ilustración nueva

1. Guarda el archivo en la subcarpeta que corresponda dentro de `assets/`
2. En `index.html`, añade la referencia con el mismo patrón que las demás:
   ```js
   const MICOSA = { a: ASSETS+'micarpeta/a.webp' };
   ```

Formato recomendado: **WebP** con fondo transparente. Pesa la mitad que PNG con la misma calidad.

## Sustituir un personaje

Basta con reemplazar el archivo correspondiente en `assets/personajes/`, respetando el nombre:

`[duende|unicornio|robot|pulpo|dragon|buho]_[normal|victoria|derrota].webp`

No hay que tocar el código.

## Nota sobre la versión de un solo archivo

Existe también `dafo_demo_arbitro_ia.html`, con todo incrustado (871 KB). Es más cómodo para pasársela a alguien por correo o mensajería, pero pesa cinco veces más y es más lenta de cargar. **Para desarrollar, usa esta versión separada.**

## Siguiente paso recomendado

Sube esto a un repositorio de GitHub. Te dará:
- Copia de seguridad real del proyecto
- Historial de cambios (puedes volver atrás si algo se rompe)
- Con GitHub Pages, una URL pública para jugar desde el móvil sin instalar nada
