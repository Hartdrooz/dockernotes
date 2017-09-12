# List of common errors

## Cannot pull an image 

Using default tag: latest
Error response from daemon: Get https://registry-1.docker.io/v2/: net/http: request canceled while waiting for connection (Client.Timeout exceeded while awaiting headers)

### Solution

Restart your docker engine and do the ``` docker login ```.

Do the the ``` docker pull <imageName> ``` again and everything
should work.