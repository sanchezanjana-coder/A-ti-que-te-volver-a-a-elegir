# Para Javi — web interactiva con diseños de Canva

**Este proyecto NO recrea los diseños.** Cada pantalla es uno de los siete archivos PNG originales de Canva. Se muestran completos, conservando sus píxeles originales; encima hay botones HTML 100 % transparentes.

## Estructura exacta

```text
A-ti-que-te-volver-a-a-elegir/
├── index.html
├── style.css
├── script.js
├── README.md
├── imagenes/
│   ├── 1(1).png
│   ├── 2(1).png
│   ├── 3(1).png
│   ├── 4(1).png
│   ├── 5(1).png
│   ├── 6(1).png
│   └── 7(1).png
└── musica/
    └── LEEME.txt
```

Los siete archivos `imagenes/` están incluidos en el ZIP sin modificar y mantienen el mismo nombre que los originales recibidos. No hace falta subir archivos de fotos: el álbum está incluido en `7(1).png`.

## Cómo navegar

- Pulsa los botones **Siguiente** de las páginas 1, 3 y 5.
- En la página 2, **Sí** avanza; **No** muestra una respuesta divertida sin cambiar el diseño.
- Pulsa cualquier etiqueta **Page 1**, ..., **Page 7** (ya dibujadas en Canva) para ir a esa página.
- En las páginas 4, 6 y 7 usa esas etiquetas superiores para avanzar o regresar.
- En ordenador: flechas ← / →, Inicio / Fin, Re Pág / Av Pág.
- En móvil: desliza horizontalmente a izquierda/derecha, si la imagen no está ampliada.
- Para **ampliar el texto**: doble clic o doble toque sobre el dibujo (fuera de los botones); doble toque de nuevo para ajustar. También puedes usar las teclas `+`, `-` y `0`. Se permite el pellizco de ampliación del navegador.
- En la pantalla final, pulsa **Page 1**, desliza a la derecha o usa la tecla **Inicio** para volver al principio.

## Música opcional (NO se incluye ningún tema musical)

1. Consigue un archivo MP3 propio o para el que tengas los derechos/permisos.
2. Cópialo dentro de `musica/` y ponle **exactamente** el nombre `cancion.mp3` (todo en minúsculas).
3. Puedes reproducirlo o pausarlo con la discreta nota musical **♫** arriba a la izquierda o la tecla **M**.
4. La música **nunca se reproduce automáticamente**. Si falta el MP3, el resto de la web sigue funcionando y al intentar reproducirlo aparece un mensaje discreto.

El control ♫ es el único elemento visual funcional añadido sobre la composición, necesario para iniciar la música de forma manual. Puedes ocultarlo eliminando el botón `musicToggle` de `index.html` si no quieres música, pero desactiva también su código en `script.js` para mantenerlo coherente.

## Publicar gratis en GitHub Pages

Destino solicitado: `sanchezanjana-coder/A-ti-que-te-volver-a-a-elegir`

1. Descomprime el ZIP en el ordenador.
2. Entra en [el repositorio](https://github.com/sanchezanjana-coder/A-ti-que-te-volver-a-a-elegir). Si no existe todavía, créalo con ese nombre y hazlo **público** para GitHub Pages gratis.
3. En la pestaña **Code**, elige **Add file → Upload files**.
4. Abre la carpeta descomprimida y arrastra **su contenido**, no la carpeta contenedora: `index.html`, `style.css`, `script.js`, `README.md` y las carpetas `imagenes/` y `musica/` con sus archivos. GitHub debería mostrar `index.html` en la raíz del repositorio.
5. Pulsa **Commit changes**, sobre la rama `main`.
6. Ve a **Settings → Pages**.
7. En **Build and deployment**, selecciona **Source: Deploy from a branch**, **Branch: main**, **Folder: /(root)**, y guarda.
8. Abre **Actions** para comprobar si el despliegue termina correctamente, y luego visita:

   `https://sanchezanjana-coder.github.io/A-ti-que-te-volver-a-a-elegir/`

   Esta es la **dirección prevista una vez publicado**, no una afirmación de que ya exista.
9. Haz una prueba desde móvil y ordenador. Si cambias las imágenes, usa exactamente los nombres indicados en `script.js` y exporta con las mismas dimensiones/proporción; si cambian las composiciones o posiciones de los botones hay que volver a medir sus zonas pulsables.

**Privacidad:** GitHub Pages público implica que las fotografías de la página 7 se harán visibles en Internet. Si no quieres publicar esas fotos, NO hagas público el repositorio ni actives Pages hasta decidir cómo compartirlo.

Documentación oficial: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Inventario de zonas pulsables verificadas

Las coordenadas originales se expresan en píxeles **(izquierda, arriba, ancho, alto)** dentro del PNG de **1366 × 818**. En la web se convierten automáticamente en porcentajes sobre la imagen para que escalen sin desplazarse.

| Página | Elemento de Canva | Caja en píxeles | Acción |
| --- | --- | --- | --- |
| 1 | Siguiente | (479, 556, 347, 79) | Página 2 |
| 2 | Sí | (493, 560, 119, 81) | Página 3 |
| 2 | No | (670, 560, 119, 81) | Mensaje juguetón, permanece en página 2 |
| 3 | Siguiente | (466, 614, 348, 80) | Página 4 |
| 5 | Siguiente | (466, 614, 348, 80) | Página 6 |
| Todas | Page 1 | (851, 7, 65, 37) aprox. | Página 1 |
| Todas | Page 2 | (925, 7, 65, 37) aprox. | Página 2 |
| Todas | Page 3 | (998, 7, 65, 37) aprox. | Página 3 |
| Todas | Page 4 | (1072, 7, 65, 37) aprox. | Página 4 |
| Todas | Page 5 | (1146, 7, 65, 37) aprox. | Página 5 |
| Todas | Page 6 | (1220, 7, 65, 37) aprox. | Página 6 |
| Todas | Page 7 | (1294, 7, 65, 37) aprox. | Página 7 |

En las páginas 4, 6 y 7 no hay otro botón dibujado. Por eso **no se han añadido falsas zonas «Siguiente» sobre la carta, el poema o las fotografías**. Los botones del menú superior sí son navegables.

El botón **No** no se mueve porque está dibujado dentro de un PNG: mover solo su zona de clic la desalinearía y mover el gráfico exigiría alterar el original. Por ello responde con un mensaje divertido en vez de fingir ese efecto.

## Recursos pendientes

- **Opcional:** `musica/cancion.mp3`, no proporcionado. No bloquea nada.
- **No faltan imágenes:** las siete páginas están en el ZIP.

## Prueba local

Puedes abrir `index.html` directamente en un navegador. Si quieres reproducir las condiciones de GitHub Pages, desde esa carpeta ejecuta `python3 -m http.server 8000` y entra en `http://localhost:8000/`. No hace falta instalar frameworks.

## Licencias y originalidad

Solo se incluyen imágenes entregadas para este proyecto; ninguna imagen se ha redibujado. No se adjunta música ajena. Las imágenes originales de Canva pueden incorporar elementos, fotografías o tipografías sujetos a derechos: comprueba su permiso de publicación antes de hacer el sitio público.
