Link de la Pagina: 
https://tpkxttxx.github.io

<!DOCTYPE html>
<html>
<head>
    <title>My PHP App</title>
</head>
<body>
    <h1>Hello, this is my PHP App!</h1>

    <?php
    // Establecer conexión a la base de datos MySQL
    $conn = new mysqli(getenv('MYSQL_HOST'), getenv('MYSQL_USER'), getenv('MYSQL_PASSWORD'), getenv('MYSQL_DATABASE'));

    // Verificar la conexión
    if ($conn->connect_error) {
        die("Error de conexión a la base de datos: " . $conn->connect_error);
    }

    echo "<p>Conexión a la base de datos MySQL exitosa.</p>";

    // Cerrar la conexión
    $conn->close();
    ?>
</body>
</html>

