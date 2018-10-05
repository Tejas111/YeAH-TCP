# <b>YeAH-TCP</b>
## <b>Yet another high speed TCP validation, using DCE(Direct-Code-Execution)</b>

### <b>What is YeAH-TCP?</b>
Yet another high speed TCP A high speed TCP congestion control algorithm which uses a mixed loss/delay approach to calculate congestion windows.
Its purpose is to target high efficiency, fairness, and minimizing link loss while keeping network elements load as
low as possible. different considerations like efficiency in the bandwidth exploitation, average packet delay, internal and RTT fairness, friendliness to Reno, robustness to random losses are taken into account. 

### <b> What are Congestion-Control Algorithms?</b>
Congestion control strategies (or algorithms) are used by TCP, the data transmission protocol used by many Internet
 applications. The main goal of a TCP algorithm is to avoid sending more data than the network is capable of transmitting,
 that is, to avoid causing network congestion. Different algorithms respond differently to network loads, but they are all
 based on the same principle of avoiding network congestion. 

### <b>Goals of YeAH-TCP</b>:
* The network capacity is exploited in an efficient way using congestion window rules by exploiting rules of other proposals like STCP,H-TCP.
* The stress induced to the network should be less or equal to that induced by Reno TCP. This means that the packet drops should be reduced.
* TCP friendliness with Reno traffic. The algorithm of YeAH-TCP should be able to compete fairly with the Reno TCP.
* The algorithm should be internally and RTT fair.
* Performance should not be impaired by lossy links.
* Small link buffers should not prevent high performance.

YeAH-TCP must address all the issues mentioned above.

### <b>Using DCE(Direct-Code-Execution) for validation of YeAH-TCP:</b>
The aim of the project is to validate ns-3 YeAH implementation using DCE( A module built on top of ns-3) by comparing the results obtained by simulating linux YeAH.

 **What is DCE(Direct-Code-Execution)?** 

 Direct Code Execution (DCE) is a module for ns-3 that provides facilities to execute, within ns-3, existing implementations
of userspace and kernelspace network protocols or applications without source code changes. 

Features of DCE:

* There is not need to change the source code except recompiling the code.
* The simulation is executed in a single process.
* DCE is memory-efficient.
* supports C,C++ and POSIX socket applications.
* It offers two modes of operation:
   *  Basic-mode where DCE uses the ns-3 TCP stacks.
   * Advanced-mode where DCE uses a Linux network stack instead.


### **References**:
* YeAH-TCP paper(
 [http://infocom.uniroma1.it/~vacirca/yeah/yeah.pdf](http://infocom.uniroma1.it/~vacirca/yeah/yeah.pdf))
* DCE Documentation ([https://www.nsnam.org/docs/dce/manual/ns-3-dce-manual.pdf](https://www.nsnam.org/docs/dce/manual/ns-3-dce-manual.pdf))
