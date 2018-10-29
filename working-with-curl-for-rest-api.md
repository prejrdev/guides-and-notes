#Working with curl to test APIs

##the dual terminal set up

1. create a named pipe:

	`mkfifo /tmp/send_the_rest`


2. in a new terminal session, use tail to continuously read the pipe:
	
	`tail -f send_the_rest`

3. pipe curl's output to `send_the_rest`:
	
	`curl -o -v the_rest http://www.example.com/index.html	
