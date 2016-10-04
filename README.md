# Localizado
Um gerente de linguas para fácil suporte ao I18N.

## Como utilizar
Você poderá utilizar esta biblioteca tanto no ambiente Node.js como também no navegador (de preferencia compilado).

```javascript

var localidade = new Localizado({
    pt_BR: 'pt_BR',
    en_US: 'en_US'
});
localidade.adicionarLocalidade(localidade.pt_BR);

localidade.carregar(localidade.pt_BR, {
  "ola": "ola!",
  "olaComUmParametro": "Olá, <%= usuario %>!",
  "aninhado": {
    "ola": "Olá aninhado!"
  }
});

localidade.carregar(localidade.en_US, {
	"ola": "Hello!",
	"olaComUmParametro": "Hello, <%= user %>!",
	"aninhado": {
		"ola": "Nested Hello!"
	}
});

console.log(localidade.gerar('ola'));
console.log(localidade.gerar('aninhado.ola'));
  
```
