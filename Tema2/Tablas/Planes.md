# Tabla de planes de alojamiento web 
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Planes de alojamiento web</title>
    <style>
        table, td, th {
            border-collapse: collapse;
            border: 1px solid black;
            padding: 10px;
        }
        thead{
            background-color: rgb(14, 34, 56);
            color: white
        }
        th, td{
            text-align: center;
            border: 1px solid #9e9999;
        }
        tfoot{
            background-color: rgb(171, 247, 95);
        }
        tbody tr:nth-child(even){
            background-color: #e6f0ee;
        }
        tbody tr:nth-child(odd){
            background-color: #f3f7f6;
        }
        caption{
            font-weight: bold;
        }  
        tbody td:first-of-type{
            text-align: left;
        }
        table{
            width: 80%;
        }
        
    </style>
</head>
<body>
    <table>
    <caption>Planes de alojamiento web · NubeTorrent</caption>
    
    <thead>
        
        <tr>
            <th colspan="2" rowspan="2">Característica</th>
            <th colspan="3">Plan</th>
        </tr>
        <tr>
            <th>Básico</th>
            <th>Pro</th>
            <th>Business</th>
        </tr>
    </thead>
    <tbody>
        <tr>    
            <th rowspan="2">Recursos</th>
            <td>Espacio en disco</td>
            <td>10 GB</td>
            <td>50 GB</td>
            <td>200 GB</td>
        </tr>
        <tr>
            <td>Dominios</td>
            <td>1</td>
            <td>5</td>
            <td>Ilimitados</td>
        </tr>
        <tr>
            <th rowspan="2">Soporte</th>
            <td>Correo electrónico</td>
            <td style="color: green;">Sí</td>
            <td style="color: green;">Sí</td>
            <td style="color: green;">Sí</td>
        </tr>
        <tr>
            <td>Teléfono 24 h</td>
            <td style="color: red;">No</td>
            <td style="color: red;">No</td>
            <td style="color: green;">Sí</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <th colspan="2">Precio al mes</th>
            <td>3€</td>
            <td>9€</td>
            <td>19€</td>
        </tr>
        
    </tfoot>
</table>
</body>
</html>
```
