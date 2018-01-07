INTEL PROCESSOR SPECTRE MELTDOWN EXPLOIT SOURCE CODE

Spectre breaks the isolation between different applications. It allows an attacker to trick error-free programs, 
which follow best practices, into leaking their secrets. In fact, the safety checks of said best practices actually 
increase the attack surface and may make applications more susceptible to Spectre

Spectre is slightly different from Meltdown. This is so because it can allow hackers to fool the applications 
(even the stable versions of the respective application) running on a machine to give up secret information from 
the Kernal module of the operating system to the hacker with the consent or knowledge of the user.

The Intel Processor core instruction sequence of Meltdown: -

; rcx = kernel address

 ; rbx = probe array

retry:

mov al, byte [rcx]

shl rax, 0xc

jz retry

mov rbx, qword [rbx + rax]




Meltdown breaks the most fundamental isolation between user applications and the operating system. 
This attack allows a program to access the memory, and thus also the secrets, of other programs and the 
operating system.

This vulnerability would allow malicious attacks to take place when a hacker could break the differentiating 
factor between the applications run by the user and the Core Memory of the Computer.
