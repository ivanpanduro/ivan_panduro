# ivan_panduro
Repositorio de prueba para implementar LLM y una aplicacion web 
# LLM Pruebas 
Repositorio de trabajo 

## 1 Intslacion 
 Como primer paso descargamos [ollama](https://ollama.com/download/linux) de su pagina web 
 utilizando el siguiente comando 
 ````bash
 $ curl -fsSL https://ollama.com/install.sh | sh
````
## 2 Ejecutar Sevidor 
Ejecutar el sevidor de API  REST de ollama con el siguiente comando 

````bash
$ ollama serve
````
## 3 Descargar un Modelo 
Desde la pagina de ollama descargar un [Modelo](https://ollama.com/library)
utilizando el siguiente comando

````bash 
$ ollama  pull tinyllama
````
## Descargar un Modelo 
Para realizar una consulta utilizamos el comando curl como se muestre en el siguiente ejemplo

````bash
curl -X POST http://localhost:11434/api/generate -d '{
  "model": "tinyllama",
  "prompt": "Why is the sky blue?"
}' 
````
## 5 Realizar un reques sin stream 
Para realizar una cosulta a la API RESTsin stream se hace de la siguiente forma 
````bash
````
## 6 Consulta GROQ
Estructura basica para realiar una consulta a GROQ mediante su API REST utilizando el siguiente comando 
````bash 
curl "https://api.groq.com/openai/v1/chat/completions" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer ${GROQ_API_KEY}" \
  -d '{
         "messages": [
           {
             "role": "user",
             "content": ""
           }
         ],
         "model": "llama3-8b-8192",
         "stream": false
        
       }'
````
