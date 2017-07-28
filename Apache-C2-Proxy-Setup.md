    # a2enmod rewrite 
    # a2enmod proxy
    # a2enmod proxy_http
    # a2enmod headers

    <VirtualHost *:80>
		RewriteEngine On
		RewriteRule ^/connect http://<IP ADDRESS>/connect [NC,P]
		RewriteRule ^/daisy http://<IP ADDRESS>/daisy [NC,P]
		RewriteRule ^/images/static/content/(.*) http://<IP ADDRESS>/images/static/content/$1 [NC,P]
		RewriteRule ^/news/(.*) http://<IP ADDRESS>/news/$1 [NC,P]
		RewriteRule ^/webapp/static/(.*) http://<IP ADDRESS>/webapp/static/$1 [NC,P]
		RewriteRule ^/images/prints/(.*) http://<IP ADDRESS>/images/prints/$1 [NC,P]
		RewriteRule ^/wordpress/site/(.*) http://<IP ADDRESS>/wordpress/site/$1 [NC,P]
		RewriteRule ^/true/images/77/(.*) http://<IP ADDRESS>/true/images/77/$1 [NC,P]
		RewriteRule ^/holidngs/images/(.*) http://<IP ADDRESS>/holidngs/images/$1 [NC,P]
		RewriteRule ^/steam(.*) http://<IP ADDRESS>/holidngs/images/$1 [NC,P]
		ServerAdmin webmaster@localhost
		DocumentRoot /var/www/html
		ErrorLog ${APACHE_LOG_DIR}/error.log
		CustomLog ${APACHE_LOG_DIR}/access.log combined
	</VirtualHost>

	<IfModule mod_ssl.c>
		<VirtualHost _default_:443>
			RewriteEngine On
			SSLProxyEngine On
			SSLProxyCheckPeerCN Off
			SSLProxyVerify none
			SSLProxyCheckPeerName off
			SSLProxyCheckPeerExpire off
			RewriteRule ^/connect https://<IP ADDRESS>/connect [NC,P]
			RewriteRule ^/daisy https://<IP ADDRESS>/daisy [NC,P]
			RewriteRule ^/images/static/content/(.*) https://<IP ADDRESS>/images/static/content/$1 [NC,P]
			RewriteRule ^/news/(.*) https://<IP ADDRESS>/news/$1 [NC,P]
			RewriteRule ^/webapp/static/(.*) https://<IP ADDRESS>/webapp/static/$1 [NC,P]
			RewriteRule ^/images/prints/(.*) https://<IP ADDRESS>/images/prints/$1 [NC,P]
			RewriteRule ^/wordpress/site/(.*) https://<IP ADDRESS>/wordpress/site/$1 [NC,P]
			RewriteRule ^/true/images/77/(.*) https://<IP ADDRESS>/true/images/77/$1 [NC,P]
			RewriteRule ^/holidngs/images/(.*) https://<IP ADDRESS>/holidngs/images/$1 [NC,P]
			RewriteRule ^/steam(.*) https://<IP ADDRESS>/holidngs/images/$1 [NC,P]
			ServerAdmin webmaster@localhost
			DocumentRoot /var/www/html
			ErrorLog ${APACHE_LOG_DIR}/error.log
			CustomLog ${APACHE_LOG_DIR}/access.log combined
			SSLEngine on
			SSLCertificateFile	/etc/ssl/certs/ssl-cert-snakeoil.pem
			SSLCertificateKeyFile /etc/ssl/private/ssl-cert-snakeoil.key
		</VirtualHost>
	</IfModule>