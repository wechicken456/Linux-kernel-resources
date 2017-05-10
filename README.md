Linux Kernel Exploitation
=========================

Some exploitation methods and techniques are outdated and don't work anymore on newer kernels.

Pull requests are welcome.

## Exploitation techniques

[2017: "New Reliable Android Kernel Root Exploitation Techniques"](http://powerofcommunity.net/poc2016/x82.pdf) [slides]

[2017: "Unleashing Use-Before-Initialization Vulnerabilities in the Linux Kernel Using Targeted Stack Spraying"](https://www.internetsociety.org/sites/default/files/ndss2017_09-2_Lu_paper.pdf) [whitepaper]

[2016: "Linux Kernel ROP - Ropping your way to # (Part 1)" by Vitaly Nikolenko](https://www.trustwave.com/Resources/SpiderLabs-Blog/Linux-Kernel-ROP---Ropping-your-way-to---(Part-1)/) [article]

[2016: "Linux Kernel ROP - Ropping your way to # (Part 2)" by Vitaly Nikolenko](https://www.trustwave.com/Resources/SpiderLabs-Blog/Linux-Kernel-ROP---Ropping-your-way-to---(Part-2)/) [article]

[2016, Ruxcon: "Exploiting COF Vulnerabilities in the Linux kernel" by Vitaly Nikolenko](https://ruxcon.org.au/assets/2016/slides/ruxcon2016-Vitaly.pdf) [slides]

[2016: "Using userfaultfd" by Lizzie Dixon](https://blog.lizzie.io/using-userfaultfd.html) [article]

[2016, DEF CON 24: "Direct Memory Attack the Kernel" by Ulf Frisk](https://www.youtube.com/watch?v=fXthwl6ShOg) [video]

[2016, MOSEC 2016: "Talk is cheap, show me the code" by Keen Lab](https://speakerdeck.com/retme7/talk-is-cheap-show-me-the-code) [slides]

[2015: "From Collision To Exploitation: Unleashing Use-After-Free Vulnerabilities in Linux Kernel"](https://loccs.sjtu.edu.cn/~romangol/download/papers/gossip_ccs2015.pdf) [whitepaper]

[2015: "Linux Kernel Exploitation" by Patrick Biernat](http://security.cs.rpi.edu/courses/binexp-spring2015/lectures/23/13_lecture.pdf) [slides]

[2014: "Writing kernel exploits" by Keegan McAllister](https://tc.gtisc.gatech.edu/bss/2014/r/kernel-exploits.pdf) [slides]

[2013: "Kernel stack overflows (basics)" by Essa Alkuwari](https://blog.0x80.org/kernel-stack-overflows-basics/) [article]

[2013, Black Hat USA: "Hacking like in the Movies: Visualizing Page Tables for Local Exploitation"](https://www.youtube.com/watch?v=Of6DemoMLaA)

[2012: "Understanding Linux Kernel Vulnerabilities" by Richard Carback](https://www.csee.umbc.edu/courses/undergraduate/421/Spring12/02/slides/ULKV.pdf) [slides]

[2012: "A Heap of Trouble: Breaking the Linux Kernel SLOB Allocator" by Dan Rosenberg](https://www.vsecurity.com//download/papers/slob-exploitation.pdf) [whitepaper]

[2012: "Attacking hardened Linux systems with kernel JIT spraying" by Keegan McAllister](https://mainisusuallyafunction.blogspot.ru/2012/11/attacking-hardened-linux-systems-with.html) [article]

[2012: "A Guide to Kernel Exploitation: Attacking the Core" by Enrico Perla and Massimiliano Oldani](https://www.pdf-archive.com/2011/02/24/a-guide-to-kernel-exploitation/a-guide-to-kernel-exploitation.pdf) [book]

[2012: "The Linux kernel memory allocators from an exploitation perspective" by Patroklos Argyroudis](https://argp.github.io/2012/01/03/linux-kernel-heap-exploitation/) [article]

[2011: "Stackjacking Your Way to grsec/PaX Bypass" by Jon Oberheide](https://jon.oberheide.org/blog/2011/04/20/stackjacking-your-way-to-grsec-pax-bypass/) [article]

[2010: "Much ado about NULL: Exploiting a kernel NULL dereference"](https://blogs.oracle.com/ksplice/entry/much_ado_about_null_exploiting1) [article]

[2010: "Exploiting Stack Overflows in the Linux Kernel" by Jon Oberheide](https://jon.oberheide.org/blog/2010/11/29/exploiting-stack-overflows-in-the-linux-kernel/) [article]

[2010, SOURCE Boston: "Linux Kernel Exploitation: Earning Its Pwnie a Vuln at a Time" by Jon Oberheide](https://jon.oberheide.org/files/source10-linuxkernel-jonoberheide.pdf) [slides]

[2009, CanSecWest: "There's a party at ring0, and you're invited" by Tavis Ormandy and Julien Tinnes](https://www.cr0.org/paper/to-jt-party-at-ring0.pdf) [slides]

[2007: "Kernel-mode exploits primer" by Sylvester Keil and Clemens Kolbitsch](http://old.iseclab.org/projects/vifuzz/docs/exploit.pdf) [whitepaper]

[2007, Phrack: "Attacking the Core : Kernel Exploiting Notes"](http://phrack.org/archives/issues/64/6.txt) [article]

[2007: "The story of exploiting kmalloc() overflows"](http://www.ouah.org/kmallocstory.html) [article]

[2005, CancSecWest: "Large memory management vulnerabilities" by Gael Delalleau](https://cansecwest.com/core05/memory_vulns_delalleau.pdf) [slides]

[2005: "The story of exploiting kmalloc() overflows"](https://argp.github.io/public/kmalloc_exploitation.pdf) [article]


## Writeups

### Information leak

[2016: "Exploiting a Linux Kernel Infoleak to bypass Linux kASLR"](https://marcograss.github.io/security/linux/2016/01/24/exploiting-infoleak-linux-kaslr-bypass.html) [article]

[2010: "Linux Kernel pktcdvd Memory Disclosure" by Jon Oberheide](https://jon.oberheide.org/blog/2010/10/23/linux-kernel-pktcdvd-memory-disclosure/) [article, CVE-2010-3437]

[2009: "Linux Kernel x86-64 Register Leak" by Jon Oberheide](https://jon.oberheide.org/blog/2009/10/04/linux-kernel-x86-64-register-leak/) [article, CVE-2009-2910]

[2009: "Linux Kernel getname() Stack Memory Disclosures" by Jon Oberheide](https://jon.oberheide.org/blog/2009/08/29/linux-kernel-getname-stack-memory-disclosures/) [article, CVE-2009-3001]


### LPE

[2017: "NDAY-2017-0105: Elevation of Privilege Vulnerability in MSM Thermal Drive" by Zuk Avraham](https://blog.zimperium.com/nday-2017-0105-elevation-of-privilege-vulnerability-in-msm-thermal-driver/) [article, CVE-2016-2411]

[2017: "NDAY-2017-0102: Elevation of Privilege Vulnerability in NVIDIA Video Driver" by Zuk Avraham](https://blog.zimperium.com/nday-2017-0102-elevation-of-privilege-vulnerability-in-nvidia-video-driver/) [article, CVE-2016-2435]

[2017: "CVE-2017-2636: exploit the race condition in the n_hdlc Linux kernel driver bypassing SMEP" by Alexander Popov](https://a13xp0p0v.github.io/2017/03/24/CVE-2017-2636.html) [article, CVE-2017-2636]

[2017: "CVE-2017-2636: local privilege escalation flaw in n_hdlc" by Alexander Popov](http://seclists.org/oss-sec/2017/q1/569) [announcement, CVE-2017-2636]

[2017: "CVE-2017-6074: DCCP double-free vulnerability (local root)" by Andrey Konovalov](http://seclists.org/oss-sec/2017/q1/471) [announcement, CVE-2017-6074]

[2016: "CVE-2016-8655 Linux af_packet.c race condition (local root)" by Philip Pettersson](http://seclists.org/oss-sec/2016/q4/607) [announcement, CVE-2016-8655]

[2016, Black Hat: "Rooting Every Android From Extension To Exploitation" by Di Shen and James Fang](https://speakerdeck.com/retme7/rooting-every-android-from-extension-to-exploitation) [slides, CVE-2015-0570, CVE-2016-0820, CVE-2016-2475, CVE-2016-8453]

[2016: "Talk is Cheap, Show Me the Code" by James Fang, Di Shen and Wen Niu](https://speakerdeck.com/retme7/talk-is-cheap-show-me-the-code) [slides, CVE-2015-1805]

[2016: "CVE-2016-3873: Arbitrary Kernel Write in Nexus 9" by Sagi Kedmi](https://sagi.io/2016/09/cve-2016-3873-arbitrary-kernel-write-in-nexus-9/) [article, CVE-2016-3873]

[2016, Project Zero: "Exploiting Recursion in the Linux Kernel" by Jann Horn](https://googleprojectzero.blogspot.de/2016/06/exploiting-recursion-in-linux-kernel_20.html) [article, CVE-2016-1583]

[2016: "ANALYSIS AND EXPLOITATION OF A LINUX KERNEL VULNERABILITY (CVE-2016-0728)" By Perception Point Research Team](http://perception-point.io/2016/01/14/analysis-and-exploitation-of-a-linux-kernel-vulnerability-cve-2016-0728/) [article, CVE-2016-072]

[2016: "CVE20160728 Exploit Code Explained" by Shilong Zhao](http://dreamhack.it/linux/2016/01/25/cve-2016-0728-exploit-code-explained.html) [article, CVE-2016-072]

[2016: "Notes about CVE-2016-7117" by Lizzie Dixon](https://blog.lizzie.io/notes-about-cve-2016-7117.html) [article, CVE-2016-7117]

[2016: "CVE-2016-2384: exploiting a double-free in the usb-midi linux kernel driver" by Andrey Konovalov](https://xairy.github.io/blog/2016/cve-2016-2384) [article, CVE-2016-2384]

[2016: "CVE-2016-6187: Exploiting Linux kernel heap off-by-one" by Vitaly Nikolenko](https://cyseclabs.com/blog/cve-2016-6187-heap-off-by-one-exploit) [article, CVE-2016-6187]

[2016: "CVE-2014-2851 group_info UAF Exploitation" by Vitaly Nikolenko](https://cyseclabs.com/page?n=02012016) [article, CVE-2014-2851]

[2016, HITB Ams: "Perf: From Profiling To Kernel Exploiting" by Wish Wu](https://conference.hitb.org/hitbsecconf2016ams/wp-content/uploads/2015/11/D2T2-Wish-Wu-Perf-From-Profiling-to-Kernel-Exploiting.pdf) [slides, CVE-2016-0819]

[2016, HITB Ams: "Perf: From Profiling To Kernel Exploiting" by Wish Wu](https://www.youtube.com/watch?v=37v14rMtALs) [video, CVE-2016-0819]

[2015: "Android linux kernel privilege escalation vulnerability and exploit (CVE-2014-4322)" by Gal Beniamini](https://bits-please.blogspot.de/2015/08/android-linux-kernel-privilege.html) [article, CVE-2014-4322]

[2015: "Exploiting "BadIRET" vulnerability" by Rafal Wojtczuk](https://labs.bromium.com/2015/02/02/exploiting-badiret-vulnerability-cve-2014-9322-linux-kernel-privilege-escalation/) [article, CVE-2014-9322]

[2015: "Follow-up on Exploiting "BadIRET" vulnerability (CVE-2014-9322)" by Adam Zabrocki](http://blog.pi3.com.pl/?p=509) [article, CVE-2014-9322]

[2015, Black Hat: "Ah! Universal Android Rooting Is Back" by Wen Xu](https://www.blackhat.com/docs/us-15/materials/us-15-Xu-Ah-Universal-Android-Rooting-Is-Back-wp.pdf) [whitepaper, CVE-2015-3636]

[2015, Black Hat: "Ah! Universal Android Rooting Is Back" by Wen Xu](https://www.blackhat.com/docs/us-15/materials/us-15-Xu-Ah-Universal-Android-Rooting-Is-Back.pdf) [slides, CVE-2015-3636]

[2015, Black Hat: "Ah! Universal Android Rooting Is Back" by Wen Xu](https://www.youtube.com/watch?v=HVP1c7Ct1nM) [video, CVE-2015-3636]

[2015: "When is something overflowing" by Keen Team](https://www.slideshare.net/PeterHlavaty/overflow-48573748) [slides]

[2015, Project Zero: "Exploiting the DRAM rowhammer bug to gain kernel privileges" by Mark Seaborn and Thomas Dullien](https://googleprojectzero.blogspot.de/2015/03/exploiting-dram-rowhammer-bug-to-gain.html) [article, rowhammer]

[2014: "Exploiting CVE-2014-0196 a walk-through of the Linux pty race condition PoC" by Samuel Gross](http://blog.includesecurity.com/2014/06/exploit-walkthrough-cve-2014-0196-pty-kernel-race-condition.html) [article, CVE-2014-0196]

[2014: "CVE-2014-4943 - PPPoL2TP DoS Analysis" by Vitaly Nikolenko](https://cyseclabs.com/page?n=01102015) [article, CVE-2014-4943]

[2014: "CVE-2014-4014: Linux Kernel Local Privilege Escalation "exploitation"" by Vitaly Nikolenko](https://cyseclabs.com/blog/cve-2014-4014-local-privilege-escalation) [article, CVE-2014-4014]

[2014: "CVE-2014-4699: Linux Kernel ptrace/sysret vulnerability analysis" by Vitaly Nikolenko](https://cyseclabs.com/blog/cve-2014-4699-linux-kernel-ptrace-sysret-analysis) [article, CVE-2014-4699]

[2014: "How to exploit the x32 recvmmsg() kernel vulnerability CVE 2014-0038" by Samuel Gross](http://blog.includesecurity.com/2014/03/exploit-CVE-2014-0038-x32-recvmmsg-kernel-vulnerablity.html) [article, CVE-2014-0038]

[2014: "Exploiting the Futex Bug and uncovering Towelroot"](http://tinyhack.com/2014/07/07/exploiting-the-futex-bug-and-uncovering-towelroot/) [article, CVE-2014-3153]

[2014: "CVE-2014-3153 Exploit" by Joel Eriksson](http://www.clevcode.org/cve-2014-3153-exploit/) [article, CVE-2014-3153]

[2013: "Privilege Escalation Kernel Exploit" by Julius Plenz](https://blog.plenz.com/2013-02/privilege-escalation-kernel-exploit.html) [article, CVE-2013-1763]

[2013: "A closer look at a recent privilege escalation bug in Linux (CVE-2013-2094)" by Joe Damato](http://timetobleed.com/a-closer-look-at-a-recent-privilege-escalation-bug-in-linux-cve-2013-2094/) [article, CVE-2013-2094]

[2012: "Linux Local Privilege Escalation via SUID /proc/pid/mem Write" by Jason Donenfeld](https://git.zx2c4.com/CVE-2012-0056/about/) [article, CVE-2012-0056]

[2011, DEF CON 19: "Kernel Exploitation Via Uninitialized Stack" by Kees Cook](https://www.defcon.org/images/defcon-19/dc-19-presentations/Cook/DEFCON-19-Cook-Kernel-Exploitation.pdf) [slides, CVE-2010-2963]

[2011, DEF CON 19: "Kernel Exploitation Via Uninitialized Stack" by Kees Cook](https://www.youtube.com/watch?v=jg-wnwnkbsy) [video, CVE-2010-2963]

[2010: "Some Notes on CVE-2010-3081 Exploitability"](https://blog.nelhage.com/2010/11/exploiting-cve-2010-3081/) [article, CVE-2010-3081]

[2010: "CVE-2010-4258: Turning Denial-of-service Into Privilege Escalation" by Nelson Elhage](https://blog.nelhage.com/2010/12/cve-2010-4258-from-dos-to-privesc/) [article, CVE-2010-4258]

[2010: "CVE-2007-4573: The Anatomy of a Kernel Exploit" by Nelson Elhage](https://blog.nelhage.com/2010/02/cve-2007-4573-the-anatomy-of-a-kernel-exploit/) [article, CVE-2007-4573]

[2010: "Linux Kernel CAN SLUB Overflow" by Jon Oberheide](https://jon.oberheide.org/blog/2010/09/10/linux-kernel-can-slub-overflow/) [article, CVE-2010-2959]

[2010: "af_can linux kernel overflow" by Ben Hawkes](http://inertiawar.com/af_can/) [article, CVE-2010-2959]

[2010: "linux compat vulns (part 1)" by Ben Hawkes](http://inertiawar.com/compat1/) [article, CVE-2010-3081]

[2010: "linux compat vulns (part 2)" by Ben Hawkes](http://inertiawar.com/compat2/) [article, CVE-2010-3301]

[2010: "CVE-2010-4258: Turning denial-of-service into privilege escalation" by Nelson Elhage](https://blog.nelhage.com/2010/12/cve-2010-4258-from-dos-to-privesc/) [article, CVE-2010-4258]

[2009: "Linux NULL pointer dereference due to incorrect proto_ops initializations (CVE-2009-2692)"](http://blog.cr0.org/2009/08/linux-null-pointer-dereference-due-to.html) [article, CVE-2009-2692]

[2009: "Even when one byte matters"](https://kernelbof.blogspot.de/2009/07/even-when-one-byte-matters.html) [article, CVE-2009-1046]

[2009: "CVE-2008-0009/CVE-2008-0010: Linux kernel vmsplice(2) Privilege Escalation"](https://xorl.wordpress.com/2009/08/10/cve-2008-0600cve-2008-0010-linux-kernel-vmsplice2-privilege-escalation/) [article, CVE-2008-0009, CVE-2008-0010]

[2008: "vmsplice(): the making of a local root exploit" by Jonathan Corbet](https://lwn.net/Articles/268783/) [article, CVE-2008-0600]

[2004: "Linux kernel do_mremap VMA limit local privilege escalation vulnerability"](http://isec.pl/vulnerabilities/isec-0014-mremap-unmap.txt) [article, CVE-2004-0077]


### RCE

[2016: "CVE Publication: CVE 2016-8633" by Eyal Itkin](https://eyalitkin.wordpress.com/2016/11/06/cve-publication-cve-2016-8633/) [article, CVE-2016-8633]

[2011, DEF CON 19: "Owned Over Amateur Radio: Remote Kernel Exploitation in 2011"](http://cs.dartmouth.edu/~sergey/cs258/2012/Dan-Rosenberg-lecture.pdf) [slides, CVE-2011-1493]

[2011, DEF CON 19: "Owned Over Amateur Radio: Remote Kernel Exploitation in 2011"](https://www.youtube.com/watch?v=kBjD0HITQZA) [video, CVE-2011-1493]

[2009: "When a "potential D.o.S." means a one-shot remote kernel exploit: the SCTP story"](https://kernelbof.blogspot.de/2009/04/kernel-memory-corruptions-are-not-just.html) [article, CVE-2009-0065]


## Protection bypass techniques

[2016: "Linux Kernel x86-64 bypass SMEP - KASLR - kptr_restric"](http://blackbunny.io/linux-kernel-x86-64-bypass-smep-kaslr-kptr_restric/) [article]

[2016, KIWICON: "Practical SMEP bypass techniques on Linux" by Vitaly Nikolenko](https://cyseclabs.com/slides/smep_bypass.pdf) [slides]

[2016: "Micro architecture attacks on KASLR" by Anders Fogh"](https://cyber.wtf/2016/10/25/micro-architecture-attacks-on-kasrl/) [article]

[2016: "Jump Over ASLR: Attacking Branch Predictors to Bypass ASLR" by Dmitry Evtyushkin, Dmitry Ponomarev and Nael Abu-Ghazaleh](http://www.cs.ucr.edu/~nael/pubs/micro16.pdf) [slides]

[2016, CCS: "Prefetch Side-Channel Attacks: Bypassing SMAP and Kernel ASLR" by Daniel Gruss, Clementine Maurice, Anders Fogh, Moritz Lipp and Stefan Mangard](https://www.youtube.com/watch?v=TJTQbs3oJx8) [video]

[2016, Black Hat USA: "Using Undocumented CPU Behavior to See Into Kernel Mode and Break KASLR in the Process"](https://www.youtube.com/watch?v=T3kmq2NLpH4) [video]

[2016, Black Hat USA: "Breaking KASLR with Intel TSX" Yeongjin Jang, Sangho Lee and Taesoo Kim](https://www.blackhat.com/docs/us-16/materials/us-16-Jang-Breaking-Kernel-Address-Space-Layout-Randomization-KASLR-With-Intel-TSX.pdf) [slides]

[2016, Black Hat USA: "Breaking KASLR with Intel TSX" Yeongjin Jang, Sangho Lee and Taesoo Kim](https://www.youtube.com/watch?v=rtuXG28g0CU) [video]

[2016: "Breaking KASLR with micro architecture" by Anders Fogh](https://dreamsofastone.blogspot.ru/2016/02/breaking-kasrl-with-micro-architecture.html) [article]

[2015: "Effectively bypassing kptr_restrict on Android" by Gal Beniamini](https://bits-please.blogspot.de/2015/08/effectively-bypassing-kptrrestrict-on.html) [article]

[2014, Black Hat Europe: "ret2dir: Deconstructing Kernel Isolation" by Vasileios P. Kemerlis, Michalis Polychronakis, Angelos D. Keromytis](https://www.blackhat.com/docs/eu-14/materials/eu-14-Kemerlis-Ret2dir-Deconstructing-Kernel-Isolation-wp.pdf) [whitepaper]

[2014, Black Hat Europe: "ret2dir: Deconstructing Kernel Isolation" by Vasileios Kemerlis](https://www.youtube.com/watch?v=kot-EQ9zf9k) [video]

[2013: "A Linux Memory Trick" by Dan Rosenberg](http://vulnfactory.org/blog/2013/02/06/a-linux-memory-trick/) [article]

[2011: "SMEP: What is It, and How to Beat It on Linux" by Dan Rosenberg](http://vulnfactory.org/blog/2011/06/05/smep-what-is-it-and-how-to-beat-it-on-linux/) [article]

[2009: "Bypassing Linux' NULL pointer dereference exploit prevention (mmap_min_addr)"](http://blog.cr0.org/2009/06/bypassing-linux-null-pointer.html) [article]


## Defensive

[2017: "KASLR is Dead: Long Live KASLR"](https://gruss.cc/files/kaiser.pdf) [whitepaper]

[2017: "Honey, I shrunk the attack surface – Adventures in Android security hardening" by Nick Kralevich](https://www.youtube.com/watch?v=ITL6VHOFQj8) [video]

[2017: "Fine Grained Control-Flow Integrity for The Linux Kernel" by Sandro Rigo, Michalis Polychronakis, Vasileios Kemerlis](https://www.blackhat.com/docs/asia-17/materials/asia-17-Moreira-Drop-The-Rop-Fine-Grained-Control-Flow-Integrity-For-The-Linux-Kernel.pdf) [slides]

[2016: "Emerging Defense in Android Kernel" by James Fang](http://keenlab.tencent.com/en/2016/06/01/Emerging-Defense-in-Android-Kernel/) [article]

[2016: "Randomizing the Linux kernel heap freelists" by Thomas Garnier](https://medium.com/@mxatone/randomizing-the-linux-kernel-heap-freelists-b899bb99c767#.3csq8t23s) [article]

[2015: "Protecting Commodity Operating Systems through Strong Kernel Isolation" by Vasileios Kemerlis](http://www.cs.columbia.edu/~angelos/Papers/theses/vpk_thesis.pdf) [whitepaper]

[2013: "KASLR: An Exercise in Cargo Cult Security" by Brad Spengler](https://forums.grsecurity.net/viewtopic.php?f=7&t=3367) [article]

[2012: "How do I mitigate against NULL pointer dereference vulnerabilities?" by RedHat](https://access.redhat.com/articles/20484) [article]

[2009, Phrack: "Linux Kernel Heap Tampering Detection" by Larry Highsmith](http://phrack.org/archives/issues/66/15.txt) [article]


## Fuzzing & detectors

[2016, Linux Plumbers: "Syzkaller, Future Developement" by Dmitry Vyukov](https://docs.google.com/presentation/d/1iAuTvzt_xvDzS2misXwlYko_VDvpvCmDevMOq2rXIcA/edit#slide=id.p) [slides]

[2016: "Coverage-guided kernel fuzzing with syzkaller"](https://lwn.net/Articles/677764/) [article]

[2016: "Filesystem Fuzzing with American Fuzzy Lop" by Vegard Nossum and Quentin Casasnovas](https://events.linuxfoundation.org/sites/events/files/slides/AFL%20filesystem%20fuzzing%2C%20Vault%202016_0.pdf) [slides]

[2016, ToorCon: "Project Triforce: AFL + QEMU + kernel = CVEs! (or) How to use AFL to fuzz arbitrary VMs"](https://github.com/nccgroup/TriforceAFL/blob/master/slides/ToorCon16_TriforceAFL.pdf) [slides]

[2015, LinuxCon North America: "KernelAddressSanitizer (KASan): a fast memory error detector for the Linux kernel" by Andrey Konovalov](http://events.linuxfoundation.org/sites/events/files/slides/LinuxCon%20North%20America%202015%20KernelAddressSanitizer.pdf) [slides]

[2015, DEF CON 23: "Introduction to USB and Fuzzing" by Matt DuHarte](https://www.youtube.com/watch?v=KWOTXypBt4E) [video]

[2015, Black Hat: "Don't Trust Your USB! How to Find Bugs in USB Device Drivers" by Sergej Schumilo, Ralf Spenneberg, and Hendrik Schwartke](https://www.youtube.com/watch?v=OAbzN8k6Am4)[video]


## Fuzzers

https://github.com/kernelslacker/trinity

https://github.com/google/syzkaller

https://github.com/schumilo/vUSBf

http://web.eece.maine.edu/~vweaver/projects/perf_events/fuzzer/

https://github.com/nccgroup/TriforceLinuxSyscallFuzzer

https://github.com/oracle/kernel-fuzzing

https://github.com/rgbkrk/iknowthis


## Exploits

https://www.exploit-db.com/search/?action=search&description=linux+kernel

https://github.com/offensive-security/exploit-database/tree/master/platforms/linux/local

https://bugs.chromium.org/p/project-zero/issues/list?can=1&q=linux+kernel&colspec=ID+Type+Status+Priority+Milestone+Owner+Summary&cells=ids

http://vulnfactory.org/exploits/

https://www.kernel-exploits.com/

https://github.com/dirtycow/dirtycow.github.io/wiki/PoCs

https://github.com/ScottyBauer/Android_Kernel_CVE_POCs

https://github.com/f47h3r/hackingteam_exploits

https://github.com/xairy/kernel-exploits

https://github.com/ScottyBauer/Android_Kernel_CVE_POCs


## Practice

### CTF tasks

CSAW CTF 2010: [writeup](https://jon.oberheide.org/blog/2010/11/02/csaw-ctf-kernel-exploitation-challenge/), [source](https://jon.oberheide.org/files/csaw.c)

CSAW CTF 2011: [writeup](https://jon.oberheide.org/blog/2011/11/27/csaw-ctf-2011-kernel-exploitation-challenge/), [source](https://jon.oberheide.org/files/SqueamishOssifrage.c)

CSAW CTF 2013: [writeup](https://poppopret.org/2013/11/20/csaw-ctf-2013-kernel-exploitation-challenge/), [source and exploit](https://github.com/mncoppola/Brad-Oberberg)

CSAW CTF 2014: [source and exploit](https://github.com/mncoppola/suckerusu)

CSAW CTF 2015: [writeup 1](https://poppopret.org/2015/11/16/csaw-ctf-2015-kernel-exploitation-challenge/), [writeup 2](http://itszn.com/blog/?p=21), [source and exploit](https://github.com/mncoppola/StringIPC)

Insomni’hack finals 2015: [writeup](https://blog.scrt.ch/2015/03/24/insomnihack-finals-sh1tty-writeup/), [source and exploit](https://github.com/Insomnihack/Insomnihack-2015/tree/master/exploit/sh1tty)

rwth2011 CTF (ps3game): [writeup](http://mslc.ctf.su/wp/rwth2011-ctf-ps3game/)

PlaidCTF 2013 (Servr): [writeup](http://blog.frizn.fr/plaidctf-2013/pwn-400-servr), [source](http://blog.frizn.fr/fil3z/pctf-2013/servr.tar.bz2)

0ctf2016: [writeup](http://dragonsector.pl/docs/0ctf2016_writeups.pdf), [exploit](https://gist.github.com/anonymous/83f96600c5ae851940d6)

0ctf2017: [source and exploit](https://github.com/lovelydream/0ctf2017_kernel_pwn)


### Misc

https://github.com/Fuzion24/AndroidKernelExploitationPlayground

https://github.com/ReverseLab/kernel-pwn-challenge

https://github.com/NoviceLive/research-rootkit

https://github.com/djrbliss/libplayground

[pwnable.kr tasks](http://pwnable.kr/play.php) (syscall, rootkit, softmmu, towelroot, kcrc, exynos)

[RPISEC kernel labs](https://github.com/RPISEC/MBE/tree/master/src/lab10) 

## Tools

https://github.com/jonoberheide/ksymhunter

https://github.com/jonoberheide/kstructhunter

https://github.com/ngalongc/AutoLocalPrivilegeEscalation

https://github.com/PenturaLabs/Linux_Exploit_Suggester

https://github.com/jondonas/linux-exploit-suggester-2

https://github.com/mzet-/linux-exploit-suggester


## Unsorted

https://github.com/mncoppola/Linux-Kernel-CTF

https://crowell.github.io/blog/2014/11/24/hosting-a-local-kernel-ctf-challenge/

https://github.com/ukanth/afwall/wiki/Kernel-security
