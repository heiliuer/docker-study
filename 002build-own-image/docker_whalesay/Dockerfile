#The FROM keyword tells Docker which image your image is based on. Whalesay is cute and has the cowsay program already, so we’ll start there.
FROM docker/whalesay:latest

#Now, add the fortunes program to the image.
RUN apt-get -y update && apt-get install -y fortunes

#Once the image has the software it needs, you instruct the software to run when the image is loaded.
CMD /usr/games/fortune -a | cowsay