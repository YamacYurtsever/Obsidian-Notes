### Vertical vs Horizontal Scaling
| Vertical                | Horizontal                 |
| ----------------------- | -------------------------- |
| Server => Bigger Server | Server => Multiple Servers | 

### Load Balancing
Decides which server a [[HTTP Requests | request]] will go to, depending on:
- Random Choice
- Round Robin
- Fewest Connections

### Session Aware Load Balancing
- **Sticky Servers**
The user is always directed to the same server where they initially signed in or opened the web page
- **Sessions in Database**
All servers share session data stored in a central [[Types of Databases | database]] and each can access and update session information, ensuring consistency
- **Client-Side Sessions**
Using cookies all servers get reminded of the session, during the lifetime of the cookie

### Autoscaling
- Automatically scaling the number of servers depending on the amount of requests

### Heartbeat
- At certain intervals, each server is pinged to check if they respond back, in order to check if a server is down

! In systems that have multiple servers, if a server goes down the oncoming traffic can be redirected to the other servers
