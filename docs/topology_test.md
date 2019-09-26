# Testing the topology
## Duplicate testing
No duplicates were found when doing pinging tests.

## Latency testing

When trying to ping from one host to another, the first ping always has a substantially larger delay, between 1 and 6 ms. The subsequent pings, however, have a delay of 0.55 ms on average. We believe this is because the firs tping goes to the controller and the controller installs a L2 forwarding rule in the switch. But after a certain time, that rule is flushed out from the switch if the traffic does not persist.

## Future concerns

Consider if adding packet delay is benficial for later testing.
Pinging switch to host always has a high delay, above 100 ms.

  * Set bandwidth on links?
  * Core pinning
