## DevOps Projects & Architecture Diagrams with Amazon Q CLI & MCP

## For MacOS
On your terminal, run the command

``` brew install amazon-q ```

## For WSL (Windows Subsystem For Linux)
Download installation zip file:

``` curl --proto '=https' --tlsv1.2 -sSf "https://desktop-release.q.us-east-1.amazonaws.com/latest/q-x86_64-linux.zip" -o "q.zip" ```

•	Unzip the installer:unzip q.zip
•	Run the install program:./q/install.shBy default, the files are installed to ~/.local/bin.

## For Linux (Ubuntu)
Make sure your machine is updated and has Libfuse2 installed
``` sudo apt-get update ```

``` sudo apt install libfuse2 ```

Install the deb file for Amazon Q

``` curl --proto '=https' --tlsv1.2 -sSf https://desktop-release.q.us-east-1.amazonaws.com/latest/amazon-q.deb -o amazon-q.deb ```

## Install Amazon Q debian file

``` sudo apt install -y ./amazon-q.deb ```

Login into Amazon Q developer by creating a BuilderID here followed by command

``` q login ```

once you have logged in, just write simple command

``` q ```

For exit type 

``` /quit ```

## MCP Support on Amazon Q CLI
Now let's power up your Amazon Q CLI with MCP Servers.
You need uv to install and Run MCP Servers

``` sudo snap install astral-uv --classic ```

Now go to ~/.aws/amazonq folder using

``` cd ~/.aws/amazonq ```

Now create a file called mcp.json in ~/.aws/amazonq

``` vim mcp.json ```



and add this

```
{

	"mcpServers" : {
    
 "awslabs.cdk-mcp-server": {
        "command": "uvx",
        "args": ["awslabs.cdk-mcp-server@latest"],
        "env": {
           "FASTMCP_LOG_LEVEL": "ERROR"
        }
   },
 "awslabs.aws-diagram-mcp-server": {
 		"command": "uvx",
 		"args": ["awslabs.aws-diagram-mcp-server"],
 		"env": {
 			"FASTMCP_LOG_LEVEL": "ERROR"
 		},
 		"autoApprove": [],
 		"disabled": false
 	}
}
}
```

That's it, you're all set to take your DevOps & Cloud skills to the next level with AI.
Write a simple prompt
Create a simple flask application that shares random motivational quotes in Hindi


