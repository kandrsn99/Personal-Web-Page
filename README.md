# Personal-Web-Page
This is a Hyper Text Mark Up Language (HTML) and Cascading Styles Sheet (CSS) template for a personal webpage. More specifically, for those in academia wishing to showcase their biography, lectures, publications, and services.

# Installation Process

In order to install this repository from the command line you will need to get the 'git' package on your unix machine. Other machines will vary, but I will treat this as if we were using BSD. Otherwise, the process remains the same across operating systems, just different command styles.

> pkg install git

Other machines will vary, but I will treat this as if we were using BSD. Otherwise, the process remains the same across operating systems, just different command styles. In  any case, we use 'git' to download this repositorty to your machine for editing. Don't forget to add your pictures, documentation, or hyper-links for your personal benefit.

> git https://github.com/kandrsn99/Personal-Web-Page.git

Assuming you are ready for set up, we must install NGINX on our machine to serve the static HTML files. 

> pkg install nginx

We must now enable NGINX on the system.

> sysrc nginx_enable=YES
> service nginx start

Whatever changes you may make to the NGINX configuration or static file path can be tested before restarting NGINX to implement any changes in the content.

> nginx -t
> service nginx reload

I included a template NGINX configuration file https://github.com/kandrsn99/Personal-Web-Page/blob/main/nginx.conf that you may use, please read through it carefully. Remember, the exact file paths matter during the initial set up. Typically, anything that came with installation will be in the path /usr/local/etc/nginx.

You may check your HTML via web hosting service on http://localhost:80/ or the server address on http://address:80/

Also, you may purchase a domain name server (DNS) register to point to your new hosts internet protocol (IP) address. Upon completion of pointing a DNS at the host you may use http://dominamename to send to all your friends and/or customers. You may read more about official NGINX documentation here at https://nginx.org/en/docs/.

Do note that you must retrieve an SSL (secure socket layer) certificate to have HTTPs working for your domain name. The NGINX configuration file is meant to be easy to follow and understand. Read it and make sure the certificates are stored in the correct locations with the proper naming schema for NGINX. An easy way to create SSL certificate may be done with openSSL, https://openssl.org/, from the command line or otherwise downloaded from the DNS provider. 

It is highly recommended that you use Cloudflare as they are the leading provider of a register for hosting a DNS. You may review their documentation here https://developers.cloudflare.com/learning-paths/get-started/ at your leisure.
