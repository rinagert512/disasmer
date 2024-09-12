# disasmer
Tiny shellcode disasmer that solves some obfuscation <br/>
It can be really useful when you analyze malware and some shellcode needs to be reverse engineered<br/>
<br/>
Disasmer resolves:
- **jmp obfuscation** when execution flow mixed by many jumps.
- **calculation**, for example:<br/>
`mov    ecx, 0xc6697c55`<br/>
`add    ecx, 0x9e1c2811`<br/>
`sub    ecx, 0xbc6e87cb`<br/>
`add    ecx, 0x612242dd`<br/>
`xor    ecx, 0x48e797e9`<br/>
`xor    ecx, 0x4aaf3067`<br/>
`sub    ecx, 0xb71f8d6`<br/>
> it is obvious, that ecx will be just **33**<br/>
> this kind of obfuscation hides some values which can be hints to understand logic of shellcode<br/>
<br/>
Inspired by **Flare-on 10** task __where_am_i__
