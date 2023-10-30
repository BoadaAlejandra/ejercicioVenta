
<center><h3>Ejercicio venta Sarafa</h3></center>
<?php
$cliente = "Pepito";
$productos = "Atun lomitos";
$canti = 13.20;
$precio = 60.52;
$subTot = $canti * $precio;
$iva = $subTot * 0.12;
$desc = 0;
$regalo = "0";
if ($subTot <= 50) {
    $desc = $subTot * 0.5;
    $regalo = "mochila";
} else {
    if ($subTot <= 51 && $subTot >= 100) {
        $desc = $subTot * 0.7;
        $regalo = "guantes";
    } else {
        if ($subTot <= 101 && $subTot >= 200) {
            $desc = $subTot * 0.10;
            $regalo = "colores";
        } else {
            if ($subTot > 200) {
                $desc = $subTot * 0.15;
                $regalo = "perro";
            }
        }
    }
}
$totpagar = $subTot + $iva + $desc;
?>
<h2><label>***Resultados***</label><br></h2>
<label> Cliente :</label> <?php echo number_format($precio,2); ?><br>
<label> Productos :</label> <?php echo $productos; ?><br>
<label> Precio :</label> <?php echo $precio; ?><br>
<label> Cantidad :</label> <?php echo $canti; ?><br>
<label> Regalo :</label> <?php echo $regalo; ?><br>
<label> total a pagar :</label> <?php echo $subTot; ?><br># ejercicioVenta
