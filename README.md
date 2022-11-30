# SysStats

This a simple Python - Flask Web App, which reads the current RAM and CPU usage and a React frontend which shows the statistics in the browser.

I used a Python based web server (Gunicorn), and a proxy web server (nginx) in front of the Python API.

There are three docker containers that are in use, API,Client and other for the proxy.

Docker container that runs the API part of the project, which is stored in the api subdirectory.
It user Python 3.10 image as base.

The second Docker container that serves the React front end to clients.
It uses Node.js 16 image as base, which comes pre-installed with node and yarn.

The third Docker container that runs an nginx server proxies requests for the API to the container.
It uses Nginx latest image as base.

The application will spin up with `docker-compose up --build` command.
![Picture1](https://user-images.githubusercontent.com/8210555/204766824-8425f19b-666a-4a11-8722-c5229f65d49f.jpg)
