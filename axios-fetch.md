
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

## Const Hook


### Service

    import  axios  from  "axios";
   
    class  AppService {
    constructor(configRequest) {
    const { method, url  = {} } = configRequest;
  
    this.method  = method;
    this.url  = url;
    
    this.axiosInstance  = axios.create({
    
    baseURL:  "https://jsonplaceholder.typicode.com/",});
    }
    
      
    
    async  getData() {
    
    try {
    
    const  req  =  await  this.axiosInstance[this.method.toLowerCase()](this.url);
    
    return req.data;
    
    } catch (error) {
    
    console.log(error);
    
    }
    
    }
    
    }
    
    export  default  AppService;

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4MzEwNjkxMzgsLTE5OTI1NDc2MDAsLT
I1Mjc3MTY1LDc5NjczMjI5Ml19
-->