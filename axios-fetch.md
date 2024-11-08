
# Axios ou fetch

- os dois permitem fazer requisições HTTP

  

## fetch

- é nativo do javascript

  

## Axios

- precisa ser instalado

- ele é baseado na fetch api mas tem algumas possibilidades a mais, possibilita cancelar requisições e adicionar configurações

  
  

## exemplo de codigos

 ### GET
#### 1 - get com fetch
 

        fetch("https://jsonplaceholder.typicode.com/todos")
         .then((response) => response.json())
         .then((data) => {
	         console.log(data);
         })
       .catch((error) => {
	         console.log(error);
       });



####  2 - get com axios
    axios.get("https://jsonplaceholder.typicode.com/todos")
    .then((response) => {
	     console.log(response.data);
     })
     .catch((error) => {
	     console.log(error);
     });

 ### POST
 ####  1 - post com fetch

     fetch("https://jsonplaceholder.typicode.com/posts", {
     method: "POST",
     headers: {
	     "Content-Type": "application/json",
	     body: JSON.stringify(data),
     .then((response) => response.json())
     .then((data) => {
	     console.log(data);
     .catch((error) => {
	    console.log(error);
    });

#### 2 - post com axios

    axios.post("https://jsonplaceholder.typicode.com/posts", data)
    .then((response) => {
	    console.log(response.data);
    })
    .catch((error) => {
	    console.log(error);
	}
