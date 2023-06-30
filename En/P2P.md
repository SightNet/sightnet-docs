So, each peer has its own database, a local reputation list. And acts as a server and a client at the same time.

When a user enters a request -> the peers distribute it using the gossip protocol. For 5 seconds the user will wait for a response from the servers which in return will also send data via gossip protocol with the recipient's id of the results. Then they are ranked.