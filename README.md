# rottenpie: pwnedcr2019

# Taller: ¿Cómo nos espían?

## Window Size:
Eje X: Ancho
```
window.innerWidth
document.documentElement.clientWidth
document.getElementsByTagName('body')[0].clientWidth
```

Eje Y: Altura
```
window.innerHeight
document.documentElement.clientHeight
document.getElementsByTagName('body')[0].clientHeight
```

## Mouse Tracking
```
onmousemove = function(e){console.log("mouse location:", e.clientX, e.clientY)}
```

## Facebook Pixel
```
<!-- Facebook Pixel Code -->
<script>
!function(f,b,e,v,n,t,s)
{if(f.fbq)return;n=f.fbq=function(){n.callMethod?
n.callMethod.apply(n,arguments):n.queue.push(arguments)};
if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
n.queue=[];t=b.createElement(e);t.async=!0;
t.src=v;s=b.getElementsByTagName(e)[0];
s.parentNode.insertBefore(t,s)}(window, document,'script', 
'https://connect.facebook.net/en_US/fbevents.js');
fbq('init', '{your-pixel-id-goes-here}');
fbq('track', 'PageView');
</script>
<noscript>
<img height="1" width="1" style="display:none" 
src="https://www.facebook.com/tr?id={your-pixel-id-goes-here}&ev=PageView&noscript=1"/>
</noscript>
<!-- End Facebook Pixel Code -->
```

## UTM
Urching traffic monitor, base de google analytics
```
http://yoursite.com/your-page/?utm_source=facebook&utm_medium=cpc &utm_campaign=spring_sale&utm_content=shoe_ad

utm_source = Fuente (Google, Facebook, Twitter, etc)
utm_medium = Tipo de tráfico desde donde se origino la llamada: cpc, email, social, referral, display, etc.
utm_campaign = Nombre de la campana de marketing.
utm_content = Contenido que origino la llamada: CTA, email, navlink, etc.
utm_term = Keywords utilizados especialmente para ads de búsqueda pagados.
```
## HTTP Headers
```
User Agent = Tipo de navegador, Sistema Operativo, Dispositivo
Referer = El último URL visitado antes de enviar la solicitud.
Cookies = En la página siguiente.
DNT = Do Not Track, se configura en el navegador.
X-Forwarded-For = Divulgación de la IP origen.
```
## Cookies
```
* Identificadores de sesión.
* Llaves de rastreo.
* Preferencias temporales del usuario.
```
