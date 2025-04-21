START
Basic
Front: 
How does TCP connection termination happen?
Back: 
The TCP connection termination happens via a 4-way handshake:
- the initiating application calls `close()`;
- the initiating kernel sends `FIN` and moves to the `FIN-WAIT-1` state;
- the receiving kernel responds with `ACK`, returns 0 from the `read(2)/recv(2)` function and enters `CLOSE-WAIT` state;
- the initiating kernel returns from `close()` and enters the `FIN-WAIT-2` state; the connection is in the half-closed state, the initiating application may still `read(2)/recv(2)` data from the remote endpoint;
- the receiving application calls `close()`;
- the receiving kernel sends `FIN` and enters the `LAST-ACK` state;
- the initiating kernel responds with `ACK` and enters the `TIME-WAIT` state, waiting for a timeout (typically 30s, 1m, 2m; this state lets the TCP client resend the final acknowledgment to the server in case the ACK is lost in transit); during this time, the local port is unavailable for new connections;
- the receiving kernel receives `ACK` and enters `CLOSED` state;
- the initiating kernel times out and moves to `CLOSED`.
<!--ID: 1745138784652-->
END
