# Multicasting Video Over IP - Computer Networks Project

## Description

This project demonstrates the concept of **multicasting video over IP**. It involves streaming video data over a network using multicast protocols. The project includes multiple components such as a **server** that sends video data, **stations** that act as intermediate nodes, and **receivers** that receive and display the video stream. The communication between the entities is done via multicast IP addresses to efficiently distribute the video stream to multiple clients.

## Files

- **client.c**: The client application that connects to the server, receives the video stream, and displays the video.
- **server.c**: The server application that streams the video over the network using multicast. It reads the video file and sends its contents to multicast clients.
- **station1.c**: An intermediate station that processes or relays the multicast stream between the server and the receiver.
- **station2.c**: Another intermediate station that may perform different actions, such as video stream transformation or additional routing.
- **receiver.c**: The receiver application that receives the multicast stream and renders the video on the screen.

## Features

- **Multicast Video Streaming**: Enables sending video streams to multiple receivers via multicast IP, improving efficiency over unicast.
- **Client-Server Model**: The client connects to a server to receive the video stream. Multiple clients can be supported simultaneously.
- **Intermediate Stations**: Stations (station1 and station2) relay or manipulate the video data before it reaches the receiver.
- **Video Display**: The receiver processes and displays the video stream on the client-side.
- **Network Communication**: Uses UDP/IP protocol for transmission, ensuring low-latency communication suitable for video streaming.
- **Multicast Protocol**: Uses multicast IP addresses to send video data, making it more efficient than sending separate unicast streams.

## Requirements

- **Operating System**: Linux/Unix-based system (Ubuntu, Debian, etc.).
- **C Compiler**: GCC or any compatible C compiler.
- **Libraries**: Standard C libraries, and any required libraries for video display (e.g., `SDL` or `OpenCV`).
- **Networking Tools**: Basic understanding of networking concepts, specifically multicast communication.

## Installation

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/your-username/multicasting-video-over-ip.git
 2.Navigate to the project directory:
     
     cd multicasting-video-over-ip
  3.Compile the C files using GCC:

      gcc -o server server.c
      gcc -o client client.c
      gcc -o station1 station1.c
      gcc -o station2 station2.c
      gcc -o receiver receiver.c
  4.Ensure you have necessary libraries for video rendering. For example, if using SDL for display:

      sudo apt-get install libsdl2-dev
  5.Run the server and the receiver(s):
  Start the server:
        
            ./server
                  
  Start the receiver:

      ./receiver
   If using stations for relaying, start them in between the server and receiver:

          ./station1
          ./station2

        
  Usage
    
  Server Setup: The server reads a video file (could be an .mp4 or .avi file) and streams it over a multicast IP address.
  Receiver Setup: Receivers listen to the multicast IP address and display the video stream. Multiple receivers can be connected at the same time, all receiving the same video stream.
  Intermediate Stations: Stations relay the multicast stream or apply additional processing to the video data, such as video transformations or compression.
  Multicast Group: The client and receiver are part of a multicast group identified by a specific multicast IP address.

  Acknowledgements
  
  Kalmesh - Developer
  
  Special thanks to  libraries  used for this project, such as SDL or OpenCV.


  
### Key Points:

- The README explains the project components: server, client, stations, and receiver.
- It provides installation, usage instructions, and examples.
- The multicast protocol and the concept of using stations in the middle are well described.
- It also includes instructions for contributing and acknowledging the contributors.



