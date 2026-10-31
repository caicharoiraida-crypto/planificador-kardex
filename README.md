# Planificador de materiales de Iraida Atsuam, con kardex

Trabajo individual · ET505 Técnicas de programación II · Semana 9 · Autora: Iraida Atsuam Caicharo (ciclo VI).
Todos los datos son ficticios.

## Propósito
Amplío mi Planificador de materiales de la semana 7 (taller de circuitos eléctricos básicos, presupuesto S/ 120.00) con un pequeño **kardex**: materiales con id estable y código, búsqueda por nombre o código, cambio de nombre por id, entradas y salidas enteras positivas, existencia = entradas − salidas, inactivación o eliminación, persistencia en localStorage y exportación de movimientos a CSV. Se conservan el cálculo en céntimos, el presupuesto y la validación del pedido.

## Archivos
- `index.html`: estructura del planificador (S7) y, al final de `<main>`, la sección `#kardex` integrada (S9). Carga `app.js` y después `kardex.js`.
- `styles.css`: estilos de la semana 7 más las reglas de `personalizacion.css` y mi personalización (etiqueta `.etiqueta-kardex` y paleta RGB).
- `app.js`: objeto `limites`, `calcularTotal`, `validarPedido` y acciones del pedido (S7). Sin cambios de lógica; sólo cambió el rótulo «Saldo del presupuesto».
- `kardex.js`: lógica del kardex (`saldoDe`, `agregarMovimiento`, `exportarCSV`), almacenamiento y eventos de pantalla.
- `README.md`: esta documentación.

## Ejecutar y usar
Local: conserve juntos todos los archivos y abra `index.html` en Chrome o Edge. No requiere instalación.
Publicado: abra el sitio de GitHub Pages indicado abajo.
Uso del kardex: cree un material, selecciónelo en la lista, elija ENTRADA o SALIDA, escriba una cantidad entera positiva y registre. «Exportar CSV» descarga `movimientos-materiales.csv`.

## Publicación
Repositorio: [PEGAR AQUÍ LA URL DEL REPOSITORIO]
Sitio GitHub Pages: [PEGAR AQUÍ LA URL QUE MUESTRA GITHUB PAGES]

## Aportes y ayuda recibida
- Recursos del curso: plantilla S7 y «Fragmentos de integración · ET505 · S9» (docente Mg. Max Aldo Hidalgo Chávez).
- Mi integración: ubiqué la sección del kardex dentro de `<main>`, fuera del formulario del pedido; enlacé `kardex.js` después de `app.js`; incorporé las reglas CSS; elegí texto y tamaño de etiqueta y la paleta azul rgb(30,64,175).
- Mejoras que añadí a los fragmentos: código corto `MAT-001…` para buscar (el id UUID sigue siendo el identificador); función `nuevoId()` de respaldo; columna «Codigo» y línea `sep=;` en el CSV; mensajes corregidos («al menos 3 caracteres»).
- Ayuda de IA: asistente Claude (Anthropic), 31/10/2026. El detalle de consultas, adaptación y comprobaciones está en el informe PDF entregado en MAXEDRA.

## Límites
- localStorage guarda los datos sólo en este navegador y en este origen; no hay base de datos compartida ni usuarios.
- El CSV es una copia de los movimientos, no una sincronización con Excel.
- La existencia (unidades físicas) es independiente del presupuesto en soles del pedido.
- El pedido del planificador no se guarda al recargar (igual que en la semana 7).
