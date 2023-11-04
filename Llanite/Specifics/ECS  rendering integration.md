## Information:
* Language - #rust
* Status - #started
## Notes
Current thought out approach is to rebuild vertex buffers stored in state of 2D and 3D rendering-related components every time a change in them is detected.

### Pain points
* Changing vertex buffers stored in state from ECS
* Performance and optimisation of when to change what VBs.