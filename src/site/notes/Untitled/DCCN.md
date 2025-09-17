---
{"dg-publish":true,"permalink":"/untitled/dccn/","created":"2025-09-17T13:46:07.595+05:30","updated":"2025-09-17T22:52:13.486+05:30"}
---

![Pasted image 20250917141205.png](/img/user/Attachments/Pasted%20image%2020250917141205.png)
Its primary significance lies in being a normalized measure of the signal-to-noise ratio (SNR) that directly determines the achievable **Bit Error Rate (BER)** for a given modulation scheme.
It tells you how much stronger the signal energy for each bit of data is compared to the noise it has to contend with. A higher E_b/N_0 value means a cleaner signal, which leads to fewer errors when the receiver interprets the data.
Eb​/N0​ is normalized for the data rate, it allows for a fair and direct comparison of the performance of different digital modulation techniques (like BPSK, QPSK, 16-QAM, etc.) regardless of the bandwidth they use.

![Pasted image 20250917141522.png](/img/user/Attachments/Pasted%20image%2020250917141522.png)
The various type of transmission impairments a signal encounter are:
- Attenuation
- Distortion
- Noise

**Attenuation** is the **loss of signal strength** as it travels through a transmission medium.
When a signal propagates, its energy is absorbed by the medium, causing its amplitude to decrease. If the signal becomes too weak, the receiver cannot distinguish it from the background noise, leading to errors in data interpretation.
Attenuation is typically measured in **decibels (dB)**
To combat attenuation, **amplifiers** (for analog signals) or **repeaters** (for digital signals) are used at regular intervals to boost the signal strength back to its original level.
![Pasted image 20250917143830.png](/img/user/Attachments/Pasted%20image%2020250917143830.png)

**Distortion** means the signal changes its shape or form. This is particularly critical for composite signals, which are made up of multiple frequencies
A common type is **delay distortion**, where different frequency components of the signal travel at different speeds through the medium.
![Pasted image 20250917144010.png](/img/user/Attachments/Pasted%20image%2020250917144010.png)

**Noise** is any unwanted random signal that gets added to and interferes with the original data signal.
![Pasted image 20250917144116.png](/img/user/Attachments/Pasted%20image%2020250917144116.png)
types of noise:
- **Thermal Noise:** Caused by the random motion of electrons in a conductor. It's unavoidable and present in all electronic devices.
- **Impulse Noise:** Consists of irregular pulses or spikes of short duration but high amplitude, often caused by lightning strikes or power surges.
- **Crosstalk:** Occurs when a signal from one wire "leaks" into an adjacent wire, like hearing a faint, different conversation on a phone line.
- **Induced Noise:** Comes from external sources like motors, power lines, and other electrical equipment that generate electromagnetic fields.

![Pasted image 20250917142857.png](/img/user/Attachments/Pasted%20image%2020250917142857.png)

see copy

![Pasted image 20250917153247.png](/img/user/Attachments/Pasted%20image%2020250917153247.png)

Here is a breakdown of each layer's function, from lowest to highest:

---

### The TCP/IP Model

|Layer|Function & Description|Examples|
|---|---|---|
|**1. Physical Layer**|Manages the physical interface between a device and the transmission medium. It defines characteristics of the medium, signals, data rate, and connectors.|Twisted-pair cable, optical fiber, satellite, terrestrial microwave.|
|**2. Network Access / Data Link Layer**|Responsible for the exchange of data between a computer and the network it is attached to. It provides the logical interface with the network hardware.|Ethernet, Wi-Fi, ATM, frame relay.|
|**3. Internet Layer**|Routes data across multiple interconnected networks using the **Internet Protocol (IP)**. This layer shields higher layers from the details of the physical network.|IPv4, IPv6, ICMP.|
|**4. Transport Layer (Host-to-Host)**|Provides for the transfer of data between end systems, offering either a reliable, connection-oriented service (**TCP**) or a simpler, connectionless service (**UDP**).|TCP, UDP.|
|**5. Application Layer**|Contains the logic needed to support various user applications, like file transfer or email. It provides access to the TCP/IP environment for users.|SMTP, FTP, HTTP, SSH.|

---

### Comparison: TCP/IP vs. OSI Model

| Feature                 | TCP/IP Model                                                                                                               | OSI Model                                                                                                                                      |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| **Number of Layers**    | 5 layers (Physical, Network Access, Internet, Transport, Application).                                                     | 7 layers (Physical, Data Link, Network, Transport, Session, Presentation, Application).                                                        |
| **Development**         | The protocols came first, and the model was developed to describe them.                                                    | The model was developed first as a theoretical framework.                                                                                      |
| **Layer Functionality** | The Application layer combines the functions of the OSI model's top three layers (Application, Presentation, and Session). | Functionality is distinctly separated. The Session layer manages dialogues, and the Presentation layer handles data formatting and encryption. |
| **Usage**               | It is the protocol suite used for the Internet and is the dominant architecture in practice.                               | It serves primarily as a standardized reference model to describe communications functions but is rarely implemented.                          |
| **Protocol Dependency** | The model is practically inseparable from its protocols (TCP, IP, etc.).                                                   | The model is theoretically independent of its protocols.                                                                                       |



![Pasted image 20250917154515.png](/img/user/Attachments/Pasted%20image%2020250917154515.png)

Here are the transmission characteristics for satellite microwave and optical fiber technology.

---

### Satellite Microwave 🛰️

The transmission characteristics of satellite microwaves are defined by their frequency range, propagation delay, and broadcast nature.

- **Optimal Frequency Range:** The best frequency range for satellite transmission is between 1 to 10 GHz1. Frequencies below 1 GHz are susceptible to significant noise from natural sources (like galactic and solar noise) and human-made interference2. Frequencies above 10 GHz are severely attenuated by atmospheric absorption and rain3.
    
- **Frequency Bands:** Satellites use different frequency bands for sending signals from Earth (uplink) and receiving them back (downlink) to avoid interference4. Common bands include:
    
    - **4/6-GHz band:** The most common band, but it has become saturated5.
        
    - **12/14-GHz band:** This band allows for smaller and cheaper earth-station receivers, though it faces greater attenuation problems6.
        
    - **20/30-GHz band:** This band offers greater bandwidth (2500 MHz vs. 500 MHz) and even smaller receivers but experiences more significant attenuation7.
        
- **Propagation Delay:** Due to the vast distances involved, signals traveling to a satellite and back experience a significant propagation delay of about a quarter of a second8. This delay is noticeable in telephone conversations and can create challenges for error and flow control protocols9.
    
- **Broadcast Nature:** Satellite microwave is an inherently broadcast technology10. Multiple stations can transmit to a satellite, and its signal can be received by many stations over a wide area11.
    

---

### Optical Fiber 💡

The transmission characteristics of optical fiber are defined by its physical components, transmission principle, and various operational modes.

- **Transmission Principle:** Optical fiber operates on the principle of **total internal reflection**, where a signal-encoded beam of light is guided through a transparent medium (a glass or plastic core)121212. The interface between the inner core and an outer layer called the cladding acts as a reflector, confining light within the core13.
    
- **Light Sources:** Two types of light sources are used14:
    
    - **Light Emitting Diode (LED):** Less expensive, has a longer operational life, and operates over a greater temperature range15.
        
    - **Injection Laser Diode (ILD):** More efficient and can support greater data rates16.
        
- **Transmission Modes:** There are three primary modes of transmission:
    
    - **Step-index multimode:** Multiple light rays reflect at various shallow angles along the fiber17. This causes signal pulses to spread out over time, limiting the data rate, making it suitable for very short distances18.
        
    - **Single-mode:** The fiber's core radius is greatly reduced, allowing only a single, direct path for light (the axial ray)19. This eliminates the signal distortion found in multimode transmission and is ideal for long-distance applications, including telephone and cable television20.
        
    - **Graded-index multimode:** The refractive index of the core is varied, causing light rays to curve helically instead of zigzagging21. This design reduces the travel distance for different rays, allowing them to arrive at the receiver at roughly the same time. It is often used in local area networks (LANs)22.
        
- **Transmission Windows:** Most optical fiber systems operate in the infrared portion of the spectrum, using four main transmission windows where signal loss is lowest23. Performance is typically specified in terms of wavelength (e.g., 850 nm, 1300 nm, 1550 nm) rather than frequency24. Lower signal loss at higher wavelengths allows for greater data rates over longer distances25.

![Pasted image 20250917160505.png](/img/user/Attachments/Pasted%20image%2020250917160505.png)

**Modulation** is the process of encoding source data onto a continuous, constant-frequency carrier signal by varying one or more of the carrier's fundamental parameters: **amplitude**, **frequency**, or **phase**. This process is necessary to transmit information effectively, especially for unguided (wireless) transmission where baseband signals are impractical to send directly.

---

## Amplitude Modulation (AM) 📻

**Amplitude Modulation (AM)** is a technique where the **amplitude** of the carrier wave is varied in proportion to the input (or modulating) signal, while its frequency and phase remain constant. It's one of the simplest forms of modulation.

Think of the carrier wave as a steady, pure tone. To send information using AM, you would make that tone louder or softer according to the shape of the information signal (like a voice). The resulting AM signal's "envelope" (its overall shape) is an exact reproduction of the original information signal

![Pasted image 20250917161219.png](/img/user/Attachments/Pasted%20image%2020250917161219.png)

Shannon's formula for channel capacity defines the theoretical maximum rate at which data can be transmitted over a communication channel for a given bandwidth and noise level, without error.

---

### The Shannon Capacity Formula Explained

The formula, developed by mathematician Claude Shannon, establishes the relationship between data rate, bandwidth, and noise. It is expressed as:

_C = B log₂ (1 + SNR)_

Where:

- **C** is the **channel capacity** in bits per second (bps), representing the maximum achievable error-free data rate.
    
- **B** is the **bandwidth** of the channel in Hertz (Hz).
    
- **SNR** is the **signal-to-noise ratio**, which is the ratio of the power in a signal to the power of the noise present in the channel.

### Significance of the Formula

Shannon's formula is significant because it provides a fundamental upper limit on communication performance and serves as a vital benchmark for communication system design. Its key implications are:

- **Defines a Theoretical Maximum:** It establishes the **error-free capacity** of a channel, which is the maximum achievable data rate under ideal conditions (assuming only white thermal noise). In practice, rates are lower due to other impairments like impulse noise and delay distortion, but the formula provides a yardstick against which real-world systems can be measured.
    
- **Highlights Key Trade-offs:** The formula clearly shows that for a given noise level, the data rate can be increased by increasing either the signal strength (which improves SNR) or the bandwidth. However, it also reveals a critical trade-off: widening the bandwidth admits more noise into the system, which can in turn decrease the SNR.
    
- **Guides System Design:** It demonstrates that no matter how complex the signal encoding or how many signal levels are used, there is a finite limit to the data rate for a given channel. As an example from the text, for a channel with a bandwidth of 1 MHz and an SNR of 251 (24 dB), the theoretical capacity is approximately 8 Mbps. This helps engineers understand the physical limitations they are working with when designing communication systems.
    

In essence, Shannon's formula is a cornerstone of information theory that defines the boundaries of what is possible in data communications.


![Pasted image 20250917163017.png](/img/user/Attachments/Pasted%20image%2020250917163017.png)
see above

![Pasted image 20250917163221.png](/img/user/Attachments/Pasted%20image%2020250917163221.png)
This is determined by first calculating the channel's maximum capacity using Shannon's formula and then using that result in Nyquist's formula to find the required number of signal levels.

---

### Step 1: Calculate Channel Capacity (Shannon's Formula)

Shannon's formula defines the maximum theoretical data rate (capacity) of a channel based on its bandwidth and signal-to-noise ratio.

The formula is:

_C = B log₂(1 + SNR)_

Given:

- **Bandwidth (B)** = 2 MHz = 2,000,000 Hz
    
- **Signal-to-Noise Ratio (SNR)** = 63
    

Calculation:

1. C = 2,000,000 × log₂(1 + 63)
    
2. C = 2,000,000 × log₂(64)
    
3. Since 2⁶ = 64, log₂(64) is 6.
    
4. C = 2,000,000 × 6
    
5. **C = 12,000,000 bps or 12 Mbps**
    

The theoretical maximum capacity of the channel is 12 Mbps.

---

### Step 2: Determine Required Signal Levels (Nyquist's Formula)

Nyquist's formula relates the data rate to the bandwidth and the number of different signal levels (M) used.

The formula for multilevel signaling is:

_C = 2B log₂(M)_

We can now solve for M using the capacity calculated in the first step.

Given:

- **Capacity (C)** = 12,000,000 bps
    
- **Bandwidth (B)** = 2,000,000 Hz
    

Calculation:

1. 12,000,000 = 2 × 2,000,000 × log₂(M)
    
2. 12,000,000 = 4,000,000 × log₂(M)
    
3. log₂(M) = 12,000,000 / 4,000,000
    
4. log₂(M) = 3
    
5. **M = 2³ = 8**
    

Therefore, 8 discrete signal levels are required to transmit data at the channel's maximum capacity of 12 Mbps.


![Pasted image 20250917163039.png](/img/user/Attachments/Pasted%20image%2020250917163039.png)
The primary difference between wired and wireless media is that wired (guided) media provide a physical path to guide signals, while wireless (unguided) media transmit signals through the air or space without a physical guide1.

Here is a detailed comparison of their transmission characteristics:

---

### Wired Media vs. Wireless Media
You are absolutely correct, my apologies. The table formatting was incorrect and caused the text to be cut off.

Here is the properly formatted table.

| Feature                 | Wired Media (Guided) 🔌                                                                                                                                               | Wireless Media (Unguided) 📡                                                                                                              |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **Basic Principle**     | Electromagnetic waves are guided along a solid, physical path like copper wire or optical fiber.                                                                      | Signals are transmitted by an antenna through the atmosphere, outer space, or water.                                                      |
| **Key Limiting Factor** | The transmission characteristics are determined more by the **medium itself**.                                                                                        | The transmission characteristics are determined more by the **bandwidth of the signal** produced by the antenna.                          |
| **Interference**        | Less susceptible to outside interference. Proper shielding can minimize interference from nearby cables (crosstalk) and other sources.                                | Highly susceptible to interference from competing signals in overlapping frequency bands, which can distort or cancel the signal.         |
| **Security**            | Generally more secure. For example, optical fiber is inherently difficult to tap and does not radiate energy, providing a high degree of security from eavesdropping. | Generally less secure. Wireless LANs can be especially vulnerable to network eavesdropping because signals are broadcast through the air. |
| **Installation**        | Installation can be costly and time-consuming, as it requires physically laying cables.                                                                               | Installation is typically faster and less expensive, as it avoids the cost of installing kilometers of cable.                             |
| **Mobility**            | Offers limited mobility, as devices must be physically connected to the network.                                                                                      | Provides high mobility, allowing users to remain connected while moving.                                                                  |
| **Examples**            | **Twisted-pair cable**, **coaxial cable**, and **optical fiber**.                                                                                                     | **Terrestrial microwave**, **satellite microwave**, **broadcast radio**, and **infrared**.                                                |

![Pasted image 20250917163050.png](/img/user/Attachments/Pasted%20image%2020250917163050.png)
![Pasted image 20250917171855.png](/img/user/Attachments/Pasted%20image%2020250917171855.png)

![Pasted image 20250917171929.png](/img/user/Attachments/Pasted%20image%2020250917171929.png)
Layered protocols are used because they break the complex task of communication into smaller, more manageable subtasks, arranging them in a vertical stack1. This modular design provides two key benefits:

- **Abstraction:** Each layer performs a specific set of functions and hides the details of how those functions are accomplished from the layer above it2. A layer relies on the next lower layer for more basic services and, in turn, provides more advanced services to the layer above it3.
    
- **Flexibility:** Ideally, layers are defined so that changes in one layer (for example, swapping out a physical network technology) do not require changes in the other layers4. This makes it easier to develop, update, and maintain communication systems.

![Pasted image 20250917171939.png](/img/user/Attachments/Pasted%20image%2020250917171939.png)
A data communications network performs numerous essential functions to facilitate the correct and efficient exchange of data between two parties1. These tasks ensure that signals are properly transmitted, managed, and received with integrity.

---

## Key Functions of a Data Communications Network

| Function                            | Explanation                                                                                                                                                                                                                                         |     |
| ----------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --- |
| **Transmission System Utilization** | This involves making efficient use of network resources. Techniques like **multiplexing** are used to allow multiple devices to share a single transmission facility.                                                                               |     |
| **Interfacing**                     | A device must have an interface to connect with the transmission system4.                                                                                                                                                                           |     |
| **Signal Generation**               | The network is responsible for generating the electromagnetic signals that are capable of being propagated through the transmission medium and interpreted as data by the receiver5.                                                                |     |
| **Synchronization**                 | The transmitter and receiver must be synchronized6. The receiver must be able to determine when a signal begins and ends, as well as the duration of each signal element7.                                                                          |     |
| **Exchange Management**             | This involves the cooperation and establishment of conventions between the two communicating parties8. It includes deciding whether both devices can transmit simultaneously or must take turns, the format of the data, and how to handle errors9. |     |
| **Error Detection and Correction**  | The system must detect and correct errors that occur during transmission, as transmitted signals are subject to distortion10.                                                                                                                       |     |
| **Flow Control**                    | This function is required to ensure that the source does not send data faster than the destination can process and absorb it11.                                                                                                                     |     |
| **Addressing and Routing**          | When more than two devices share a transmission facility, the source must identify the intended destination12. The system must then choose a specific route through the network to deliver the data13.                                              |     |
| **Recovery**                        | This is a mechanism to resume an information exchange that was interrupted by a fault in the system, or at least to restore the systems to their state before the exchange began14.                                                                 |     |
| **Message Formatting**              | This refers to the agreement between the two communicating parties on the form of the data being exchanged, such as the binary code used for characters15.                                                                                          |     |
| **Security**                        | The network must provide security measures to ensure that only the intended receiver gets the data and that the data is not altered in transit16.                                                                                                   |     |
| **Network Management**              | This includes the capabilities needed to configure the system, monitor its status, react to failures and overloads, and plan for future growth17.                                                                                                   |     |

![Pasted image 20250917172000.png](/img/user/Attachments/Pasted%20image%2020250917172000.png)
see above
![Pasted image 20250917172015.png](/img/user/Attachments/Pasted%20image%2020250917172015.png)
see above

![Pasted image 20250917172032.png](/img/user/Attachments/Pasted%20image%2020250917172032.png)
You are absolutely right. My apologies for that error in the previous table. Thank you for the correction.

Single-mode fiber allows only a **single path** for light, which is its key advantage over multi-mode fiber.

Here is the corrected comparison table:

---

### Corrected Comparison: Single-Mode vs. Multi-Mode Fiber

| Feature               | Multi-Mode Fiber                                                                                                                                           | Single-Mode Fiber                                                                                                                   |
| --------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| **Light Path**        | Light rays travel along **multiple paths** at various angles within a larger core.                                                                         | Light travels along a **single path**, the axial ray, through a very narrow core.                                                   |
| **Core Radius**       | Has a larger core radius (typically 50 or 62.5 µm).                                                                                                        | Has a much smaller core radius, reduced to the order of a light's wavelength (typically around 10 µm).                              |
| **Signal Distortion** | Experiences distortion because the multiple paths have different lengths, causing light pulses to spread out over time. This limits the maximum data rate. | The distortion found in multi-mode fiber cannot occur because there is only one transmission path, leading to superior performance. |
| **Typical Use**       | Best suited for **short-distance** applications, such as in Local Area Networks (LANs).                                                                    | Typically used for **long-distance** applications, including telephone networks and cable television.                               |
![Pasted image 20250917172053.png](/img/user/Attachments/Pasted%20image%2020250917172053.png)
The required bit rate is **27,200 bps**.

This is calculated by determining the minimum sampling rate based on the highest frequency in the analog signal and then multiplying it by the number of bits used for each digital sample.

---

### Explanation

The conversion of an analog signal to a digital signal involves two main steps: sampling and quantization.

**1. Determine the Sampling Rate (Nyquist Theorem)**

According to the

**Sampling Theorem**, to accurately represent an analog signal, it must be sampled at a rate that is at least twice its highest frequency component1.

- Highest frequency in the signal = **3400 Hz**
    
- Minimum Sampling Rate = 2 × 3400 Hz = **6800 samples per second**
    

**2. Identify the Bits per Sample**

The problem states that a **4-bit converter** is used, which means each of the 6800 samples taken per second will be represented by 4 bits.

**3. Calculate the Total Bit Rate**

The final bit rate is the product of the sampling rate and the number of bits per sample.

- **Bit Rate** = Sampling Rate × Bits per Sample
    
- **Bit Rate** = 6800 samples/sec × 4 bits/sample = **27,200 bps**


![Pasted image 20250917172104.png](/img/user/Attachments/Pasted%20image%2020250917172104.png)
**Sampling Theorem** states that if an analog signal is sampled at regular intervals at a rate higher than twice the highest frequency component of the signal, then the samples contain all the information of the original signal.

![Pasted image 20250917172126.png](/img/user/Attachments/Pasted%20image%2020250917172126.png)
**Delta modulation (DM)** is a technique used to transform analog data into digital signals. It is one of the primary methods employed in **codecs** (coder-decoders). DM offers an alternative to Pulse Code Modulation (PCM) and aims to improve performance or reduce complexity.

Here's a breakdown of the delta modulation technique:

• **Approximation Method**

    ◦ An analog input signal is approximated by a **staircase function**.

    ◦ This staircase function is characterized by its binary behavior: at each sampling interval (Ts), it moves either up or down by a constant amount, known as one **quantization level (δ)**.

    ◦ Essentially, DM produces a bit stream by approximating the _derivative_ of the analog signal, rather than its amplitude directly.

• **Generation of Binary Output**

    ◦ At each sampling time, the analog input is compared to the most recent value of the approximating staircase function.

    ◦ If the value of the sampled analog waveform exceeds that of the staircase function, a **binary '1'** is generated.

    ◦ If the value of the sampled analog waveform does not exceed the staircase function, a **binary '0'** is generated.

    ◦ This ensures that the staircase function constantly changes in the direction of the input signal. Therefore, a '1' is generated if the staircase is to go up, and a '0' if it is to go down.

• **Reconstruction**

    ◦ The binary sequence produced by the DM process is sent to the receiver.

    ◦ At the receiver, this binary sequence is used to reconstruct the staircase function.

    ◦ The reconstructed staircase function can then be smoothed, typically by an integration process or a lowpass filter, to produce an analog approximation of the original analog input signal
    
![Pasted image 20250917175259.png](/img/user/Attachments/Pasted%20image%2020250917175259.png)
The main difference is that

**half-duplex** communication allows data to flow in both directions but only one way at a time, while **full-duplex** communication allows data to flow in both directions simultaneously1.

A good analogy is a conversation:

- **Half Duplex 🚶‍♂️↔️🚶‍♀️:** Like using a walkie-talkie. You have to say "over" to signal that you're done talking and are now listening. Both parties can speak, but not at the same time.
    
- **Full Duplex 🗣️📞🗣️:** Like a telephone call. Both people can talk and listen simultaneously without waiting for the other to finish.
    

---

### Comparison of Half Duplex and Full Duplex

|Feature|Half Duplex|Full Duplex|
|---|---|---|
|**Direction of Flow**|Two-way, but only one direction at a time2.|Two-way, simultaneously3.|
|**Simultaneous Action**|A station can either transmit OR receive at any given moment.|A station can transmit AND receive at the same time4.|
|**Analogy**|Walkie-Talkie|Telephone Call|
|**Performance**|Less efficient because the channel is only used for one direction at a time.|More efficient as it can potentially double the capacity of the link compared to half duplex.|

For context, there is also

**simplex** transmission, where signals are transmitted in only one direction, like a one-way street or a standard radio broadcast5.

![Pasted image 20250917184822.png](/img/user/Attachments/Pasted%20image%2020250917184822.png)

A **protocol** is a set of rules or conventions that govern how corresponding, or peer, layers in two systems communicate

features:
- syntax
- Sematic
- Timing
Examples of protocols include:

• **Transmission Control Protocol (TCP)**, which provides reliable communication between processes across networks and internets.

• **Internet Protocol (IP)**, which is the foundation for internet-based protocols and internetworking.

• **User Datagram Protocol (UDP)**, a connectionless service often used for transaction-oriented applications.

• **High-Level Data Link Control (HDLC)**, a widely used standardized data link control protocol that serves as a baseline for many others.

• **Simple Mail Transfer Protocol (SMTP)**, which provides basic electronic mail transport.

• **Hypertext Transfer Protocol (HTTP)**, the foundation protocol of the World Wide Web.

• **Real-Time Transport Protocol (RTP)**, designed for real-time data transfer in applications like audio and video conferencing.

• **Datagram Congestion Control Protocol (DCCP)**, an alternative transport protocol for multimedia applications needing congestion control without TCP's overhead


![Pasted image 20250917184831.png](/img/user/Attachments/Pasted%20image%2020250917184831.png)
see above

![Pasted image 20250917184844.png](/img/user/Attachments/Pasted%20image%2020250917184844.png)
A **communication model** is a framework that describes the fundamental process of exchanging data between two parties. Its primary purpose is the **exchange of data between a source and a destination**.

The key elements of a communication model are:

• **Source**: This device **generates the data to be transmitted**. Examples include telephones and personal computers. In an electronic mail scenario, the user's input (the message `m`) is the information generated by the source.

• **Transmitter**: This component **transforms and encodes the data generated by the source** into electromagnetic signals suitable for transmission across a physical system. For instance, a modem converts a digital bit stream from a personal computer into an analog signal that can be carried over a telephone network. In the email example, the personal computer's I/O device (transmitter) converts the input data (`g(t)`) into a signal (`s(t)`) for the medium.

• **Transmission System**: This is the **physical or logical path connecting the source and destination**. It can be a single transmission line or a complex network. This system carries the transmitted signal (`s(t)`), which is subject to impairments before reaching the receiver.

• **Receiver**: The receiver **accepts the signal from the transmission system and converts it into a form usable by the destination device**. For example, a modem takes an analog signal from the network and converts it back into a digital bit stream. It attempts to estimate the original signal (`s(t)`) from the received signal (`r(t)`) to produce the output bits (`g'(t)`).

• **Destination**: This device **takes the incoming data from the receiver**. In the email example, the output personal computer buffers the received bits (`g'`) and presents the message (`m'`) to the user, typically as an exact copy of the original message


![Pasted image 20250917184856.png](/img/user/Attachments/Pasted%20image%2020250917184856.png)

Session layer establishes, manages and terminates connection between two devices

The Transport Layer is responsible for end-to-end communication of data packets.
 It is positioned between the network and session layers in the OSI paradigm. The data packets must be taken and sent to the appropriate machine by the network layer. After that, the transport layer receives the packets, sorts them, and looks for faults. Subsequently, it directs them to the session layer of the appropriate computer program. Now, the properly structured packets are used by the session layer to hold the data for the application.

![Pasted image 20250917192841.png](/img/user/Attachments/Pasted%20image%2020250917192841.png)

![Pasted image 20250917184908.png](/img/user/Attachments/Pasted%20image%2020250917184908.png)
The main difference between analog and digital transmission is how they handle signals and deal with attenuation (signal weakening) over distance. **Analog transmission** uses amplifiers to boost the signal, which also amplifies noise, while **digital transmission** uses repeaters to regenerate a fresh, clean signal, preventing the accumulation of noise.

---

### Comparison of Transmission Methods

| Feature                           | Analog Transmission                                                                                                                       | Digital Transmission                                                                                                                               |
| --------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Signal Handling**               | Transmits analog signals without regard to their content, whether they represent analog data (like voice) or digital data (from a modem). | Assumes a binary content in the signal, which can represent digital data or a digitized version of analog data.                                    |
| **Method for Extending Distance** | Uses **amplifiers** to boost the energy of the entire signal, including any noise that has been introduced.                               | Uses **repeaters**, which receive the digital signal, recover the pattern of 1s and 0s, and then retransmit a new, clean signal.                   |
| **Effect of Noise**               | Noise and signal impairments are **cumulative**. As the signal travels through cascaded amplifiers, it becomes more and more distorted.   | The effects of noise are **not cumulative**. Because the signal is regenerated at each repeater, data integrity is maintained over long distances. |

![Pasted image 20250917184921.png](/img/user/Attachments/Pasted%20image%2020250917184921.png)

see above


![Pasted image 20250917184937.png](/img/user/Attachments/Pasted%20image%2020250917184937.png)

see copy

![Pasted image 20250917184956.png](/img/user/Attachments/Pasted%20image%2020250917184956.png)



![Pasted image 20250917185011.png](/img/user/Attachments/Pasted%20image%2020250917185011.png)
The main difference is that a **unipolar signal** uses signal elements that all have the same algebraic sign (either all positive or all negative), while **polar signaling** uses elements with opposite signs (one positive and one negative).

---

### Unipolar vs. Polar Signaling

|Feature|Unipolar Signaling|Polar Signaling|
|---|---|---|
|**Voltage Levels**|Uses two voltage levels, but one is always zero. For example, a binary **1** might be represented by a positive voltage (+V) and a binary **0** by zero voltage (0V).|Uses two non-zero voltage levels of opposite polarity. For example, a binary **1** might be represented by a positive voltage (+V) and a binary **0** by a negative voltage (-V).|
|**Algebraic Sign**|All signal elements have the same sign (e.g., all are non-negative).|Signal elements have both positive and negative signs.|

In simpler terms, a unipolar signal turns "on" (positive voltage) and "off" (zero voltage), while a polar signal switches between "positive" and "negative" states.

![Pasted image 20250917185021.png](/img/user/Attachments/Pasted%20image%2020250917185021.png)

![Untitled.jpg](/img/user/Attachments/Untitled.jpg)

![Pasted image 20250917185038.png](/img/user/Attachments/Pasted%20image%2020250917185038.png)

The Modulation rate is the rate at which signal element are transmitted over a communication channel. It is measured in baud. which means signal element per second.

### Modulation Rate vs. Data Rate

It is important to distinguish the modulation rate from the **data rate**.

- **Data Rate:** The rate at which data (bits) are transmitted, measured in bits per second (bps).
    
- **Modulation Rate:** The rate at which the signal level changes.

**D = R / L** defines the relationship between the **modulation rate** and the **data rate** in a digital communication system

The general relationship is given by the formula: _D = R / log₂(M)_

Where:

- **D** = Modulation rate (baud)
    
- **R** = Data rate (bps)
    
- **M** = Number of different signal elements used (M = 2ᴸ)
- **L** is the **number of bits per signal element**.

![Pasted image 20250917185046.png](/img/user/Attachments/Pasted%20image%2020250917185046.png)

**Amplitude Shift Keying (ASK)** is a modulation technique where digital data is represented by varying the **amplitude** (or strength) of a carrier wave. The frequency and phase of the carrier wave remain constant

In the most common form of ASK, one of the two amplitudes is zero.

- **Binary 1:** Represented by the presence of the carrier wave at a constant amplitude.
    
- **Binary 0:** Represented by the absence of the carrier wave (zero amplitude).
    

This can be expressed mathematically as:

_s(t)_ = { Acos(2π f_c t) for binary 1, 0 for binary 0 }

# 2023

![Pasted image 20250917214017.png](/img/user/Attachments/Pasted%20image%2020250917214017.png)
**TCP/IP protocol architecture** is a five-layer model that organizes the complex task of computer communication into a set of manageable, independent layers. Each layer is responsible for a specific function and provides services to the layer above it while using the services of the layer below.

### The TCP/IP Model

| Layer                                   | Function & Description                                                                                                                                                         | Examples                                                             |     |
| --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------- | --- |
| **1. Physical Layer**                   | Manages the physical interface between a device and the transmission medium. It defines characteristics of the medium, signals, data rate, and connectors.                     | Twisted-pair cable, optical fiber, satellite, terrestrial microwave. |     |
| **2. Network Access / Data Link Layer** | Responsible for the exchange of data between a computer and the network it is directly attached to. It provides the logical interface with the network hardware.               | Ethernet, Wi-Fi, ATM, frame relay.                                   |     |
| **3. Internet Layer**                   | Routes data packets across multiple interconnected networks using the **Internet Protocol (IP)**. This layer shields higher layers from the details of the physical network.   | IPv4, IPv6, ICMP.                                                    |     |
| **4. Transport Layer (Host-to-Host)**   | Provides for the end-to-end transfer of data between applications. It can be reliable (**TCP**) or unreliable (**UDP**) and handles tasks like error control and flow control. | TCP, UDP.                                                            |     |
| **5. Application Layer**                | Contains the logic needed to support various user applications, like file transfer or email. It provides access to the TCP/IP environment for users.                           | SMTP, FTP, HTTP, SSH.                                                |     |
|                                         |                                                                                                                                                                                |                                                                      |     |
|                                         |                                                                                                                                                                                |                                                                      |     |
|                                         |                                                                                                                                                                                |                                                                      |     |




![Pasted image 20250917214025.png](/img/user/Attachments/Pasted%20image%2020250917214025.png)
see above for fist part

Impairments solution:
Solutions for transmission impairments involve a combination of boosting signal strength, compensating for distortion, and using higher-level protocols to handle errors.

---

### Solution for Attenuation

Attenuation, the weakening of a signal over distance, is managed in two ways:

- **Boosting Signal Strength:** For both analog and digital signals, **amplifiers** or **repeaters** are inserted at regular intervals along a transmission line to boost the signal strength and ensure it is detectable at the receiver. 1
    
- **Correcting Attenuation Distortion:** Because attenuation is often greater at higher frequencies, **equalization techniques** are used to balance the loss across the entire spectrum. This can be done with
    
    **loading coils** on telephone lines or with specialized amplifiers that boost higher frequencies more than lower ones. 2
    

---

### Solution for Delay Distortion

Delay distortion, where different frequency components of a signal travel at different speeds, is also corrected using

**equalizing techniques**. 3These equalizers compensate for the varying delays, ensuring that all components of the signal arrive at the receiver at roughly the same time to prevent

**intersymbol interference**. 4

---

### Solutions for Noise

The solution for noise depends on the type:

- **Thermal Noise:** This type of noise is unavoidable and cannot be eliminated. 5 The solution is to design a system with a high enough
    
    **Signal-to-Noise Ratio (SNR)** so the signal is strong enough to be intelligible despite the background noise.
    
- **Crosstalk and Intermodulation Noise:** These are managed through proper physical design, such as using **shielded cabling** to prevent unwanted coupling between signal paths and ensuring system components are not overloaded. 6
    
- **Impulse Noise:** This is the primary cause of errors in digital data. 7 Rather than being filtered out, its effects are handled at higher protocol layers using:
    
    - **Error detection and correction codes** to find and, in some cases, fix bit errors caused by noise spikes. 8
        
    - **Automatic Repeat Request (ARQ)** protocols that retransmit any data frames corrupted by noise. 9


![Pasted image 20250917214038.png](/img/user/Attachments/Pasted%20image%2020250917214038.png)
The power of the signal at 10 km is **2.52 mW**.

---

## Step-by-Step Calculation

1. Calculate the Total Loss in dB:
    
    The total loss is the loss per kilometer multiplied by the total distance.
    
    - **Loss per km:** -0.2 dB/km
        
    - **Distance:** 10 km
        
    - **Total Loss (L_dB):** -0.2 dB/km × 10 km = **-2 dB**
        
2. Use the Decibel Formula to Find the Final Power:
    
    The formula for loss in decibels (dB) is:
    
    - _L_dB = 10 log₁₀(P_out / P_in)_
        
    
    Where:
    
    - **L_dB** = Total loss in decibels (-2 dB)
        
    - **P_in** = Input power (4 mW)
        
    - **P_out** = Output power (the value we need to find)
        
    
    Plugging in the values:
    
    -2 = 10 log₁₀(P_out / 4)
    
    -0.2 = log₁₀(P_out / 4)
    
    To solve for P_out, we take the antilog (10 to the power of) of both sides:
    
    10⁻⁰·² = P_out / 4
    
    0.6309 = P_out / 4
    
    P_out = 0.6309 × 4
    
    P_out ≈ 2.52 mW

![Pasted image 20250917214054.png](/img/user/Attachments/Pasted%20image%2020250917214054.png)

Guided transmission media are physical cables that guide electromagnetic waves along a solid path. The three primary types are twisted-pair cable, coaxial cable, and optical fiber.

---

### Twisted-Pair Cable 銅線

Twisted-pair cable is the least expensive and most widely used guided medium1.

- **Description:** It consists of two insulated copper wires twisted together in a spiral pattern2. The twisting helps to reduce electrical interference, known as crosstalk, between adjacent pairs in a cable3. These pairs are often bundled together into a larger cable.
    
- **Applications:** It's the most common medium for both analog and digital signals in telephone networks (as subscriber loops) and is widely used for Local Area Networks (LANs), such as Ethernet44.
    

**Advantages:**

- It is the least expensive guided medium5.
    
- It is easier to install and work with than other cable types6.
    

**Disadvantages:**

- It is limited in distance, bandwidth, and data rate compared to coaxial and optical fiber cable7.
    
- It is susceptible to signal reflections and interference from crosstalk8.
    

---

### Coaxial Cable 同軸ケーブル

Coaxial cable can operate over a wider range of frequencies and support more stations on a shared line than twisted-pair cable9.

- **Description:** It consists of a single inner wire conductor surrounded by a hollow outer cylindrical conductor10. An insulating material separates the two conductors, and the entire cable is covered by a protective jacket11.
    
- **Applications:** Coaxial cable is widely used for television distribution (cable TV), long-distance telephone transmission, and short-run computer system links12.
    

**Advantages:**

- It has superior frequency characteristics compared to twisted-pair and can be used at higher frequencies and data rates13.
    
- Its shielded, concentric construction makes it much less susceptible to interference and crosstalk than twisted-pair14.
    

**Disadvantages:**

- It suffers from attenuation, thermal noise, and intermodulation noise, which constrain its performance15.
    
- For long-distance transmission, amplifiers are required every few kilometers16.
    

---

### Optical Fiber Cable 光ファイバーケーブル

Optical fiber is a thin, flexible medium made of glass or plastic that is capable of guiding an optical ray17.

- **Description:** An optical fiber strand consists of three concentric sections: an inner **core**, an outer **cladding** that reflects light back into the core, and a protective **buffer coating**18. These strands are bundled into a cable protected by an outer jacket19.
    
- **Applications:** Optical fiber is used extensively in long-haul telecommunications trunks, metropolitan and rural trunks, and is increasingly used for subscriber loops and LANs20.
    

**Advantages:**

- **Greater Capacity:** It offers immense potential bandwidth, with demonstrated data rates of hundreds of gigabits per second (Gbps) over long distances21.
    
- **Smaller Size and Lighter Weight:** It is considerably thinner and lighter than coaxial or twisted-pair cable for a comparable information-carrying capacity22.
    
- **Lower Attenuation:** Signal weakening is significantly lower for optical fiber and is constant over a wide range of frequencies23.
    
- **Electromagnetic Isolation:** It is not affected by external electromagnetic fields, making it immune to interference, impulse noise, and crosstalk. It is also highly secure from eavesdropping24.
    
- **Greater Repeater Spacing:** Repeaters, which regenerate the signal, can be spaced tens or even hundreds of kilometers apart, reducing cost and sources of error25.
    

**Disadvantages:**

- The manufacturing of ultrapure fiber is difficult, and higher-loss multicomponent glass fibers are used as a more economical alternative26.
    
- Plastic fiber, while less costly, has higher losses and is only suitable for shorter-haul links27.


![Pasted image 20250917214113.png](/img/user/Attachments/Pasted%20image%2020250917214113.png)
see copy

![Pasted image 20250917214130.png](/img/user/Attachments/Pasted%20image%2020250917214130.png)
![Pasted image 20250917222923.png](/img/user/Attachments/Pasted%20image%2020250917222923.png)
![Pasted image 20250917214145.png](/img/user/Attachments/Pasted%20image%2020250917214145.png)

Here are the transmission characteristics for terrestrial and satellite microwave communications.

---

## Terrestrial Microwave 🗼

Terrestrial microwave systems use highly directional, point-to-point antennas. Their transmission characteristics are defined by their frequency range, attenuation, and susceptibility to interference.

- **Frequency Range:** Common frequencies used are in the range of 1 to 40 GHz1. The higher the frequency, the higher the potential bandwidth and data rate2.
    
- **Attenuation:** The primary source of signal loss is attenuation, which increases with distance3. Unlike wired media, this loss varies as the square of the distance, which allows for much longer repeater spacing of 10 to 100 km4. Signal attenuation is increased by rainfall, with the effect becoming especially noticeable above 10 GHz5.
    
- **Interference:** As microwave transmission areas can overlap, interference is a potential issue6. Because of this, the assignment of frequency bands is strictly regulated7.
    

---

## Satellite Microwave 🛰️

A communication satellite acts as a microwave relay station, linking two or more ground-based stations.

- **Optimal Frequency Range:** The optimal frequency range for satellite transmission is between 1 and 10 GHz8. Below 1 GHz, signals are subject to significant natural and human-made noise, while above 10 GHz, signals are severely attenuated by atmospheric absorption and precipitation9.
    
- **Uplink/Downlink Frequencies:** To avoid interference, a satellite must transmit and receive on different frequencies10. Signals are sent from an earth station on an
    
    **uplink** frequency and retransmitted by the satellite on a **downlink** frequency11. Common frequency bands include the 4/6-GHz, 12/14-GHz, and 20/30-GHz bands12.
    
- **Propagation Delay:** Due to the long distances involved, there is a significant signal propagation delay of about a quarter of a second from an earth station to the satellite and back13.
    
- **Broadcast Nature:** Satellite transmission is an inherently broadcast facility14. A signal transmitted from a satellite can be received by many stations over a wide geographic area15.


![Pasted image 20250917214157.png](/img/user/Attachments/Pasted%20image%2020250917214157.png)

**Delta Modulation (DM)** is a technique for converting an analog signal into a digital bit stream. Its working principle is to approximate the analog input with a **staircase function** that moves up or down by a fixed step size at each sampling interval.

---

### How Delta Modulation Works

The process generates a single binary digit for each sample based on a simple comparison:

1. **Comparison:** At each sampling time, the analog input signal is compared to the most recent value of the approximating staircase function. 1
    
2. **Binary Output:**
    
    - If the input signal is
        
        **greater** than the staircase value, a **1** is generated, and the staircase moves **up** by one step (δ). 2
        
    - If the input signal is
        
        **less** than the staircase value, a **0** is generated, and the staircase moves **down** by one step (δ). 3
        

The output of this process is a binary sequence that represents the change, or derivative, of the analog signal rather than its direct amplitude. 4At the receiving end, this bit stream is used to reconstruct the staircase function, which is then smoothed to produce an approximation of the original analog signal. 5

### Errors in Delta Modulation

The accuracy of Delta Modulation depends on the chosen step size (δ), which creates a trade-off between two types of errors6:

- **Slope Overload Noise:** If the analog signal changes more rapidly than the staircase can follow, the staircase falls behind. 7 This occurs when the step size is too small.
    
- **Quantizing Noise:** If the analog signal changes very slowly, the staircase function overshoots the signal, alternating between steps above and below it. 8 This occurs when the step size is too large.
