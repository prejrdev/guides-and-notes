#Working with curl to test APIs

##the dual terminal set up

1. create a named pipe:

	`mkfifo send_the_rest`

2. in a new terminal session, use tail to continuously read the pipe:
	
	`tail -f send_the_rest`
