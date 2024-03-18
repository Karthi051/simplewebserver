![image](https://github.com/Karthi051/simplewebserver/assets/148327224/475aca46-c0b2-46f2-bedd-cd61ac46e751)# EX01 Developing a Simple Webserver
## Date:1:3:24

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>My webserver</title>
</head>
<body>
    <table align="center" border="2" cellspacing="5" cellpadding="5" width="1200" height="50">
        <caption>TOP IT COMPANIES</caption>
		<tr>
			<th>S.NO</th>
			<th>COMPANIES NAME</th>
			<th>COMPANIES FOUNDER</th>
		</tr>
        <tr>
			<th>1</th>
			<th>GOOGLE</th>
			<th> LARRY PAGE & SERGEY BRIN</th>
		</tr>
        <tr>
			<th>2</th>
			<th>MICROSOFT</th>
			<th>BILL GATES</th>
		</tr>
        <tr>
			<th>3</th>
			<th>TCS</th>
			<th>RATAN TATA</th>
		</tr>
        <tr>
			<th>4</th>
			<th>WIPRO</th>
			<th>M.H. HASHAM PREMJI</th>
		</tr>
        <tr>
			<th>5</th>
			<th>INFOSES</th>
			<th>NARAYANA MURTHY</th>
		</tr>
    </table>
</body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```


## OUTPUT:
![image](https://github.com/Karthi051/simplewebserver/assets/148327224/e98b6e3e-845b-4903-91f1-a79cd055cc74)

![image](https://github.com/Karthi051/simplewebserver/assets/148327224/946a6f52-345a-444c-b0a8-361b45d17e8f)




## RESULT:
The program for implementing simple webserver is executed successfully.
