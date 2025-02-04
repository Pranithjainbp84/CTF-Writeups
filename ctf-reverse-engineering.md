🕵️ Incident:

In this challenge, we were tasked with reverse-engineering a cracked executable file to retrieve the hidden flag. The executable was obfuscated and attempted to detect debugging tools.

🔎 Investigation:

- Step 1: Used IDA Pro and Ghidra to disassemble and analyze the binary code.
- Step 2: Found that the binary had anti-debugging techniques, including checking for the presence of a debugger and obfuscating certain functions.
- Step 3: Disabled the anti-debugging techniques using a combination of x64dbg and custom patching.
- Step 4: Analyzed the control flow to locate the point where the flag was being generated and found a hidden XOR key used to encrypt the flag.
- Step 5: Decrypted the XOR-encrypted string to reveal the flag.

🛡️ Mitigation:

- Step 1: Documented the anti-debugging techniques used and shared them with the team.
- Step 2: Advised developers to improve the security of binaries by implementing more advanced anti-tamper mechanisms.
- Step 3: Recommended using Code Obfuscation and Code Signing to reduce the risk of executable cracking.
