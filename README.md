# catalogo



<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Catálogo con Filtros</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            margin: 0;
            padding: 20px;
        }
        .catalog {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
        }
        .item {
            background-color: white;
            margin: 10px;
            padding: 10px;
            border-radius: 5px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            max-width: 200px;
            text-align: center;
            display: none; /* Ocultar por defecto */
        }
        .item img {
            max-width: 100%;
            border-radius: 5px;
        }
        .item h3 {
            font-size: 18px;
            margin: 10px 0;
        }
        .item p {
            font-size: 14px;
            color: #666;
        }
        .filter {
            margin-bottom: 20px;
            text-align: center;
        }
        .filter select {
            padding: 10px;
            font-size: 16px;
        }
    </style>
</head>
<body>
    <div class="filter">
        <label for="category">Filtrar por categoría:</label>
        <select id="category" onchange="filterItems()">
            <option value="all">Todos</option>
            <option value="electronics">cascos</option>
            <option value="clothing">guantes</option>
            <option value="books">llantas</option>
                <option value="books">accesorio</option>
        </select>
    </div>
    <div class="catalog">
        <div class="item electronics">
            <img src="1.jpg" alt="Descripción de la imagen 1">
            <h3>accesorio de moto  </h3>
            <p>accesorio.</p>
        </div>
        <div class="item clothing">
            <img src="2.jpg" alt="Descripción de la imagen 2">
            <h3>accesorio de moto  </h3>
            <p>acessorio.</p>
        </div>
        <div class="item books">
            <img src="3.jpg" alt="Descripción de la imagen 3">
            <h3>accesorio de moto</h3>
            <p>accesorio</p>
        </div>
 <div class="item books">
            <img src="3.jpg" alt="Descripción de la imagen 3">
            <h3>accesorio de moto</h3>
            <p>accesorio</p>
        </div>
 <div class="item books">
            <img src="3.jpg" alt="Descripción de la imagen 3">
            <h3>accesorio de moto</h3>
            <p>accesorio</p>
        </div>

 <div class="item books">
            <img src="3.jpg" alt="Descripción de la imagen 3">
            <h3>accesorio de moto</h3>
            <p>accesorio</p>
        </div>
 <div class="item books">
            <img src="3.jpg" alt="Descripción de la imagen 3">
            <h3>accesorio de moto</h3>
            <p>accesorio</p>
        </div>
        <!-- Añade más elementos de catálogo aquí -->
    </div>
    <script>
        function filterItems() {
            var category = document.getElementById("category").value;
            var items = document.getElementsByClassName("item");
            for (var i = 0; i < items.length; i++) {
                if (category === "all") {
                    items[i].style.display = "block";
                } else {
                    if (items[i].classList.contains(category)) {
                        items[i].style.display = "block";
                    } else {
                        items[i].style.display = "none";
                    }
                }
            }
        }
    // Mostrar todos los elementos por defecto
        filterItems();
    </script>
</body>
</html>



<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Imagen de Fondo</title>
    <style>
        body {
            background-image: url('ruta/a/tu/imagen.jpg'); /* Imagen de fondo */
            background-size: cover; /* Ajusta la imagen para cubrir toda la pantalla */
            background-position: center; /* Centra la imagen */
            background-repeat: no-repeat; /* Evita que la imagen se repita */
            margin: 0;
            font-family: Arial, sans-serif;
        }
    </style>
</head>
<body>
    <h1>¡Hola Mundo!</h1>
    <p>Este es un ejemplo de una página con una imagen de fondo.</p>
</body>
</html>




