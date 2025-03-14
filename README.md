<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Servicios Dentales - Dental Clinic Plus</title>
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            background-color: #f8f9fa;
            margin: 0;
            padding: 0;
        }
        .container {
            width: 90%;
            margin: auto;
            overflow: hidden;
        }
        .header {
            background: linear-gradient(90deg, #007bff, #00c6ff);
            color: #fff;
            padding: 20px 0;
            text-align: center;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .header h1 {
            margin: 0;
            font-size: 2.5em;
            letter-spacing: 1px;
        }
        .services {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            margin: 20px 0;
        }
        .service {
            background: #fff;
            border: 1px solid #ddd;
            border-radius: 10px;
            margin: 10px;
            padding: 20px;
            text-align: center;
            width: calc(30% - 20px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
            display: flex;
            flex-direction: column;
            align-items: center;
            position: relative;
            cursor: pointer;
        }
        .service .icon {
            font-size: 3em;
            color: #007bff;
            margin-bottom: 10px;
            animation: float 4s ease-in-out infinite;
        }
        .service h2 {
            margin: 10px 0;
            color: #007bff;
            font-size: 1.5em;
        }
        .service p {
            color: #555;
            margin: 5px 0;
            word-wrap: break-word;
            font-size: 1.1em;
        }
        .service:hover {
            transform: translateY(-10px);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
        }
        .tooltip {
            display: none;
            position: absolute;
            top: -130px;
            left: 50%;
            transform: translateX(-50%);
            background-color: rgba(0, 0, 0, 0.8);
            color: #fff;
            text-align: center;
            border-radius: 10px;
            padding: 15px;
            font-size: 1em;
            width: 100%;
            max-width: 250px;
            z-index: 1;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            pointer-events: none;
        }
        .footer {
            background: linear-gradient(90deg, #007bff, #00c6ff);
            color: #fff;
            text-align: center;
            padding: 20px 0;
            margin-top: 20px;
            box-shadow: 0 -4px 8px rgba(0, 0, 0, 0.1);
        }
        @keyframes float {
            0% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-10px);
            }
            100% {
                transform: translateY(0);
            }
        }
    </style>
    <!-- Link to Font Awesome for icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- Link to Google Fonts for custom fonts -->
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap">
    <script>
        document.addEventListener("DOMContentLoaded", function() {
            var services = document.querySelectorAll('.service');
            document.addEventListener('click', function(e) {
                services.forEach(function(service) {
                    var tooltip = service.querySelector('.tooltip');
                    tooltip.style.display = 'none';
                });
            });
            services.forEach(function(service) {
                service.addEventListener('click', function(e) {
                    e.stopPropagation();
                    var tooltip = service.querySelector('.tooltip');
                    if (tooltip.style.display === 'block') {
                        tooltip.style.display = 'none';
                    } else {
                        var allTooltips = document.querySelectorAll('.tooltip');
                        allTooltips.forEach(function(t) {
                            t.style.display = 'none';
                        });
                        tooltip.style.display = 'block';
                    }
                });
            });
        });
    </script>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>¡Tu sonrisa en las mejores manos! 😊</h1>
        </div>
        <div class="services">
            <div class="service">
                <i class="fas fa-tooth icon"></i>
                <h2>Inspección y Diagnóstico</h2>
                <p>500 CUP</p>
                <p>(Si realizas algún procedimiento, solo se cobra el valor del mismo)</p>
                <div class="tooltip">Se realiza una inspección detallada de tu salud bucal y diagnóstico de posibles problemas.</div>
            </div>
            <div class="service">
                <i class="fas fa-tooth icon"></i>
                <h2>Restauración de Diente</h2>
                <p>1,250 CUP</p>
                <div class="tooltip">Reparación y restauración de dientes dañados para devolverles su funcionalidad y estética.</div>
            </div>
            <div class="service">
                <i class="fas fa-tooth icon"></i>
                <h2>Restauración de Diente con Anestesia</h2>
                <p>1,750 CUP</p>
                <div class="tooltip">Procedimiento similar a la restauración de diente, pero con el uso de anestesia para mayor comodidad.</div>
            </div>
            <div class="service">
                <i class="fas fa-tooth icon"></i>
                <h2>Restauración de Muela con Resina (Blanco)</h2>
                <p>1,500 CUP</p>
                <div class="tooltip">Restauración de muelas usando resina blanca para una apariencia más natural.</div>
            </div>
            <div class="service">
                <i class="fas fa-tooth icon"></i>
                <h2>Restauración de Muela con Anestesia</h2>
                <p>2,000 CUP</p>
                <div class="tooltip">Restauración de muelas con resina blanca y uso de anestesia para mayor confort.</div>
            </div>
            <div class="service">
                <i class="fas fa-tooth icon"></i>
                <h2>Cambio de Amalgama por Resina</h2>
                <p>1,500 CUP</p>
                <div class="tooltip">Sustitución de empastes oscuros por resina blanca para una mejor estética.</div>
            </div>
            <div class="service">
                <i class="fas fa-tooth icon"></i>
                <h2>Reconstrucción de Dientes o Muelas</h2>
                <p>3,000 CUP</p>
                <p>(Mitad o más de la mitad)</p>
                <div class="tooltip">Reparación extensa de dientes o muelas que han sufrido daño significativo.</div>
            </div>
            <div class="service">
                <i class="fas fa-tooth icon"></i>
                <h2>Limpieza Dental</h2>
                <p>1,250 CUP</p>
                <div class="tooltip">Limpieza profesional para eliminar placa, sarro y mantener una salud bucal óptima.</div>
            </div>
            <div class="service">
                <i class="fas fa-tooth icon"></i>
                <h2>Aclaramiento Dental</h2>
                <p>3,000 CUP</p>
                <div class="tooltip">Tratamiento para blanquear los dientes y mejorar la estética de tu sonrisa.</div>
            </div>
        </div>
        <div class="footer">
            <p>Radicamos en el municipio Moa, provincia Holguín</p>
            <p>¡Agenda tu cita hoy mismo!</p>
            <p>Déjanos tu Nombre, Apellidos y número de teléfono para agendarte una cita.</p>
        </div>
    </div>
</body>
</html>
