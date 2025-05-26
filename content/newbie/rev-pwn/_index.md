---
title: "Rev/Pwn"
date: 2024-06-18T13:49:17+02:00
---

We have decided to put two common CTF categories together
because they share tools and mindset: **reverse engineering**
and **pwn** (also known as binary exploitation).

So you may be aware that some programming languages are compiled (such
as C, Java, Rust), while others are interpreted (Python, JavaScript,
PHP). To run a C program you first need to compile it to an executable
binary (like a .exe file). Python on the other hand interprets the
instructions directly from the source code.

```
main.c -> compiler -> main.exe
python.exe main.py
```

If you try to open an executable binary in a text editor you
will be greeted by lots of incoherent characters. That is because the
compiler has translated the source code to machine code.
The art of reverse engineering tries to turn machine code into
source code again!

Binary exploitation (pwn) challenges may include a step to reverse 
the machine code, but it is common that you will get the source code
from the start. Here the goal is instead to figure out how insecure
code can be exploited. If you give the binary unexpected input it
might behave in an interesting way. What happens if the name you
enter is too long? What if you order a negative amount of items?
Can you circumvent certain checks?

### Useful platforms
- [Liveoverflow (YouTube playlist)](https://www.youtube.com/playlist?list=PLhixgUqwRTjxglIswKp9mpkfPNfHkzyeN)
- https://overthewire.org/wargames/narnia/
- https://academy.hackthebox.com/module/details/85

### Useful tools
- gdb (GNU debugger)
- radare2
- Ghidra
- pwntools
- [dogbolt.org](https://dogbolt.org)
- [binary.ninja](https://binary.ninja/)
- [cutter.re](https://cutter.re/)

### Try your skills
If you feel ready then you can try to solve out [Rev/Pwn
challenges](http://intro.crl.kauotic.se) (registration code: 1337). When you
have solved three of them, head over to one of our CTF events and you will
get a sticker!

