# PRACTICA-1





##1. DESCARGAR Y COMPROBAR QUE UNA IMAGEN ESTÁ EN TU REPOSITORIO

Para descargar la imagen de _ubuntu_ ejecutamos el comando 

   ` docker pull ubuntu`
   
Posteriormente, para comprobar que la imagen está en el equipo 


   `docker images `


##2. CREAR UN CONTENEDOR SIN NOMBRE,QUEDA ARRANCADO? COMO SE OBTIENE EL NOMBRE?

Para crear un contenedor sin nombre ejecutamos

    `docker run -d ubuntu`

Este comando ejecuta _ubuntu_ en segundo plano.Para comprobar que está arrancado 


    `docker ps`
    
        
    
El comando anterior mostrará entre otro tipo de infomación un ID de contenedor como un identificador único



##3. CREAR UN CONTENEDOR CON EL NOMBRE _U1_, COMO SE ACCEDE A ÉL?


Para crear un contenedor con el nombre requerido 



     `docker run -d --name u1 ubuntu`
     
     
Para acceder al contenedor 



      `docker exec -it u1 bash`
      
      
      
##4. COMPROBAR SU IP Y HACER PING A GOOGLE.COM


Una vez dentro del contenedor se ejecuta



      `ip addr show`
      
      
Para hacer ping a google.com


      `ping google.com`
      
      

##5. CREAR UN CONTENEDOR CON EL NOMBRE _BONO_, PUEDES HACER PING ENTRE LOS CONTENEDORES?


Para crear el contenedor con el nombre especificado 


     `docker run -d --name bono ubuntu`
     

Posteriormente , dentro del contenedor 


     `docker exec -it u1 ping bono`
     
     

##6. SI CIERRAS LA TERMINAL , QUÉ LE PASA AL CONTENEDOR ?


Si cierro la terminal los contenedores siguen funciondo ya que fueron inicializados en segundo plano (opción -d)



##7. CUÁNTA MEMORIA DE DISCO DURO OCUPASTE? USA DOCKER PARA CALCULARLO 


Para visualizar la el grado de utilización del disco duro usamos el siguiente comando


       `docker system df`


Se muestra el espacio ocupado del disco por el contenedor ,imágenes y volúmenes



##8. CUÁNTA RAM OCUPAN LOS CONTENEDORES? 


Para ver la memoria RAM consumida por los contenedores.



       `docker stats`
       
       
Este comando mostrará en tiempo real el uso de CPU, Memoria y otros recursos asociados 



##9. COMO HICISTE PARA CLONAR EL REPOSITORIO 


Ejecutando el comando 


      `git clone https://github.com/danielcg33/PRACTICA-1`
      


##10. COMO AÑADES EL ARCHIVO _README.md_

Desde el lugar remoto , a la hora de crear el repositorio marcamos la opción de generar un archivo readme.md 


##11. LOS PASOS QUE TIENES QUE SEGUIR PARA SUBIR EL ARCHIVO 


Para subir los cambios al repositorio remoto, se ejecutan los siguientes comandos 


Añadimos los ficheros al grupo de seguimiento 


        `git add .`
        
Realizamos _commit_ de los cambios ejecutados 



        `git commit -m "añadiendo primera versión"`


Finalmente se suben los cambios al repositorio remoto 



        `git push origin main`
        
        

##12. COMO SE COMPROBARÍA QUE EXISTEN DIFERENCIAS ENTRE EL REPOSITORIO LOCAL Y EL REPOSITORIO REMOTO 


Primeramente se realiza un 



        `git fech`
        
        
Esto permite traer las últimas actualizaciones del repositorio remoto


Posteriormente para las diferencia 



        `git diff origin/main        

                                      

       
        

                                  
     

        
       
