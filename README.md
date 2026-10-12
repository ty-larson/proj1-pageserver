# CIS 322 Project 1: Simple Web Server

## Author: Ty Larson, tyl@uoregon.edu

### Description
This project is a lightweight, custom web server written in Python for CIS 322. It is capable of serving `.html` and `.css` files from a specified document root directory. 

The server includes basic HTTP response handling, specifically:
* **200 OK:** Successfully serves valid `.html` and `.css` files.
* **404 Not Found:** Generates an appropriate error response when a requested file does not exist in the directory.
* **403 Forbidden:** Enforces basic security by returning a forbidden error for illegal URL paths containing `~`, `//`, or `..`.

### Usage
The server port and document root are configured via the `credentials.ini` file. Once configured, the server can be started using the provided `Makefile`:
* `make run` (Runs the server in the foreground)
* `make start` (Runs the server in the background)
* `make stop` (Stops the background server process)