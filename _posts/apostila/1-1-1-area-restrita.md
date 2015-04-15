---
layout: alunos
simpletitle: Área Restrita
title: Área Restrita <i class="fa fa-lock"></i> 
tagline:
tags: []
special: [apostila]
hidenotes: true
---

<div id="secret-div">
</div>

<div id="default-div" style="display:block;" class="bs-callout bs-callout-warning" >
	<h4><i class="fa fa-exclamation-triangle"></i> Atenção</h4>
	<p>Esta página é apenas para alunos registrados. Ela contém apenas dados e formulários de perguntas sobre a oficina em andamento.</p>
	Caso você esteja resgistrado na oficina em andamento, insira a senha da turma:
	<input type="password" id="apassword" size="10">
	<button onclick="decryptSection()" title="Acessar"><i class="fa fa-unlock"></i></button>
	<center>
		<a style="color:gray" href="#" onclick="showDiv();"><i class="fa fa-key fa-fw"></i></a>
	</center>

	<div id="encrypt-div" style="display:none;" class="answer_list">
		<br>
		<center>
			<textarea id="in" rows="20" cols="38"></textarea> <textarea readonly id="out" rows="20" cols="38"></textarea>
			<br>
			<i class="fa fa-key fa-fw"> </i>
			<input type="text" id="password" size="10">
			<button onclick="encrypt(false)" title="Criptografar"><i class="fa fa-lock fa-fw"></i></button>
			<button onclick="decrypt()" title="Decriptografar"><i class="fa fa-unlock-alt fa-fw"></i></button>
			<button onclick="copy()" title="Copiar"><i class="fa fa-caret-left fa-fw"></i></button>
			<button onclick="getfile()" title="Carregar"><i class="fa fa-cloud-download fa-fw"></i></button>
			<button onclick="convert()" title="Converter"><i class="fa fa-bolt fa-fw"></i></button>
			<button onclick="erase()" title="Limpar"><i class="fa fa-eraser fa-fw"></i></button>
			<button onclick="hideDiv()" title="Ocultar"><i class="fa fa-times fa-fw"></i></button>
		</center>
	</div>
</div>

<script src="http://crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/aes.js"></script>
<script>
	function decryptSection() {
		var pw = document.getElementById("apassword").value;
		$.ajax({
			url : "/crypto.txt",
			success : function(encrypted){
				var decrypted = CryptoJS.AES.decrypt(encrypted.trim(), pw).toString(CryptoJS.enc.Utf8);
				if (decrypted.length > 0){
					decrypted = markdown.toHTML(decrypted);
					document.getElementById('secret-div').insertAdjacentHTML('afterbegin', decrypted);
					document.getElementById('encrypt-div').style.display = "none";
					document.getElementById("default-div").className = "bs-callout bs-callout-success";
					document.getElementById('default-div').style.display = "none";
				} else {
					document.getElementById("default-div").className = "bs-callout bs-callout-danger";
				}
			}
		});
	}
	function getfile() {
		$.ajax({
			url : "/crypto.txt",
			success : function(encrypted){
				document.getElementById("in").value = encrypted.trim();
				if (encrypted.length > 0){
					document.getElementById("default-div").className = "bs-callout bs-callout-success";
				} else {
					document.getElementById("default-div").className = "bs-callout bs-callout-danger";
				}
			}
		});
	}
	function convert() {
		document.getElementById("out").value = markdown.toHTML(document.getElementById("in").value);
	}
	function erase() {
		document.getElementById("in").value = "";
		document.getElementById("out").value = "";
		document.getElementById("password").value = "";
	}
	function copy() {
		document.getElementById("in").value = document.getElementById("out").value;
	}
	function decrypt() {
		var pw = document.getElementById("password").value;
		var encrypted = document.getElementById("in").value;
		var decrypted = CryptoJS.AES.decrypt(encrypted.trim(), pw).toString(CryptoJS.enc.Utf8);
		document.getElementById("out").value = decrypted;	
		if (decrypted.length > 0){
			document.getElementById("default-div").className = "bs-callout bs-callout-success";
		} else {
			document.getElementById("default-div").className = "bs-callout bs-callout-danger";
		}
	}
	function encrypt(){
		var pw = document.getElementById("password").value;
		var input = document.getElementById("in").value;
		var encrypted = CryptoJS.AES.encrypt(input, pw);
		document.getElementById("out").value = encrypted;
	}
	function showDiv() {
		document.getElementById('encrypt-div').style.display = "block";
	}
	function hideDiv() {
		document.getElementById('encrypt-div').style.display = "none";
	}
	
</script>

