<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<link rel="preconnect" href="https://fonts.gstatic.com">
	<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet"> 
	<link rel="stylesheet" href="css/estilos.css">
	<link rel="stylesheet" href="css/buscador.css">
	<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css"/>
	<title>Cancionero IATec</title>
	<script src="https://cdn.lordicon.com/xdjxvujz.js"></script>
</head>
<body>
	<main>
		<h1 class="titulo"> 
			<img src="img/logoIATec.png" width="80px" alt="">
			<br>Cancionero <br> IATec</h1>
		<div class="buscador">
			<div class="search-box">
				<input type="text" placeholder="Busquemos..">
				<div class="search-icon">
				  <i class="fas fa-search"></i>
				</div>
				  <div class="cancel-icon">
				  <i class="fas fa-times"></i>
				</div>
				  <div class="search-data">
				 </div>
			</div>
		</div>
		<h5 class="subTitulo">Encuentra Canticos e Himnos Adventistas</h5>
	  <script>
			const searchBox = document.querySelector(".search-box");
			const searchBtn = document.querySelector(".search-icon");
			const cancelBtn = document.querySelector(".cancel-icon");
			const searchInput = document.querySelector("input");
			const searchData = document.querySelector(".search-data");
			searchBtn.onclick =()=>{
			  searchBox.classList.add("active");
			  searchBtn.classList.add("active");
			  searchInput.classList.add("active");
			  cancelBtn.classList.add("active");
			  searchInput.focus();
			  if(searchInput.value != ""){
				var values = searchInput.value;
				searchData.classList.remove("active");
				// searchData.innerHTML = "You just typed " + "<span style='font-weight: 500;'>" + values + "</span>";
			  }else{
				searchData.textContent = "";
			  }
			}
			cancelBtn.onclick =()=>{
			  searchBox.classList.remove("active");
			  searchBtn.classList.remove("active");
			  searchInput.classList.remove("active");
			  cancelBtn.classList.remove("active");
			  searchData.classList.toggle("active");
			  searchInput.value = "";
			}
		  </script>
		<div class="categorias" id="categorias">
			<div class="categoria activa" data-categoria="himnario">
				<lord-icon
					src="https://cdn.lordicon.com/mmspidej.json"
					trigger="loop"
					colors="primary:#545454,secondary:#16a9c7"
					style="width:80px;height:80px">
				</lord-icon>
				<p>Himnario</p>
			</div>
			<div class="categoria" data-categoria="canticos">
				<lord-icon
					src="https://cdn.lordicon.com/vnxmkidq.json"
					trigger="loop"
					colors="primary:#545454,secondary:#16a9c7"
					style="width:80px;height:80px">
				</lord-icon>
				<p>Canticos</p>
			</div>
			<div class="categoria" data-categoria="acordes">
				<lord-icon
					src="https://cdn.lordicon.com/xqndcrvb.json"
					trigger="loop"
					colors="primary:#545454,secondary:#16a9c7"
					style="width:80px;height:80px">
				</lord-icon>
				<p>Acordes</p>
			</div>
			<div class="categoria" data-categoria="videos">
				<lord-icon
					src="https://cdn.lordicon.com/tdxypxgp.json"
					trigger="loop"
					colors="primary:#545454,secondary:#16a9c7"
					style="width:80px;height:80px">
				</lord-icon>
				<p>Videos</p>
			</div>
		</div>
		<!-- <h1 class="titulo"> 
			<br>Cancionero <br> IATec</h1> -->
		<div class="preguntas">

			<!-- Himnario -->
			<div class="contenedor-preguntas activo" data-categoria="himnario">
				<div class="contenedor-pregunta">
					<p class="pregunta">1. Cantad Alegres <img src="./img/suma.svg" alt="Abrir Respuesta" /></p>
					<p class="respuesta">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptatum laborum porro voluptates, sequi aliquam mollitia! <br><br>  Nostrum eius iure sapiente, voluptates soluta adipisci, perferendis voluptatibus eligendi vel saepe harum. Consectetur, doloribus.adipisicing elit.</p>
				</div>
				<div class="contenedor-pregunta">
					<p class="pregunta">61. Santo Santo <img src="./img/suma.svg" alt="Abrir Respuesta" /></p>
					<p class="respuesta">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptatum laborum porro voluptates, sequi aliquam mollitia! <br><br>  Nostrum eius iure sapiente, voluptates soluta adipisci, perferendis voluptatibus eligendi vel saepe harum. Consectetur, doloribus.adipisicing elit.</p>
				</div>
			</div>

			<!-- Canticos -->
			<div class="contenedor-preguntas" data-categoria="canticos">
				<div class="contenedor-pregunta">
					<p class="pregunta">Lado a lado estoy<img src="./img/suma.svg" alt="Abrir Respuesta" /></p>
					<p class="respuesta">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptatum laborum porro voluptates, sequi aliquam mollitia! <br><br>  Nostrum eius iure sapiente, voluptates soluta adipisci, perferendis voluptatibus eligendi vel saepe harum. Consectetur, doloribus.adipisicing elit.</p>
				</div>
				<div class="contenedor-pregunta">
					<p class="pregunta">Al son del cocodrilo <img src="./img/suma.svg" alt="Abrir Respuesta" /></p>
					<p class="respuesta">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptatum laborum porro voluptates, sequi aliquam mollitia! <br><br>  Nostrum eius iure sapiente, voluptates soluta adipisci, perferendis voluptatibus eligendi vel saepe harum. Consectetur, doloribus.adipisicing elit.</p>
				</div>
			</div>

			<!-- Acordes -->
			<div class="contenedor-preguntas" data-categoria="acordes">
				<div class="contenedor-pregunta">
					<p class="pregunta">Guitarra<img src="./img/suma.svg" alt="Abrir Respuesta" /></p>
					<p class="respuesta">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptatum laborum porro voluptates, sequi aliquam mollitia! Nostrum eius iure sapiente, voluptates soluta adipisci, perferendis voluptatibus eligendi vel saepe harum. Consectetur, doloribus.adipisicing elit. Voluptatum laborum porro voluptates, sequi aliquam mollitia! Nostrum eius iure sapiente, voluptates soluta adipisci, perferendis voluptatibus eligendi vel saepe harum. Consectetur, doloribus.adipisicing elit. Voluptatum laborum porro voluptates, sequi aliquam mollitia! Nostrum eius iure sapiente, voluptates soluta adipisci, perferendis voluptatibus eligendi vel saepe harum. Consectetur, doloribus.</p>
				</div>
				<div class="contenedor-pregunta">
					<p class="pregunta">Ukulele <img src="./img/suma.svg" alt="Abrir Respuesta" /></p>
					<p class="respuesta">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptatum laborum porro voluptates, sequi aliquam mollitia! Nostrum eius iure sapiente, voluptates soluta adipisci, perferendis voluptatibus eligendi vel saepe harum. Consectetur, doloribus.adipisicing elit. Voluptatum laborum porro voluptates, sequi aliquam mollitia! Nostrum eius iure sapiente, voluptates soluta adipisci, perferendis voluptatibus eligendi vel saepe harum. Consectetur, doloribus.</p>
				</div>
			</div>

			<!-- Videos -->
			<div class="contenedor-preguntas" data-categoria="videos">
				<div class="contenedor-pregunta">
					<p class="pregunta">Video 1 <img src="./img/suma.svg" alt="Abrir Respuesta" /></p>
					<p class="respuesta">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptatum laborum porro voluptates, sequi aliquam mollitia! Nostrum eius iure sapiente, voluptates soluta adipisci, perferendis voluptatibus eligendi vel saepe harum. Consectetur, doloribus.adipisicing elit. Voluptatum laborum porro voluptates, sequi aliquam mollitia! Nostrum eius iure sapiente, voluptates soluta adipisci, perferendis voluptatibus eligendi vel saepe harum. Consectetur, doloribus.adipisicing elit. Voluptatum laborum porro voluptates, sequi aliquam mollitia! Nostrum eius iure sapiente, voluptates soluta adipisci, perferendis voluptatibus eligendi vel saepe harum. Consectetur, doloribus.</p>
				</div>
				<div class="contenedor-pregunta">
					<p class="pregunta">Video 2 <img src="./img/suma.svg" alt="Abrir Respuesta" /></p>
					<p class="respuesta">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptatum laborum porro voluptates, sequi aliquam mollitia! Nostrum eius iure sapiente, voluptates soluta adipisci, perferendis voluptatibus eligendi vel saepe harum. Consectetur, doloribus.adipisicing elit. Voluptatum laborum porro voluptates, sequi aliquam mollitia! Nostrum eius iure sapiente, voluptates soluta adipisci, perferendis voluptatibus eligendi vel saepe harum. Consectetur, doloribus.</p>
				</div>
			</div>




		</div>
	</main>

	<script src="js/categorias.js"></script>
	<script src="js/preguntasFrecuentes.js"></script>
</body>
</html>