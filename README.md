# VestaCP-Force-HTTP-HTTPS-templates
Nginx templates for VestaCP. Force website to use http or https and redirect to forced protocal

When you have multiple web-sites and one of them uses SSL,all other sites without SSL accessed via https:// will redirect to the first web-site that have SSL certificate.

For example:
domain1.ru has SSL and can be accessed with http://doamin1.ru and https://domain1.ru
domain2.ru has no SSL and can be accessed only with http://domain2.ru and when someone tries to access domain2
via https://domain2.ru - domain1 web-site will be displayed.

With force-http nginx template you can force web-site without SSL to use only http connection.
So https://domain2.ru will automatically redirect to http://domain2.ru and won't display domain1.ru web-site

With force-https nginx template you can force web-site with SSL to use only https connection.
So http://domain1.ru will automatically redirect to https://domain1.ru

All templates should be placed in '/usr/local/vesta/data/templates/web/nginx' path.
After that they can be easily accessed with Vesta panel.
