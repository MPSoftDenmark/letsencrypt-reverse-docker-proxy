Why?
You need a reverse proxy for ex. Microsoft Exchnage OWA, 
 or a website.  So is this mabe some for you.
 Useing LetsEncrypt SSL - Automatic renew via cron

Get with
`docker pull mpsoftdenmark/letsencrypt-reverse-proxy`

Build with
`docker build -t mpsoftdenmark/letsencrypt-reverse-proxy .`

Run with
`docker run -d -p 80:80 -p 443:443 --name nginx --restart=always -v /etc/Certs:/etc/letsencrypt -v /var/DockerData/Nginx/Sites:/etc/nginx/sites-available -e LETSENCRYPT_EMAIL="hostmaster@mpsoft.dk" mpsoftdenmark/letsencrypt-reverse-proxy`

Get on thw console
`docker attach nginx`