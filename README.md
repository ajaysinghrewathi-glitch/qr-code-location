[index.html](https://github.com/user-attachments/files/24158898/index.html)
<!DOCTYPE html>
<html>
<head>
  <title>QR Test</title>
</head>
<body>

<h2>QR Code Scan Test</h2>

<button onclick="getLocation()">Location Lo</button>
<button onclick="openCamera()">Camera Open</button>

<p id="loc"></p>

<script>
function getLocation() {
  navigator.geolocation.getCurrentPosition(function(pos){
    document.getElementById("loc").innerHTML =
    "Latitude: " + pos.coords.latitude + "<br>Longitude: " + pos.coords.longitude;
  });
}

function openCamera(){
  navigator.mediaDevices.getUserMedia({ video:true })
  .then(stream => alert("Camera open ho gaya"))
  .catch(err => alert("Camera error"));
}
</script>

</body>
</html>
