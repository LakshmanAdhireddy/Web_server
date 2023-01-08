# Developing a Simple Webserver

# AIM:

Name:Lakshman Adhireddy
reference id:22004423

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
~~~
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
</head>
</head>
<body>
<h1>WELCOME</h1>
<h2>NAME:Lakshman reddy B</h2>
<h2>REF.NO.:22004423</h2>
<h3>LIST OF FRAMEWORKS</h3>
<h4>-Django</h4>
<h4>-Ruby on Rails</h4>
<h4>-Angular</h4>
</body>
</html>
"""

class Hellohandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type','text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',80)
httpd = HTTPServer(server_address, Hellohandler)
httpd.serve_forever()
~~~

# OUTPUT:
![WhatsApp Image 2023-01-06 at 13 46 41](https://user-images.githubusercontent.com/118707265/211209119-6ad6c605-44f2-46b4-b05f-ffe56dc12c45.jpg)




# RESULT:

The program is executed succesfully
