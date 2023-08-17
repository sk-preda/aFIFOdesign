# aFIFOdesign
this project is created by shubham khobragade 
I just wanted to design and implement the synchronous and asynchronous fifo.

A. synchronous FIFO
Synchronous FIFOs are widely used in digital systems to enable seamless data transfer between different parts of a circuit operating at the same clock frequency. This repository offers a Verilog implementation of a synchronous FIFO that maintains data integrity and ensures reliable data transfer.
The synchronous FIFO design is based on a classic two-clock memory structure with separate read and write pointers. The core components of the design include:

Write Pointer: Keeps track of the location where the next data element should be written.

Read Pointer: Indicates the position from which the next data element should be read.

Memory Array: Stores the data elements in an array-like structure.

Empty and Full Flags: Indicate whether the FIFO is empty or full, respectively.

Control Logic: Manages the read and write operations, as well as the flags.


B. Asynchronous FIFO.
Asynchronous FIFOs are essential in digital systems that involve transferring data between clock domains that operate independently. This repository offers a Verilog implementation of an asynchronous FIFO that ensures reliable data transfer across different clock frequencies.

In the case of asynchronous FIFO write pointer is aligned to the write clock domain whereas the read pointer is aligned to the read clock domain. Hence, it requires domain crossing to calculate FIFO full and empty conditions. This causes metastability in the actual design. In order to resolve this metastability, 2 flip flops or 3 flip flops synchronizer can be used to pass write and read pointers.  I have designed with 2 flip-flop synchronizers. Please note that a single “2 FF synchronizer” can resolve metastability for only one bit. Hence, depending on write and read pointers multiple 2FF synchronizers are required.


