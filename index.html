<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NoisyBoy Control</title>
    <style>
        body { font-family: Arial, sans-serif; background-color: #f0f0f0; text-align: center; margin: 0; }
        .header { background: #3f51b5; color: white; padding: 15px; font-size: 20px; }
        .status { margin: 10px; color: #555; }
        
        /* Contenedor de flechas */
        .joystick-container {
            display: grid;
            grid-template-areas: ". up ." "left stop right" ". down .";
            gap: 10px;
            justify-content: center;
            margin-top: 20px;
        }
        
        button {
            border: none; border-radius: 8px; color: white; cursor: pointer;
            font-weight: bold; font-size: 16px; user-select: none;
        }

        .btn-move { background: #e67e22; width: 80px; height: 100px; border-radius: 15px; }
        .btn-stop-main { background: #4caf50; width: 100px; height: 100px; border-radius: 50%; grid-area: stop; }
        
        .up { grid-area: up; } .down { grid-area: down; }
        .left { grid-area: left; } .right { grid-area: right; }

        /* Controles Sierra */
        .sierra-container { margin-top: 30px; display: flex; justify-content: center; gap: 20px; }
        .btn-boot { background: #00bcd4; width: 100px; height: 50px; }
        .btn-stop-sierra { background: #9c27b0; width: 100px; height: 50px; }
        
        .connect-btn { background: #444; padding: 10px 20px; margin-top: 20px; }
    </style>
</head>
<body>

    <div class="header">Pantalla de Control - NoisyBoy</div>
    
    <button class="connect-btn" onclick="conectarBT()">🔗 Conectar Bluetooth</button>
    <div class="status" id="status">Estado: Desconectado</div>

    <div class="joystick-container">
        <button class="btn-move up" onmousedown="enviar('f')" onmouseup="enviar('s')" ontouchstart="enviar('f')" ontouchend="enviar('s')">▲</button>
        <button class="btn-move left" onmousedown="enviar('l')" onmouseup="enviar('s')" ontouchstart="enviar('l')" ontouchend="enviar('s')">◀</button>
        <button class="btn-stop-main" onclick="enviar('s')">STOP</button>
        <button class="btn-move right" onmousedown="enviar('r')" onmouseup="enviar('s')" ontouchstart="enviar('r')" ontouchend="enviar('s')">▶</button>
        <button class="btn-move down" onmousedown="enviar('b')" onmouseup="enviar('s')" ontouchstart="enviar('b')" ontouchend="enviar('s')">▼</button>
    </div>

    <div class="sierra-container">
        <button class="btn-boot" onclick="enviar('p')">BOOT (ON)</button>
        <button class="btn-stop-sierra" onclick="enviar('a')">STOP (OFF)</button>
    </div>

    <script>
        let caracteristicaBT = null;

        async function conectarBT() {
            try {
                const dispositivo = await navigator.bluetooth.requestDevice({
                    filters: [{ name: 'NoisyBoy' }],
                    optionalServices: ['00001101-0000-1000-8000-00805f9b34fb'] // UUID estándar Serial Port
                });
                
                const servidor = await dispositivo.gatt.connect();
                const servicio = await servidor.getPrimaryService('00001101-0000-1000-8000-00805f9b34fb');
                caracteristicaBT = await servicio.getCharacteristic('00001101-0000-1000-8000-00805f9b34fb');
                
                document.getElementById('status').innerText = "Estado: Conectado a NoisyBoy";
            } catch (error) {
                console.log("Error: " + error);
                alert("Asegúrate de usar HTTPS o localhost y que el Bluetooth esté activo.");
            }
        }

        async function enviar(comando) {
            if (caracteristicaBT) {
                const encoder = new TextEncoder();
                await caracteristicaBT.writeValue(encoder.encode(comando));
            } else {
                console.log("No conectado. Comando: " + comando);
            }
        }
    </script>
</body>
</html>
