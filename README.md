# ComputerNetwrokPa2
Programming Assignment 2 

Include your answers to the following questions in your README file. Remember to keep answers brief.

1. Why do you see a difference in webpage fetch times with small and large router buffers?
Ans: The average webpage fetch time for small router buffer is  . The average webpage fetch time for large router buffer is . We can observe that the webpage fetch time for large router buffer is larger than that of small router buffer. This is because the larger router buffers has longer queue size, so the packets being sent have to wait in the queue for longer time hence causing latency and result in the longer time for large router buffers. 

2. Bufferbloat can occur in other places such as your network interface card (NIC). Check the output of ifconfig eth0 on your VirtualBox VM. What is the (maximum) transmit queue length on the network interface reported by ifconfig? For this queue size and a draining rate of 100 Mbps, what is the maximum time a packet might wait in the queue before it leaves the NIC?
Ans: The maximum transmit queue length reported by ifconfig is 1000.For this queue size and a draining rate of 100 Mbps, the maixum time a packet might wait in the queue before it leav NIC is (packet in TCP layter around 1500 bytes): 
1500 * 1500 * 8 / ( 100 * 10^6) = 0.12s




3. How does the RTT reported by ping vary with the queue size? Write a symbolic equation to describe the relation between the two (ignore computation overheads in ping that might affect the final result).
Ans: approximately the average RTT = 2 * queuesize


4. Identify and describe two ways to mitigate the bufferbloat problem.
Ans:(1)The first way is to reduce the queue size, as indicated by this assignment this can help reduce the latency. (2)The second way is to underutilize the link, use less than capacity, although this might causing waste, this can effectively reduce the latency (as packet will less likly get into buffer due to lower sending rate).