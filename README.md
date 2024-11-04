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
            <option value="classB">llantas</option>
            <option value="classC">guantes C</option>
             <option value="classD">accesorioC</option>
        </select>
    </div>
    <div class="catalog">
        <div class="item classA">
            <h3>Marca: yamaha</h3>
            <p>Modelo: black </p>
            <p>Cantidad: 10</p>
              <p>precio : 300</p>
        </div>
        <div class="item classA">
            <h3>Marca: suzuki</h3>
            <p>Modelo: 90 te x</p>
            <p>Cantidad: 5</p>
              <p>precio : 300</p>
        </div>
        <div class="item classA">
            <h3>Marca: serpento</h3>
            <p>Modelo: Focus 14</p>
            <p>Cantidad: 7</p>
             <p>precio : 300</p>
        </div>
 <div class="item classA">
            <h3>Marca: serpento</h3>
            <p>Modelo: extreme 14</p>
            <p>Cantidad: 14</p>
      <p>precio : 500</p>
        </div>
        <div class="item classA">
            <h3>Marca: yamaha</h3>
            <p>Modelo: c90</p>
            <p>Cantidad: 14</p>
            <p>precio : 700</p> 
        </div>
<div class="item classA">
            <h3>Marca: suzuki</h3>
            <p>Modelo: serie sport</p>
            <p>Cantidad: 14</p>
     <p>precio : 360</p>
        </div> 
        <div class="item classA">
            <h3>Marca: serpento</h3>
            <p>Modelo: xxx 15</p>
            <p>Cantidad: 16</p>
             <p>precio : 600</p>
        </div>
   <div class="item classB">
            <h3>Marca : yamaha</h3>
            <p>Modelo: anti derrape </p>
            <p>Cantidad: 16</p>
             <p>precio : 900</p>
        </div>
  <div class="item classB">
            <h3>Marca: suzuki</h3>
            <p>Modelo: sport racing </p>
            <p>Cantidad: 16</p>
             <p>precio : 600</p>
        </div>
  <div class="item classB">
            <h3>Marca: serpento</h3>
            <p>Modelo: lluvia</p>
            <p>Cantidad: 16</p>
             <p>precio : 600</p>
        </div>
  <div class="item classB">
            <h3>Marca: serpento</h3>
            <p>Modelo: xxx 15</p>
            <p>Cantidad: 16</p>
             <p>precio : 600</p>
        </div>
  <div class="item classB">
            <h3>Marca: tornado </h3>
            <p>Modelo: c90</p>
            <p>Cantidad: 16</p>
             <p>precio : 1000</p>
        </div>
  <div class="item classB">
            <h3>Marca: pulsar</h3>
            <p>Modelo: pulsar 890</p>
            <p>Cantidad: 16</p>
             <p>precio : 6000</p>
        </div>
 <div class="item classC">
            <h3>Marca: guantes</h3>
            <p>Modelo: cueron</p>
            <p>Cantidad: 16</p>
             <p>precio : 90</p>
        </div>
 <div class="item classC">
            <h3>Marca: guantes</h3>
            <p>Modelo: goma</p>
            <p>Cantidad: 86</p>
             <p>precio : 90</p>
        </div>
 <div class="item classC">
            <h3>Marca: guantes</h3>
            <p>Modelo: yamaha 90 classic</p>
            <p>Cantidad: 16</p>
             <p>precio : 90</p>
        </div>
 <div class="item classC">
            <h3>Marca: guantes</h3>
            <p>Modelo: suzuki classic</p>
            <p>Cantidad: 16</p>
             <p>precio : 100</p>
        </div>
 <div class="item classD">
            <h3>Marca: yamaha</h3>
            <p>Modelo: x90 </p>
            <p>luces  </p>
             <p>precio : 100</p>
        </div>
<div class="item classD">
            <h3>Marca: suzuki</h3>
            <p>Modelo: x90 </p>
            <p> frenos  </p>
             <p>precio : 100</p>
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




