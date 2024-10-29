<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registro de Respuesta</title>
    <script>
        async function registrarRespuesta() {
            const respuesta = document.getElementById('respuesta').value;

            // Aquí deberías agregar la lógica para enviar la respuesta a tu hoja de cálculo
            // Por ejemplo, usando fetch para llamar a un endpoint de tu backend
            const response = await fetch('URL_DE_TU_BACKEND', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json'
                },
                body: JSON.stringify({ respuesta })
            });

            if (response.ok) {
                alert('Respuesta registrada correctamente.');
            } else {
                alert('Error al registrar la respuesta.');
            }
        }
    </script>
</head>
<body>
    <h1>Formulario de Registro</h1>
    <input type="text" id="respuesta" placeholder="Ingresa tu respuesta aquí">
    <button onclick="registrarRespuesta()">Enviar</button>
</body>
</html>
