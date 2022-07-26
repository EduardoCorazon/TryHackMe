# FTP

# File Transport Protocol

PORT [21]

based on client server model: server validates the login credentials thus opening up the initial session, once session is open the client can execute FTP commands on the server

uses two channels:

1) Command /control channel: which transmits commands and replies

2) Data channel: which is used for transferring data and

## FTP connection:

Active Connection:

-a client [you] opens a port and listens, server needs to actively connect to it

-like a reverse shell using netcat

Passive Connection:

-server opens a port and listens passively, the client [you] connects to it

Why 2 different types of channels?

- The server doesn’t have to wait for the current data transfer to finish
- If they were interlinked you could only enter commands between data transfers or slow internet connections

# Enumerating FTP

Scan for ports: nmap -A -p- {targetIP}

To check if it allows anonymous log in:

ftp {target IP} ←connect to ftp server

type “anonymous” for username and don’t enter a password

if we get a connection then take note of potential usernames

NOTE: one some older systems there is a bug we can exploit in which we type “cwd” as n ftp command and see a user without inputting credentials

# Exploiting FTP

Just like telnet command and data channels are unencrypted so any data can be intercepted and read

so we can use a man-in-middle attack like an ARP-poisoning ([https://www.jscape.com/blog/bid/91906/Countering-Packet-Sniffers-Using-Encrypted-FTP](https://www.jscape.com/blog/bid/91906/Countering-Packet-Sniffers-Using-Encrypted-FTP))

But most of our exploitation is due to weak passwords or misconfigurations

So we brute force passwords using the Hydra tool:

hydra -t {#parallel connections} -l {user} -P {wordlist path} -vV  {IP} ftp

so for example:

hydra -t 4 -l Mike -P /usr/share/wordlist/rockyou.txt -vV 10.0.0.3 ftp

Boom now we have a password so we can connect to the FTP server as Mike and gain full access

For more info:

[https://www.ietf.org/rfc/rfc959.txt](https://www.ietf.org/rfc/rfc959.txt)