# Developing a Simple Webserver

# AIM:

Develop a webserver to display about top five web application development frameworks.

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver

# PROGRAM:

from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
</head>
<body>
<h1>Welcome</h1>
<h2>WEB FRAMEWORKS</h2>
<p>React for Javascript</p>
<p>Django for Python</p>
<p>Laravel for PHP</p>
<p>Angular for Typescript</p>
</body>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type','text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
        
    server_address = ('',80)
    httpd = HTTPServer(server_address, HelloHandler)
    httpd.serve_forever()

# OUTPUT:

![Screenshot_20230127_094133](https://user-images.githubusercontent.com/118706984/215140486-34060a44-0983-44c9-973d-7b597151cb4d.png)

![Screenshot_20230127_094108](https://user-images.githubusercontent.com/118706984/215140537-0ac9ed82-3f47-4f29-b449-53b86db16a8e.png)





# RESULT:

The program is executed succesfully
