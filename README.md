I have made the following Changes:

The port number 5001 exposed in dockerfile, but the same is not updated in app.py 
Hence i made the necessary changes i.e., initialized port no 5001 in app.py app.run(host='0.0.0.0', port=int("5001"))

In the "docker-compose.yml", the flask app is listening on port no 80 according to flaskapp.conf. 
But the port number was not in order in the yml file. I have Changed the ports accordingly. "8080:80"

Also in the yml file, local folder where the data need to be stored is specified incorrectly. "data" -> "./data"
