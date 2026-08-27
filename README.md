<!DOCTYPE html>
<html lang="es">

<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Conocimiento Cultural</title>

<style>

/* ==============================
   CONFIGURACIÓN GENERAL
================================ */

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    scroll-behavior:smooth;
}

body{
    font-family:Arial, Helvetica, sans-serif;
    background:#f5eee6;
    color:#333;
    overflow-x:hidden;
}

/* ==============================
   FONDO ANIMADO
================================ */

.fondo{
    position:fixed;
    width:100%;
    height:100%;
    top:0;
    left:0;
    z-index:-1;
    overflow:hidden;
}

.circulo{
    position:absolute;
    border-radius:50%;
    opacity:.25;
    animation:mover 12s infinite alternate ease-in-out;
}

.c1{
    width:300px;
    height:300px;
    background:#d97706;
    top:5%;
    left:-100px;
}

.c2{
    width:250px;
    height:250px;
    background:#166534;
    right:-80px;
    top:40%;
    animation-delay:2s;
}

.c3{
    width:200px;
    height:200px;
    background:#b91c1c;
    bottom:-50px;
    left:40%;
    animation-delay:4s;
}

@keyframes mover{

    0%{
        transform:translate(0,0) scale(1);
    }

    50%{
        transform:translate(100px,-70px) scale(1.2);
    }

    100%{
        transform:translate(-80px,80px) scale(.9);
    }
}


/* ==============================
   ENCABEZADO
================================ */

header{

    min-height:650px;

    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;

    text-align:center;

    color:white;

    padding:30px;

    background:
    linear-gradient(
        rgba(0,0,0,.60),
        rgba(0,0,0,.60)
    ),
    url("https://images.unsplash.com/photo-1518638150340-f706e86654de?auto=format&fit=crop&w=1800&q=85");

    background-size:cover;
    background-position:center;

    background-attachment:fixed;
}

header h1{

    font-size:65px;

    text-shadow:
    0 0 10px #000,
    0 0 25px #000;

    animation:titulo 2s ease;
}

header p{

    font-size:24px;

    max-width:800px;

    margin-top:20px;

    animation:subir 2.5s ease;
}

@keyframes titulo{

    from{
        opacity:0;
        transform:scale(.5) rotate(-5deg);
    }

    to{
        opacity:1;
        transform:scale(1) rotate(0);
    }
}

@keyframes subir{

    from{
        opacity:0;
        transform:translateY(70px);
    }

    to{
        opacity:1;
        transform:translateY(0);
    }
}


/* ==============================
   MENÚ
================================ */

nav{

    position:sticky;
    top:0;

    z-index:1000;

    background:#651f12;

    padding:17px;

    text-align:center;

    box-shadow:0 5px 15px rgba(0,0,0,.3);
}

nav a{

    color:white;

    text-decoration:none;

    font-weight:bold;

    margin:0 12px;

    transition:.3s;
}

nav a:hover{

    color:#ffd166;

    transform:scale(1.1);

}


/* ==============================
   SECCIONES
================================ */

section{

    max-width:1150px;

    margin:60px auto;

    padding:40px;

    background:rgba(255,255,255,.95);

    border-radius:25px;

    box-shadow:0 10px 30px rgba(0,0,0,.15);

    animation:entrada 1s ease;
}

@keyframes entrada{

    from{
        opacity:0;
        transform:translateY(50px);
    }

    to{
        opacity:1;
        transform:translateY(0);
    }
}

h2{

    color:#7b2d1d;

    font-size:36px;

    margin-bottom:25px;

    border-bottom:4px solid #d97706;

    padding-bottom:12px;
}

h3{

    color:#8b4513;

    margin-bottom:10px;

}

p{

    font-size:18px;

    line-height:1.8;

    margin-bottom:18px;
}


/* ==============================
   TARJETAS
================================ */

.contenedor{

    display:grid;

    grid-template-columns:
    repeat(auto-fit,minmax(240px,1fr));

    gap:25px;

    margin-top:30px;
}

.tarjeta{

    background:white;

    border-radius:20px;

    overflow:hidden;

    box-shadow:
    0 5px 18px rgba(0,0,0,.18);

    transition:.5s;

    transform-style:preserve-3d;
}

.tarjeta:hover{

    transform:
    translateY(-15px)
    rotateX(4deg)
    rotateY(-3deg)
    scale(1.03);

    box-shadow:
    0 20px 40px rgba(0,0,0,.3);
}

.tarjeta img{

    width:100%;

    height:210px;

    object-fit:cover;

    transition:.7s;
}

.tarjeta:hover img{

    transform:scale(1.15);

}

.contenido{

    padding:25px;
}


/* ==============================
   IMÁGENES FLOTANTES
================================ */

.imagen{

    width:100%;

    max-width:850px;

    display:block;

    margin:35px auto;

    border-radius:25px;

    box-shadow:
    0 10px 30px rgba(0,0,0,.3);

    animation:flotar 4s infinite ease-in-out;
}

@keyframes flotar{

    0%,100%{
        transform:translateY(0);
    }

    50%{
        transform:translateY(-18px);
    }
}


/* ==============================
   LISTAS
================================ */

ul{

    padding-left:30px;

}

li{

    font-size:18px;

    margin:15px 0;

}


/* ==============================
   CAJAS INFORMATIVAS
================================ */

.info{

    background:
    linear-gradient(
        135deg,
        #fff0d5,
        #f5c98b
    );

    padding:30px;

    border-left:
    8px solid #8b4513;

    border-radius:15px;

    margin-top:25px;
}


/* ==============================
   CONTADOR
================================ */

.contador{

    text-align:center;

    background:#7b2d1d;

    color:white;

    padding:35px;

    border-radius:20px;

}

.numero{

    font-size:60px;

    font-weight:bold;

    animation:pulso 2s infinite;
}

@keyframes pulso{

    0%,100%{
        transform:scale(1);
    }

    50%{
        transform:scale(1.15);
    }
}


/* ==============================
   BARRAS
================================ */

.barra{

    width:100%;

    height:25px;

    background:#ddd;

    border-radius:20px;

    overflow:hidden;

    margin:15px 0 25px;
}

.progreso{

    height:100%;

    border-radius:20px;

    animation:llenar 3s ease;
}

.musica{
    width:90%;
    background:#b45309;
}

.gastronomia{
    width:95%;
    background:#15803d;
}

.tradiciones{
    width:88%;
    background:#b91c1c;
}

.artes{
    width:82%;
    background:#7c3aed;
}

@keyframes llenar{

    from{
        width:0;
    }

}


/* ==============================
   TIMELINE
================================ */

.timeline{

    border-left:5px solid #8b4513;

    padding-left:30px;

}

.evento{

    margin:35px 0;

    padding:20px;

    background:#fff7ed;

    border-radius:15px;

    transition:.4s;
}

.evento:hover{

    transform:translateX(15px);

    box-shadow:0 8px 20px rgba(0,0,0,.15);
}


/* ==============================
   BOTONES
================================ */

.botones{

    text-align:center;

    margin-top:30px;
}

.boton{

    display:inline-block;

    padding:15px 25px;

    margin:8px;

    background:#7b2d1d;

    color:white;

    text-decoration:none;

    border-radius:30px;

    font-weight:bold;

    transition:.4s;

}

.boton:hover{

    background:#d97706;

    transform:
    scale(1.08)
    rotate(-2deg);

    box-shadow:
    0 8px 20px rgba(0,0,0,.25);
}


/* ==============================
   FRASE
================================ */

.frase{

    text-align:center;

    font-size:30px;

    font-weight:bold;

    color:#7b2d1d;

    padding:40px;

    animation:latido 3s infinite;
}

@keyframes latido{

    0%,100%{
        transform:scale(1);
    }

    50%{
        transform:scale(1.03);
    }
}


/* ==============================
   PIE
================================ */

footer{

    background:#42140c;

    color:white;

    text-align:center;

    padding:45px;

    margin-top:70px;
}


/* ==============================
   RESPONSIVE
================================ */

@media(max-width:700px){

    header h1{
        font-size:42px;
    }

    header p{
        font-size:18px;
    }

    nav a{
        display:inline-block;
        margin:6px;
        font-size:14px;
    }

    section{
        margin:25px 12px;
        padding:25px;
    }

    h2{
        font-size:28px;
    }

}

</style>

</head>


<body>


<!-- FONDO -->

<div class="fondo">

    <div class="circulo c1"></div>
    <div class="circulo c2"></div>
    <div class="circulo c3"></div>

</div>


<!-- =========================
     ENCABEZADO
========================= -->

<header>

    <h1>🌎 Conocimiento Cultural</h1>

    <p>
        Historia, tradiciones, costumbres,
        identidad y diversidad cultural.
    </p>

    <p>
        “Conocer una cultura es conocer
        la historia de las personas que la construyeron.”
    </p>

</header>


<!-- =========================
     MENÚ
========================= -->

<nav>

    <a href="#inicio">Inicio</a>

    <a href="#concepto">Concepto</a>

    <a href="#elementos">Elementos</a>

    <a href="#mexico">México</a>

    <a href="#patrimonio">Patrimonio</a>

    <a href="#transmision">Transmisión</a>

    <a href="#importancia">Importancia</a>

    <a href="#enlaces">Enlaces</a>

</nav>


<!-- =========================
     INTRODUCCIÓN
========================= -->

<section id="inicio">

    <h2>📚 Introducción</h2>

    <p>

        El conocimiento cultural es todo aquello que una sociedad
        aprende, conserva y transmite a través de las generaciones.

        Incluye costumbres, tradiciones, valores, conocimientos,
        creencias, música, gastronomía, lenguaje, arte y diferentes
        formas de relacionarse con el mundo.

    </p>

    <p>

        La cultura no es algo estático. Se transforma con el paso
        del tiempo debido a los cambios sociales, tecnológicos y
        a la interacción entre diferentes comunidades.

    </p>

    <img
        class="imagen"
        src="https://images.unsplash.com/photo-1531219572328-a0171b4448a3?auto=format&fit=crop&w=1400&q=85"
        alt="Diversidad cultural">

</section>


<!-- =========================
     CONCEPTO
========================= -->

<section id="concepto">

    <h2>🧠 ¿Qué es el conocimiento cultural?</h2>

    <p>

        Es el conjunto de saberes y experiencias que pertenecen
        a una comunidad y que permiten comprender su manera de
        vivir, pensar, expresarse y relacionarse.

    </p>

    <div class="info">

        <h3>Ejemplo</h3>

        <p>

            Una receta tradicional que una abuela enseña a sus
            hijos y nietos es una forma de conocimiento cultural.

            No solamente se transmite la receta, sino también
            técnicas, historias y costumbres relacionadas con ella.

        </p>

    </div>

</section>


<!-- =========================
     ELEMENTOS
========================= -->

<section id="elementos">

    <h2>🎭 Elementos del conocimiento cultural</h2>

    <div class="contenedor">


        <div class="tarjeta">

            <img
            src="https://images.unsplash.com/photo-1506157786151-b8491531f063?auto=format&fit=crop&w=900&q=85">

            <div class="contenido">

                <h3>🎵 Música</h3>

                <p>
                    Canciones, instrumentos y estilos musicales
                    que representan la historia de una comunidad.
                </p>

            </div>

        </div>


        <div class="tarjeta">

            <img
            src="https://images.unsplash.com/photo-1515003197210-e0cd71810b5f?auto=format&fit=crop&w=900&q=85">

            <div class="contenido">

                <h3>🌮 Gastronomía</h3>

                <p>
                    Recetas, ingredientes y técnicas culinarias
                    transmitidas entre generaciones.
                </p>

            </div>

        </div>


        <div class="tarjeta">

            <img
            src="https://images.unsplash.com/photo-1564399579883-451a5d44ec08?auto=format&fit=crop&w=900&q=85">

            <div class="contenido">

                <h3>🎨 Arte</h3>

                <p>
                    Pinturas, esculturas, tejidos y artesanías
                    que expresan la identidad de una cultura.
                </p>

            </div>

        </div>


        <div class="tarjeta">

            <img
            src="https://images.unsplash.com/photo-1509644851169-2acc08aa25b6?auto=format&fit=crop&w=900&q=85">

            <div class="contenido">

                <h3>🎉 Tradiciones</h3>

                <p>
                    Fiestas, ceremonias y costumbres que forman
                    parte de la identidad de una comunidad.
                </p>

            </div>

        </div>


    </div>

</section>


<!-- =========================
     MÉXICO
========================= -->

<section id="mexico">

    <h2>🇲🇽 Conocimiento cultural en México</h2>

    <p>

        México posee una enorme diversidad cultural. En el país
        existen diferentes pueblos originarios, comunidades
        afrodescendientes y numerosas expresiones culturales
        regionales.

    </p>

    <p>

        Esta diversidad puede observarse en las lenguas,
        la gastronomía, la música, las fiestas, las artesanías,
        las formas de organización comunitaria y las tradiciones.

    </p>

    <div class="info">

        <h3>🌎 Diversidad cultural</h3>

        <p>

            El INAH explica que la cultura comprende manifestaciones
            materiales y sociales, incluyendo objetos, vestimenta,
            construcciones, ideas, costumbres, tradiciones, creencias
            y valores.

        </p>

    </div>

</section>


<!-- =========================
     PATRIMONIO
========================= -->

<section id="patrimonio">

    <h2>🏛️ Patrimonio cultural de México</h2>

    <p>

        El patrimonio cultural está formado por elementos que una
        sociedad considera valiosos y que busca conservar para las
        futuras generaciones.

    </p>

    <p>

        UNESCO registra actualmente 13 elementos mexicanos dentro
        de la Lista Representativa del Patrimonio Cultural
        Inmaterial de la Humanidad.

    </p>

    <div class="contador">

        <div class="numero">13</div>

        <p>
            elementos mexicanos inscritos
            en el patrimonio cultural inmaterial
        </p>

    </div>


    <div class="contenedor">


        <div class="tarjeta">

            <div class="contenido">

                <h3>🎺 Mariachi</h3>

                <p>
                    Música tradicional mexicana reconocida por
                    UNESCO en 2011.
                </p>

            </div>

        </div>


        <div class="tarjeta">

            <div class="contenido">

                <h3>💀 Fiestas de los muertos</h3>

                <p>
                    Tradición relacionada con la memoria y el
                    regreso simbólico de familiares fallecidos.
                </p>

            </div>

        </div>


        <div class="tarjeta">

            <div class="contenido">

                <h3>🌮 Cocina tradicional</h3>

                <p>
                    Conocimientos culinarios comunitarios,
                    ancestrales y vivos.
                </p>

            </div>

        </div>


        <div class="tarjeta">

            <div class="contenido">

                <h3>🏺 Talavera</h3>

                <p>
                    Procesos artesanales tradicionales de
                    Puebla y Tlaxcala.
                </p>

            </div>

        </div>


        <div class="tarjeta">

            <div class="contenido">

                <h3>🐎 Charrería</h3>

                <p>
                    Tradición ecuestre reconocida como patrimonio
                    cultural inmaterial.
                </p>

            </div>

        </div>


        <div class="tarjeta">

            <div class="contenido">

                <h3>🎶 Pirekua</h3>

                <p>
                    Canto tradicional del pueblo p'urhépecha.
                </p>

            </div>

        </div>

    </div>

</section>


<!-- =========================
     TRANSMISIÓN
========================= -->

<section id="transmision">

    <h2>🔄 ¿Cómo se transmite?</h2>

    <div class="timeline">


        <div class="evento">

            <h3>1️⃣ Familia</h3>

            <p>
                Los padres, abuelos y familiares enseñan
                historias, recetas, valores y costumbres.
            </p>

        </div>


        <div class="evento">

            <h3>2️⃣ Comunidad</h3>

            <p>
                Las fiestas, ceremonias y actividades
                comunitarias permiten aprender tradiciones.
            </p>

        </div>


        <div class="evento">

            <h3>3️⃣ Escuela</h3>

            <p>
                La educación permite conocer la historia,
                patrimonio y diversidad cultural.
            </p>

        </div>


        <div class="evento">

            <h3>4️⃣ Tecnología</h3>

            <p>
                Internet permite documentar y compartir
                conocimientos culturales con personas de
                diferentes lugares.
            </p>

        </div>

    </div>

</section>


<!-- =========================
     IMPORTANCIA
========================= -->

<section id="importancia">

    <h2>⭐ Importancia del conocimiento cultural</h2>

    <div class="info">

        <ul>

            <li>Fortalece la identidad de las personas.</li>

            <li>Ayuda a conservar las tradiciones.</li>

            <li>Permite conocer nuestra historia.</li>

            <li>Promueve el respeto entre culturas.</li>

            <li>Favorece la convivencia.</li>

            <li>Protege conocimientos ancestrales.</li>

            <li>Ayuda a valorar la diversidad.</li>

            <li>Permite transmitir conocimientos a nuevas generaciones.</li>

        </ul>

    </div>

</section>


<!-- =========================
     REPRESENTACIÓN VISUAL
========================= -->

<section>

    <h2>📊 Diferentes expresiones culturales</h2>

    <p>
        Estas barras representan ejemplos de áreas en las que
        podemos encontrar conocimiento cultural.
    </p>


    <h3>🎵 Música</h3>

    <div class="barra">
        <div class="progreso musica"></div>
    </div>


    <h3>🌮 Gastronomía</h3>

    <div class="barra">
        <div class="progreso gastronomia"></div>
    </div>


    <h3>🎉 Tradiciones</h3>

    <div class="barra">
        <div class="progreso tradiciones"></div>
    </div>


    <h3>🎨 Artes</h3>

    <div class="barra">
        <div class="progreso artes"></div>
    </div>

</section>


<!-- =========================
     RESPETO
========================= -->

<section>

    <h2>🤝 Respeto por la diversidad cultural</h2>

    <p>

        Respetar la diversidad cultural significa reconocer
        que las personas pueden tener diferentes costumbres,
        lenguas, creencias y formas de vivir.

    </p>

    <p>

        Conocer otras culturas ayuda a evitar prejuicios y
        favorece una convivencia basada en el respeto y la
        comprensión.

    </p>

</section>


<!-- =========================
     ENLACES
========================= -->

<section id="enlaces">

    <h2>🔗 Enlaces para aprender más</h2>

    <p>

        Estos sitios contienen información relacionada con
        patrimonio, cultura e historia:

    </p>


    <div class="botones">


        <a
        class="boton"
        href="https://ich.unesco.org/es/estado/mexico-MX"
        target="_blank">

        🌎 UNESCO - México

        </a>


        <a
        class="boton"
        href="https://ich.unesco.org/es/RL/dia-de-muertos-00054"
        target="_blank">

        💀 Día de Muertos

        </a>


        <a
        class="boton"
        href="https://ich.unesco.org/es/RL/el-mariachi-musica-decuerdas-canto-y-trompeta-00575"
        target="_blank">

        🎺 Mariachi

        </a>


        <a
        class="boton"
        href="https://lugares.inah.gob.mx/es/patrimonio-inmaterial"
        target="_blank">

        🏛️ INAH - Patrimonio Inmaterial

        </a>


        <a
        class="boton"
        href="https://patrimoniomundialmexico.inah.gob.mx/"
        target="_blank">

        🇲🇽 Patrimonio Mundial de México

        </a>


        <a
        class="boton"
        href="https://ich.unesco.org/es/"
        target="_blank">

        📚 UNESCO - Patrimonio Cultural

        </a>

    </div>

</section>


<!-- =========================
     FRASE FINAL
========================= -->

<section>

    <div class="frase">

        🌎 “Una cultura se mantiene viva
        cuando sus conocimientos,
        historias y tradiciones
        se siguen compartiendo.”

    </div>

</section>


<!-- =========================
     CONCLUSIÓN
========================= -->

<section>

    <h2>📝 Conclusión</h2>

    <p>

        El conocimiento cultural es fundamental porque nos permite
        conocer nuestras raíces y comprender la diversidad que existe
        en nuestra sociedad.

    </p>

    <p>

        Cada tradición, lengua, receta, canción, danza, historia,
        artesanía y celebración representa una parte importante de
        la identidad de una comunidad.

    </p>

    <p>

        Por esta razón debemos conocer, respetar y conservar las
        diferentes expresiones culturales para que también puedan
        ser conocidas por las futuras generaciones.

    </p>

</section>


<!-- =========================
     FOOTER
========================= -->

<footer>

    <h2 style="color:white;border:none;">
        🌎 Conocimiento Cultural
    </h2>

    <p>
        Proyecto escolar de conocimiento cultural
    </p>

    <p>
        © 2026
    </p>

</footer>


</body>

</html>
