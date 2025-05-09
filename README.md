# pbr-diw-4961102-AJAX_testes

Exemplos de requisição AJAX

XHR

	function success () { console.log(JSON.parse(this.responseText)); } 
	function error (err) { console.log('Erro:', err); }
	var xhr = new XMLHttpRequest(); 
	xhr.onload = success; 
	xhr.onerror = error;
	xhr.open('GET', 'https://api.github.com/users/paulopta'); 
	xhr.send();


FETCH

  fetch('https://api.github.com/users/paulopta')
  .then(res => res.json())
  .then (data => console.log(data))
  .catch(err => console.error('Erro:', err))


JQUERY

$.ajax({
  url: "your-api-endpoint",
  method: "GET",
  data: { key: "value" },
  success: function(response) {
    // Handle successful response
    console.log(response);
  },
  error: function(error) {
    // Handle errors
    console.error(error);
  },
  beforeSend : function() {
     // Handle before send
  },
  complete : function() {
     // Handle complette 
  }
});

