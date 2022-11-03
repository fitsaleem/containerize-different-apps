# To containerze this applcation follow these steps

docker build -t (give any name) . (this command create the image of this application and don't forget to give . in last )
  
  # step 1
  docker build -t helloworld . 
  
  docker container run --name <give-name-any> -d -p 5050:80 (give-name-of-image or give-id)
  
 # step 2
  docker container run --name myApp -d -p 5050:80 helloworld
  
  
  
