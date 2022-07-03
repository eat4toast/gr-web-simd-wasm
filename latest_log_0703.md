## state:
current finish building gr-web(yeah! make webapp success!)
but stall in page display, seems some configuration are lost and a icon file is missing.

## console output:

GET http://localhost:8000/favicon.ico  [HTTP/1.0 404 File not found 0ms]

SETTING ENVIRONMENT VARIABLES localhost:8000:32:15
Could not find platform independent libraries <prefix>             
Could not find platform dependent libraries <exec_prefix>             
Python path configuration:             
  PYTHONHOME = (not set)             
  PYTHONPATH = (not set)             
  program name = './this.program'             
  isolated = 0             
  environment = 1             
  user site = 1             
  import site = 1             
  is in build tree = 0             
  stdlib dir = '/opt/cpython/wasm/lib/python3.11'             
  sys._base_executable = '//this.program'                        
  sys.base_prefix = '/opt/cpython/wasm'                          
  sys.base_exec_prefix = '/opt/cpython/wasm'                     
  sys.platlibdir = 'lib'                                         
  sys.executable = '//this.program'                              
  sys.prefix = '/opt/cpython/wasm'                               
  sys.exec_prefix = '/opt/cpython/wasm'                          
  sys.path = [             
    '/opt/cpython/wasm/lib/python311.zip',                       
    '/opt/cpython/wasm/lib/python3.11',                          
    '/opt/cpython/wasm/lib/python3.11/lib-dynload',              
  ]                                                              

Fatal Python error: init_fs_encoding: failed to get the Python codec of the filesystem encoding             
Python runtime state: core initialized             
ModuleNotFoundError: No module named 'encodings'             
<empty string>             
Current thread 0x00adde0c (most recent call first):             
  <no Python frame>


## terminal output
$ sudo ./server.py 
Serving HTTP on 0.0.0.0 port 8000 (http://0.0.0.0:8000/) ...
127.0.0.1 - - [03/Jul/2022 19:30:34] "GET / HTTP/1.1" 200 -
127.0.0.1 - - [03/Jul/2022 19:30:34] "GET /python.data.js HTTP/1.1" 200 -
127.0.0.1 - - [03/Jul/2022 19:30:35] "GET /python.data HTTP/1.1" 304 -
127.0.0.1 - - [03/Jul/2022 19:30:35] "GET /python.worker.js HTTP/1.1" 200 -
127.0.0.1 - - [03/Jul/2022 19:30:35] "GET /python.worker.js HTTP/1.1" 200 -
127.0.0.1 - - [03/Jul/2022 19:30:35] "GET /python.worker.js HTTP/1.1" 200 -
127.0.0.1 - - [03/Jul/2022 19:30:35] "GET /python.worker.js HTTP/1.1" 200 -
127.0.0.1 - - [03/Jul/2022 19:30:35] code 404, message File not found
127.0.0.1 - - [03/Jul/2022 19:30:35] "GET /favicon.ico HTTP/1.1" 404 -

