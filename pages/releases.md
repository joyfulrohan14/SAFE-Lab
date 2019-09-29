---
layout: page
title: Releases
permalink: /facility/
navbar-index: 4
---

The git repo of the lab is available at <a href = "https://gitlab.com/safelab">https://gitlab.com/safelab</a>. The contents are organized into the following topics and sub-topics.


### Industrial Control System Security and Forensics
<a href="#control">Control Logic Attack Datasets</a> <br>
<a href="#shade">Shade Tool for Deep Packet Inspection</a><br>
<a href="#clik">CLIK Toolkit for Attacking Control Logic with Decompilation and Virtual PLC</a><br>

### Cybersecurity Education
<a href="#peer">Peer Instruction</a><br>
<a href="#concept">Concept Maps</a><br>
<a href="#vmi">Virtual Machine Introspection (VMI) for OS Kernel and Application Security</a><br>

-----------------

<h1><center>Industrial Control System Security and Forensics</center></h1>

<a name="control"></a>

### Control Logic Attack Datasets

Remote control-logic injection attacks on programmable logic controllers  (PLCs) impose critical threats to industrial control system(ICS) environments. For instance, Stuxnet infects the control logic of Siemens  S7-300  PLC to sabotage nuclear plants. We present two new stealthy control-logic injection attacks:  1)  Data  Execution and  2)  Fragmentation and  Noise Padding. Data Execution attack subverts signatures (based-on packet-header fields) by transferring control logic to the data blocks of a PLC and then, changes the PLC’s system control flow to execute the attacker’s logic. Fragmentation and Noise Padding attack subverts deep packet inspection (DPI) by appending a sequence of padding bytes in control logic packets while keeping the size of the attacker’s logic in packet payloads significantly small. 

We have created the attack datasets for Schneider Electric's Modicon M221 PLC and Allen-Bradley's MicroLogix 1400 PLC and released them under the MIT license at <a href="https://gitlab.com/safelab/control-logic-attack-datasets" target="_blank">https://gitlab.com/safelab/control-logic-attack-datasets</a>

-----------------

<a name="shade"></a>

### Shade tool for Deep Packet Inspection

We have developed Shade, a novel shadow memory technique that observes the network traffic to maintain a local copy of the current state of a PLC memory. To analyze the memory contents, Shade employs a classification algorithm with 42 unique features categorized into five types at different semantic levels of a control logic code, such as number of rungs, number of consecutive decompiled instructions, and n-grams. We evaluated Shade against control logic injection attacks (i.e., data execution, and fragmentation and noise padding) on two PLCs, Modicon M221 and MicroLogix 1400 from two ICS vendors, Schneider electric and Allen-Bradley, respectively.

We have released the tool, which is available under the MIT license at <a href="https://gitlab.com/safelab/shade-tool-for-deep-packet-inspection" target="_blank">https://gitlab.com/safelab/shade-tool-for-deep-packet-inspection</a>

-----------------


<a name="clik"></a>

### CLIK Toolkit for Attacking Control Logic with Decompilation and Virtual PLC

CLIK is a  new  remote  attack toolkit on  the  control  logic  of  a  programmable  logic  controller  (PLC) in  industrial  control  systems.  It   modifies   the control  logic  running  in  a  remote  target  PLC  automatically  to disrupt  a  physical  process. CLIK also  employs  a  new  virtual PLC approach that hides the malicious modifications by engaging the  engineering  software  with  a  captured  network  traffic  of  the original  (uninfected)  control  logic.  It  is  fully  implemented  on real  hardware/software  used  in  industrial  settings. CLIK consists  of  four  phases  and  takes  less  than  a  minute to  complete  an  attack  cycle.  As  part  of  the  implementation, we  found  a  critical  (zero-day)  vulnerability  in  the  password authentication  mechanism  of  a  target  PLC,  which  allows  the attacker  to  overwrite  password  hash  in  the  PLC  during  the authentication process and gain access to the (protected) control logic. For more details, check out ICS-CERT link, https://ics-cert.us-cert.gov/advisories/ICSA-18-240-01
 
We have released the toolkit, which is available under the MIT license at <a href="https://gitlab.com/safelab/clik" target="_blank">https://gitlab.com/safelab/clik</a>

-----------------


<h1><center>Cybersecurity Education</center></h1>

<a name="peer"></a>

### Peer Instruction

Peer instruction is a well-documented student-centric teaching approach. It encourages each student to actively participate during lectures via structured conceptual questions, to which each student has to reply and then discuss with fellow students. It is markedly different from a traditional lecture-centric method, where, as a common practice, students are asked informal questions during lectures, which typically engages only a few highly motivated students. Peer instruction is effective in engaging students across a variety of classes sizes, from large to small. 

We have developed and released the peer instruction questions for three cybersecurity courses under the MIT license at <a href="https://gitlab.com/safelab/peer-instruction-for-cybersecurity-education" target="_blank">https://gitlab.com/safelab/peer-instruction-for-cybersecurity-education</a>:

* Introduction to Computer Security, 
* Network Penetration Testing
* Digital Forensics

The material is also hosted by <a href="https://www.peerinstruction4cs.org" target="_blank">https://www.peerinstruction4cs.org</a>

-----------------

<a name="concept"></a>
### Concept Maps

The concept map is a graphical tool to represent concepts and the relationships among them on a particular topic. The mapping organizes the concepts in a hierarchy, with the most general ones at the top of the map and the most specific concepts at the bottom. The concepts are connected through arrows (or links) and propositions - a word or phrase describing the link. The concept mapping is a cognitively intensive task that examines the level of a student’s understanding of concepts. It is particularly useful for in-class activities and homework assignments and offers opportunities to improve the effectiveness of the instruction.

Concept mapping can be used to measure the level of a student’s understanding of cybersecurity concepts throughout the course, via Concept Map-based exercises. In particular, a poorly constructed (by a student) map that has missing links and gaps in logic, or incorrect information can allow the instructor to quickly correct misconceptions developed by a student. Conversely, instructors can use a correct map in class as the basis for in-class discussion. The map requires students to actively build their understanding of foundational concepts, and allow them to reason about the bigger picture and the connections among concepts.

We have developed and released the concept maps for three cybersecurity courses under the MIT license at <a href="https://gitlab.com/safelab/concept-maps-for-cybersecurity-education" target="_blank">https://gitlab.com/safelab/concept-maps-for-cybersecurity-education</a>:

* Introduction to Computer Security, 
* Network Penetration Testing
* Digital Forensics

The material is also hosted by <a href="https://clark.center" target="_blank">https://clark.center</a>, a project supported by the National Security Agency (NSA).

-----------------

<a name="vmi"></a>
### Virtual Machine Introspection (VMI) for OS Kernel and Application Security

System virtualization provides a virtual machine introspection (VMI) capability to examine the system resources of a guest VM, such as physical memory, and hard disk from a privileged VM, directly from outside of the VM. In our view, VMI is a powerful functionality to improve the state-of-the-art of cybersecurity hands-on exercises with the goal of providing a holistic view and more insight into students.

We have developed and released a VMI toolkit that is able to access the physical memory of a VM directly from outside the box, and provide the capability of studying not only the user level attacks and defenses, but also the kernel level attacks and defenses. For example, with our VMI toolkit, students can directly manipulate the content of the memory for the demonstration of the underlying computer security concepts. Previously, when performing a traditional hands-on exercise, students ran (benign/malicious) software that eventually made changes in the physical memory, but the changes were transparent to students. Our VMI toolkit allows students to perform such essential changes directly in the memory, and then observe their intended behavior outside the VM. Meanwhile, students can also use our toolkit to perform DKOM attack by modifying the pointers in the process doubly-linked list in memory, and then observe the effect within VM that the process of interest is not visible in the process list.

The toolkit is available under the MIT license at  <a href="https://gitlab.com/safelab/vmi-toolkit-for-cybersecurity-education" target="_blank">https://gitlab.com/safelab/vmi-toolkit-for-cybersecurity-education</a>

-----------------





