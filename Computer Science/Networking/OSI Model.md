A conceptual framework that divides [[Network | network]] communications functions into seven layers

![[OSI.png| 350]]

1. **Physical Layer**
- Concerned with the physical connection between devices.
- It deals with hardware specifications, such as cables, connectors, and electrical signals
2. **Data Link Layer**
- Responsible for creating a reliable link between two directly connected nodes
- It handles error detection and correction, as well as flow control.
3. **Network Layer**  ^7e919f
 - Manages routing and addressing
 - It is responsible for logical addressing, [[Data Transmission#^206809 | packet]] forwarding between [[Network Hardware#^3c8292 | router]], and determining the best path for data to travel
4. **Transport Layer**
- Ensures end-to-end communication and reliability
- It handles segmentation, flow control, error recovery, and reordering of data
5. **Session Layer** 
- Manages sessions or connections between applications
- It establishes, maintains, and terminates communication sessions, providing services such as dialog control and synchronization
6. **Presentation Layer**
- Deals with data format translation and encryption/decryption
7. **Application Layer**
- Provides network services directly to end-users or applications
- It includes [[Network Protocols | protocols]] for email, file transfer, remote login, and other application-level services