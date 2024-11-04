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
            width: 200px;
            text-align: center;
            display: none; /* Ocultar por defecto */
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
        <label for="classFilter">Filtrar por clase:</label>
        <select id="classFilter" onchange="filterItems()">
            <option value="all">Todos</option>
            <option value="classA">cascos</option>
            <option value="classB">Clase B</option>
            <option value="classC">Clase C</option>
        </select>
    </div>
    <div class="catalog">
        <div class="item classA">
            <h3>Marca: yamaha</h3>
            <p>Modelo: black </p>
            <p>Cantidad: 10</p>
        </div>
        <div class="item classA">
            <h3>Marca: suzuki</h3>
            <p>Modelo: 90 te x</p>
            <p>Cantidad: 5</p>
        </div>
        <div class="item classA">
            <h3>Marca: serpento</h3>
            <p>Modelo: Focus 14</p>
            <p>Cantidad: 7</p>
        </div>
        <!-- Añade más elementos de catálogo aquí -->
    </div>
    <script>
        function filterItems() {
            var classFilter = document.getElementById("classFilter").value;
            var items = document.getElementsByClassName("item");
            for (var i = 0; i < items.length; i++) {
                if (classFilter === "all") {
                    items[i].style.display = "block";
                } else {
                    if (items[i].classList.contains(classFilter)) {
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




