<!DOCTYPE html>
<html>
<head><title>script html</title></head>
<body onload="generar()">
<form>
<div id="prueba">
</div>
</form>
</body>
</html>
<script>
function generar()
{
    var contenido="";
	    contenido+="<h1 ><img src='uleam.png'>  Inscripciones para el curso de conduccion </h1> "
        contenido+=" <label for='cedula'>cedula*</label> <input type='text' name='cedula'id='cedula'placeholder='999999999-9'/required pattern='([/0-9/-]{11})'> <br>";
		contenido+="<label for='apellidos'>apellidos*</label> <input type='text' name='apellidos' id='apellidos'placeholder='APELLIDOS MAY'required pattern='([A-Z ]{5,20})'/> <br>"
		contenido+="<label for='nombres'>nombres*</label> <input type='text' name='nombres' id='nombres'placeholder='NOMBRES MAY'required pattern='([A-Z ]{5,20})'/> <br>"
		contenido+="<label for='email'>email*</label> <input type='email' name='email' id='email'placeholder='example@example'required/>  <br>"
		contenido+="<input type='submit' value='enviar datos'onclick='enviado()'/> <br>"
		contenido+="<h3>  video Informativo <br><video src='Kickboxing Exercises - Kickboxing technique- uppercut - YouTube.MP4'  controls></video></h3>"
		contenido+="<audio src='My_AudioRecord[1].mp3' autoplay></audio>"

    
    
    document.getElementById('prueba').innerHTML=contenido;
}
function enviado()
	{
		var cedulavalida=document.getElementById('cedula').checkValidity();
		var apellidosvalidos=document.getElementById('apellidos').checkValidity();
		var nombresvalidos=document.getElementById('nombres').checkValidity();
		var emailvalidos=document.getElementById('email').checkValidity();
		if(cedulavalida && apellidosvalidos && nombresvalidos && emailvalidos)
			alert(" solicitud enviado");
		else
			alert("revise sus campos");
	}

</script>
