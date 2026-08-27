```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>📸 Para May 🌷</title>

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            min-height: 100vh;
            font-family: "Segoe UI", Arial, sans-serif;
            background: linear-gradient(135deg, #ffd6e7, #ffc1d9, #ffe4ef);
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            color: #6d3150;
        }

        .contenedor {
            width: 95%;
            max-width: 700px;
            min-height: 90vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            position: relative;
        }

        h1 {
            font-size: 34px;
            margin-bottom: 10px;
            color: #a83f69;
            text-shadow: 0 2px 5px rgba(150, 50, 90, .15);
        }

        .subtitulo {
            font-size: 17px;
            margin-bottom: 10px;
            color: #8b4865;
        }

        /* RAMO */
        .ramo {
            position: relative;
            width: 470px;
            height: 430px;
            margin-top: 5px;
        }

        /* TALLOS */
        .tallo {
            position: absolute;
            width: 8px;
            height: 260px;
            background: linear-gradient(to right, #4d9b5c, #76bd70, #43894d);
            border-radius: 10px;
            bottom: 80px;
            left: 50%;
            transform-origin: bottom;
            box-shadow: 1px 2px 3px rgba(0,0,0,.15);
        }

        .tallo::after {
            content: "";
            position: absolute;
            width: 45px;
            height: 22px;
            background: #65aa62;
            border-radius: 100% 0 100% 0;
            top: 120px;
            left: -35px;
            transform: rotate(-25deg);
        }

        .tallo::before {
            content: "";
            position: absolute;
            width: 42px;
            height: 20px;
            background: #65aa62;
            border-radius: 0 100% 0 100%;
            top: 170px;
            right: -34px;
            transform: rotate(25deg);
        }

        .t1 { transform: rotate(-30deg); }
        .t2 { transform: rotate(-21deg); }
        .t3 { transform: rotate(-12deg); }
        .t4 { transform: rotate(-4deg); }
        .t5 { transform: rotate(5deg); }
        .t6 { transform: rotate(13deg); }
        .t7 { transform: rotate(22deg); }
        .t8 { transform: rotate(30deg); }

        /* FLORES */
        .flor {
            position: absolute;
            width: 85px;
            height: 85px;
            z-index: 3;
            animation: flotar 3s ease-in-out infinite;
        }

        /* Posiciones */
        .flor1 { left: 45px; top: 25px; }
        .flor2 { left: 105px; top: 80px; animation-delay: .2s; }
        .flor3 { left: 145px; top: 25px; animation-delay: .4s; }
        .flor4 { left: 190px; top: 80px; animation-delay: .6s; }
        .flor5 { left: 235px; top: 25px; animation-delay: .8s; }
        .flor6 { left: 280px; top: 80px; animation-delay: 1s; }
        .flor7 { left: 330px; top: 25px; animation-delay: 1.2s; }
        .flor8 { left: 375px; top: 80px; animation-delay: 1.4s; }

        /* TULIPÁN */
        .tulipan {
            position: relative;
            width: 75px;
            height: 75px;
        }

        .tulipan .petalo {
            position: absolute;
            bottom: 5px;
            width: 45px;
            height: 65px;
            background: linear-gradient(135deg, #ffffff, #f5edf2);
            border: 1px solid #eadde5;
            border-radius: 50% 50% 40% 40%;
            box-shadow: 0 4px 8px rgba(120,70,100,.12);
        }

        .tulipan .p1 {
            left: 0;
            transform: rotate(-18deg);
        }

        .tulipan .p2 {
            left: 16px;
            bottom: 0;
            height: 72px;
        }

        .tulipan .p3 {
            right: 0;
            transform: rotate(18deg);
        }

        /* GERBERA */
        .gerbera {
            position: relative;
            width: 82px;
            height: 82px;
        }

        .petalo-gerbera {
            position: absolute;
            left: 31px;
            top: 1px;
            width: 19px;
            height: 40px;
            background: linear-gradient(to bottom, #ff8fbc, #ed5e99);
            border-radius: 50% 50% 45% 45%;
            transform-origin: 9px 40px;
            box-shadow: 0 1px 2px rgba(160,50,100,.15);
        }

        .g1 { transform: rotate(0deg); }
        .g2 { transform: rotate(30deg); }
        .g3 { transform: rotate(60deg); }
        .g4 { transform: rotate(90deg); }
        .g5 { transform: rotate(120deg); }
        .g6 { transform: rotate(150deg); }
        .g7 { transform: rotate(180deg); }
        .g8 { transform: rotate(210deg); }
        .g9 { transform: rotate(240deg); }
        .g10 { transform: rotate(270deg); }
        .g11 { transform: rotate(300deg); }
        .g12 { transform: rotate(330deg); }

        .centro {
            position: absolute;
            width: 28px;
            height: 28px;
            background: radial-gradient(circle, #7d3d45, #4e252c);
            border-radius: 50%;
            left: 27px;
            top: 27px;
            z-index: 5;
            box-shadow: 0 2px 4px rgba(0,0,0,.2);
        }

        /* PAPEL DEL RAMO */
        .envoltura {
            position: absolute;
            bottom: 10px;
            left: 50%;
            transform: translateX(-50%);
            width: 300px;
            height: 170px;
            background: linear-gradient(135deg, #fff1f5, #ffd9e7);
            clip-path: polygon(8% 0, 92% 0, 100% 100%, 50% 80%, 0 100%);
            z-index: 4;
            filter: drop-shadow(0 7px 5px rgba(100,50,80,.18));
        }

        .cinta {
            position: absolute;
            bottom: 80px;
            left: 50%;
            transform: translateX(-50%);
            width: 75px;
            height: 45px;
            z-index: 7;
        }

        .cinta::before,
        .cinta::after {
            content: "";
            position: absolute;
            width: 35px;
            height: 35px;
            background: #e982a9;
            border-radius: 70% 10% 70% 10%;
            top: 0;
        }

        .cinta::before {
            left: 2px;
            transform: rotate(25deg);
        }

        .cinta::after {
            right: 2px;
            transform: rotate(65deg);
        }

        .nudo {
            position: absolute;
            width: 24px;
            height: 24px;
            background: #d95d8d;
            border-radius: 50%;
            left: 25px;
            top: 10px;
            z-index: 8;
        }

        /* BOTONES */
        button {
            border: none;
            padding: 15px 32px;
            border-radius: 30px;
            background: linear-gradient(135deg, #e85c91, #c83d76);
            color: white;
            font-size: 17px;
            font-weight: bold;
            cursor: pointer;
            box-shadow: 0 6px 15px rgba(190,50,110,.25);
            transition: .25s;
            margin-top: 8px;
        }

        button:hover {
            transform: translateY(-3px) scale(1.04);
            box-shadow: 0 9px 20px rgba(190,50,110,.35);
        }

        button:active {
            transform: scale(.96);
        }

        /* MENSAJES */
        .mensaje {
            display: none;
            animation: aparecer .7s ease;
        }

        .mensaje h2 {
            font-size: 38px;
            color: #a92d60;
            margin-bottom: 15px;
        }

        .mensaje p {
            font-size: 22px;
            color: #7d3a59;
            margin-bottom: 10px;
        }

        .final h2 {
            font-size: 36px;
        }

        .final p {
            font-size: 25px;
            font-weight: bold;
        }

        @keyframes flotar {
            0%, 100% {
                transform: translateY(0) rotate(0deg);
            }

            50% {
                transform: translateY(-7px) rotate(2deg);
            }
        }

        @keyframes aparecer {
            from {
                opacity: 0;
                transform: scale(.7) translateY(20px);
            }

            to {
                opacity: 1;
                transform: scale(1) translateY(0);
            }
        }

        /* CELULAR */
        @media (max-width: 600px) {

            h1 {
                font-size: 27px;
            }

            .subtitulo {
                font-size: 15px;
            }

            .ramo {
                transform: scale(.72);
                margin-top: -35px;
                margin-bottom: -35px;
            }

            .mensaje h2 {
                font-size: 30px;
            }

            .mensaje p {
                font-size: 19px;
            }

            .final h2 {
                font-size: 28px;
            }

            .final p {
                font-size: 21px;
            }
        }
    </style>
</head>

<body>

    <div class="contenedor">

        <!-- PANTALLA INICIAL -->
        <div id="inicio">

            <h1>🌷 Un pequeño detalle para ti 🌸</h1>

            <p class="subtitulo">
                He preparado algo especialmente para ti...
            </p>

            <div class="ramo">

                <!-- TALLOS -->
                <div class="tallo t1"></div>
                <div class="tallo t2"></div>
                <div class="tallo t3"></div>
                <div class="tallo t4"></div>
                <div class="tallo t5"></div>
                <div class="tallo t6"></div>
                <div class="tallo t7"></div>
                <div class="tallo t8"></div>

                <!-- TULIPÁN 1 -->
                <div class="flor flor1">
                    <div class="tulipan">
                        <div class="petalo p1"></div>
                        <div class="petalo p2"></div>
                        <div class="petalo p3"></div>
                    </div>
                </div>

                <!-- GERBERA 1 -->
                <div class="flor flor2">
                    <div class="gerbera">
                        <div class="petalo-gerbera g1"></div>
                        <div class="petalo-gerbera g2"></div>
                        <div class="petalo-gerbera g3"></div>
                        <div class="petalo-gerbera g4"></div>
                        <div class="petalo-gerbera g5"></div>
                        <div class="petalo-gerbera g6"></div>
                        <div class="petalo-gerbera g7"></div>
                        <div class="petalo-gerbera g8"></div>
                        <div class="petalo-gerbera g9"></div>
                        <div class="petalo-gerbera g10"></div>
                        <div class="petalo-gerbera g11"></div>
                        <div class="petalo-gerbera g12"></div>
                        <div class="centro"></div>
                    </div>
                </div>

                <!-- TULIPÁN 2 -->
                <div class="flor flor3">
                    <div class="tulipan">
                        <div class="petalo p1"></div>
                        <div class="petalo p2"></div>
                        <div class="petalo p3"></div>
                    </div>
                </div>

                <!-- GERBERA 2 -->
                <div class="flor flor4">
                    <div class="gerbera">
                        <div class="petalo-gerbera g1"></div>
                        <div class="petalo-gerbera g2"></div>
                        <div class="petalo-gerbera g3"></div>
                        <div class="petalo-gerbera g4"></div>
                        <div class="petalo-gerbera g5"></div>
                        <div class="petalo-gerbera g6"></div>
                        <div class="petalo-gerbera g7"></div>
                        <div class="petalo-gerbera g8"></div>
                        <div class="petalo-gerbera g9"></div>
                        <div class="petalo-gerbera g10"></div>
                        <div class="petalo-gerbera g11"></div>
                        <div class="petalo-gerbera g12"></div>
                        <div class="centro"></div>
                    </div>
                </div>

                <!-- TULIPÁN 3 -->
                <div class="flor flor5">
                    <div class="tulipan">
                        <div class="petalo p1"></div>
                        <div class="petalo p2"></div>
                        <div class="petalo p3"></div>
                    </div>
                </div>

                <!-- GERBERA 3 -->
                <div class="flor flor6">
                    <div class="gerbera">
                        <div class="petalo-gerbera g1"></div>
                        <div class="petalo-gerbera g2"></div>
                        <div class="petalo-gerbera g3"></div>
                        <div class="petalo-gerbera g4"></div>
                        <div class="petalo-gerbera g5"></div>
                        <div class="petalo-gerbera g6"></div>
                        <div class="petalo-gerbera g7"></div>
                        <div class="petalo-gerbera g8"></div>
                        <div class="petalo-gerbera g9"></div>
                        <div class="petalo-gerbera g10"></div>
                        <div class="petalo-gerbera g11"></div>
                        <div class="petalo-gerbera g12"></div>
                        <div class="centro"></div>
                    </div>
                </div>

                <!-- TULIPÁN 4 -->
                <div class="flor flor7">
                    <div class="tulipan">
                        <div class="petalo p1"></div>
                        <div class="petalo p2"></div>
                        <div class="petalo p3"></div>
                    </div>
                </div>

                <!-- GERBERA 4 -->
                <div class="flor flor8">
                    <div class="gerbera">
                        <div class="petalo-gerbera g1"></div>
                        <div class="petalo-gerbera g2"></div>
                        <div class="petalo-gerbera g3"></div>
                        <div class="petalo-gerbera g4"></div>
                        <div class="petalo-gerbera g5"></div>
                        <div class="petalo-gerbera g6"></div>
                        <div class="petalo-gerbera g7"></div>
                        <div class="petalo-gerbera g8"></div>
                        <div class="petalo-gerbera g9"></div>
                        <div class="petalo-gerbera g10"></div>
                        <div class="petalo-gerbera g11"></div>
                        <div class="petalo-gerbera g12"></div>
                        <div class="centro"></div>
                    </div>
                </div>

                <!-- ENVOLTURA -->
                <div class="envoltura"></div>

                <!-- CINTA -->
                <div class="cinta">
                    <div class="nudo"></div>
                </div>

            </div>

            <button onclick="primerMensaje()">
                🌷 Presióname 🌷
            </button>

        </div>


        <!-- PRIMER MENSAJE -->
        <div id="mensaje1" class="mensaje">

            <h2>Me caes mal</h2>

            <p>
                Bueno... eso era lo que quería decirte...
            </p>

            <button onclick="segundoMensaje()">
                Presiona otra vez
            </button>

        </div>


        <!-- MENSAJE FINAL -->
        <div id="mensaje2" class="mensaje final">

            <h2>¡BROMITA CIBERNÉTICA!</h2>

            <p>
                🌸May, me caes súper bien🌸
            </p>

            <p>
                🌷🌸🌷🌸🌷🌸🌷🌸
            </p>

        </div>

    </div>


    <script>

        function primerMensaje() {

            document.getElementById("inicio").style.display = "none";

            document.getElementById("mensaje1").style.display = "block";

        }


        function segundoMensaje() {

            document.getElementById("mensaje1").style.display = "none";

            document.getElementById("mensaje2").style.display = "block";

        }

    </script>

</body>
</html>
```
