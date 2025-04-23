# SVG-Phishing
## Phishing attack using a malicious SVG with embedded JavaScript.

1 - User is served an SVG file containing a hidden redirect to a phishing page.<br>
2 - Upon clicking the SVG, embedded JavaScript executes and decodes a base64-encoded phishing URL.<br>
3 - The user is redirected to a fake Google sign-in page.<br>
4 - Credentials entered are sent to the attacker.<br>
5 - The user is then redirected to the legitimate Google page to avoid suspicion.<br>

## How to run:
1 - Open a terminal and launch netcat as listener:
    `sudo nc -l -p 8081`

2 - In a different terminal, go to the folder where the HTML is located and start an HTTP server:
    `python3 -m http.server 8000`

3 - Open the `payload_obf.svg` in browser.
