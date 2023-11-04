## Information:
* Language - #rust
* Status - #not-started
## Notes
This server should be ran as root and interact with the #kernel module over IPC. When a program is requested for execution, the kernel module will ask the kernel module to generate and gather two hashes:
* The hash for the requested program locally
* The hash found online for the program (if there is one)

If they match **exactly**, the program will pass and continue as usual. However, if either they do not match or the online hash does not exist, another message should be passed to the client which will talk to the backend and report the user for trying to run an application that was not allowed.

An example report could look like this:
* Name   - Geoferry
* File       - /usr/bin/cowsay
* Date     - 4.04.23
* Reason - Unkown
:w
The backend could use something like protobufs and gRPC to communicate this. [[Lanboard/Summary|Lanboard]] could be used as an example for protobufs and gRPCS with Rust and Go.
