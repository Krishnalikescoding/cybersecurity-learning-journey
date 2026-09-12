# Web-Based Exploits & Cross-Site Scripting (XSS) 

## Web-Based Exploits
- Malicious code/behavior that takes advantage of coding flaws in web applications.
- Common target: sensitive personal information.
- Occur because web apps interact with **multiple users across multiple networks**.

## Injection Attacks
- **Injection attack**: malicious code inserted into a vulnerable application.
- Infected app appears to work normally — malicious code runs silently in the background.
- **Why apps are vulnerable**: they're built to receive data inputs (typed, clicked, or shared between programs); if input isn't properly validated/sanitized, attackers can exploit it.
- Web apps are especially at risk due to high interactivity (many objects like images/buttons) — hard for developers to sanitize every input type.

## Cross-Site Scripting (XSS)
- **XSS**: injection attack that inserts code into a vulnerable website/web app.
- Usually delivered by exploiting **HTML and JavaScript**.
- Can give attackers access to session cookies, geolocation, even webcams/microphones.

### 3 Types of XSS

#### 1. Reflected XSS
- Malicious script sent to server, activated in the server's **response** (e.g., via search bar).
- Process:
  1. Attacker sends victim a link that looks trustworthy.
  2. Victim clicks → HTTP request sent to vulnerable server.
  3. Malicious script reflected back to victim's browser.
  4. Browser trusts server response, loads script.
  5. Info (e.g., session cookies) sent back to attacker.

#### 2. Stored XSS
- Malicious script **injected directly onto the server** (not sent via a link).
- Targets site elements served to users (images, buttons, etc.).
- Script activates automatically when a user visits the site.
- Especially dangerous — user has no way to know the site is infected beforehand.

#### 3. DOM-Based XSS
- **DOM (Document Object Model)** = source code of a website.
- Malicious script exists directly in the web page a browser loads.
- Doesn't need to be sent to the server to activate (unlike reflected XSS).
- Often hidden in URL parameter values (e.g., a color theme selector's URL parameter is manipulated to hide malicious JavaScript in HTML tags).
- Browser processes HTML and executes the injected JavaScript.

## Key Takeaways
- XSS attacks are used to steal sensitive information.
- Security analysts should be familiar with all three XSS types.
- Injection attacks are a broader category — XSS is just one type; more to come.