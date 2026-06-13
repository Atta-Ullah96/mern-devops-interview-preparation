What Happens When We Type google.com?

When we type google.com in the browser, the browser first checks cache. If the IP address is not available in cache, the browser performs a DNS lookup. DNS converts the domain name google.com into an IP address.

After getting the IP address, the browser connects to the server. If the website uses HTTPS, a TLS handshake happens to create a secure encrypted connection.

Then the browser sends an HTTP GET request to the server. The server processes the request and sends an HTTP response back to the browser. The response may contain HTML, CSS, JavaScript, images, fonts, and other resources.

Finally, the browser parses the HTML, creates the DOM, applies CSS, runs JavaScript, and renders the webpage for the user.

Full Flow

User types google.com
↓
Browser checks cache
↓
DNS converts google.com to IP address
↓
Browser connects to server IP
↓
TCP connection is created
↓
TLS handshake happens for HTTPS
↓
Browser sends HTTP GET request
↓
Server processes request
↓
Server sends HTTP response
↓
Browser receives HTML, CSS, and JavaScript
↓
Browser creates DOM and CSSOM
↓
Browser renders the page