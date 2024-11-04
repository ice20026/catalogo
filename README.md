# catalogo


<!DOCTYPE html>
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
            <option value="electronics">Electrónica</option>
            <option value="clothing">Ropa</option>
            <option value="books">Libros</option>
        </select>
    </div>
    <div class="catalog">
        <div class="item electronics">
            <img src="ruta/a/tu/imagen1.jpg" alt="Descripción de la imagen 1">
            <h3>Producto Electrónico 1</h3>
            <p>Descripción del producto electrónico 1.</p>
        </div>
        <div class="item clothing">
            <img src="ruta/a/tu/imagen2.jpg" alt="Descripción de la imagen 2">
            <h3>Producto de Ropa 1</h3>
            <p>Descripción del producto de ropa 1.</p>
        </div>
        <div class="item books">
            <img src="ruta/a/tu/imagen3.jpg" alt="Descripción de la imagen 3">
            <h3>Libro 1</h3>
            <p>Descripción del libro 1.</p>
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
