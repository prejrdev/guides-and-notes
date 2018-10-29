# Working with curl to test APIs

## the dual terminal set up

1. create a named pipe:

	`mkfifo /tmp/send_the_rest`


2. in a new terminal session, use tail to continuously read the pipe:
	
	`tail -f send_the_rest`

3. pipe curl's output to `send_the_rest` by redirecting stderr to our pipe:
	
	`curl --request GET <endpoint-url> 2>send_the_rest`	

or better yet, redirect its output so prompts to stdin and errors can appear where they belong. 

	`curl --request GET "<endpoint>" -o send_the_rest`

