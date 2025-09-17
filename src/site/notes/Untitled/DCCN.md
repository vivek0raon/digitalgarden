---
{"dg-publish":true,"permalink":"/untitled/dccn/","created":"2025-09-17T13:46:07.595+05:30","updated":"2025-09-17T18:45:38.794+05:30"}
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

| Layer                                   | Function & Description                                                                                                                                                                                                                                                                                    | Examples                                                                                                                                                                                                               |                                   |           |
| --------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------- | --------- |
| **1. Physical Layer**                   | This layer manages the physical interface between a device (like a computer) and the transmission medium (like a cable or wireless signal). It is concerned with the characteristics of the medium, the nature of the signals, the data rate, and the physical connectors.                                | Twisted-pair cable, optical fiber, satellite, terrestrial microwave.                                                                                                                                                   |                                   |           |
| **2. Network Access / Data Link Layer** | This layer is responsible for the exchange of data between a computer and the network it is attached to. It provides the logical interface with the network hardware. When two devices are on different networks, this layer handles access to and routing across the initial network to a router.        | Ethernet, Wi-Fi, ATM, frame relay.                                                                                                                                                                                     |                                   |           |
| **3. Internet Layer**                   | The primary function of this layer is to route data across multiple interconnected networks (an internetwork). It uses the                                                                                                                                                                                | **Internet Protocol (IP)**, which is implemented in both the end systems and the routers connecting the networks. This layer effectively shields higher layers from the details of the physical network configuration. | IPv4, IPv6, ICMP.                 |           |
| **4. Transport Layer (Host-to-Host)**   | This layer provides for the transfer of data between end systems. It can offer a reliable, connection-oriented service using the                                                                                                                                                                          | **Transmission Control Protocol (TCP)**, which includes mechanisms for error control and flow control. Alternatively, it can provide a simpler, connectionless "best-effort" delivery service using the                | **User Datagram Protocol (UDP)**. | TCP, UDP. |
| **5. Application Layer**                | This layer contains the logic needed to support various user applications, such as file transfer or email. For each different application, a separate module is needed that is specific to that application. It provides access to the TCP/IP environment for users and distributed information services. | SMTP, FTP, HTTP, SSH.                                                                                                                                                                                                  |                                   |           |

|                         |                                                                                                                            |                                                                                                                                                                 |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Number of Layers**    | 5 layers (Physical, Network Access, Internet, Transport, Application) as described in this book's primary model.           | 7 layers (Physical, Data Link, Network, Transport, Session, Presentation, Application).                                                                         |
| **Development**         | The protocols came first, and the model was developed to describe the existing protocols.                                  | The model was developed first as a theoretical framework, and then protocols were developed to fit the model.                                                   |
| **Layer Functionality** | The Application layer combines the functions of the OSI model's top three layers (Application, Presentation, and Session). | Functionality is more distinctly separated into layers. The Session layer manages dialogues, and the Presentation layer handles data formatting and encryption. |
| **Usage**               | It is the protocol suite used for the Internet and is the dominant architecture in practice.                               | It serves primarily as a standardized reference model to describe communications functions but is rarely implemented in practice.                               |
| **Protocol Dependency** | The model is practically inseparable from its protocols (TCP, IP, etc.).                                                   | The model is theoretically independent of its protocols, which can be replaced.                                                                                 |

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

| Feature                 | Wired Media (Guided) 🔌                                                                                                                                                | Wireless Media (Unguided) 📡                                                                                                                |                                                             |                                                                                              |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| **Basic Principle**     | Electromagnetic waves are guided along a solid, physical path like copper wire or optical fiber2.                                                                      | Signals are transmitted by an antenna through the atmosphere, outer space, or water3.                                                       |                                                             |                                                                                              |
| **Key Limiting Factor** | The transmission characteristics are determined more by the                                                                                                            | **medium itself**4.                                                                                                                         | The transmission characteristics are determined more by the | **bandwidth of the signal** produced by the antenna5.                                        |
| **Interference**        | Less susceptible to outside interference6. Proper shielding can minimize interference from nearby cables (crosstalk) and other sources7.                               | Highly susceptible to interference from competing signals in overlapping frequency bands, which can distort or cancel the signal8.          |                                                             |                                                                                              |
| **Security**            | Generally more secure. For example, optical fiber is inherently difficult to tap and does not radiate energy, providing a high degree of security from eavesdropping9. | Generally less secure. Wireless LANs can be especially vulnerable to network eavesdropping because signals are broadcast through the air10. |                                                             |                                                                                              |
| **Installation**        | Installation can be costly and time-consuming, as it requires physically laying cables11.                                                                              | Installation is typically faster and less expensive, as it avoids the cost of installing kilometers of cable12.                             |                                                             |                                                                                              |
| **Mobility**            | Offers limited mobility, as devices must be physically connected to the network.                                                                                       | Provides high mobility, allowing users to remain connected while moving.                                                                    |                                                             |                                                                                              |
| **Examples**            |                                                                                                                                                                        | **Twisted-pair cable**, **coaxial cable**, and **optical fiber**13.                                                                         |                                                             | **Terrestrial microwave**, **satellite microwave**, **broadcast radio**, and **infrared**14. |


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

| Function                            | Explanation                                                                                                                                                                                                                                         |                                                                                               |
| ----------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| **Transmission System Utilization** | This involves making efficient use of network resources2. Techniques like                                                                                                                                                                           | **multiplexing** are used to allow multiple devices to share a single transmission facility3. |
| **Interfacing**                     | A device must have an interface to connect with the transmission system4.                                                                                                                                                                           |                                                                                               |
| **Signal Generation**               | The network is responsible for generating the electromagnetic signals that are capable of being propagated through the transmission medium and interpreted as data by the receiver5.                                                                |                                                                                               |
| **Synchronization**                 | The transmitter and receiver must be synchronized6. The receiver must be able to determine when a signal begins and ends, as well as the duration of each signal element7.                                                                          |                                                                                               |
| **Exchange Management**             | This involves the cooperation and establishment of conventions between the two communicating parties8. It includes deciding whether both devices can transmit simultaneously or must take turns, the format of the data, and how to handle errors9. |                                                                                               |
| **Error Detection and Correction**  | The system must detect and correct errors that occur during transmission, as transmitted signals are subject to distortion10.                                                                                                                       |                                                                                               |
| **Flow Control**                    | This function is required to ensure that the source does not send data faster than the destination can process and absorb it11.                                                                                                                     |                                                                                               |
| **Addressing and Routing**          | When more than two devices share a transmission facility, the source must identify the intended destination12. The system must then choose a specific route through the network to deliver the data13.                                              |                                                                                               |
| **Recovery**                        | This is a mechanism to resume an information exchange that was interrupted by a fault in the system, or at least to restore the systems to their state before the exchange began14.                                                                 |                                                                                               |
| **Message Formatting**              | This refers to the agreement between the two communicating parties on the form of the data being exchanged, such as the binary code used for characters15.                                                                                          |                                                                                               |
| **Security**                        | The network must provide security measures to ensure that only the intended receiver gets the data and that the data is not altered in transit16.                                                                                                   |                                                                                               |
| **Network Management**              | This includes the capabilities needed to configure the system, monitor its status, react to failures and overloads, and plan for future growth17.                                                                                                   |                                                                                               |

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