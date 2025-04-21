START
Basic
Front: 
Explain the TCP handshake and the related states.
Back: 
- initially, the server is in the `LISTEN` state, and is waiting for a connection request from a remote endpoint;
- the client sends a `SYN` segment (a connection request) and moves to the `SYN-SENT` state, waiting for a matching `SYN-ACK` segment; the sequence number A is randomly generated;
- the server receives `SYN`, sends a `SYN-ACK` segment and moves to the `SYN-RECEIVED` state, waiting for a matching `ACK` from the client; the acknowledgement number is A+1, the sequence number is another randomly generated number B;
- the client receives `SYN-ACK`, sends `ACK` and moves to the `ESTABLISHED` state; the sequence number is A+1, the acknowledgement number is B+1;
- the server receives `ACK` and moves to the `ESTABLISHED` state.
<!--ID: 1745138784648-->
END
