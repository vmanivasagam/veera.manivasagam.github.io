---
layout: post
title:  "What is CTF"
date:   2021-02-26 20:54:23 -0700
categories: Software Security
---

I learnt about the Capture the Flag competitions during my Masters degree and our final project was actually a Project Capture the Flag competion and we thoroughly enjoyed it.

`Capture the Flag`: There are different types of Capture the Flag competitions like Jeopardy style and Attack style.

`Jeopardy Style`: Here there are several questions in different categories and as and when the teams solve them they acquire points. The teams will be allowed to move to the next level only when they solve the previous levels.

`Attack-Defense`: Here there is a local network in which each of the teams will get their own system and a copy of the same vulnerable services. The teams will have to race to both attack and defend their services submitting the flags captured from other teams to the gamebot. 

Reference: [CTF][ctf]

`Project Capture The Flag` that I played had a mixture of binary and web vulnerabilities that had to be both attacked and defended. 

Some of the tools that we built that were helpful to the game were 
<ul><li>Availability Checker (Web and Binary applications)</li><li>Network Packet Capturing Tools</li><li>Automatic Exploit thrower</li><li>Backup and Restoration Tool</li><li>Several CheatSheets</li></ul>

Some of the tools that we used during the competition were
<ul><li>gdb - GNU Debugger</li><li>Ghidra (for binary decompiler)</li><li>pwntools</li><li>Socks Proxy</li><li>Wireshark</li><li>objdump</li><li>tcpdump</li></ul>

The framework that the game was built upon was `swpag_client`

Reference: [CTF Codebase][ctfCodebase] - Due to academic integrity, I am maintaining this repo as a private repository.



[ctf]: https://ctftime.org/ctf-wtf/
[ctfCodebase]: https://github.com/545team24/final_code