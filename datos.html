<?php
	require_once "conexion.php";
?>

<?php
	$inicio = $_GET['inicio'];
	$fin = $_GET['fin'];
?>

<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Datos historicos de accidentalidad en Medellín</title>
	<link rel="stylesheet" type="text/css" href="librerias/boostrap/css/boostrap.css">
	<script src="librerias/jquery-3.5.1.min.js"></script>
	<script src="librerias/plotly-latest.min.js"></script>
  </head>
  <link rel="stylesheet" href="style.css" />
  <body>
  
  <h1>Historico de datos desde el: <?php echo $inicio ?> hasta el: <?php echo $fin ?></h1>
  <div align="CENTER" height="100px">
  <table border="2" bgcolor="#FFFFFF" width="30%" style="font-size:25px">
	<tr class="headt">
		<td bgcolor="#BDCEE1" align="CENTER" height="50"><font size=5><b>CLASE</b></font></td>
		<td bgcolor="#BDCEE1" align="CENTER" height="50"><font size=5><b>CANTIDAD</b></font</td>
	</tr>
	<?php
	$sql="SELECT CLASE, sum(CANTIDAD) as CANTIDAD FROM accidente WHERE FECHA between '$inicio' and '$fin' group by CLASE order by CANTIDAD desc;";
	$result=mysqli_query($conexion,$sql);
	$valoresY=array();
	$valoresX=array();
	while($mostrar=mysqli_fetch_array($result)){
		$valoresX[]=$mostrar[0];
		$valoresY[]=$mostrar[1];
	?>
	<tr class="headt">
		<td height="50"><?php echo $mostrar['CLASE'] ?></td>
		<td align="CENTER"><?php echo $mostrar['CANTIDAD'] ?></td>
	</tr>
	<?php
	}
	$datosX=json_encode($valoresX);
	$datosY=json_encode($valoresY);
	?>
  </table>
  </div>
  <br><br>
  <div class="contiene">
	<div class="row">
		<div class="col-sm-12">
			<div class="panel panel-primary">
				<div class="panel panel-heading">
				</div>
				<div class="panel panel-body">
					<div id="cargaBarras">
						<div id="graficaBarras">
						</div>

					<script type="text/javascript">
						function crearCadenaBarras(json){
							var parsed = JSON.parse(json);
							var arr = [];
							for(var x in parsed){
								arr.push(parsed[x]);
							}
							return arr;
						}
					</script>	
					<script type="text/javascript">
					
						datosX=crearCadenaBarras('<?php echo $datosX ?>');
						datosY=crearCadenaBarras('<?php echo $datosY ?>');
						
						var trace1 = {
							type: 'bar',
							x: datosX,
							y: datosY,
							marker: {
								color: '#BDCEE1',
								line: {
									width: 2
								}
							}
						};

						var data = [ trace1 ];

						var layout = { 
							title: 'Accidentalidad en Medellín por tipo de accidente',
							font: {
								size: 18
								},
							xaxis:{
								tickangle: 0,
								title: 'Tipo de accidente'
							},
							yaxis:{
								zeroline: false,
								title: 'Número de accidentes'
							},
							bargap :0.2
						};
							
						var config = {responsive: true}

						Plotly.newPlot('graficaBarras', data, layout, config );
					</script>
					
					</div>
					
				</div>
			</div>
		</div>
	</div>
  </div>
  
  <br><br>
  <div class="center">
  <a href="historico.php"><input type="button" value="Regresar" style="width:170px; height:70px; FONT-SIZE: 20pt"></a>
  </div>
  
</body>
</html>

