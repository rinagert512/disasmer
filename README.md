# disasmer
Tiny shellcode disasmer that solves some obfuscation
It can be really useful when you analyze malware and some shellcode needs to be reverse engineered

Disasmer resolves:
- **jmp obfuscation** when execution flow mixed by many jumps.
- **calculation**, for example:
> mov    ecx, 0xc6697c55
> add    ecx, 0x9e1c2811
> sub    ecx, 0xbc6e87cb
> add    ecx, 0x612242dd
> xor    ecx, 0x48e797e9
> xor    ecx, 0x4aaf3067
> sub    ecx, 0xb71f8d6
>
> it is obvious, that ecx will be just **33**
> this kind of obfuscation hides some values which can be hints to understand logic of shellcode

Inspired by **Flare-on 10** task __where_am_i__
