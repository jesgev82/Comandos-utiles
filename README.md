# comandos-utiles 

pwd  📍 Dice en qué carpeta estás
ls  📄 Ve qls -la  📄 Todo, incluidos archivos ocultos 
 cd nombre  ⬅️ Entra a una carpeta 
 cd ..  ⬆️ Regresa a la carpeta de arriba 
 mkdir nombre  📁 Crea una carpeta nuevaué archivos hay aquí


nano archivo.txt  ✍️ Crea o edita un archivo (Ctrl+O guarda, Ctrl+X sale) 
 cat archivo.txt  👀 Muestra el contenido de un archivo 
 cp origen destino  📋 Copia un archivo 
 mv origen destino  🔄 Mueve o renombra un archivo 
 rm archivo  🗑️ Borra un archivo 
 rm -rf carpeta  ⚠️ Borra una carpeta y TODO lo que tiene

 ip a  🔍 Muestra tu dirección IP 
 ping 8.8.8.8  📶 Comprueba si tienes internet 
 nmap -sn 192.168.1.0/24  🔍 Ve qué dispositivos están en tu red 
 curl -L ejemplo.com  🌐 Descarga el contenido de una página

 pkg update && pkg upgrade  🔄 Actualiza todo en Termux 
 pkg install nombre  📦 Instala algo nuevo 
 sudo apt update && sudo apt upgrade  🔄 Actualiza todo en Kali 
 sudo apt install nombre  📦 Instala algo en Kali

 Ctrl + C  ✋ Detiene cualquier comando que esté corriendo 
 Ctrl + L  🧹 Limpia la pantalla 
 Flecha ↑ ↓  ⏮️ Vuelve a ver comandos que ya escribiste 
 Tab  ✅ Completa nombres automáticamente

[mi-dispositivo.html](https://github.com/user-attachments/files/34596622/mi-dispositivo.html)
 
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Información de mi Dispositivo</title>
<style>
body {
font-family: Arial, sans-serif;
max-width: 500px;
margin: 50px auto;
padding: 20px;
background: #f0f4f8;
}
h1 {
text-align: center;
color: #2d3748;
}
.dato {
background: white;
padding: 15px;
margin: 10px 0;
border-radius: 8px;
box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}
.etiqueta {
font-weight: bold;
color: #2b6cb0;
}
</style>
</head>
<body>

<h1>📱 Información de mi Dispositivo</h1>

<div class="dato">
<span class="etiqueta">Modelo/Dispositivo:</span>
<span id="modelo"></span>
</div>

<div class="dato">
<span class="etiqueta">Sistema Operativo:</span>
<span id="so"></span>
</div>

<div class="dato">
<span class="etiqueta">Navegador:</span>
<span id="navegador"></span>
</div>

<div class="dato">
<span class="etiqueta">Resolución de pantalla:</span>
<span id="pantalla"></span>
</div>

<div class="dato">
<span class="etiqueta">Idioma:</span>
<span id="idioma"></span>
</div>

<div class="dato">
<span class="etiqueta">Batería:</span>
<span id="bateria"></span>
</div>

<script>
// Mostrar información
document.getElementById("modelo").textContent = navigator.platform || "No disponible";
document.getElementById("so").textContent = navigator.appVersion;
document.getElementById("navegador").textContent = navigator.userAgent;
document.getElementById("pantalla").textContent = screen.width + " × " + screen.height + " píxeles";
document.getElementById("idioma").textContent = navigator.language;

// Mostrar batería
if (navigator.getBattery) {
navigator.getBattery().then(function(bateria) {
document.getElementById("bateria").textContent =
Math.round(bateria.level * 100) + "% " +
(bateria.charging ? "⚡ Cargando" : "🔋 Descargando");
});
} else {
document.getElementById("bateria").textContent = "No disponible en este navegador";
}
</script>

</body>
</html>
