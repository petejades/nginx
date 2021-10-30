# nginx

docker build -t webserver .

docker run -it --rm -d -p 8080:80 --name web webserver

Open your browser and navigate to http://localhost:8080 to make sure our html page is being served correctly.
