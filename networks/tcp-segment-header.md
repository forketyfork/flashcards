START
Basic
Front: Describe the TCP segment header.
Back: 
- **source port** (16 bits): sender port
- **destination port** (16 bits): receiver port
- **sequence number** (32 bits):
	- if SYN=1, this is the initial sequence number; the sequence number of the actual first data byte and the acknowledged number in the corresponding ACK are then this sequence number plus 1;
	- if SYN=0, this is the accumulated sequence number of the first data byte of this segment for the current session;
	- used to reassemble data if it arrives out of order;
- **acknowledgement number** (32 bits): if ACK=1, this field's value is the next sequence number that the sender of the ACK is expecting. This acknowledges receipt of all prior bytes (if any). The first ACK sent by each end acknowledges the other end's initial sequence number itself, but no data;
- **data offset** (4 bits): the size of the TCP header in 32-bit words;
- **reserved** (4 bits): should be zero; the last bit was used as the NS-ECN (nonce sum for explicit congestion notification) — no longer used;
- **flags** (8 bits):
	- CWR: Congestion Window Reduced; the sender received a TCP segment with ECE=1 and responded by reducing its sending rate;
    - ECE: ECN Echo:
	    - if SYN=1, the TCP peer is ECN-capable;
	    - if SYN=0, indicates that a packet with the Congestion Experienced (ECN=11) flag in its IP header was received;
    - URG: Urgent; the Urgent Pointer field is significant;
    - ACK: Acknowledgment; the Acknowledgment Number field is significant; all packets after the initial SYN packet sent by the client should have this flag set;
    - PSH: Push; the receiver should push the buffered data to the receiving application;
    - RST: reset the connection;
    - SYN: synchronize sequence numbers; only the first packet sent from each end should have this set;
    - FIN: last packet from the sender.
- **window size** (16 bit): size of the receive window (number of bytes the sender is willing to receive);
- **checksum** (16 bits): for error checking of the TCP header, payload and IP pseudo-header;
- **Urgent pointer** (16 bits): if the URG flag is set, then this is an offset from the sequence number indicating the last urgent data byte.
- **Options** (0-320 bits, in units of 32 bits), padded at the end with 0 if necessary;
- **Data**.
<!--ID: 1745138784650-->
END
