### Vertical vs Horizontal Scaling
| Vertical                | Horizontal                |
| ----------------------- | ------------------------- |
| Server => Bigger Server | Server => Multiple Server | 

### Load Balancing
Decides which server a [[HTTP Requests | request]] will go to, depending on:
- Random Choice
- Round Robin
- Fewest Connections

#### Session Aware Load Balancing
- **Sticky Servers**
The user is always directed to the same server where they initially signed in or opened the web page
- **Sessions in Database**
All servers share session data stored in a central [[Types of Databases
 database]] and each can access and update session information, ensuring consistency
- **Client-Side Sessions**
Using cookies all servers get reminded of the session, during the lifetime of the cookie

### Autoscaling
- Automatically scaling the number of servers depending on the amount of requests

### Heartbeat
- At certain intervals, the load balancer 
