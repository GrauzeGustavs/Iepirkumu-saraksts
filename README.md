<!DOCTYPE html>

<body>
	<ul id="list"></ul>
	<input type="text" id="beta" />
    <!-- pievienoju funkciju kas izveido pogu "pievienot" un "nonemt"-->
	<button onclick="addItem()" class="buttonClass">
	pievienot iepirkumu</button>
	<button onclick="removeItem()" class="buttonClass">
	nonemt iepirkumu</button>
	<script>
        //veidoju funkciju kas pievieno tekstu
		function addItem() {
			var a = document.getElementById("list");
			var beta = document.getElementById("beta");
			var li = document.createElement("li");
			li.setAttribute('id', beta.value);
			li.appendChild(document.createTextNode(beta.value));
			a.appendChild(li);
		}
		// funkcija lai nonemtu tekstu no lista
		function removeItem() {
			var a = document.getElementById("list");
			var beta = document.getElementById("beta");
			var item = document.getElementById(beta.value);
			a.removeChild(item);
		}
	</script>
</body>

</html>
