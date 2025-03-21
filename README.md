
<!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Teorema de Bolzano</title>
    <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
    <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
        }

        #content {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
            max-width: 1024px;
            /* Pantalla más grande */
            width: 95%;
            min-height: 600px;
            /* Altura mínima */
            transition: all 0.5s ease;
            text-align: left;
            /* Alineación a la izquierda */
            cursor: pointer;
            /* Cambiar el cursor a una mano */
        }

        h1 {
            color: #333;
            margin-top: 0;
            /* Eliminar margen superior */
            margin-bottom: 20px;
            /* Añadir espacio debajo del título */
        }

        h2 {
            color: #555;
            margin-top: 30px;
            /* Añadir espacio antes del subtítulo */
            margin-bottom: 15px;
        }

        p {
            color: black;
            transition: color 0.5s ease;
            margin-bottom: 10px;
            /* Espacio entre párrafos */
            line-height: 1.6;
            /* Espaciado entre líneas */
        }

        .blue {
            color: blue;
        }

        img {
            max-width: 100%;
            height: auto;
            margin-top: 20px;
            /* Espacio antes de la imagen */
        }

        ul,
        ol {
            margin-left: 30px;
            /* Indentación de listas */
            margin-bottom: 15px;
        }

        li {
            margin-bottom: 8px;
        }
    </style>
</head>

<body>
    <div id="content">
        <h1>Teorema de Bolzano</h1>
    </div>

    <script>
        const contentDiv = document.getElementById('content');
        const content = [
            { type: 'text', value: 'Sea \\(f: [a,b] \\to \\mathbb{R}\\)' },
            { type: 'text', value: 'Si \\(f\\) es continua en \\([a,b]\\)' },
            { type: 'text', value: 'y \\(f(a)\\) y \\(f(b)\\) tienen signos opuestos' },
            { type: 'text', value: '(es decir, \\(f(a) \\cdot f(b) < 0\\))' },
            { type: 'text', value: 'Entonces existe al menos un \\(c \\in (a,b)\\) tal que \\(f(c) = 0\\)' },
            { type: 'image', value: 'bolzano_html.png' },
            { type: 'clear', value: 'Ejercicio 1' },
            { type: 'title', value: 'Demostración de la existencia de una solución usando el Teorema de Bolzano' },
            { type: 'text', value: 'Queremos demostrar que la ecuación \\( 2x^3 - 6x + 1 = 0 \\) tiene al menos una solución en el intervalo \\( (0, 1) \\), utilizando el Teorema de Bolzano.' },
            { type: 'subtitle', value: 'Planteamiento del problema' },
            { type: 'text', value: 'Sea la función:' },
            { type: 'text', value: '\\( f(x) = 2x^3 - 6x + 1. \\)' },
            { type: 'text', value: 'Sabemos que \\( f(x) \\) es un polinomio, por lo tanto, es continua en todo \\( \\mathbb{R} \\). En particular, es continua en el intervalo cerrado \\([0, 1]\\).' },
            { type: 'text', value: 'El Teorema de Bolzano establece que si \\( f(x) \\) es continua en \\([a, b]\\) y \\( f(a) \\cdot f(b) < 0 \\), entonces existe al menos un \\( c \\in (a, b) \\) tal que \\( f(c) = 0 \\).' },
            { type: 'subtitle', value: 'Evaluación de \\( f(x) \\) en los extremos del intervalo' },
            { type: 'text', value: 'Evaluamos \\( f(x) \\) en los extremos del intervalo:' },
            { type: 'text', value: '\\( f(0) = 2(0)^3 - 6(0) + 1 = 1. \\)' },
            { type: 'text', value: '\\( f(1) = 2(1)^3 - 6(1) + 1 = 2 - 6 + 1 = -3. \\)' },
            { type: 'text', value: 'Por lo tanto:' },
            { type: 'text', value: '\\( f(0) = 1 \\quad \\text{y} \\quad f(1) = -3. \\)' },
            { type: 'subtitle', value: 'Verificación del cambio de signo' },
            { type: 'text', value: 'Observamos que:' },
            { type: 'text', value: '\\( f(0) > 0 \\quad \\text{y} \\quad f(1) < 0. \\)' },
            { type: 'text', value: 'Esto implica que:' },
            { type: 'text', value: '\\( f(0) \\cdot f(1) = (1)(-3) = -3 < 0. \\)' },
            { type: 'text', value: 'Es decir, \\( f(x) \\) cambia de signo en el intervalo \\([0, 1] \\).' },
            { type: 'subtitle', value: 'Conclusión' },
            { type: 'text', value: 'Dado que \\( f(x) \\) es continua en el intervalo cerrado \\([0, 1] \\), y que \\( f(0) \\cdot f(1) < 0 \\), por el Teorema de Bolzano existe al menos un punto \\( c \\in (0, 1) \\) tal que:' },
            { type: 'text', value: '\\( f(c) = 0. \\)' },
            { type: 'text', value: 'Por lo tanto, la ecuación \\( 2x^3 - 6x + 1 = 0 \\) tiene al menos una solución en el intervalo \\( (0, 1). \\)' },
            { type: 'clear', value: 'Ejercicio 2' },
            { type: 'title', value: 'Probar que las funciones \\( f(x) = \\ln(x) \\) y \\( g(x) = e^{-x} \\) se cortan en algún punto.' },
            { type: 'subtitle', value: 'Demostración' },
            { type: 'text', value: 'Para demostrar que las funciones se cortan, debemos probar que existe al menos un punto donde \\( f(x) = g(x) \\). Aplicaremos el Teorema de Bolzano a la función diferencia.' },
            { type: 'text', value: '1. Definimos \\( h(x) = f(x) - g(x) = \\ln(x) - e^{-x} \\).' },
            { type: 'text', value: '2. \\( h(x) \\) es continua en \\( (0,\\infty) \\) ya que es la diferencia de dos funciones continuas en ese intervalo.' },
            { type: 'subtitle', value: 'Evaluamos \\( h(x) \\) en dos puntos:' },
            { type: 'text', value: 'Para \\( x = 1 \\):' },
            { type: 'text', value: '\\( h(1) = \\ln(1) - e^{-1} = 0 - \\frac{1}{e} \\approx -0.368 < 0. \\)' },
            { type: 'text', value: 'Para \\( x = 2 \\):' },
            { type: 'text', value: '\\( h(2) = \\ln(2) - e^{-2} \\approx 0.693 - 0.135 \\approx 0.558 > 0. \\)' },
            { type: 'text', value: '3. Observamos que \\( h(1) < 0 \\) y \\( h(2) > 0 \\), por lo tanto \\( h(1) \\cdot h(2) < 0 \\).' },
            { type: 'subtitle', value: 'Aplicando el Teorema de Bolzano:' },
            { type: 'text', value: 'Como \\( h(x) \\) es continua en \\( [1,2] \\) y \\( h(1) \\cdot h(2) < 0 \\), existe al menos un punto \\( c \\in (1,2) \\) tal que \\( h(c) = 0 \\).' },
            { type: 'text', value: '\\( h(c) = 0 \\) implica que \\( \\ln(c) - e^{-c} = 0 \\), o equivalentemente, \\( \\ln(c) = e^{-c} \\).' },
            { type: 'text', value: 'Por lo tanto, hemos demostrado que existe al menos un punto \\( c \\in (1,2) \\) donde \\( f(c) = g(c) \\), es decir, donde las funciones \\( f(x) = \\ln(x) \\) y \\( g(x) = e^{-x} \\) se cortan.' },
            { type: 'clear', value: 'Ejercicio 3' },
            { type: 'title', value: 'Probar que las funciones \\( f(x) = \\sin(x) \\) y \\( g(x) = \\dfrac{1}{x} \\) se cortan en algún punto del intervalo \\( \\left(2\\pi, \\dfrac{5\\pi}{2}\\right) \\).' },
            { type: 'subtitle', value: 'Solución' },
            { type: 'text', value: 'Para probar que las funciones \\( f(x) = \\sin(x) \\) y \\( g(x) = \\dfrac{1}{x} \\) se cortan en algún punto del intervalo \\( \\left(2\\pi, \\dfrac{5\\pi}{2}\\right) \\), consideramos la función \\( h(x) = f(x) - g(x) = \\sin(x) - \\dfrac{1}{x} \\).' },
            { type: 'subtitle', value: 'Evaluamos \\( h(x) \\) en los extremos del intervalo:' },
            { type: 'text', value: '1. En \\( x = 2\\pi \\):' },
            { type: 'text', value: '\\( h(2\\pi) = \\sin(2\\pi) - \\dfrac{1}{2\\pi} = 0 - \\dfrac{1}{2\\pi} = -\\dfrac{1}{2\\pi} < 0. \\)' },
            { type: 'text', value: '2. En \\( x = \\dfrac{5\\pi}{2} \\):' },
            { type: 'text', value: '\\( h\\left(\\dfrac{5\\pi}{2}\\right) = \\sin\\left(\\dfrac{5\\pi}{2}\\right) - \\dfrac{1}{\\dfrac{5\\pi}{2}} = 1 - \\dfrac{2}{5\\pi} > 0. \\)' },
            { type: 'text', value: 'Dado que \\( h(x) \\) es continua en el intervalo \\( \\left[2\\pi, \\dfrac{5\\pi}{2}\\right] \\) y \\( h(2\\pi) < 0 \\) mientras que \\( h\\left(\\dfrac{5\\pi}{2}\\right) > 0 \\), por el teorema de Bolzano, existe al menos un punto \\( c \\in \\left(2\\pi, \\dfrac{5\\pi}{2}\\right) \\) tal que \\( h(c) = 0 \\). Esto implica que \\( f(c) = g(c) \\), es decir, las funciones \\( f(x) \\) y \\( g(x) \\) se cortan en \\( c \\).' },
            { type: 'text', value: 'Por lo tanto, las funciones \\( f(x) = \\sin(x) \\) y \\( g(x) = \\dfrac{1}{x} \\) se cortan en algún punto del intervalo \\( \\left(2\\pi, \\dfrac{5\\pi}{2}\\right) \\).' }
        ];

        let i = 0;
        contentDiv.addEventListener('click', displayNext);

        function displayNext() {
            if (i < content.length) {
                const item = content[i];

                if (item.type === 'text') {
                    const p = document.createElement('p');
                    p.innerHTML = item.value;
                    MathJax.typesetPromise([p]).then(() => {
                        contentDiv.appendChild(p);
                    });
                } else if (item.type === 'image') {
                    const img = document.createElement('img');
                    img.src = item.value;
                    contentDiv.appendChild(img);
                } else if (item.type === 'title') {
                    const h2 = document.createElement('h2');
                    h2.innerHTML = item.value;
                    MathJax.typesetPromise([h2]).then(() => {
                        contentDiv.appendChild(h2);
                    });
                } else if (item.type === 'subtitle') {
                    const h3 = document.createElement('h3');
                    h3.innerHTML = item.value;
                    MathJax.typesetPromise([h3]).then(() => {
                        contentDiv.appendChild(h3);
                    });
                } else if (item.type === 'clear') {
                    contentDiv.innerHTML = `<h2>${item.value}</h2>`;
                }

                i++;
            }
        }
    </script>
</body>

</html>
