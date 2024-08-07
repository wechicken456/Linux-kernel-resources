Linux Kernel Exploitation
=========================

A collection of links related to Linux kernel security and exploitation.

Updated bimonthly. Pull requests are welcome as well.

Follow [@andreyknvl](https://twitter.com/andreyknvl) on Twitter or [@xairy@infosec.exchange](https://infosec.exchange/@xairy) on Mastodon to be notified of updates.

Subscribe to @linkersec on [Telegram](https://t.me/linkersec), [Twitter](https://twitter.com/linkersec), [Mastodon](https://infosec.exchange/@linkersec), or [Reddit](https://www.reddit.com/r/linkersec) for highlights.


## Trainings

See [xairy.io/trainings/](https://xairy.io/trainings/).


## Contents

- [Books](#books)
- [Concepts](#concepts)
- [Techniques](#techniques)
	- [Exploitation](#exploitation)
	- [Protection Bypasses](#protection-bypasses)
- [Vulnerabilities](#vulnerabilities)
	- [Info-leaks](#info-leaks)
	- [LPE](#lpe)
	- [RCE](#rce)
	- [Other](#other)
- [Finding Bugs](#finding-bugs)
- [Defensive](#defensive)
- [Exploits](#exploits)
- [Tools](#tools)
	- [Fuzzers](#fuzzers)
	- [Assorted](#assorted)
- [Practice](#practice)
	- [Workshops](#workshops)
	- [CTF Tasks](#ctf-tasks)
	- [Other Tasks](#other-tasks)
	- [Playgrounds](#playgrounds)
	- [Infrastructure](#infrastructure)
- [Misc](#misc)


## Books

2014: "Android Hacker's Handbook" by Joshua J. Drake [[book](https://www.goodreads.com/book/show/17628293-android-hacker-s-handbook)]

2012: "A Guide to Kernel Exploitation: Attacking the Core" by Enrico Perla and Massimiliano Oldani [[book](https://www.goodreads.com/book/show/9224826-a-guide-to-kernel-exploitation)] [[materials](https://github.com/yrp604/atc-sources)]

## Concepts
### [Linux Virtual File System (VFS)](https://www.kernel.org/doc/html/latest/filesystems/vfs.html?highlight=inode)

### io_uring
[Authors' paper](https://kernel.dk/io_uring.pdf)

(Examples of usage)[https://unixism.net/2020/04/io-uring-by-example-part-1-introduction/]

<https://chomp.ie/Blog+Posts/Put+an+io_uring+on+it+-+Exploiting+the+Linux+Kernel>

<https://anatomic.rip/cve-2023-2598/#poc>


## Techniques

### Exploitation

[2024: "Binary Exploitation Notes: Kernel" by Andrej Ljubic](https://ir0nstone.gitbook.io/notes/types/kernel) [articles]

[2024: "Take a Step Further: Understanding Page Spray in Linux Kernel Exploitation"](https://arxiv.org/pdf/2406.02624) [paper]

[2024: "GhostRace: Exploiting and Mitigating Speculative Race Conditions"](https://www.vusec.net/projects/ghostrace/) [paper]

[2024: "K-LEAK: Towards Automating the Generation of Multi-Step Infoleak Exploits against the Linux Kernel"](https://www.ndss-symposium.org/wp-content/uploads/2024-935-paper.pdf) [paper]

[2024: "Beyond Control: Exploring Novel File System Objects for Data-Only Attacks on Linux Systems"](https://arxiv.org/pdf/2401.17618.pdf) [paper]

[2023: "No Tux Given: Diving Into Contemporary Linux Kernel Exploitation" by sam4k](https://sam4k.com/content/files/2024/01/no_tux_given.pdf) [slides]

[2023: "Linux Kernel Exploitation series" by santaclz](https://santaclz.github.io/2023/11/03/Linux-Kernel-Exploitation-Getting-started-and-BOF.html) [article] [[part2](https://santaclz.github.io/2024/01/20/Linux-Kernel-Exploitation-Heap-techniques.html)] [[part 3](https://santaclz.github.io/2024/01/29/Linux-Kernel-Exploitation-exploiting-race-condition-and-UAF.html)]

[2023: "RetSpill: Igniting User-Controlled Data to Burn Away Linux Kernel Protections"](https://kylebot.net/papers/retspill.pdf) [paper]

[2023: "Understanding Dirty Pagetable - m0leCon Finals 2023 CTF Writeup"](https://ptr-yudai.hatenablog.com/entry/2023/12/08/093606) [article]

[2023: "Abusing RCU callbacks with a Use-After-Free read to defeat KASLR"](https://anatomic.rip/abusing_rcu_callbacks_to_defeat_kaslr/) [article]

[2023: "Evils in the Sparse Texture Memory: Exploit Kernel Based on Undefined Behaviors of Graphic APIs"](https://i.blackhat.com/EU-23/Presentations/EU-23-Jin-Evils-in-the-Sparse-Texture.pdf) [slides] [[abstract](https://www.blackhat.com/eu-23/briefings/schedule/index.html#evils-in-the-sparse-texture-memory-exploit-kernel-based-on-undefined-behaviors-of-graphic-apis-35059)]

[2023: "Breaking Hardware-Assisted Kernel Control-Flow Integrity with Page-Oriented Programming" by Seunghun Han](https://i.blackhat.com/BH-US-23/Presentations/US-23-Han-Lost-Control-Breaking-Hardware-Assisted-Kernel.pdf) [slides]

[2023: "Make KSMA Great Again: The Art of Rooting Android devices by GPU MMU features" by Yong Wang](https://i.blackhat.com/BH-US-23/Presentations/US-23-WANG-The-Art-of-Rooting-Android-devices-by-GPU-MMU-features.pdf) [[video](https://www.youtube.com/watch?v=2qkwSPnQqrU)] [slides]

[2023: "A new method for container escape using file-based DirtyCred" by Choo Yi Kai](https://starlabs.sg/blog/2023/07-a-new-method-for-container-escape-using-file-based-dirtycred/) [article]

[2023: "prctl anon_vma_name: An Amusing Linux Kernel Heap Spray" by Cherie-Anne Lee](https://starlabs.sg/blog/2023/07-prctl-anon_vma_name-an-amusing-heap-spray/) [article]

[2023: "Dirty Pagetable: A Novel Exploitation Technique To Rule Linux Kernel" by Nicolas Wu](https://yanglingxi1993.github.io/dirty_pagetable/dirty_pagetable.html) [article]

[2023: "Exploit Engineering – Attacking the Linux Kernel" by Alex Plaskett and Cedric Halbronn](https://research.nccgroup.com/wp-content/uploads/2023/05/exploit-engineering-linux-kernel.pdf) [slides] [[video](https://www.youtube.com/watch?v=9wgHENj_YNk)]

[2023: "Algorithmic Heap Layout Manipulation in the Linux Kernel" by Max Ufer and Daniel Baier](https://escholarship.org/content/qt8ss3f7w1/qt8ss3f7w1.pdf) [paper] [[artifacts](https://github.com/fkie-cad/Algorithmic-Heap-Layout-Manipulation-in-the-Linux-Kernel)]

[2023: "The Return of Stack Overflows in the Linux Kernel" by Davide Ornaghi](https://conference.hitb.org/hitbsecconf2023ams/materials/D2%20COMMSEC%20-%20The%20Return%20of%20Stack%20Overflows%20in%20the%20Linux%20Kernel%20-%20Davide%20Ornaghi.pdf) [slides] [[video](https://www.youtube.com/watch?v=5b9UlBrzvG0)]

[2023: "Exploiting null-dereferences in the Linux kernel" by Seth Jenkins](https://googleprojectzero.blogspot.com/2023/01/exploiting-null-dereferences-in-linux.html) [article]

[2023: "PSPRAY: Timing Side-Channel based Linux Kernel Heap Exploitation Technique"](https://www.usenix.org/system/files/sec23summer_79-lee-prepub.pdf) [paper] [[video](https://www.youtube.com/watch?v=C3ta-uUthfA)]

[2023: "Linux Kernel PWN | 06 DirtyCred"](https://blog.wohin.me/posts/linux-kernel-pwn-06/) [article]

[2023: "Linux Kernel PWN | 05 ret2dir"](https://blog.wohin.me/posts/linux-kernel-pwn-05/) [article]

[2022: "Ret2page: The Art of Exploiting Use-After-Free Vulnerabilities in the Dedicated Cache"](https://i.blackhat.com/USA-22/Thursday/US-22-WANG-Ret2page-The-Art-of-Exploiting-Use-After-Free-Vulnerabilities-in-the-Dedicated-Cache.pdf) [slides] [[video](https://www.youtube.com/watch?v=HZk2egYDXxg)]

[2022: "Devils Are in the File Descriptors: It Is Time To Catch Them All" by Le Wu](https://i.blackhat.com/USA-22/Wednesday/US-22-Wu-Devils-Are-in-the-File.pdf) [slides] [[video](https://www.youtube.com/watch?v=dIVjQrqpKC0)]

[2022: "FUSE for Linux Exploitation 101"](https://exploiter.dev/blog/2022/FUSE-exploit.html) [article]

[2022: "Kernel Exploit Recipes"](https://drive.google.com/file/d/1kRHgQ9qDr4vgxJ4rVL-UNKvCamva_TRB/view) [brochure]

[2022: "pipe_buffer arbitrary read write" by Jayden R](https://interruptlabs.co.uk/labs/pipe_buffer/) [article]

[2022: "Joy of exploiting the Kernel"](https://docs.google.com/presentation/d/e/2PACX-1vR4mpH3aARLMOhJemVGEw1cduXPEo_PvrbZMum8QwOJ6rhZvvezsif4qtgSydVVt8jPT1fztgD5Mj7q/pub?slide=id.p) [slides]

[2022: "An exploit primitive in the Linux kernel inspired by DirtyPipe"](https://github.com/veritas501/pipe-primitive) [article]

[2022: "DirtyCred: Escalating Privilege in Linux Kernel"](https://zplin.me/papers/DirtyCred.pdf) [paper] [[slides](https://zplin.me/papers/DirtyCred_CCS_slides.pdf)] [[artifacts](https://github.com/Markakd/DirtyCred)]

[2022: "DirtyCred: Cautious! A New Exploitation Method! No Pipe but as Nasty as Dirty Pipe"](https://i.blackhat.com/USA-22/Thursday/US-22-Lin-Cautious-A-New-Exploitation-Method.pdf) [slides] [[artifacts](https://github.com/Markakd/DirtyCred)]

[2022: "CoRJail: From Null Byte Overflow To Docker Escape Exploiting poll_list Objects In The Linux Kernel"](https://syst3mfailure.io/corjail) [article]

[2022: "Reviving Exploits Against Cred Structs - Six Byte Cross Cache Overflow to Leakless Data-Oriented Kernel Pwnage"](https://www.willsroot.io/2022/08/reviving-exploits-against-cred-struct.html) [article]

[2022: "USMA: Share Kernel Code With Me" by Yong Liu, Jun Yao, and Xiaodong Wang](https://i.blackhat.com/Asia-22/Thursday-Materials/AS-22-YongLiu-USMA-Share-Kernel-Code.pdf) [slides] [[paper](https://i.blackhat.com/Asia-22/Thursday-Materials/AS-22-YongLiu-USMA-Share-Kernel-Code-wp.pdf)] [[article](https://vul.360.net/archives/391?continueFlag=2065c4d6bed3a8e7a80c495d7066e013)]

[2022: "Linux kernel heap feng shui in 2022" by Michael S and Vitaly Nikolenko](https://duasynt.com/blog/linux-kernel-heap-feng-shui-2022) [article]

[2022: "LiKE: A Series on Linux Kernel Exploitation" by sam4k](https://sam4k.com/like-a-series-on-linux-kernel-exploitation/) [article] [[modprobe_path](https://sam4k.com/like-techniques-modprobe_path/)]

[2022: "Racing against the clock -- hitting a tiny kernel race window" by Jann Horn](https://googleprojectzero.blogspot.com/2022/03/racing-against-clock-hitting-tiny.html) [article]

[2022: "Playing for K(H)eaps: Understanding and Improving Linux Kernel Exploit Reliability"](https://www.usenix.org/system/files/sec22fall_zeng.pdf) [paper] [[artifacts](https://github.com/sefcom/KHeaps)]

[2022: "Learning Linux kernel exploitation" by 0x434b](https://0x434b.dev/dabbling-with-linux-kernel-exploitation-ctf-challenges-to-learn-the-ropes/) [article] [[part 2](https://0x434b.dev/learning-linux-kernel-exploitation-part-2-cve-2022-0847/)]

[2021: "ExpRace: Exploiting Kernel Races through Raising Interrupts" at USENIX](https://www.usenix.org/system/files/sec21-lee-yoochan.pdf) [paper] [[slides](https://www.usenix.org/system/files/sec21_slides_lee_yoochan.pdf)] [[video](https://www.youtube.com/watch?v=CIHRw5YPr9o)]

[2021: "Utilizing msg_msg Objects for Arbitrary Read and Arbitrary Write in the Linux Kernel"](https://www.willsroot.io/2021/08/corctf-2021-fire-of-salvation-writeup.html) [article] [[part2](https://syst3mfailure.io/wall-of-perdition)]

[2021: "Linux Kernel Exploitation Technique: Overwriting modprobe_path"](https://lkmidas.github.io/posts/20210223-linux-kernel-pwn-modprobe/) [article]

[2021: "Learning Linux Kernel Exploitation"](https://lkmidas.github.io/posts/20210123-linux-kernel-pwn-part-1/) [article] [[part 2](https://lkmidas.github.io/posts/20210128-linux-kernel-pwn-part-2/)] [[part 3](https://lkmidas.github.io/posts/20210205-linux-kernel-pwn-part-3/)]

[2020: "PTMA (Page Table Manipulation Attack): Attacking the core of memory permission"](https://www.slideshare.net/JungseungLee2/page-table-manipulation-attack) [slides]

[2020: "Exploiting Kernel Races Through Taming Thread Interleaving"](https://i.blackhat.com/USA-20/Thursday/us-20-Lee-Exploiting-Kernel-Races-Through-Taming-Thread-Interleaving.pdf) [slides] [[video](https://www.youtube.com/watch?v=5M3WhLVLCzs)]

[2020: "Locating the kernel PGD on Android/aarch64" by Vitaly Nikolenko](https://duasynt.com/blog/android-pgd-page-tables) [article]

[2020: "A Systematic Study of Elastic Objects in Kernel Exploitation"](https://zplin.me/papers/ELOISE.pdf) [paper] [[video](https://www.youtube.com/watch?v=yXhH0IJAxkE)]

[2020: "Exploiting Uses of Uninitialized Stack Variables in Linux Kernels to Leak Kernel Pointers"](https://www.usenix.org/system/files/woot20-paper1-slides-cho.pdf) [slides] [[paper](https://www.usenix.org/system/files/woot20-paper-cho.pdf)] [[video](https://www.youtube.com/watch?v=uI377m9S0qs)]

[2020: "BlindSide: Speculative Probing: Hacking Blind in the Spectre Era"](https://www.vusec.net/projects/blindside/) [paper]

[2020: "Linux Kernel Stack Smashing" by Silvio Cesare](https://blog.infosectcbr.com.au/2020/02/linux-kernel-stack-smashing.html?m=1) [article]

[2020: "Structures that can be used in kernel exploits"](https://ptr-yudai.hatenablog.com/entry/2020/03/16/165628) [article]

[2019: "The Route to Root: Container Escape Using Kernel Exploitation" by Nimrod Stoler](https://www.cyberark.com/resources/threat-research-blog/the-route-to-root-container-escape-using-kernel-exploitation) [article]

[2019: "Linux Kernel: the ROP Exploit of Stack Overflow in Android Kernel"](https://medium.com/@knownsec404team/linux-kernel-the-rop-exploit-of-stack-overflow-in-android-kernel-87aa8eda770d) [article]

[2019: "Hands Off and Putting SLAB/SLUB Feng Shui in Blackbox" by Yueqi (Lewis) Chen at Black Hat Europe](https://i.blackhat.com/eu-19/Wednesday/eu-19-Chen-Hands-Off-And-Putting-SLAB-SLUB-Feng-Shui-In-A-Blackbox.pdf) [slides] [[code](https://www.dropbox.com/sh/2kwcwqb8rjro80j/AAC8QBCIhcCylNUDLUd1OZCZa?dl=0)]

[2019: "SLAKE: Facilitating Slab Manipulation for Exploiting Vulnerabilities in the Linux Kernel" by Yueqi (Lewis) Chen and Xinyu Xing](http://personal.psu.edu/yxc431/publications/SLAKE_Slides.pdf) [slides] [[paper](http://personal.psu.edu/yxc431/publications/SLAKE.pdf)]

[2019: "Exploiting Race Conditions Using the Scheduler" by Jann Horn at Linux Security Summit EU](https://static.sched.com/hosted_files/lsseu2019/04/LSSEU2019%20-%20Exploiting%20race%20conditions%20on%20Linux.pdf) [slides] [[video](https://www.youtube.com/watch?v=MIJL5wLUtKE)]

[2019: "Kepler: Facilitating Control-flow Hijacking Primitive Evaluation for Linux Kernel Vulnerabilities"](https://www.usenix.org/sites/default/files/conference/protected-files/sec19_slides_wu-wei.pdf) [slides] [[video](https://www.youtube.com/watch?v=4b_GbFs5XZI)] [[paper](https://www.usenix.org/system/files/sec19-wu-wei.pdf)]

[2019: "Leak kernel pointer by exploiting uninitialized uses in Linux kernel" by Jinbum Park](https://jinb-park.github.io/leak-kptr.html) [slides]

[2019: "Kernel IDT priviledge escalation"](https://github.com/rdomanski/kernel/tree/master/writeups/Kernel-IDT-priviledge-escalation) [article]

[2018: "FUZE: Towards Facilitating Exploit Generation for Kernel Use-After-Free Vulnerabilities"](http://personal.psu.edu/yxc431/publications/FUZE_Slides.pdf) [slides] [[paper](http://personal.psu.edu/yxc431/publications/FUZE.pdf)]

[2018: "Linux Kernel universal heap spray" by Vitaly Nikolenko](https://cyseclabs.com/blog/linux-kernel-heap-spray) [article]

[2018: "Linux-Kernel-Exploit Stack Smashing"](https://web.archive.org/web/20190421131414/http://tacxingxing.com/2018/02/15/linux-kernel-exploit-stack-smashing/) [article]

[2018: "Entering God Mode  -  The Kernel Space Mirroring Attack"](https://hackernoon.com/entering-god-mode-the-kernel-space-mirroring-attack-8a86b749545f) [article]

[2018: "Mirror Mirror: Rooting Android 8 with a Kernel Space Mirroring Attack" by Wang Yong at HitB](https://conference.hitb.org/hitbsecconf2018ams/materials/D1T2%20-%20Yong%20Wang%20&%20Yang%20Song%20-%20Rooting%20Android%208%20with%20a%20Kernel%20Space%20Mirroring%20Attack.pdf) [slides]

[2018: "KSMA: Breaking Android kernel isolation and Rooting with ARM MMU features" by Wang Yong at BlackHat](https://www.blackhat.com/docs/asia-18/asia-18-WANG-KSMA-Breaking-Android-kernel-isolation-and-Rooting-with-ARM-MMU-features.pdf) [slides]

[2018: "Still Hammerable and Exploitable: on the Effectiveness of Software-only Physical Kernel Isolation"](https://arxiv.org/pdf/1802.07060.pdf) [paper]

[2018: "linux kernel pwn notes"](https://www.cnblogs.com/hac425/p/9416886.html) [article]

[2018: "Use of timer_list structure in linux kernel exploit"](https://xz.aliyun.com/t/3455) [article]

[2018: "Entering God Mode — The Kernel Space Mirroring Attack"](https://medium.com/hackernoon/entering-god-mode-the-kernel-space-mirroring-attack-8a86b749545f) [article]

[2017: "Escalating Privileges in Linux using Fault Injection" by Niek Timmers and Cristofaro Mune](https://www.riscure.com/uploads/2017/10/escalating-privileges-in-linux-using-fi-presentation-fdtc-2017.pdf) [slides] [[video](https://www.youtube.com/watch?v=nqF_IjXg_uM)] [[paper](https://www.riscure.com/uploads/2017/10/Riscure_Whitepaper_Escalating_Privileges_in_Linux_using_Fault_Injection.pdf)]

[2017: "Kernel Driver mmap Handler Exploitation" by Mateusz Fruba](https://labs.withsecure.com/content/dam/labs/docs/mwri-mmap-exploitation-whitepaper-2017-09-18.pdf) [paper]

[2017: "Linux kernel addr_limit bug / exploitation" by Vitaly Nikolenko](https://www.youtube.com/watch?v=UFakJa3t8Ls) [video]

[2017: "The Stack Clash" by Qualys Research Team](https://www.qualys.com/2017/06/19/stack-clash/stack-clash.txt) [article]

[2017: "New Reliable Android Kernel Root Exploitation Techniques"](http://powerofcommunity.net/poc2016/x82.pdf) [slides]

[2017: "Unleashing Use-Before-Initialization Vulnerabilities in the Linux Kernel Using Targeted Stack Spraying"](https://www-users.cs.umn.edu/~kjlu/papers/tss.pdf) [paper]

[2017: "Breaking KASLR with perf" by Lizzie Dixon](https://blog.lizzie.io/kaslr-and-perf.html) [article]

[2017: "Linux kernel exploit cheetsheet"](https://github.com/verctor/MyNotes/blob/master/linux/linux_kernel_exploit_cheetsheet.md) [article]

[2016: "Getting Physical Extreme abuse of Intel based Paging Systems" by Nicolas Economou and Enrique Nissim](https://cansecwest.com/slides/2016/CSW2016_Economou-Nissim_GettingPhysical.pdf) [slides]

[2016: "Linux Kernel ROP - Ropping your way to # (Part 1)" by Vitaly Nikolenko](https://www.trustwave.com/Resources/SpiderLabs-Blog/Linux-Kernel-ROP---Ropping-your-way-to---(Part-1)/) [article] [[exercise](https://github.com/vnik5287/kernel_rop)]

[2016: "Linux Kernel ROP - Ropping your way to # (Part 2)" by Vitaly Nikolenko](https://www.trustwave.com/Resources/SpiderLabs-Blog/Linux-Kernel-ROP---Ropping-your-way-to---(Part-2)/) [article]

[2016: "Exploiting COF Vulnerabilities in the Linux kernel" by Vitaly Nikolenko at Ruxcon](https://ruxcon.org.au/assets/2016/slides/ruxcon2016-Vitaly.pdf) [slides]

[2016: "Using userfaultfd" by Lizzie Dixon](https://blog.lizzie.io/using-userfaultfd.html) [article]

[2016: "Direct Memory Attack the Kernel" by Ulf Frisk at DEF CON](https://www.youtube.com/watch?v=fXthwl6ShOg) [video]

[2016: "Randomization Can't Stop BPF JIT Spray" by Elena Reshetova at Black Hat](https://www.blackhat.com/docs/eu-16/materials/eu-16-Reshetova-Randomization-Can't-Stop-BPF-JIT-Spray.pdf) [slides] [[video](https://www.youtube.com/watch?v=_F7iQQ1Um2M)] [[paper](https://www.blackhat.com/docs/eu-16/materials/eu-16-Reshetova-Randomization-Can't-Stop-BPF-JIT-Spray-wp.pdf)]

[2015: "Kernel Data Attack is a Realistic Security Threat"](https://www.eecis.udel.edu/~hnw/paper/kerneldata.pdf) [paper]

[2015: "From Collision To Exploitation: Unleashing Use-After-Free Vulnerabilities in Linux Kernel"](http://repository.root-me.org/Exploitation%20-%20Syst%C3%A8me/Unix/EN%20-%20From%20collision%20to%20exploitation%3A%20Unleashing%20Use-After-Free%20vulnerabilities%20in%20Linux%20Kernel.pdf) [paper]

[2015: "Modern Binary Exploitation: Linux Kernel Exploitation" by Patrick Biernat](http://security.cs.rpi.edu/courses/binexp-spring2015/lectures/23/13_lecture.pdf) [slides] [[exercise](https://github.com/RPISEC/MBE/tree/master/src/lab10)]

[2013: "Hacking like in the Movies: Visualizing Page Tables for Local Exploitation" at Black Hat](https://www.youtube.com/watch?v=Of6DemoMLaA)

[2013: "Exploiting linux kernel heap corruptions" by Mohamed Channam](http://resources.infosecinstitute.com/exploiting-linux-kernel-heap-corruptions-slub-allocator/) [article]

[2012: "Writing kernel exploits" by Keegan McAllister](https://tc.gtisc.gatech.edu/bss/2014/r/kernel-exploits.pdf) [slides]

[2012: "Understanding Linux Kernel Vulnerabilities" by Richard Carback](https://www.csee.umbc.edu/courses/undergraduate/421/Spring12/02/slides/ULKV.pdf) [slides]

[2012: "A Heap of Trouble: Breaking the Linux Kernel SLOB Allocator" by Dan Rosenberg](https://www.vsecurity.com//download/papers/slob-exploitation.pdf) [paper]

[2012: "Attacking hardened Linux systems with kernel JIT spraying" by Keegan McAllister](https://mainisusuallyafunction.blogspot.ru/2012/11/attacking-hardened-linux-systems-with.html) [article] [[code 1](https://github.com/kmcallister/alameda)] [[code 2](https://github.com/01org/jit-spray-poc-for-ksp)]

[2012: "The Linux kernel memory allocators from an exploitation perspective" by Patroklos Argyroudis](https://argp.github.io/2012/01/03/linux-kernel-heap-exploitation/) [article]

[2012: "The Stack is Back" by Jon Oberheide](https://jon.oberheide.org/files/infiltrate12-thestackisback.pdf) [slides]

[2012: "Stackjacking" by Jon Oberheide and Dan Rosenberg](https://www.slideshare.net/scovetta/stackjacking) [slides]

[2011: "Stackjacking Your Way to grsec/PaX Bypass" by Jon Oberheide](https://jon.oberheide.org/blog/2011/04/20/stackjacking-your-way-to-grsec-pax-bypass/) [article]

[2010: "Much ado about NULL: Exploiting a kernel NULL dereference"](https://blogs.oracle.com/ksplice/entry/much_ado_about_null_exploiting1) [article]

[2010: "Exploiting Stack Overflows in the Linux Kernel" by Jon Oberheide](https://jon.oberheide.org/blog/2010/11/29/exploiting-stack-overflows-in-the-linux-kernel/) [article]

[2010: "Linux Kernel Exploitation: Earning Its Pwnie a Vuln at a Time" by Jon Oberheide at SOURCE Boston](https://jon.oberheide.org/files/source10-linuxkernel-jonoberheide.pdf) [slides]

[2009: "There's a party at ring0, and you're invited" by Tavis Ormandy and Julien Tinnes at CanSecWest](https://www.cr0.org/paper/to-jt-party-at-ring0.pdf) [slides]

[2007: "Kernel-mode exploits primer" by Sylvester Keil and Clemens Kolbitsch](http://old.iseclab.org/projects/vifuzz/docs/exploit.pdf) [paper]

[2007: "Attacking the Core : Kernel Exploiting Notes"](http://phrack.org/archives/issues/64/6.txt) [article]

[2007: "The story of exploiting kmalloc() overflows"](http://www.ouah.org/kmallocstory.html) [article]

[2007: "Linux 2.6 Kernel Exploits" by Stephane Duverger](https://airbus-seclab.github.io/kernsploit/kernel_exploit_syscan07.pdf) [slides]

[2005: "Large memory management vulnerabilities" by Gael Delalleau at CancSecWest](https://cansecwest.com/core05/memory_vulns_delalleau.pdf) [slides]

[2005: "The story of exploiting kmalloc() overflows"](https://argp.github.io/public/kmalloc_exploitation.pdf) [article]


### Protection Bypasses

[2024: "TikTag: Breaking ARM's Memory Tagging Extension with Speculative Execution" by Juhee Kim et al.](https://arxiv.org/pdf/2406.08719) [paper] [[code](https://github.com/compsec-snu/tiktag)]

[2023: "Leaky Address Masking: Exploiting Unmasked Spectre Gadgets with Noncanonical Address Translation"](https://download.vusec.net/papers/slam_sp24.pdf) [paper]

[2023: "MTE As Implemented, Part 3: The Kernel" by Mark Brand](https://googleprojectzero.blogspot.com/2023/08/mte-as-implemented-part-3-kernel.html) [article]

[2023: "Breaking Hardware-Assisted Kernel Control-Flow Integrity with Page-Oriented Programming" by Seunghun Han](https://i.blackhat.com/BH-US-23/Presentations/US-23-Han-Lost-Control-Breaking-Hardware-Assisted-Kernel.pdf) [slides]

[2023: "MTE As Implemented, Part 3: The Kernel" by Mark Brand](https://googleprojectzero.blogspot.com/2023/08/mte-as-implemented-part-3-kernel.html) [article]

[2023: "EPF: Evil Packet Filter" by Di Jin, Vaggelis Atlidakis, and Vasileios P. Kemerlis](https://cs.brown.edu/~vpk/papers/epf.atc23.pdf) [paper]

[2023: "Bypassing SELinux with init_module" by Sean Pesce](https://seanpesce.blogspot.com/2023/05/bypassing-selinux-with-initmodule.html) [article]

[2023: "Finding Gadgets for CPU Side-Channels with Static Analysis Tools" by Jordy Zomer and Alexandra Sandulescu](https://github.com/google/security-research/tree/master/pocs/cpus/spectre-gadgets) [article]

[2023: "Linux Kernel: Spectre-v1 gadgets" by Jordy Zomer and Alexandra Sandulescu](https://github.com/google/security-research/security/advisories/GHSA-m7j5-797w-vmrh) [article]

[2023: "Linux Kernel: Spectre v2 SMT mitigations problem" by Eduardo Vela](https://github.com/google/security-research/security/advisories/GHSA-mj4w-6495-6crx) [article]

[2022: "A Dirty Little History: Bypassing Spectre Hardware Defenses to Leak Kernel Data"](https://i.blackhat.com/USA-22/Thursday/US-22-Frigo-A-Dirty-Little-History.pdf) [slides]

[2022: "Tetragone: A Lesson in Security Fundamentals" by Pawel Wieczorkiewicz and Brad Spengler](https://grsecurity.net/tetragone_a_lesson_in_security_fundamentals) [article]

[2021: "Characterizing, Exploiting, and Detecting DMA Code Injection Vulnerabilities in the Presence of an IOMMU"](https://www.cs.tau.ac.il/~mad/publications/eurosys2021-dma.pdf) [paper]

[2021: "A General Approach to Bypassing Many Kernel Protections and its Mitigation" by Yueqi Chen](https://i.blackhat.com/asia-21/Friday-Handouts/as-21-Chen-A-General-Approach-To-Bypassing-Many-Kernel-Protections-And-Its-Mitigation.pdf) [slides] [[video](https://www.youtube.com/watch?v=EIwEF3tCtg4)]

[2021: "Attacking Samsung RKP" by Alexandre Adamski](https://blog.impalabs.com/2111_attacking-samsung-rkp.html) [article]

[2020: "Things not to do when using an IOMMU" by Ilja van Sprundel and Joseph Tartaro](https://www.youtube.com/watch?v=p1HUpSkHcZ0) [video]

[2020: "SELinux RKP misconfiguration on Samsung S20 devices" by Vitaly Nikolenko](https://duasynt.com/blog/samsung-s20-rkp-selinux-disable) [article]

[2020: "TagBleed: Breaking KASLR on the Isolated Kernel Address Space using Tagged TLBs"](https://download.vusec.net/papers/tagbleed_eurosp20.pdf) [paper]

[2020: "Weaknesses in Linux Kernel Heap Hardening" by Silvio Cesare](https://blog.infosectcbr.com.au/2020/03/weaknesses-in-linux-kernel-heap.html) [article]

[2020: "An Analysis of Linux Kernel Heap Hardening" by Silvio Cesare](https://blog.infosectcbr.com.au/2020/04/an-analysis-of-linux-kernel-heap.html) [article]

[2020: "PAN: Another day, another broken mitigation" by Siguza](https://siguza.github.io/PAN/) [article]

[2019: "KNOX Kernel Mitigation Bypasses" by Dong-Hoon You at PoC](http://powerofcommunity.net/poc2019/x82.pdf) [slides]

[2017: "Lifting the (Hyper) Visor: Bypassing Samsung’s Real-Time Kernel Protection" by Gal Beniamini](https://googleprojectzero.blogspot.com/2017/02/lifting-hyper-visor-bypassing-samsungs.html) [article]

[2016: "Linux Kernel x86-64 bypass SMEP - KASLR - kptr_restric"](https://web.archive.org/web/20171029060939/http://www.blackbunny.io/linux-kernel-x86-64-bypass-smep-kaslr-kptr_restric/) [article]

[2016: "Practical SMEP bypass techniques on Linux" by Vitaly Nikolenko at KIWICON](https://cyseclabs.com/slides/smep_bypass.pdf) [slides]

[2016: "Micro architecture attacks on KASLR" by Anders Fogh"](https://cyber.wtf/2016/10/25/micro-architecture-attacks-on-kasrl/) [article]

[2016: "Jump Over ASLR: Attacking Branch Predictors to Bypass ASLR" by Dmitry Evtyushkin, Dmitry Ponomarev and Nael Abu-Ghazaleh](http://www.cs.ucr.edu/~nael/pubs/micro16.pdf) [slides]

[2016: "Prefetch Side-Channel Attacks: Bypassing SMAP and Kernel ASLR" by Daniel Gruss, Clementine Maurice, Anders Fogh, Moritz Lipp and Stefan Mangard at CCS](https://www.youtube.com/watch?v=TJTQbs3oJx8) [video]

[2016: "Using Undocumented CPU Behavior to See Into Kernel Mode and Break KASLR in the Process" at Black Hat](https://www.youtube.com/watch?v=T3kmq2NLpH4) [video]

[2016: "Breaking KASLR with Intel TSX" Yeongjin Jang, Sangho Lee and Taesoo Kim at Black Hat](https://www.blackhat.com/docs/us-16/materials/us-16-Jang-Breaking-Kernel-Address-Space-Layout-Randomization-KASLR-With-Intel-TSX.pdf) [slides] [[video](https://www.youtube.com/watch?v=rtuXG28g0CU)]

[2016: "Breaking KASLR with micro architecture" by Anders Fogh](https://dreamsofastone.blogspot.ru/2016/02/breaking-kasrl-with-micro-architecture.html) [article]

[2015: "Effectively bypassing kptr_restrict on Android" by Gal Beniamini](https://bits-please.blogspot.de/2015/08/effectively-bypassing-kptrrestrict-on.html) [article]

[2014: "ret2dir: Deconstructing Kernel Isolation" by Vasileios P. Kemerlis, Michalis Polychronakis and Angelos D. Keromytis at Black Hat Europe](https://www.blackhat.com/docs/eu-14/materials/eu-14-Kemerlis-Ret2dir-Deconstructing-Kernel-Isolation-wp.pdf) [paper] [[video](https://www.youtube.com/watch?v=kot-EQ9zf9k)]

[2013: "A Linux Memory Trick" by Dan Rosenberg](http://vulnfactory.org/blog/2013/02/06/a-linux-memory-trick/) [article]

[2011: "SMEP: What is It, and How to Beat It on Linux" by Dan Rosenberg](http://vulnfactory.org/blog/2011/06/05/smep-what-is-it-and-how-to-beat-it-on-linux/) [article]

[2009: "Bypassing Linux' NULL pointer dereference exploit prevention (mmap_min_addr)"](http://blog.cr0.org/2009/06/bypassing-linux-null-pointer.html) [article]


## Vulnerabilities

[Project Zero bug reports](https://bugs.chromium.org/p/project-zero/issues/list?can=1&q=linux%20kernel&colspec=ID%20Type%20Status%20Priority%20Milestone%20Owner%20Summary&cells=ids&sort=-id)

[Linux Kernel CVEs](https://www.linuxkernelcves.com/)

[Assorted advisories by Gyorgy Miru and kutyacica](https://labs.taszk.io/blog/)


### Info-leaks

[2024: "Out of the kernel, into the tokens" by Max Ammann and Emilio Lopez](https://blog.trailofbits.com/2024/03/08/out-of-the-kernel-into-the-tokens/) [article]

[2023: "The code that wasn’t there: Reading memory on an Android device by accident" by Man Yue Mo](https://github.blog/2023-02-23-the-code-that-wasnt-there-reading-memory-on-an-android-device-by-accident/) [article] [CVE-2022-25664]

[2023: "EntryBleed: A Universal KASLR Bypass against KPTI on Linux"](https://dl.acm.org/doi/pdf/10.1145/3623652.3623669) [paper] [CVE-2022-4543]

[2022: "EntryBleed: Breaking KASLR under KPTI with Prefetch (CVE-2022-4543)"](https://www.willsroot.io/2022/12/entrybleed.html) [article] [CVE-2022-4543]

[2022: "Yet another bug into Netfilter" by Arthur Mongodin](https://www.randorisec.fr/yet-another-bug-netfilter/) [article] [CVE-2022-1972]

[2022: "The AMD Branch (Mis)predictor: Just Set it and Forget it!" by Pawel Wieczorkiewicz](https://grsecurity.net/amd_branch_mispredictor_just_set_it_and_forget_it) [article] [Spectre]

[2022: "The AMD Branch (Mis)predictor Part 2: Where No CPU has Gone Before (CVE-2021-26341)" by Pawel Wieczorkiewicz](https://grsecurity.net/amd_branch_mispredictor_part_2_where_no_cpu_has_gone_before) [article] [Spectre]

[2021: "Samsung S10+/S9 kernel 4.14 (Android 10) Kernel Function Address (.text) and Heap Address Information Leak"](https://ssd-disclosure.com/ssd-advisory-samsung-s10-s9-kernel-4-14-android-10-kernel-function-address-text-and-heap-address-information-leak/) [article] [CVE-TBD]

[2021: "Linux Kernel /proc/pid/syscall information disclosure vulnerability"](https://talosintelligence.com/vulnerability_reports/TALOS-2020-1211) [article] [CVE-2020-28588]

[2021: "Spectre exploits in the "wild""](https://dustri.org/b/spectre-exploits-in-the-wild.html) [article]

[2021: "VDSO As A Potential KASLR Oracle" by Philip Pettersson and Alex Radocea](https://www.longterm.io/vdso_sidechannel.html) [article]

[2020: "PLATYPUS: Software-based Power Side-Channel Attacks on x86"](https://platypusattack.com/platypus.pdf) [paper]

[2019: "CVE-2018-3639 / CVE-2019-7308 - Analysis of Spectre Attacking Linux Kernel ebpf"](https://xz.aliyun.com/t/4230) [article] [CVE-2018-3639, CVE-2019-7308]

[2019: "From IP ID to Device ID and KASLR Bypass (Extended Version)"](https://arxiv.org/pdf/1906.10478.pdf) [paper]

[2018: "Kernel Memory disclosure & CANVAS Part 1 - Spectre: tips & tricks"](https://www.immunityinc.com/downloads/Kernel-Memory-Disclosure-and-Canvas_Part_1.pdf) [article] [Spectre]

[2018: "Kernel Memory disclosure & CANVAS Part 2 - CVE-2017-18344 analysis & exploitation notes"](https://www.immunityinc.com/downloads/Kernel-Memory-Disclosure-and-Canvas_Part_2.pdf) [article] [CVE-2017-18344]

[2018: "CVE-2017-18344: Exploiting an arbitrary-read vulnerability in the Linux kernel timer subsystem" by Andrey Konovalov](https://xairy.io/articles/cve-2017-18344) [article] [CVE-2017-18344]

[2017: "Linux kernel 2.6.0 to 4.12-rc4 infoleak due to a data race in ALSA timer" by Alexander Potapenko](http://seclists.org/oss-sec/2017/q2/455) [announcement] [CVE-2017-1000380]

[2017: "The Infoleak that (Mostly) Wasn't" by Brad Spengler](https://grsecurity.net/the_infoleak_that_mostly_wasnt.php) [article] [CVE-2017-7616]

[2016: "Exploiting a Linux Kernel Infoleak to bypass Linux kASLR"](https://marcograss.github.io/security/linux/2016/01/24/exploiting-infoleak-linux-kaslr-bypass.html) [article]

[2010: "Linux Kernel pktcdvd Memory Disclosure" by Jon Oberheide](https://jon.oberheide.org/blog/2010/10/23/linux-kernel-pktcdvd-memory-disclosure/) [article] [CVE-2010-3437]

[2009: "Linux Kernel x86-64 Register Leak" by Jon Oberheide](https://jon.oberheide.org/blog/2009/10/04/linux-kernel-x86-64-register-leak/) [article] [CVE-2009-2910]

[2009: "Linux Kernel getname() Stack Memory Disclosures" by Jon Oberheide](https://jon.oberheide.org/blog/2009/08/29/linux-kernel-getname-stack-memory-disclosures/) [article] [CVE-2009-3001]


### LPE

[2024: "Driving forward in Android drivers" by Seth Jenkins](https://googleprojectzero.blogspot.com/2024/06/driving-forward-in-android-drivers.html) [article] [[video](https://archive.org/details/shmoocon2024/Shmoocon2024-SethJenkins-Driving_Forward_in_Android_Drivers.mp4)] [CVE-2023-32837] [CVE-2023-32832]

[2024: "Attacking Android Binder: Analysis and Exploitation of CVE-2023-20938" by Eugene Rodionov, Zi Fan Tan, and Gulshan Singh](https://androidoffsec.withgoogle.com/posts/attacking-android-binder-analysis-and-exploitation-of-cve-2023-20938/) [article] [CVE-2023-20938]

[2024: "How to Fuzz Your Way to Android Universal Root: Attacking Android Binder" by Eugene Rodionov and Zi Fan Tan](https://androidoffsec.withgoogle.com/posts/attacking-android-binder-analysis-and-exploitation-of-cve-2023-20938/offensivecon_24_binder.pdf) [slides] [[video](https://www.youtube.com/watch?v=U-xSM159YLI)] [CVE-2023-20938]

[2024: "Linux Kernel nft_validate_register_store Integer Overflow Privilege Escalation"](https://ssd-disclosure.com/ssd-advisory-linux-kernel-nft_validate_register_store-integer-overflow-privilege-escalation/) [article] [CVE-UNKNOWN]

[2024: "Game of Cross Cache: Let's win it in a more effective way!" by Le Wu](https://i.blackhat.com/Asia-24/Presentations/Asia-24-Wu-Game-of-Cross-Cache.pdf) [slides] [CVE-2023-21400]

[2024: "LinkDoor: A Hidden Attack Surface in the Android Netlink Kernel Modules" by Chao Ma et al.](https://i.blackhat.com/Asia-24/Presentations/Asia-24-Ma-LinkDoor-A-Hidden-Attack.pdf) [slides] [CVE-2023-32878] [CVE-2023-32882]

[2024: "Flipping Pages: An analysis of a new Linux vulnerability in nf_tables and hardened exploitation techniques" by notselwyn](https://pwning.tech/nftables/) [article] [[exploit](https://github.com/Notselwyn/CVE-2024-1086)] [CVE-2024-1086]

[2024: "64 bytes and a ROP chain – A journey through nftables" by Davide Ornaghi](https://betrusted.it/blog/64-bytes-and-a-rop-chain-part-1/) [article] [[part 2](https://betrusted.it/blog/64-bytes-and-a-rop-chain-part-2/)] [[exploit](https://github.com/TurtleARM/CVE-2023-0179-PoC)] [CVE-2023-0179]

[2024: "Mind the Patch Gap: Exploiting an io_uring Vulnerability in Ubuntu" by Oriol Castejon](https://blog.exodusintel.com/2024/03/27/mind-the-patch-gap-exploiting-an-io_uring-vulnerability-in-ubuntu/) [CVE-2024-0582]

[2024: "CVE-2022-2586 Writeup"](https://jmpeax.dev/CVE-2022-2586-writeup.html) [article] [CVE-2022-2586]

[2024: "n_gsm_exploit"](https://github.com/fff-vr/n_gsm_exploit) [article]

[2024: "The tale of a GSM Kernel LPE"](https://jmpeax.dev/The-tale-of-a-GSM-Kernel-LPE.html) [article] [[exploit](https://github.com/jmpe4x/GSM_Linux_Kernel_LPE_Nday_Exploit)] [[notes](https://mastodon.social/@gabe_k/112251322421680553)] [[discussion](https://www.openwall.com/lists/oss-security/2024/04/10/18)]

[2024: "Gaining kernel code execution on an MTE-enabled Pixel 8" by Man Yue Mo](https://github.blog/2024-03-18-gaining-kernel-code-execution-on-an-mte-enabled-pixel-8/) [article] [[exploit](https://github.com/github/securitylab/tree/main/SecurityExploits/Android/Mali/CVE_2023_6241)] [CVE-2023-6241]

[2024: "Mali GPU Kernel LPE: Android 14 kernel exploit for Pixel7/8 Pro" by Mohamed Ghannam](https://github.com/0x36/Pixel_GPU_Exploit) [article] [CVE-2023-26083]

[2023: "Linux Kernel GSM Multiplexing Race Condition Local Privilege Escalation Vulnerability (CVE-2023-6546)" by Nassim Asrir](https://github.com/Nassim-Asrir/ZDI-24-020/) [CVE-2023-6546]

[2023: "Conquering the memory through io_uring - Analysis of CVE-2023-2598"](https://anatomic.rip/cve-2023-2598/) [article] [[exploit](https://github.com/ysanatomic/io_uring_LPE-CVE-2023-2598)] [CVE-2023-2598]

[2023: "Conquering a Use-After-Free in nf_tables: Detailed Analysis and Exploitation of CVE-2022-32250" by Yordan Stoychev](https://anatomic.rip/cve-2022-32250/) [article] [CVE-2022-32250]

[2023: "One shot, Triple kill: Pwning all three Google kernelCTF instances with a single 1-day Linux vulnerability"](https://kaist-hacking.github.io/pubs/2023/kim:kernel-ctf-slides.pdf) [slides] [[abstract](https://kaist-hacking.github.io/publication/kim-kernel-ctf/)] [CVE-2023-3390]

[2023: "Exploiting a bug in the Linux kernel with Zig" by Richard Palethorpe](https://richiejp.com/linux-kernel-exploit-tls_context-uaf) [article] [[video](https://www.youtube.com/watch?v=g7ATRgat0v4)] [CVE-2023-0461]

[2023: "Escaping the Google kCTF Container with a Data-Only Exploit" by h0mbre](https://h0mbre.github.io/kCTF_Data_Only_Exploit/) [article] [CVE-2022-3910]

[2023: "Analyzing a Modern In-the-wild Android Exploit" by Seth Jenkins](https://googleprojectzero.blogspot.com/2023/09/analyzing-modern-in-wild-android-exploit.html) [article] [CVE-2023-0266] [CVE-2023-26083]

[2023: "Google: Security Research: CVE-2023-3390](https://github.com/google/security-research/tree/master/pocs/linux/kernelctf/CVE-2023-3390_lts_cos_mitigation/docs) [article] [CVE-2023-3390]

[2023: "Google: Security Research: CVE-2023-0461](https://github.com/google/security-research/tree/master/pocs/linux/kernelctf/CVE-2023-0461_mitigation/docs) [article] [CVE-2023-0461]

[2023: "Old bug, shallow bug: Exploiting Ubuntu at Pwn2Own Vancouver 2023" by Tanguy Dubroca](https://www.synacktiv.com/publications/old-bug-shallow-bug-exploiting-ubuntu-at-pwn2own-vancouver-2023) [article] [CVE-2023-35001]

[2023: "Linux Kernel Exploit (CVE-2022–32250) with mqueue"](https://blog.theori.io/linux-kernel-exploit-cve-2022-32250-with-mqueue-a8468f32aab5) [article] [CVE-2022–32250]

[2023: "Bad io_uring: A New Era of Rooting for Android" by Zhenpeng Lin](https://i.blackhat.com/BH-US-23/Presentations/US-23-Lin-bad_io_uring.pdf) [slides] [[video](https://www.youtube.com/watch?v=fhx3W1z7YD0)] [CVE-2022-20409]

[2023: "CVE-2023-3389 - LinkedPoll" by Querijn Voet](https://qyn.app/posts/CVE-2023-3389/) [article] [CVE-2023-3389]

[2023: "GameOver(lay): Easy-to-exploit local privilege escalation vulnerabilities in Ubuntu Linux" by Sagi Tzadik and Shir Tamari](https://www.wiz.io/blog/ubuntu-overlayfs-vulnerability) [article] [CVE-2023-2640] [CVE-2023-32629]

[2023: "StackRot (CVE-2023-3269): Linux kernel privilege escalation vulnerability" by Ruihan Li](https://github.com/lrh2000/StackRot) [article] [CVE-2023-3269]

[2023: "No CVE for this. It has never been in the official kernel"](https://soez.github.io/posts/no-cve-for-this.-It-has-never-been-in-the-official-kernel/) [article]

[2023: "CVE-2020-27786 exploitation userfaultfd + patching file struct etc passwd"](https://soez.github.io/posts/CVE-2020-27786-exploitation-userfaultfd-+-patching-file-struct-etc-passwd/) [article] [CVE-2020-27786]

[2023: "Breaking the Code - Exploiting and Examining CVE-2023-1829 in cls_tcindex Classifier Vulnerability" by Vu Thi Lan](https://starlabs.sg/blog/2023/06-breaking-the-code-exploiting-and-examining-cve-2023-1829-in-cls_tcindex-classifier-vulnerability/) [article] [CVE-2023-1829]

[2023: "CVE-2023-2008 - Analyzing and exploiting a bug in the udmabuf driver"](https://labs.bluefrostsecurity.de/blog/cve-2023-2008.html) [article] [CVE-2023-2008]

[2023: "Rooting with root cause: finding a variant of a Project Zero bug" by Man Yue Mo](https://github.blog/2023-05-25-rooting-with-root-cause-finding-a-variant-of-a-project-zero-bug/) [article] [CVE-2022-46395]

[2023: "Racing Against the Lock: Exploiting Spinlock UAF in the Android Kernel" by Moshe Kol](https://0xkol.github.io/assets/files/Racing_Against_the_Lock__Exploiting_Spinlock_UAF_in_the_Android_Kernel.pdf) [article] [[slides](https://0xkol.github.io/assets/files/OffensiveCon23_Racing_Against_the_Lock__Exploiting_Spinlock_UAF_in_the_Android_Kernel.pdf)] [[video](https://www.youtube.com/watch?v=E3CVDOlcHC4)] [[exploit](https://github.com/0xkol/badspin)] [CVE-2022-20421]

[2023: "Two bugs with one PoC: Roo2ng Pixel 6 from Android 12 to Android 1" by Yong Wang](https://i.blackhat.com/Asia-23/AS-23-WANG-Two-bugs-with-one-PoC-Rooting-Pixel-6-from-Android-12-to-Android-13.pdf) [slides] [CVE-2021-28664]

[2023: "The OverlayFS vulnerability CVE-2023-0386: Overview, detection, and remediation"](https://securitylabs.datadoghq.com/articles/overlayfs-cve-2023-0386/) [article] [CVE-2023-0386]

[2023: "Pwning Pixel 6 with a leftover patch" by Man Yue Mo](https://github.blog/2023-04-06-pwning-pixel-6-with-a-leftover-patch/) [article] [GHSL-2023-005]

[2023: "Revisiting CVE-2017-11176" by Nils Ole Timm](https://labs.bluefrostsecurity.de/revisiting-cve-2017-11176) [article] [CVE-2017-11176]

[2023: "Rooting the FiiO M6" by Jack Maginnes](https://stigward.github.io/posts/fiio-m6-kernel-bug/) [article] [[part 2](https://stigward.github.io/posts/fiio-m6-exploit/)] [[video](https://www.youtube.com/watch?v=Cd_CAYe4M_M&t=3s)]

[2023: "Exploiting CVE-2021-3490 for Container Escapes" by Karsten Kyonig](https://www.crowdstrike.com/blog/exploiting-cve-2021-3490-for-container-escapes/) [article] [CVE-2021-3490]

[2023: "Pwning the all Google phone with a non-Google bug"](https://github.blog/2023-01-23-pwning-the-all-google-phone-with-a-non-google-bug/) [article] [CVE-2022-38181]

[2022: "CVE-2022-1015: A validation flaw in Netfilter leading to Local Privilege Escalation" by Yordan Stoychev](https://anatomic.rip/cve-2022-1015/) [article] [CVE-2022-1015]

[2022: "CVE-2022-22265: Samsung NPU device driver double free in Android" by Xingyu Jin](https://googleprojectzero.github.io/0days-in-the-wild/0day-RCAs/2022/CVE-2022-22265.html) [article] [CVE-2022-22265]

[2022: "Linux Kernel: Exploiting a Netfilter Use-after-Free in kmalloc-cg" by Sergi Martinez](https://blog.exodusintel.com/2022/12/19/linux-kernel-exploiting-a-netfilter-use-after-free-in-kmalloc-cg/) [article] [CVE-2022-32250]

[2022: "Exploiting CVE-2022-42703 - Bringing back the stack attack" by Seth Jenkins](https://googleprojectzero.blogspot.com/2022/12/exploiting-CVE-2022-42703-bringing-back-the-stack-attack.html) [article] [CVE-2022-42703]

[2022: "CVE-2022-2602: DirtyCred File Exploitation applied on an io_uring UAF"](https://1day.dev/notes/CVE-2022-2602-DirtyCred-File-Exploitation-applied-on-an-io_uring-UAF/) [article] [CVE-2022-2602]

[2022: "DirtyCred Remastered: how to turn an UAF into Privilege Escalation"](https://exploiter.dev/blog/2022/CVE-2022-2602.html) [article] [CVE-2022-2602]
- Some prereq readings (in order):
	1. [2019: https://lwn.net/Articles/779472/] [article]
	2. [2021: https://googleprojectzero.blogspot.com/2022/08/the-quantum-state-of-linux-kernel.html] [CVE-2021-0920 Part 1]

[2022: "Exploiting cross table object reference in Linux Netfilter table (NFT) module"](https://docs.google.com/presentation/d/1qcPPz9E_X3z5h_E-Cc7Qmy1ppP4hWjFZQCQ5ZCb9hw8/edit?usp=sharing) [slides] [CVE-2022-2078] [CVE-2022-2586]

[2022: "Linux Kernel n-day exploit development"](https://1day.dev/notes/Linux-Kernel-n-day-exploit-development/) [article] [CVE-2020-27786]

[2022: "Linux Kernel Exploit Development: 1day case study" by Alessandro Groppo](https://blog.hacktivesecurity.com/index.php/2022/06/13/linux-kernel-exploit-development-1day-case-study/) [article] [CVE-2020-27786]

[2022: "[CVE-2022-1786] A Journey To The Dawn"](https://blog.kylebot.net/2022/10/16/CVE-2022-1786/) [article] [CVE-2022-1786]

[2022: "A Very Powerful Clipboard: Analysis of a Samsung in-the-wild exploit chain" by Maddie Stone](https://googleprojectzero.blogspot.com/2022/11/a-very-powerful-clipboard-samsung-in-the-wild-exploit-chain.html) [article] [CVE-2021-25369] [CVE-2021-25370]

[2022: "Attacking the Android kernel using the Qualcomm TrustZone" by Tamir Zahavi-Brunner](https://tamirzb.com/attacking-android-kernel-using-qualcomm-trustzone) [article] [[video](https://www.youtube.com/watch?v=WXqff23dT5I)] [CVE-2021-1961]

[2022: "SETTLERS OF NETLINK: Exploiting a limited UAF in nf_tables (CVE-2022-32250)"](https://research.nccgroup.com/2022/09/01/settlers-of-netlink-exploiting-a-limited-uaf-in-nf_tables-cve-2022-32250/) [article] [[slides](https://conference.hitb.org/hitbsecconf2022sin/materials/D1T1%20-%20Settlers%20of%20Netlink%20-%20Exploiting%20a%20Limited%20UAF%20on%20Ubuntu%2022.04%20to%20Achieve%20LPE%20-%20Aaron%20Adams.pdf)] [[video](https://www.youtube.com/watch?v=7T_ajYpRWJw)] [CVE-2022-32250]

[2022: "Linux Kernel Exploit (CVE-2022-32250) with mqueue"](https://blog.theori.io/research/CVE-2022-32250-linux-kernel-lpe-2022/) [article] [CVE-2022-32250]

[2022: "N-day exploit for CVE-2022-2586: Linux kernel nft_object UAF" by Alejandro Guerrero](https://www.openwall.com/lists/oss-security/2022/08/29/5) [article] [CVE-2022-2586]

[2022: "Monitoring Surveillance Vendors: A Deep Dive into In-the-Wild Android Full Chains in 2021"](https://i.blackhat.com/USA-22/Wednesday/US-22-Jin-Monitoring-Surveillance-Vendors.pdf) [slides] [CVE-2021-0920]

[2022: "CVE-2022-29582: An io_uring vulnerability" by Awarau and David Bouman](https://ruia-ruia.github.io/2022/08/05/CVE-2022-29582-io-uring/) [article] [CVE-2022-29582]

[2022: "Linux kernel io_uring module pbuf_ring vulnerability and privilege escalation 0day"](https://dawnslab.jd.com/linux-5.19-rc2_pbuf_ring_0day/) [article]

[2022: "Corrupting memory without memory corruption" by Man Yue Mo](https://github.blog/2022-07-27-corrupting-memory-without-memory-corruption/) [article] [CVE-2022-20186]

[2022: "[CVE-2022-34918] A crack in the Linux firewall" by Arthur Mongodin](https://www.randorisec.fr/crack-linux-firewall/) [article] [CVE-2022-34918] [[exploit](https://github.com/randorisec/CVE-2022-34918-LPE-PoC)]

[2022: "CVE-2022-34918: netfilter analysis notes"](https://veritas501.github.io/2022_08_02-CVE-2022-34918%20netfilter%20%E5%88%86%E6%9E%90%E7%AC%94%E8%AE%B0/) [article] [CVE-2022-34918]

[2022: "Practice of USMA-based Kernel Universal EXP Writing Ideas on CVE-2022-34918"](https://veritas501.github.io/2022_08_11_%E5%9F%BA%E4%BA%8EUSMA%E7%9A%84%E5%86%85%E6%A0%B8%E9%80%9A%E7%94%A8EXP%E7%BC%96%E5%86%99%E6%80%9D%E8%B7%AF%E5%9C%A8%20CVE-2022-34918%20%E4%B8%8A%E7%9A%84%E5%AE%9E%E8%B7%B5/) [article] [CVE-2022-34918]

[2022: "The Android kernel mitigations obstacle race" by Man Yue Mo](https://github.blog/2022-06-16-the-android-kernel-mitigations-obstacle-race/) [article] [CVE-2022-22057]

[2022: "io_uring - new code, new bugs, and a new exploit technique" by Lam Jun Rong](https://starlabs.sg/blog/2022/06/io_uring-new-code-new-bugs-and-a-new-exploit-technique/) [article] [CVE-2021-41073]

[2022: "Exploration of the Dirty Pipe Vulnerability (CVE-2022-0847)" by lolcads](https://lolcads.github.io/posts/2022/06/dirty_pipe_cve_2022_0847/) [article] [CVE-2022-0847]

[2022: "DirtyPipe-Android/TECHNICAL-DETAILS.md" by polygraphene](https://github.com/polygraphene/DirtyPipe-Android/blob/master/TECHNICAL-DETAILS.md) [article] [CVE-2022-0847]

[2022: "Weaponizing dirtypipe on android" by Giovanni Rocca](https://docs.google.com/presentation/d/1Tq00gy1GtiK0OvNYOy_kCz0er9ZECBXGoy5Lfy5MD3M/edit?usp=sharing) [slides] [[exploit](https://github.com/iGio90/DirtyPipeZ)] [CVE-2022-0847]

[2022: "How The Tables Have Turned: An analysis of two new Linux vulnerabilities in nf_tables" by David Bouman](https://blog.dbouman.nl/2022/04/02/How-The-Tables-Have-Turned-CVE-2022-1015-1016/) [CVE-2022-1015] [CVE-2022-1016]

[2022: "The Discovery and Exploitation of CVE-2022-25636" by Nick Gregory](https://nickgregory.me/linux/security/2022/03/12/cve-2022-25636/) [article] [CVE-2022-25636]

[2022: "CVE-2022-27666: Exploit esp6 modules in Linux kernel" by ETenal](https://etenal.me/archives/1825) [article] [CVE-2022-27666]

[2022: "Put an io_uring on it: Exploiting the Linux Kernel" by Valentina Palmiotti](https://www.graplsecurity.com/post/iou-ring-exploiting-the-linux-kernel) [article] [CVE-2021-41073]

[2022: "The Dirty Pipe Vulnerability" by Max Kellermann](https://dirtypipe.cm4all.com/) [article] [CVE-2022-0847]

[2022: "CVE-2022-0185 - Winning a $31337 Bounty after Pwning Ubuntu and Escaping Google's KCTF Containers"](https://www.willsroot.io/2022/01/cve-2022-0185.html) [article] [CVE-2022-0185]

[2022: "CVE-2022-0185: Linux kernel slab out-of-bounds write: exploit and writeup" by Alejandro Guerrero](https://www.openwall.com/lists/oss-security/2022/01/25/14) [article] [CVE-2022-0185]

[2022: "CVE-2022-0185: A Case Study"](https://www.hackthebox.com/blog/CVE-2022-0185:_A_case_study) [article] [CVE-2022-0185]

[2022: "CVE-2022-0185: Analysis and utilization and thinking and practice of new primitives for pipe"](https://veritas501.github.io/2022_03_16-CVE_2022_0185%E5%88%86%E6%9E%90%E5%8F%8A%E5%88%A9%E7%94%A8%E4%B8%8Epipe%E6%96%B0%E5%8E%9F%E8%AF%AD%E6%80%9D%E8%80%83%E4%B8%8E%E5%AE%9E%E8%B7%B5/#%E7%9C%9F%E2%80%A2%E6%AD%A3%E6%96%87-%E6%96%B0%E5%9E%8B%E5%88%A9%E7%94%A8%E5%8E%9F%E8%AF%AD-pipe) [article] [CVE-2022-0185]

[2022: "Linux kernel Use-After-Free (CVE-2021-23134) PoC"](https://web.archive.org/web/20220616193522/https://ruia-ruia.github.io/NFC-UAF/) [article] [CVE-2021-23134]

[2022: "Exploiting CVE-2021-26708 (Linux kernel) with ssh"](https://hardenedvault.net/2022/03/01/poc-cve-2021-26708.html) [article] [CVE-2021-26708]

[2022: "exploiting CVE-2019-2215" by cutesmilee](https://cutesmilee.github.io/kernel/linux/android/2022/02/17/cve-2019-2215_writeup.html) [article] [CVE-2019-2215]

[2022: "Linux Kernel PWN | 02 CVE-2009-1897"](https://blog.wohin.me/posts/linux-kernel-pwn-02/) [article] [CVE-2009-1897]

[2021: "Your Trash Kernel Bug, My Precious 0-day" by Zhenpeng Lin](https://zplin.me/talks/BHEU21_trash_kernel_bug.pdf) [slides] [CVE-2021-3715]

[2021: "[CVE-2021-42008] Exploiting A 16-Year-Old Vulnerability In The Linux 6pack Driver"](https://syst3mfailure.io/sixpack-slab-out-of-bounds) [article] [CVE-2021-42008]

[2021: "PWN2OWN Local Escalation of Privilege Category, Ubuntu Desktop Exploit"](https://flatt.tech/assets/reports/210401_pwn2own/whitepaper.pdf) [article] [CVE-TBD]

[2021: "Reversing and Exploiting Samsung's NPU" by Maxime Peterlin](https://blog.impalabs.com/2103_reversing-samsung-npu.html) [article] [[part 2](https://blog.impalabs.com/2110_exploiting-samsung-npu.html)] [slides](https://github.com/Impalabs/conferences/blob/master/2021-barbhack21/21-Barbhack21-Reversing_and_Exploiting_Samsungs_Neural_Processing_Unit.pdf)

[2021: "Fall of the machines: Exploiting the Qualcomm NPU (neural processing unit) kernel driver" by Man Yue Mo](https://securitylab.github.com/research/qualcomm_npu/) [article] [CVE-2021-1940, CVE-2021-1968, CVE-2021-1969]

[2021: "Exploiting CVE-2021-43267" by Blasty](https://haxx.in/posts/pwning-tipc/) [article] [CVE-2021-43267]

[2021: "How a simple Linux kernel memory corruption bug can lead to complete system compromise" by Jann Horn](https://googleprojectzero.blogspot.com/2021/10/how-simple-linux-kernel-memory.html) [article] [CVE-TBD]

[2021: "SuDump: Exploiting suid binaries through the kernel" by Itai Greenhut](https://alephsecurity.com/2021/10/20/sudump/) [article] [CVE-TBD]

[2021: "CVE-2021-34866 Writeup" by HexRabbit](https://blog.hexrabbit.io/2021/11/03/CVE-2021-34866-writeup/) [article] [CVE-2021-34866]

[2021: "Kernel Pwning with eBPF: a Love Story" by Valentina Palmiotti](https://www.graplsecurity.com/post/kernel-pwning-with-ebpf-a-love-story) [article] [CVE-2021-3490]

[2021: "The Art of Exploiting UAF by Ret2bpf in Android Kernel" by Xingyu Jin and Richard Neal](https://i.blackhat.com/EU-21/Wednesday/EU-21-Jin-The-Art-of-Exploiting-UAF-by-Ret2bpf-in-Android-Kernel-wp.pdf) [article] [[slides](https://conference.hitb.org/hitbsecconf2021sin/materials/D1T1%20-%20%20The%20Art%20of%20Exploiting%20UAF%20by%20Ret2bpf%20in%20Android%20Kernel%20-%20Xingyu%20Jin%20&%20Richard%20Neal.pdf)] [[video](https://www.youtube.com/watch?v=7UXtirV1Vzg)] [CVE-2021-0399]

[2021: "Internal of the Android kernel backdoor vulnerability"](https://vul.360.net/archives/263) [article] [CVE-2021-28663]

[2021: "Escape from chrome sandbox to root"](https://vul.360.net/archives/217) [article] [CVE-2020-0423]

[2021: "CVE-2017-11176" by Maher Azzouzi](https://github.com/MaherAzzouzi/LinuxKernelStudy/tree/main/CVE-2017-11176) [article] [CVE-2017-11176]

[2021: "Sequoia: A deep root in Linux's filesystem layer (CVE-2021-33909)" by Qualys Research Team](https://www.qualys.com/2021/07/20/cve-2021-33909/sequoia-local-privilege-escalation-linux.txt) [article] [CVE-2021-33909]

[2021: "CVE-2021-22555: Turning \x00\x00 into 10000$" by Andy Nguyen](https://google.github.io/security-research/pocs/linux/cve-2021-22555/writeup.html) [CVE-2021-22555, article]

[2021: "Exploitation of a double free vulnerability in Ubuntu shiftfs driver (CVE-2021-3492)" by Vincent Dehors](https://www.synacktiv.com/publications/exploitation-of-a-double-free-vulnerability-in-ubuntu-shiftfs-driver-cve-2021-3492.html) [article] [CVE-2021-3492]

[2021: "CVE-2021-20226 a reference counting bug which leads to local privilege escalation in io_uring"](https://flattsecurity.medium.com/cve-2021-20226-a-reference-counting-bug-which-leads-to-local-privilege-escalation-in-io-uring-e946bd69177a) [article] [CVE-2021–20226]

[2021: "CVE-2021-32606: CAN ISOTP local privilege escalation"](https://github.com/nrb547/kernel-exploitation/blob/main/cve-2021-32606/cve-2021-32606.md) [article] [CVE-2021-32606]

[2021: "CVE-2021-3609: CAN BCM local privilege escalation"](https://github.com/nrb547/kernel-exploitation/blob/main/cve-2021-3609/cve-2021-3609.md) [article] [[announcement](https://www.openwall.com/lists/oss-security/2021/06/19/1)] [CVE-2021-3609]

[2021: "Blue Klotski (CVE-2021-3573) and the story for fixing" by f0rm2l1n](https://f0rm2l1n.github.io/2021-07-23-Blue-Klotski/) [article] [[announcement](https://www.openwall.com/lists/oss-security/2021/06/08/2)] [CVE-2021-3573]

[2021: "ZDI-20-1440: An Incorrect Calculation Bug in the Linux Kernel eBPF Verifier" by Lucas Leong](https://www.zerodayinitiative.com/blog/2021/1/18/zdi-20-1440-an-incorrect-calculation-bug-in-the-linux-kernel-ebpf-verifier) [article]

[2021: "ZDI-20-1440 Writeup" by HexRabbit](https://blog.hexrabbit.io/2021/02/07/ZDI-20-1440-writeup/) [article]

[2021: "SSD Advisory – OverlayFS PE"](https://ssd-disclosure.com/ssd-advisory-overlayfs-pe/) [article] [CVE-2021-3493]

[2021: "[BugTales] A Nerve-Racking Bug Collision in Samsung's NPU Driver" by Gyorgy Miru](https://labs.taszk.io/articles/post/bug_collision_in_samsungs_npu_driver/) [article] [CVE-2020-28343, SVE-2020-18610]

[2021: "CVE-2021-20226: A Reference-Counting Bug in the Linux Kernel io_uring Subsystem" by Lucas Leong](https://www.zerodayinitiative.com/blog/2021/4/22/cve-2021-20226-a-reference-counting-bug-in-the-linux-kernel-iouring-subsystem) [article] [CVE-2021-20226]

[2021: "One day short of a full chain: Part 1 - Android Kernel arbitrary code execution" by Man Yue Mo](https://securitylab.github.com/research/one_day_short_of_a_fullchain_android/) [article] [GHSL-2020-375]

[2021: "New Old Bugs in the Linux Kernel"](https://blog.grimm-co.com/2021/03/new-old-bugs-in-linux-kernel.html) [article] [CVE-2021-27365, CVE-2021-27363, CVE-2021-27364]

[2021: "Four Bytes of Power: exploiting CVE-2021-26708 in the Linux kernel"](https://a13xp0p0v.github.io/2021/02/09/CVE-2021-26708.html) [article] [[slides](https://a13xp0p0v.github.io/img/CVE-2021-26708.pdf)] [[video](https://www.youtube.com/watch?v=EMcjHfceX44)] [CVE-2021-26708]

[2021: "Improving the exploit for CVE-2021-26708 in the Linux kernel to bypass LKRG" by Alexander Popov](https://a13xp0p0v.github.io/2021/08/25/lkrg-bypass.html) [article] [[slides](https://a13xp0p0v.github.io/img/CVE-2021-26708_LKRG_bypass.pdf)] [[video](https://www.youtube.com/watch?v=n6YLiYiCIMA)]

[2021: "Gaining root access in Linux using the CVE-2021-26708 vulnerability" by Markel Azpeitia Loiti](https://addi.ehu.es/bitstream/handle/10810/53355/GrAL_MAzpeitia.pdf) [paper]

[2021: "CVE-2014-3153" by Maher Azzouzi](https://github.com/MaherAzzouzi/LinuxKernelStudy/tree/main/CVE-2014-3153) [article] [CVE-2014-3153]

[2021: "The curious case of CVE-2020-14381"](https://blog.frizn.fr/linux-kernel/cve-2020-14381) [article] [CVE-2020-14381]

[2021: "Galaxy's Meltdown - Exploiting SVE-2020-18610"](https://github.com/vngkv123/articles/blob/main/Galaxy's%20Meltdown%20-%20Exploiting%20SVE-2020-18610.md) [article] [CVE-2020-28343, SVE-2020-18610]

[2021: "In-the-Wild Series: Android Exploits" by Mark Brand](https://googleprojectzero.blogspot.com/2021/01/in-wild-series-android-exploits.html) [article]

[2021: "Exploiting CVE-2014-3153 (Towelroot)" by Elon Gliksberg](https://elongl.github.io/exploitation/2021/01/08/cve-2014-3153.html) [article] [CVE-2014-3153]

[2021: "CVE-2014-3153" by Maher Azzouzi](https://github.com/MaherAzzouzi/LinuxKernelStudy/tree/main/CVE-2014-3153) [article] [CVE-2014-3153]

[2020: "An iOS hacker tries Android" by Brandon Azad](https://googleprojectzero.blogspot.com/2020/12/an-ios-hacker-tries-android.html) [article] [CVE-2020-28343, SVE-2020-18610]

[2020: "Exploiting a Single Instruction Race Condition in Binder"](https://blog.longterm.io/cve-2020-0423.html) [article] [CVE-2020-0423]

[2020: "Three Dark clouds over the Android kernel" by Jun Yao](https://github.com/2freeman/Slides/blob/main/PoC-2020-Three%20Dark%20clouds%20over%20the%20Android%20kernel.pdf) [slides] [CVE-2020-3680]

[2020: "Kernel Exploitation With A File System Fuzzer"](https://cyberweek.ae/materials/2020/D1T2%20-%20Kernel%20Exploitation%20with%20a%20File%20System%20Fuzzer.pdf) [slides] [[video](https://www.youtube.com/watch?v=95f1b4FcrQ4)] [CVE-2019-19377]

[2020: "Finding and exploiting a bug (LPE) in an old Android phone" by Brandon Falk](https://www.youtube.com/watch?v=g62FXds2pt8) [stream] [[part 2](https://www.youtube.com/watch?v=qnyFk-f3Koo)] [[summary](https://www.youtube.com/watch?v=t-t7D0vQNmo)]

[2020: "CVE-2020-14386: Privilege Escalation Vulnerability in the Linux kernel" by Or Cohen](https://unit42.paloaltonetworks.com/cve-2020-14386/) [article] [CVE-2020-14386]

[2020: "Attacking the Qualcomm Adreno GPU" by Ben Hawkes](https://googleprojectzero.blogspot.com/2020/09/attacking-qualcomm-adreno-gpu.html) [article] [CVE-2020-11179]

[2020: "TiYunZong: An Exploit Chain to Remotely Root Modern Android Devices" by Guang Gong at Black Hat](https://github.com/secmob/TiYunZong-An-Exploit-Chain-to-Remotely-Root-Modern-Android-Devices/blob/master/us-20-Gong-TiYunZong-An-Exploit-Chain-to-Remotely-Root-Modern-Android-Devices.pdf) [slides] [[paper](https://github.com/secmob/TiYunZong-An-Exploit-Chain-to-Remotely-Root-Modern-Android-Devices/blob/master/us-20-Gong-TiYunZong-An-Exploit-Chain-to-Remotely-Root-Modern-Android-Devices-wp.pdf)] [CVE-2019-10567]

[2020: "Binder - Analysis and exploitation of CVE-2020-0041" by Jean-Baptiste Cayrou](https://www.synacktiv.com/posts/exploit/binder-analysis-and-exploitation-of-cve-2020-0041.html) [article] [CVE-2020-0041]

[2020: "Binder IPC and its vulnerabilities" by Jean-Baptiste Cayrou at THCON](https://www.synacktiv.com/ressources/thcon2020_binder.pdf) [slides] [CVE-2019-2215, CVE-2019-2025, CVE-2019-2181, CVE-2019-2214, CVE-2020-0041]

[2020: "Exploiting CVE-2020-0041 - Part 2: Escalating to root" by Eloi Sanfelix and Jordan Gruskovnjak](https://labs.bluefrostsecurity.de/blog/2020/04/08/cve-2020-0041-part-2-escalating-to-root/) [article] [CVE-2020-0041]

[2020: "A bug collision tale" by Eloi Sanfelix at OffensiveCon](https://labs.bluefrostsecurity.de/files/OffensiveCon2020_bug_collision_tale.pdf) [slides] [[video](https://www.youtube.com/watch?v=WOdRkZwGYDQ)] [CVE-2019-2025]

[2020: "CVE-2020-8835: Linux Kernel Privilege Escalation via Improper eBPF Program Verification" by Manfred Paul](https://www.zerodayinitiative.com/blog/2020/4/8/cve-2020-8835-linux-kernel-privilege-escalation-via-improper-ebpf-program-verification) [article] [CVE-2020-8835]

[2020: "Mitigations are attack surface, too" by Jann Horn](https://googleprojectzero.blogspot.com/2020/02/mitigations-are-attack-surface-too.html) [article]

[2020: "CVE-2019-18683: Exploiting a Linux kernel vulnerability in the V4L2 subsystem" by Alexander Popov](https://a13xp0p0v.github.io/2020/02/15/CVE-2019-18683.html) [article] [[slides](https://a13xp0p0v.github.io/img/CVE-2019-18683.pdf)] [CVE-2019-18683]

[2020: "Multiple Kernel Vulnerabilities Affecting All Qualcomm Devices" by Tamir Zahavi-Brunner](https://blog.zimperium.com/multiple-kernel-vulnerabilities-affecting-all-qualcomm-devices/) [article] [CVE-2019-14040, CVE-2019-14041]

[2019: "CVE-2017-16995 Analysis - eBPF Sign Extension LPE" by senyuuri](https://blog.senyuuri.info/2019/01/19/kernel-epbf-sign-extension/) [article] [CVE-2017-16995]

[2019: "Kernel Research / mmap handler exploitation" by deshal3v](https://deshal3v.github.io/blog/kernel-research/mmap_exploitation) [article] [CVE-2019-18675]

[2019: "Bad Binder: Android In-The-Wild Exploit" by Maddie Stone](https://googleprojectzero.blogspot.com/2019/11/bad-binder-android-in-wild-exploit.html) [article] [CVE-2019-2215]

[2019: "Analyzing Android's CVE-2019-2215 (/dev/binder UAF)"](https://dayzerosec.com/posts/analyzing-androids-cve-2019-2215-dev-binder-uaf/) [article] [CVE-2019-2215]

[2019: "Stream Cut: Android Kernel Exploitation with Binder Use-After-Free (CVE-2019-2215)"](https://www.youtube.com/watch?v=yrLXvmzUQME) [video] [CVE-2019-2215]

[2019: "CVE-2019-2215 - Android kernel binder vulnerability analysis"](https://xz.aliyun.com/t/6853) [article] [CVE-2019-2215]

[2019: "Deep Analysis of Exploitable Linux Kernel Vulnerabilities" by Tong Lin and Luhai Chen at Linux Security Summit EU](https://www.youtube.com/watch?v=MYEAGmP_id4) [video] [CVE-2017-16995, CVE-2017-10661]

[2019: "Tailoring CVE-2019-2215 to Achieve Root" by Grant Hernandez](https://hernan.de/blog/2019/10/15/tailoring-cve-2019-2215-to-achieve-root/) [article] [CVE-2019-2215]

[2019: "From Zero to Root: Building Universal Android Rooting with a Type Confusion Vulnerability" by Wang Yong](https://github.com/ThomasKing2014/slides/blob/master/Building%20universal%20Android%20rooting%20with%20a%20type%20confusion%20vulnerability.pdf) [slides] [CVE-2018-9568, WrongZone]

[2019: "KARMA takes a look at offense and defense: WrongZone from exploitation to repair"](https://mp.weixin.qq.com/s?__biz=MzA3NTQ3ODI0NA==&mid=2247485060&idx=1&sn=b3773b0478f7b5ee39fa1a6527b4f3ff) [article] [CVE-2018-9568, WrongZone]

[2019: "Android Binder: The Bridge To Root" by Hongli Han and Mingjian Zhou](https://conference.hitb.org/hitbsecconf2019ams/materials/D2T2%20-%20Binder%20-%20The%20Bridge%20to%20Root%20-%20Hongli%20Han%20&%20Mingjian%20Zhou.pdf) [slides] [CVE-2019-2025]

[2019: "The ‘Waterdrop’ in Android: A Binder Kernel Vulnerability" by Hongli Han](http://blogs.360.cn/post/Binder_Kernel_Vul_EN.html) [article] [CVE-2019-2025]

[2019: "An Exercise in Practical Container Escapology" by Nick Freeman](https://capsule8.com/blog/practical-container-escape-exercise/) [article] [CVE-2017-1000112]

[2019: "Taking a page from the kernel's book: A TLB issue in mremap()" by Jann Horn](https://googleprojectzero.blogspot.com/2019/01/taking-page-from-kernels-book-tlb-issue.html) [article] [CVE-2018-18281]

[2019: "CVE-2018-18281 - Analysis of TLB Vulnerabilities in Linux Kernel"](https://xz.aliyun.com/t/4005) [article]

[2019: "Analysis of Linux xfrm Module Cross-Border Read-Write Escalation Vulnerability (CVE-2017-7184)"](http://p4nda.top/2019/02/16/CVE-2017-7184/) [article] [CVE-2017-7184]

[2019: "Analysis of Escalation Vulnerability Caused by Integer Extension of Linux ebpf Module (CVE-2017-16995)"](http://p4nda.top/2019/01/18/CVE-2017-16995/) [article] [CVE-2017-16995]

[2019: "Linux kernel 4.20 BPF integer overflow vulnerability analysis"](http://p4nda.top/2019/01/02/kernel-bpf-overflow/) [article]

[2019: "Attacking DRM subsystem to gain kernel privilege on Chromebooks" by Di Shen](https://speakerdeck.com/retme7/attacking-drm-subsystem-to-gain-kernel-privilege-on-chromebooks) [slides] [[video](https://www.youtube.com/watch?v=lBgtZvIxEwA)] [CVE-2019-16508]

[2018: "Linux kernel 4.20 BPF integer overflow-heap overflow vulnerability and its exploitation"](https://www.anquanke.com/post/id/166819) [article]

[2018: "CVE-2017-11176: A step-by-step Linux Kernel exploitation](https://blog.lexfo.fr/) [article] [CVE-2017-11176]

[2018: "A cache invalidation bug in Linux memory management" by Jann Horn](https://googleprojectzero.blogspot.com/2018/09/a-cache-invalidation-bug-in-linux.html) [article] [CVE-2018-17182]

[2018: "Dissecting a 17-year-old kernel bug" by Vitaly Nikolenko at beVX](https://cyseclabs.com/slides/bevx-talk.pdf) [slides] [CVE-2018-6554, CVE-2018-6555]

[2018: "SSD Advisory – IRDA Linux Driver UAF"](https://blogs.securiteam.com/index.php/archives/3759) [article] [CVE-2018-6554, CVE-2018-6555]

[2018: "Integer overflow in Linux's create_elf_tables()"](https://www.openwall.com/lists/oss-security/2018/09/25/4) [announcement] [CVE-2018-14634]

[2018: "MMap Vulnerabilities – Linux Kernel"](https://research.checkpoint.com/mmap-vulnerabilities-linux-kernel/) [article] [CVE-2018-8781]

[2018: "Ubuntu kernel eBPF 0day analysis"](https://security.tencent.com/index.php/blog/msg/124) [article] [CVE-2017-16995]

[2018: "eBPF and Analysis of the get-rekt-linux-hardened.c Exploit for CVE-2017-16995"](https://ricklarabee.blogspot.com/2018/07/ebpf-and-analysis-of-get-rekt-linux.html) [article] [CVE-2017-16695]

[2017: "Challenge Impossible -- Multiple Exploit On Android" by Hanxiang Wen and Xiaodong Wang](https://hitcon.org/2017/CMT/slide-files/d1_s4_r2.pdf) [slides] [CVE-2017-0437]

[2017: "CVE-2017-1000112: Exploiting an out-of-bounds bug in the Linux kernel UFO packets" by Andrey Konovalov](https://xairy.io/articles/cve-2017-1000112) [article] [CVE-2017-1000112]

[2017: "Linux Kernel Vulnerability Can Lead to Privilege Escalation: Analyzing CVE-2017-1000112" by Krishs Patil](https://securingtomorrow.mcafee.com/mcafee-labs/linux-kernel-vulnerability-can-lead-to-privilege-escalation-analyzing-cve-2017-1000112/) [article] [CVE-2017-1000112]

[2017: "Adapting the POC for CVE-2017-1000112 to Other Kernels"](https://ricklarabee.blogspot.de/2017/12/adapting-poc-for-cve-2017-1000112-to.html) [article] [CVE-2017-1000112]

[2017: "The Art of Exploiting Unconventional Use-after-free Bugs in Android Kernel" by Di Shen](https://speakerdeck.com/retme7/the-art-of-exploiting-unconventional-use-after-free-bugs-in-android-kernel) [slides] [CVE-2017-0403, CVE-2016-6787] [[video](https://www.youtube.com/watch?v=U2qvK1hJ6zg)]

[2017: "Exploiting CVE-2017-5123 with full protections. SMEP, SMAP, and the Chrome Sandbox!" by Chris Salls](https://salls.github.io/Linux-Kernel-CVE-2017-5123/) [article] [CVE-2017-5123]

[2017: "Exploiting CVE-2017-5123" by Federico Bento](https://reverse.put.as/2017/11/07/exploiting-cve-2017-5123/) [article] [CVE-2017-5123]

[2017: "Escaping Docker container using waitid() – CVE-2017-5123" by Daniel Shapira](https://www.twistlock.com/2017/12/27/escaping-docker-container-using-waitid-cve-2017-5123/) [article] [CVE-2017-5123]

[2017: "LKE v4.13.x - waitid() LPE" by HyeongChan Kim](http://kozistr.tech/sec-res/2017/10/29/LKE-CVE-2017-5123.html) [article] [CVE-2017-5123]

[2017: "Exploiting on CVE-2016-6787"](https://hardenedlinux.github.io/system-security/2017/10/16/Exploiting-on-CVE-2016-6787.html) [article] [CVE-2016-6787]

[2017: "Race For Root: The Analysis Of The Linux Kernel Race Condition Exploit" by Alexander Popov](https://www.youtube.com/watch?v=g7Qm0NpPAz4) [video] [CVE-2017-2636]

[2017: "Race For Root: The Analysis Of The Linux Kernel Race Condition Exploit" by Alexander Popov](https://program.sha2017.org/system/event_attachments/attachments/000/000/111/original/a13xp0p0v_race_for_root_SHA2017.pdf) [slides] [CVE-2017-2636]

[2017: "CVE-2017-2636: exploit the race condition in the n_hdlc Linux kernel driver bypassing SMEP" by Alexander Popov](https://a13xp0p0v.github.io/2017/03/24/CVE-2017-2636.html) [article] [CVE-2017-2636]

[2017: "CVE-2017-2636: local privilege escalation flaw in n_hdlc" by Alexander Popov](http://seclists.org/oss-sec/2017/q1/569) [announcement] [CVE-2017-2636]

[2017: "Dirty COW and why lying is bad even if you are the Linux kernel"](https://chao-tic.github.io/blog/2017/05/24/dirty-cow) [article] [CVE-2016-5195]

[2017: "NDAY-2017-0103: Arbitrary kernel write in sys_oabi_epoll_wait" by Zuk Avraham](https://blog.zimperium.com/nday-2017-0103-arbitrary-kernel-write-in-sys_oabi_epoll_wait/) [article] [CVE-2016-3857]

[2017: "NDAY-2017-0106: Elevation of Privilege in NVIDIA nvhost-vic driver" by Zuk Avraham](https://blog.zimperium.com/nday-2017-0106-elevation-of-privilege-in-nvidia-nvhost-vic-driver/) [article] [CVE-2016-2434]

[2017: "PWN2OWN 2017 Linux kernel privilege escalation analysis"](https://zhuanlan.zhihu.com/p/26674557) [article] [CVE-2017-7184]

[2017: "Exploiting the Linux kernel via packet sockets" by Andrey Konovalov](https://googleprojectzero.blogspot.com/2017/05/exploiting-linux-kernel-via-packet.html) [article] [CVE-2017-7308]

[2017: "Solving a post exploitation issue with CVE-2017-7308"](https://www.coresecurity.com/core-labs/articles/solving-post-exploitation-issue-cve-2017-7308) [article] [CVE-2017-7308]

[2017: "NDAY-2017-0105: Elevation of Privilege Vulnerability in MSM Thermal Drive" by Zuk Avraham](https://blog.zimperium.com/nday-2017-0105-elevation-of-privilege-vulnerability-in-msm-thermal-driver/) [article] [CVE-2016-2411]

[2017: "NDAY-2017-0102: Elevation of Privilege Vulnerability in NVIDIA Video Driver" by Zuk Avraham](https://blog.zimperium.com/nday-2017-0102-elevation-of-privilege-vulnerability-in-nvidia-video-driver/) [article] [CVE-2016-2435]

[2017: "CVE-2017-6074: Exploiting a double-free in the Linux kernel DCCP sockets" by Andrey Konovalov](https://xairy.io/articles/cve-2017-6074) [article] [CVE-2017-6074]

[2016: "CVE-2016-8655 Linux af_packet.c race condition (local root)" by Philip Pettersson](http://seclists.org/oss-sec/2016/q4/607) [announcement] [CVE-2016-8655]

[2016: "Rooting Every Android From Extension To Exploitation" by Di Shen and James Fang at Black Hat](https://speakerdeck.com/retme7/rooting-every-android-from-extension-to-exploitation) [slides] [[article](https://www.blackhat.com/docs/eu-16/materials/eu-16-Shen-Rooting-Every-Android-From-Extension-To-Exploitation-wp.pdf)] [CVE-2015-0570, CVE-2016-0820, CVE-2016-2475, CVE-2016-8453]

[2016: "Talk is Cheap, Show Me the Code" by James Fang, Di Shen and Wen Niu](https://speakerdeck.com/retme7/talk-is-cheap-show-me-the-code) [slides] [CVE-2015-1805]

[2016: "CVE-2016-3873: Arbitrary Kernel Write in Nexus 9" by Sagi Kedmi](https://sagi.io/2016/09/cve-2016-3873-arbitrary-kernel-write-in-nexus-9/) [article] [CVE-2016-3873]

[2016: "Exploiting Recursion in the Linux Kernel" by Jann Horn](https://googleprojectzero.blogspot.de/2016/06/exploiting-recursion-in-linux-kernel_20.html) [article] [CVE-2016-1583]

[2016: "ANALYSIS AND EXPLOITATION OF A LINUX KERNEL VULNERABILITY (CVE-2016-0728)" By Perception Point Research Team](http://perception-point.io/2016/01/14/analysis-and-exploitation-of-a-linux-kernel-vulnerability-cve-2016-0728/) [article] [CVE-2016-0728]

[2016: "CVE20160728 Exploit Code Explained" by Shilong Zhao](http://dreamhack.it/linux/2016/01/25/cve-2016-0728-exploit-code-explained.html) [article] [CVE-2016-0728]

[2016: "CVE-2016-0728 vs Android" by Collin Mulliner](https://www.mulliner.org/blog/blosxom.cgi/security/CVE-2016-0728_vs_android.writeback?advanced_search=1) [article] [CVE-2016-0728]

[2016: "Notes about CVE-2016-7117" by Lizzie Dixon](https://blog.lizzie.io/notes-about-cve-2016-7117.html) [article] [CVE-2016-7117]

[2016: "CVE-2016-2384: exploiting a double-free in the usb-midi linux kernel driver" by Andrey Konovalov](https://xairy.github.io/blog/2016/cve-2016-2384) [article] [CVE-2016-2384]

[2016: "CVE-2016-6187: Exploiting Linux kernel heap off-by-one" by Vitaly Nikolenko](https://cyseclabs.com/blog/cve-2016-6187-heap-off-by-one-exploit) [article] [CVE-2016-6187]

[2016: "CVE-2014-2851 group_info UAF Exploitation" by Vitaly Nikolenko](https://cyseclabs.com/page?n=02012016) [article] [CVE-2014-2851]

[2016: "Perf: From Profiling To Kernel Exploiting" by Wish Wu at HITB Ams](https://conference.hitb.org/hitbsecconf2016ams/wp-content/uploads/2015/11/D2T2-Wish-Wu-Perf-From-Profiling-to-Kernel-Exploiting.pdf) [slides] [[video](https://www.youtube.com/watch?v=37v14rMtALs)] [CVE-2016-0819]

[2016: "QUADROOTER: NEW VULNERABILITIES AFFECTING OVER 900 MILLION ANDROID DEVICES"](https://www.blackhat.com/docs/eu-16/materials/eu-16-Donenfeld-Stumping-The-Mobile-Chipset-wp.pdf) [article] [CVE-2016-2503, CVE-2106-2504, CVE-2016-2059, CVE-2016-5340]

[2016: "STUMPING THE MOBILE CHIPSET: New 0days from down under" by Adam Donenfeld at DEF CON](https://media.defcon.org/DEF%20CON%2024/DEF%20CON%2024%20presentations/DEF%20CON%2024%20-%20Adam-Donenfeld-Stumping-The-Mobile-Chipset.pdf) [slides] [CVE-2016-2503, CVE-2106-2504, CVE-2016-2059, CVE-2016-5340]

[2015: "Android linux kernel privilege escalation vulnerability and exploit (CVE-2014-4322)" by Gal Beniamini](https://bits-please.blogspot.de/2015/08/android-linux-kernel-privilege.html) [article] [CVE-2014-4322]

[2015: "Exploiting "BadIRET" vulnerability" by Rafal Wojtczuk](https://web.archive.org/web/20171118232027/https://blogs.bromium.com/exploiting-badiret-vulnerability-cve-2014-9322-linux-kernel-privilege-escalation/) [article] [CVE-2014-9322]

[2015: "Follow-up on Exploiting "BadIRET" vulnerability (CVE-2014-9322)" by Adam Zabrocki](http://blog.pi3.com.pl/?p=509) [article] [CVE-2014-9322]

[2015: "Ah! Universal Android Rooting Is Back" by Wen Xu at Black Hat](https://www.blackhat.com/docs/us-15/materials/us-15-Xu-Ah-Universal-Android-Rooting-Is-Back.pdf) [slides] [[video](https://www.youtube.com/watch?v=HVP1c7Ct1nM)] [[paper](https://www.blackhat.com/docs/us-15/materials/us-15-Xu-Ah-Universal-Android-Rooting-Is-Back-wp.pdf)] [CVE-2015-3636]

[2015: "When is something overflowing" by Keen Team](https://www.slideshare.net/PeterHlavaty/overflow-48573748) [slides]

[2015: "Exploiting the DRAM rowhammer bug to gain kernel privileges" by Mark Seaborn and Thomas Dullien](https://googleprojectzero.blogspot.de/2015/03/exploiting-dram-rowhammer-bug-to-gain.html) [article] [Rowhammer]

[2015: "CVE-2014-4943 - PPPoL2TP DoS Analysis" by Vitaly Nikolenko](https://cyseclabs.com/page?n=01102015) [article] [CVE-2014-4943]

[2015: "CVE-2015-0568: Use-After-Free Vulnerability in the Camera Driver of Qualcomm MSM 7x30"](http://c0reteam.org/2015/11/18/cve-20150568) [article] [CVE-2015-0568]

[2014: "Exploiting CVE-2014-0196 a walk-through of the Linux pty race condition PoC" by Samuel Gross](http://blog.includesecurity.com/2014/06/exploit-walkthrough-cve-2014-0196-pty-kernel-race-condition.html) [article] [CVE-2014-0196]

[2014: "CVE-2014-4014: Linux Kernel Local Privilege Escalation "exploitation"" by Vitaly Nikolenko](https://cyseclabs.com/blog/cve-2014-4014-local-privilege-escalation) [article] [CVE-2014-4014]

[2014: "CVE-2014-4699: Linux Kernel ptrace/sysret vulnerability analysis" by Vitaly Nikolenko](https://cyseclabs.com/blog/cve-2014-4699-linux-kernel-ptrace-sysret-analysis) [article] [CVE-2014-4699]

[2014: "How to exploit the x32 recvmmsg() kernel vulnerability CVE 2014-0038" by Samuel Gross](http://blog.includesecurity.com/2014/03/exploit-CVE-2014-0038-x32-recvmmsg-kernel-vulnerablity.html) [article] [CVE-2014-0038]

[2014: "Exploiting the Futex Bug and uncovering Towelroot"](http://tinyhack.com/2014/07/07/exploiting-the-futex-bug-and-uncovering-towelroot/) [article] [CVE-2014-3153]

[2014: "CVE-2014-3153 Exploit" by Joel Eriksson](http://www.clevcode.org/cve-2014-3153-exploit/) [article] [CVE-2014-3153]

[2013: "Privilege Escalation Kernel Exploit" by Julius Plenz](https://blog.plenz.com/2013-02/privilege-escalation-kernel-exploit.html) [article] [CVE-2013-1763]

[2013: "A closer look at a recent privilege escalation bug in Linux (CVE-2013-2094)" by Joe Damato](http://timetobleed.com/a-closer-look-at-a-recent-privilege-escalation-bug-in-linux-cve-2013-2094/) [article] [CVE-2013-2094]

[2012: "Linux Local Privilege Escalation via SUID /proc/pid/mem Write" by Jason Donenfeld](https://git.zx2c4.com/CVE-2012-0056/about/) [article] [CVE-2012-0056]

[2011: "Kernel Exploitation Via Uninitialized Stack" by Kees Cook at DEF CON](https://www.defcon.org/images/defcon-19/dc-19-presentations/Cook/DEFCON-19-Cook-Kernel-Exploitation.pdf) [slides] [[video](https://www.youtube.com/watch?v=jg-wnwnkbsy)] [CVE-2010-2963]

[2010: "CVE-2010-2963 v4l compat exploit" by Kees Cook](https://outflux.net/blog/archives/2010/10/19/cve-2010-2963-v4l-compat-exploit/) [article] [CVE-2010-2963]

[2010: "Exploiting large memory management vulnerabilities in Xorg server running on Linux" by Rafal Wojtczuk](http://invisiblethingslab.com/resources/misc-2010/xorg-large-memory-attacks.pdf) [article] [CVE-2010-2240]

[2010: "CVE-2007-4573: The Anatomy of a Kernel Exploit" by Nelson Elhage](https://blog.nelhage.com/2010/02/cve-2007-4573-the-anatomy-of-a-kernel-exploit/) [article] [CVE-2007-4573]

[2010: "Linux Kernel CAN SLUB Overflow" by Jon Oberheide](https://jon.oberheide.org/blog/2010/09/10/linux-kernel-can-slub-overflow/) [article] [CVE-2010-2959]

[2010: "af_can linux kernel overflow" by Ben Hawkes](http://inertiawar.com/af_can/) [article] [CVE-2010-2959]

[2010: "linux compat vulns (part 1)" by Ben Hawkes](http://inertiawar.com/compat1/) [article] [CVE-2010-3081]

[2010: "linux compat vulns (part 2)" by Ben Hawkes](http://inertiawar.com/compat2/) [article] [CVE-2010-3301]

[2010: "Some Notes on CVE-2010-3081 Exploitability"](https://blog.nelhage.com/2010/11/exploiting-cve-2010-3081/) [article] [CVE-2010-3081]

[2010: "Anatomy of an exploit: CVE-2010-3081"](https://blogs.oracle.com/ksplice/anatomy-of-an-exploit%3a-cve-2010-3081) [article] [CVE-2010-3081]

[2010: "CVE-2010-4258: Turning denial-of-service into privilege escalation" by Nelson Elhage](https://blog.nelhage.com/2010/12/cve-2010-4258-from-dos-to-privesc/) [article] [CVE-2010-4258]

[2009: "Linux NULL pointer dereference due to incorrect proto_ops initializations (CVE-2009-2692)"](http://blog.cr0.org/2009/08/linux-null-pointer-dereference-due-to.html) [article] [CVE-2009-2692]

[2009: "Even when one byte matters"](https://kernelbof.blogspot.de/2009/07/even-when-one-byte-matters.html) [article] [CVE-2009-1046]

[2009: "CVE-2008-0009/CVE-2008-0010: Linux kernel vmsplice(2) Privilege Escalation"](https://xorl.wordpress.com/2009/08/10/cve-2008-0600cve-2008-0010-linux-kernel-vmsplice2-privilege-escalation/) [article] [CVE-2008-0009, CVE-2008-0010]

[2008: "vmsplice(): the making of a local root exploit" by Jonathan Corbet](https://lwn.net/Articles/268783/) [article] [CVE-2008-0600]

[2004: "Linux kernel do_mremap VMA limit local privilege escalation vulnerability"](http://isec.pl/vulnerabilities/isec-0014-mremap-unmap.txt) [article] [CVE-2004-0077]


### RCE

[2023: "Abusing Linux In-Kernel SMB Server to Gain Kernel Remote Code Execution" by Guillaume Teissier and Quentin Minster](https://www.youtube.com/watch?v=XT6jLBbzwFM) [video] [CVE-2022-47943] [CVE-2023-2593]

[2022: "Writing a Linux Kernel Remote in 2022" by Samuel Page](https://blog.immunityinc.com/p/writing-a-linux-kernel-remote-in-2022/) [article] [[slides](https://conference.hitb.org/hitbsecconf2022sin/materials/D1T1%20-%20Erybody%20Gettin%20TIPC%20-%20Demystifying%20Remote%20Linux%20Kernel%20Exploitation%20-%20Sam%20Page.pdf)] [CVE-2022-0435]

[2022: "Zenith: Pwn2Own TP-Link AC1750 Smart Wi-Fi Router Remote Code Execution Vulnerability" by Axel Souchet](https://github.com/0vercl0k/zenith) [article] [CVE-2022-24354]

[2021: "BleedingTooth: Linux Bluetooth Zero-Click Remote Code Execution" by Andy Nguyen](https://google.github.io/security-research/pocs/linux/bleedingtooth/writeup): [BadChoice](https://github.com/google/security-research/security/advisories/GHSA-7mh3-gq28-gfrq), [BadKarma](https://github.com/google/security-research/security/advisories/GHSA-h637-c88j-47wq), [BadVibes](https://github.com/google/security-research/security/advisories/GHSA-ccx2-w2r4-x649) [article] [CVE-2020-12352, CVE-2020-12351, CVE-2020-24490]

[2017: "Over The Air: Exploiting Broadcom’s Wi-Fi Stack (Part 2)" by Gal Beniamini](https://googleprojectzero.blogspot.com/2017/04/over-air-exploiting-broadcoms-wi-fi_11.html) [article] [CVE-2017-0569]

[2017: "BlueBorn: The dangers of Bluetooth implementations: Unveiling zero day vulnerabilities and security flaws in modern Bluetooth stacks"](http://go.armis.com/hubfs/BlueBorne%20Technical%20White%20Paper.pdf?t=1505222709963) [paper] [CVE-2017-1000251]

[2016: "CVE Publication: CVE 2016-8633" by Eyal Itkin](https://eyalitkin.wordpress.com/2016/11/06/cve-publication-cve-2016-8633/) [article] [CVE-2016-8633]

[2011: "Owned Over Amateur Radio: Remote Kernel Exploitation in 2011" at DEF CON](http://cs.dartmouth.edu/~sergey/cs258/2012/Dan-Rosenberg-lecture.pdf) [slides] [[video](https://www.youtube.com/watch?v=kBjD0HITQZA)] [CVE-2011-1493]

[2009: "When a "potential D.o.S." means a one-shot remote kernel exploit: the SCTP story"](https://kernelbof.blogspot.de/2009/04/kernel-memory-corruptions-are-not-just.html) [article] [CVE-2009-0065]


### Other

[2024: "Race condition in 9p file system"](https://r00tkitsmm.github.io/fuzzing/2024/05/29/Race-into-9p.html) [article]

[2024: "Notes about ZDI-24-195 in ksmbd"](https://twitter.com/Shiftreduce/status/1773385937893896206) [thread] [ZDI-24-195]

[2024: "PowerVR GPU - GPU Firmware may overwrite arbitrary kernel pages by RGXCreateFreeList"](https://bugs.chromium.org/p/apvi/issues/detail?id=140) [report]

[2024: "PowerVR GPU - UAF race conditon by DevmemIntPFNotify and DevmemIntCtxRelease"](https://bugs.chromium.org/p/apvi/issues/detail?id=141) [report]

[2023: "Ubuntu Shiftfs: Unbalanced Unlock Exploitation Attempt" by Jean-Baptiste Cayrou](https://www.synacktiv.com/sites/default/files/2023-11/ubuntu_shiftfs.pdf) [slides] [CVE-2023-2612]

[2023: "Attacking NPUs of Multiple Platforms"](https://i.blackhat.com/EU-23/Presentations/EU-23-Zhang-Attacking-NPUs-of-Multiple-Platforms.pdf) [slides] [CVE-2022-22265] [CVE-2020-28343] [SVE-2021-20204] [CVE-2023-42483] [CVE-2023-45864]

[2023: "Deep Dive: Qualcomm MSM Linux Kernel & ARM Mali GPU 0-day Exploit Attacks of October 2023" by Alisa Esage](https://zerodayengineering.com/insights/qualcomm-msm-arm-mali-0days.html) [article] [CVE-2023-33063] [CVE-2023-33106] [CVE-2023-33107] [CVE-2022-22071] [CVE-2023-4211]

[2023: "Unleashing ksmbd: remote exploitation of the Linux kernel (ZDI-23-979, ZDI-23-980)" by notselwyn](https://pwning.tech/ksmbd/) [article] [CVE-2023-3866] [CVE-2023-3865] [[exploits](https://github.com/Notselwyn/exploits)]

[2023: "CVE-2023-4273: a vulnerability in the Linux exFAT driver" by Maxim Suhanov](https://dfir.ru/2023/08/23/cve-2023-4273-a-vulnerability-in-the-linux-exfat-driver/) [article] [CVE-2023-4273]

[2023: "Linux IPv6 'Route of Death' 0day" by Max VA](https://www.interruptlabs.co.uk/articles/linux-ipv6-route-of-death) [article] [CVE-2023-2156]

[2022: "Linux Kernel: Infoleak in Bluetooth L2CAP Handling"](https://github.com/google/security-research/security/advisories/GHSA-vccx-8h74-2357) [advisory] [CVE-2022-42895]

[2022: "Linux Kernel: UAF in Bluetooth L2CAP Handshake"](https://github.com/google/security-research/security/advisories/GHSA-pf87-6c9q-jvm4) [advisory] [CVE-2022-42896]

[2022: "Vulnerability Details for CVE-2022-41218"](https://github.com/V4bel/CVE-2022-41218) [article] [CVE-2022-41218]

[2022: "Racing Cats to the Exit: A Boring Linux Kernel Use-After-Free"](https://accessvector.net/2022/linux-itimers-uaf) [article]

[2022: "Android Universal Root: Exploiting xPU Drivers"](https://i.blackhat.com/USA-22/Wednesday/US-22-Jin-Android-Universal-Root.pdf) [slides] [CVE-2022-20122] [CVE-2021-39815]

[2022: "The quantum state of Linux kernel garbage collection CVE-2021-0920 (Part I)" by Xingyu Jin](https://googleprojectzero.blogspot.com/2022/08/the-quantum-state-of-linux-kernel.html) [article] [CVE-2021-0920]

[2022: "Finding bugs in the Linux Kernel Bluetooth Subsystem" by Itay Iellin](https://itayie.me/linux/2022/07/29/finding-bugs-in-the-linux-kernel-bt-subsystem-part-1.html) [article] [[part 2](https://itayie.me/linux/2022/07/29/finding-bugs-in-the-linux-kernel-bt-subsystem-part-2.html)]

[2022: "CVE-2022-0435: A Remote Stack Overflow in The Linux" by Samuel Page](https://blog.immunityinc.com/p/a-remote-stack-overflow-in-the-linux-kernel/) [article] [CVE-2022-0435]

[2022: "CVE-2021-45608 | NetUSB RCE Flaw in Millions of End User Routers" by Max Van Amernngen](https://www.sentinelone.com/labs/cve-2021-45608-netusb-rce-flaw-in-millions-of-end-user-routers/) [article] [CVE-2021-45608]

[2021: "CVE-2021-1048: refcount increment on mid-destruction file" by Jann Horn](https://googleprojectzero.github.io/0days-in-the-wild/0day-RCAs/2021/CVE-2021-1048.html) [article] [CVE-2021-1048]

[2021: "Achieving Linux Kernel Code Execution Through a Malicious USB Device" by Martijn Bogaard and Dana Geist](https://i.blackhat.com/EU-21/Thursday/EU-21-Bogaard-Geist-Achieving-Linux-Kernel-Code-Execution-Through-A-Malicious-USB-Device.pdf) [slides] [CVE-2016-2384]

[2021: "SLUB overflow CVE-2021-42327"](https://docfate111.github.io/blog/securityresearch/2021/11/08/SLUBoverflow.html) [article] [CVE-2021-42327]

[2021: "CVE-2021-44733: Fuzzing and exploitation of a use-after-free in the Linux kernel TEE subsystem" by pjlantz](https://github.com/pjlantz/optee-qemu) [article] [[poc](https://github.com/pjlantz/optee_examples/tree/master/exploit/host)] [CVE-2021-44733]

[2021: "CVE-2021-43267: Remote Linux Kernel Heap Overflow | TIPC Module Allows Arbitrary Code Execution" by Max Van Amerongen](https://www.sentinelone.com/labs/tipc-remote-linux-kernel-heap-overflow-allows-arbitrary-code-execution/) [article] [CVE-2021-43267]

[2021: "An EPYC escape: Case-study of a KVM breakout" by Felix Wilhelm](https://googleprojectzero.blogspot.com/2021/06/an-epyc-escape-case-study-of-kvm.html) [article] [CVE-2021-29657]

[2021: "CVE-2021-1905: Qualcomm Adreno GPU memory mapping use-after-free" by Ben Hawkes](https://googleprojectzero.github.io/0days-in-the-wild/0day-RCAs/2021/CVE-2021-1905.html) [article] [CVE-2021-1905]

[2021: "A foray into Linux kernel exploitation on Android" by Ayaz Mammadov](https://mcyoloswagham.github.io/linux/) [article]

[2020: "CVE-2020-16119"](https://github.com/HadarManor/Public-Vulnerabilities/blob/master/CVE-2020-16119/CVE-2020-16119.md) [article] [CVE-2020-16119]

[2020: "The short story of 1 Linux Kernel Use-After-Free bug and 2 CVEs (CVE-2020-14356 and CVE-2020-25220)" by Adam Zabrocki](http://blog.pi3.com.pl/?p=720) [article] [CVE-2020-14356, CVE-2020-25220]

[2020: "Curiosity around 'exec_id' and some problems associated with it" by Adam Zabrocki](https://www.openwall.com/lists/kernel-hardening/2020/03/25/1) [article]

[2020: "The never ending problems of local ASLR holes in Linux"](https://blog.blazeinfosec.com/the-never-ending-problems-of-local-aslr-holes-in-linux/) [article] [CVE-2019-11190]

[2019: "Reverse-engineering Broadcom wireless chipsets" by Hugues Anguelkov](https://blog.quarkslab.com/reverse-engineering-broadcom-wireless-chipsets.html) [article] [CVE-2019-9503, CVE-2019-9500]

[2019: "CVE-2019-2000 - Android kernel binder vulnerability analysis"](https://xz.aliyun.com/t/4494) [article] [CVE-2019-2000]

[2019: "Linux: virtual address 0 is mappable via privileged write() to /proc/\*/mem"](https://bugs.chromium.org/p/project-zero/issues/detail?id=1792&desc=2) [article] [CVE-2019-9213]

[2019: "CVE-2019-9213 - Analysis of Linux Kernel User Space 0 Virtual Address Mapping Vulnerability"](https://cert.360.cn/report/detail?id=58e8387ec4c79693354d4797871536ea) [article] [CVE-2019-9213]

[2018: "IOMMU-resistant DMA attacks" by Gil Kupfer](http://www.cs.technion.ac.il/users/wwwb/cgi-bin/tr-get.cgi/2018/MSC/MSC-2018-21.pdf) [thesis]

[2017: "initroot: Bypassing Nexus 6 Secure Boot through Kernel Command-line Injection"](https://alephsecurity.com/2017/05/23/nexus6-initroot/#anecdote-a-linux-kernel-out-of-bounds-write-cve-2017-1000363) [article] [CVE-2017-1000363]

[2016: "Motorola Android Bootloader Kernel Cmdline Injection Secure Boot Bypass"](https://alephsecurity.com/vulns/aleph-2017011) [article] [CVE-2016-10277]

[2015: "Vulnerability in the Linux Crypto API that allows unprivileged users to load arbitrary kernel modules" by Mathias Krause](https://plus.google.com/+MathiasKrause/posts/PqFCo4bfrWu) [annnouncement]


## Finding Bugs

[2024: "So You Wanna Find Bugs In The Linux Kernel?" by Sam Page](https://github.com/sam4k/talk-slides/blob/main/so_you_wanna_find_bugs_in_the_linux_kernel.pdf) [slides]

[2024: "A bug hunter's reflections on fuzzing" by Alexander Popov](https://a13xp0p0v.github.io/img/Alexander_Popov-Reflections_on_Fuzzing.pdf) [slides] [[video](https://www.youtube.com/watch?v=wTbFmdx7wG8)]

[2024: "To Boldly Go Where No Fuzzer Has Gone Before: Finding Bugs in Linux’ Wireless Stacks through VirtIO Devices" by Sonke Huster et al.](https://www.uni-goettingen.de/de/document/download/6b0d1e9d8e2fb7f57cc1a2fab1b071e7.pdf/huster_S&P24.pdf) [paper] [[code](https://github.com/seemoo-lab/VirtFuzz)]

[2024: "Your NVMe Had Been Syz’ed: Fuzzing NVMe-oF/TCP Driver for Linux with Syzkaller" by Alon Zavahi](https://www.cyberark.com/resources/threat-research-blog/your-nvme-had-been-syzed-fuzzing-nvme-of-tcp-driver-for-linux-with-syzkaller) [article] [[slides](https://download.scrt.ch/insomnihack/ins24-slides/Syzkaller%20NVMe-oF.pdf)] [[video](https://www.youtube.com/watch?v=Jc25CM1Ppgo)]

[2024: "Structure-Aware linux kernel Fuzzing with libFuzzer"](https://r00tkitsmm.github.io/fuzzing/2024/03/27/libffuzzerkernel.html) [article]

[2024: "Enhancing Kernel Bug Discovery with Large Language Models" by Zahra Tarkhani](https://static.sched.com/hosted_files/lssna24/ed/LSSNA-Enhancing%20Kernel%20Bug%20Discovery%20with%20Large%20Language%20Models%20%E2%80%8B.pdf) [slides] [[video](https://www.youtube.com/watch?v=ewv3kX-p7-o)]

[2024: "SyzRisk: A Change-Pattern-Based Continuous Kernel Regression Fuzzer"](https://nebelwelt.net/files/24AsiaCCS.pdf) [paper]

[2024: "SyzBridge: Bridging the Gap in Exploitability Assessment of Linux Kernel Bugs in the Linux Ecosystem"](https://zhyfeng.github.io/files/2024-NDSS-SyzBridge.pdf) [paper]

[2024: "SyzRetrospector: A Large-Scale Retrospective Study of Syzbot"](https://arxiv.org/pdf/2401.11642.pdf) [paper]

[2023: "KernelGPT: Enhanced Kernel Fuzzing via Large Language Models"](https://arxiv.org/pdf/2401.00563.pdf) [paper]

[2023: "SyzDirect: Directed Greybox Fuzzing for Linux Kernel"](https://yuanxzhang.github.io/paper/syzdirect-ccs23.pdf) [paper]

[2023: "Using ASAN and KASAN and then Interpreting their shadow memory reports" by Kaiwan N Billimoria](https://kernelmeetup.files.wordpress.com/2023/11/lt_1_using_asan_and_kasan_and_then_interpreting_their_shadow_memory_repo.pdf) [article]

[2023: "GWP-ASan: Sampling-Based Detection of Memory-Safety Bugs in Production"](https://arxiv.org/pdf/2311.09394.pdf) [paper]

[2023: "Tickling ksmbd: fuzzing SMB in the Linux kernel" by notselwyn](https://pwning.tech/ksmbd-syzkaller/) [article]

[2023: "DDRace: Finding Concurrency UAF Vulnerabilities in Linux Drivers with Directed Fuzzing"](https://www.usenix.org/system/files/usenixsecurity23-yuan-ming.pdf) [paper] [[slides](https://www.usenix.org/system/files/sec23_slides_yuan.pdf)]

[2023: "BoKASAN: Binary-only Kernel Address Sanitizer for Effective Kernel Fuzzing"](https://www.usenix.org/system/files/usenixsecurity23-cho.pdf) [paper] [[slides](https://www.usenix.org/system/files/sec23_slides_cho-mingi.pdf)] [[artifacts](https://github.com/seclab-yonsei/BoKASAN)]

[2023: "FirmSolo: Enabling dynamic analysis of binary Linux-based IoT kernel modules](https://www.usenix.org/system/files/usenixsecurity23-angelakopoulos.pdf) [paper] [[slides](https://www.usenix.org/system/files/sec23_slides_angelakopoulos.pdf)]

[2023: "ACTOR: Action-Guided Kernel Fuzzing"](https://www.usenix.org/system/files/usenixsecurity23-fleischer.pdf) [paper] [[slides](https://www.usenix.org/system/files/sec23_slides_fleischer.pdf)] [[artifacts](https://github.com/ucsb-seclab/actor)]

[2023: "UNCONTAINED: Uncovering Container Confusion in the Linux Kernel" by Jakob Koschel, Pietro Borrello, et al.](https://download.vusec.net/papers/uncontained_sec23.pdf) [paper]

[2023: "KIT: Testing OS-Level Virtualization for Functional Interference Bugs"](https://dl.acm.org/doi/pdf/10.1145/3575693.3575731) [paper]

[2023: "SyzDescribe: Principled, Automated, Static Generation of Syscall Descriptions for Kernel Drivers"](https://www.cs.ucr.edu/~zhiyunq/pub/oakland23_syzdescribe.pdf) [paper] [[slides](https://static.sched.com/hosted_files/lssna2023/94/LSS-NA-23-SyzDescribe.pdf)]

[2023: "Precise Detection of Kernel Data Races with Probabilistic Lockset Analysis"](https://www.cs.columbia.edu/~gabe/files/oakland2023_pla.pdf) [paper]

[2023: "No Grammar, No Problem: Towards Fuzzing the Linux Kernel without System-Call Descriptions"](https://www.ndss-symposium.org/wp-content/uploads/2023/02/ndss2023_f688_paper.pdf) [paper]

[2023: "FirmSolo: Enabling dynamic analysis of binary Linux-based IoT kernel modules"](https://www.usenix.org/system/files/sec23summer_190-angelakopoulos-prepub.pdf) [paper]

[2022: "Event-based Fuzzing, Patch-based Research, and Comment Police: Finding Bugs Through a Bug"](https://i.blackhat.com/EU-22/Thursday-Briefings/EU-22-LiYang-Event-based-Fuzzing-Patch-based.pdf) [slides] [[video](https://www.youtube.com/watch?v=mPiv0eZlx9w)]

[2022: "Breaking the Glass Sandbox - Find Linux Kernel Bugs and Escape" by Valentina Palmiotti at REcon](https://cfp.recon.cx/media/2022/submissions/EVBN3B/resources/recon_7TKNBIm.pdf) [slides] [[video](https://www.youtube.com/watch?v=2R46lJsOOTE)]

[2022: "Sanitizing the Linux kernel: On KASAN and other Dynamic Bug-finding Tools" by Andrey Konovalov](https://docs.google.com/presentation/d/1qA8fqRDHKX_WM_ZdDN37EQQZwSTNJ4FFws82tbUSKxY/edit?usp=sharing) [slides] [[video](https://www.youtube.com/watch?v=KmFVPyHyfqQ)] [[article](https://lwn.net/Articles/909245/)]

[2022: "PrIntFuzz: Fuzzing Linux Drivers via Automated Virtual Device Simulation"](https://dl.acm.org/doi/pdf/10.1145/3533767.3534226) [paper]

[2022: "KSG: Augmenting Kernel Fuzzing with System Call Specification Generation"](http://www.wingtecher.com/themes/WingTecherResearch/assets/papers/atc22.pdf) [paper]

[2022: "Demystifying the Dependency Challenge in Kernel Fuzzing"](https://github.com/ZHYfeng/Dependency/blob/master/Paper.pdf) [paper]

[2022: "Hunting for Linux kernel public vulnerabilities"](https://1day.dev/notes/Hunting-for-Linux-kernel-public-vulnerabilities/) [article]

[2022: "DangZero: Efficient Use-After-Free Detection via Direct Page Table Access"](https://download.vusec.net/papers/dangzero_ccs22.pdf) [paper]

[2022: "How I started chasing speculative type confusion bugs in the kernel and ended up with 'real' ones" by Jakob Koschel](https://lpc.events/event/16/contributions/1211/attachments/979/1981/LPC2022_slides_Jakob_Koschel.pdf) [slides] [[video](https://www.youtube.com/watch?v=LigVc74INaA)]

[2022: "Technical analysis of syzkaller based fuzzers: It's not about VaultFuzzer!"](https://hardenedvault.net/blog/2022-08-07-state-based-fuzzer-update/) [article]

[2022: "GREBE: Unveiling Exploitation Potential for Linux Kernel Bugs"](https://zplin.me/papers/GREBE.pdf) [paper]

[2022: "An In-depth Analysis of Duplicated Linux Kernel Bug Reports"](https://zplin.me/papers/bug_analysis.pdf) [paper]

[2022: "Looking for Remote Code Execution bugs in the Linux kernel" by Andrey Konovalov](https://xairy.io/articles/syzkaller-external-network) [article]

[2022: "Demystifying the Dependency Challenge in Kernel Fuzzing"](https://github.com/ZHYfeng/Dependency/blob/master/Paper.pdf) [paper]

[2022: "Progressive Scrutiny: Incremental Detection of UBI bugs in the Linux Kernel"](https://www.ndss-symposium.org/wp-content/uploads/2022-380-paper.pdf) [paper]

[2022: "Syzkaller diving 01: Learn basic KCOV and how fuzzer adopts it" by f0rm2l1n](https://f0rm2l1n.github.io/2021-02-02-syzkaller-diving-01/) [article]

[2022: "Syzkaller diving 02: How syzkaller describe syscalls" by f0rm2l1n](https://f0rm2l1n.github.io/2021-02-04-syzkaller-diving-02/) [article]

[2022: "Syzkaller diving 03: What is the remote KCOV?" by f0rm2l1n](https://f0rm2l1n.github.io/2021-02-10-syzkaller-diving-03/) [article]

[2022: "Case Studies of Fuzzing with Xen" by Tamas K Lengyel at OffensiveCon](https://www.slideshare.net/tklengyel/offensivecon2022-case-studies-of-fuzzing-with-xen) [slides]

[2021: "Rtkaller: State-aware Task Generation for RTOS Fuzzing"](http://www.wingtecher.com/themes/WingTecherResearch/assets/papers/emsoft21.pdf) [paper]

[2021: "BSOD: Binary-only Scalable fuzzing Of device Drivers" by Fabian Toepfer and Dominik Maier](https://dmnk.co/raid21-bsod.pdf) [paper]

[2021: "LinKRID: Vetting Imbalance Reference Counting in Linux kernel with Symbolic Execution" at USENIX](https://www.usenix.org/system/files/sec22summer_liu-jian.pdf) [paper] [[slides](https://www.usenix.org/system/files/sec22_slides-liu_jian.pdf)]

[2021: "An Analysis of Speculative Type Confusion Vulnerabilities in the Wild" at USENIX](https://www.usenix.org/system/files/sec21-kirzner.pdf) [paper] [[slides](https://www.usenix.org/system/files/sec21_slides_kirzner.pdf)] [[video](https://www.youtube.com/watch?v=Gxv6LcabKrg)]

[2021: "SyzVegas: Beating Kernel Fuzzing Odds with Reinforcement Learning" at USENIX](https://www.usenix.org/system/files/sec21-wang-daimeng.pdf) [paper] [[slides](https://www.usenix.org/system/files/sec21_slides_wang-daimeng.pdf)] [[video](https://www.youtube.com/watch?v=72Ngu3305TU)]

[2021: "Detecting Kernel Refcount Bugs with Two-Dimensional Consistency Checking" at USENIX](https://www.usenix.org/system/files/sec21-tan.pdf) [paper] [[slides](https://www.usenix.org/system/files/sec21_slides_tan.pdf)] [[video](https://www.youtube.com/watch?v=tUzeuJTzpx4)]

[2021: "Ruffling the penguin! How to fuzz the Linux kernel" by Andrey Konovalov and xakep.ru](https://hackmag.com/security/linux-fuzzing/) [article]

[2021: "CoLaFUZE: Coverage-Guided and Layout-Aware Fuzzing for Android Drivers"](https://www.jstage.jst.go.jp/article/transinf/E104.D/11/E104.D_2021NGP0005/_pdf) [paper]

[2021: "CVEHound: Audit Kernel Sources for Missing CVE Fixes" by Denis Efremov](https://speakerdeck.com/efremov/cvehound-audit-kernel-sources-for-missing-cve-fixes) [slides] [[video](https://www.youtube.com/watch?v=jIDnVeZNUA8)]

[2021: "Finding Multiple Bug Effects for More Precise Exploitability Estimation" by Zhenpeng Lin and Yueqi Chen](https://static.sched.com/hosted_files/lssna2021/5a/LSS_2021_Multiple_Error_Behavior.pdf) [slides] [[video](https://www.youtube.com/watch?v=J3frKpcJ9vg)]

[2021: "Triaging Kernel Out-Of-Bounds Write Vulnerabilities" by Weiteng Chen](https://static.sched.com/hosted_files/lssna2021/07/koobe-LSS.pdf) [slides] [[video](https://www.youtube.com/watch?v=YUHy58hyDq0)]

[2021: "SyzScope: Revealing High-Risk Security Impacts of Fuzzer-Exposed Bugs" by Xiaochen Zou](https://etenal.me/wp-content/uploads/2021/10/SyzScope-final.pdf) [paper] [[slides](https://static.sched.com/hosted_files/lssna2021/55/SyzScope%20in%20Linux%20Security%20Summit.pdf)] [[video](https://www.youtube.com/watch?v=MJbqeo5qtQ0)] [[lwn article](https://lwn.net/Articles/872649/)]

[2021: "HEALER: Relation Learning Guided Kernel Fuzzing"](http://www.wingtecher.com/themes/WingTecherResearch/assets/papers/healer-sosp21.pdf) [paper]

[2021: "Snowboard: Finding Kernel Concurrency Bugs through Systematic Inter-thread Communication Analysis"](https://dl.acm.org/doi/pdf/10.1145/3477132.3483549) [paper]

[2021: "Detecting semantic bugs using differential fuzzing" by Mara Mihali](https://linuxplumbersconf.org/event/11/contributions/1033/attachments/742/1621/syz-verifier%20-%20Linux%20Plumbers%202021.pdf) [slides] [[video](https://www.youtube.com/watch?v=Y_minEhZNm8&t=2388s)]

[2021: "Fuzzing Linux with Xen" by Tamas K Lengyel](https://media.defcon.org/DEF%20CON%2029/DEF%20CON%2029%20presentations/Tamas%20K%20Lengyel%20-%20Fuzzing%20Linux%20with%20Xen.pdf) [slides] [[video](https://www.youtube.com/watch?v=_dXC_I2ybr4)]

[2021: "Variant analysis of the ‘Sequoia’ bug" by Jordy Zomer](https://pwning.systems/posts/sequoia-variant-analysis/) [article]

[2021: "KMSAN, a look under the hood" by Alexander Potapenko](https://github.com/ramosian-glider/talks-and-presentations/blob/master/2021/KernelMemorySanitizer_a_look_under_the_hood.pdf) [slides] [[video](https://www.youtube.com/watch?v=LNs2U-3m3yg)]

[2021: "Detecting Kernel Memory Leaks in Specialized Modules with Ownership Reasoning"](https://github.com/QiushiWu/QiushiWu.github.io/blob/main/papers/k-meld.pdf) [paper]

[2021: "Understanding and Detecting Disordered Error Handling with Precise Function Pairing"](https://www.usenix.org/system/files/sec21summer_wu-qiushi.pdf) [paper]

[2021: "KFENCE - Detecting memory bugs in production kernels"](https://thomasw.dev/post/kfence/) [article]

[2021: "Fuzzing the Linux Kernel" by Andrey Konovalov](https://linuxfoundation.org/wp-content/uploads/2021-Linux-Foundation-Mentorship-Series_-Fuzzing-the-Linux-Kernel.pdf) [slides] [[video](https://www.youtube.com/watch?v=4IBWj21tg-c)]

[2021: "Dynamic program analysis for fun and profit" by Dmitry Vyukov](https://linuxfoundation.org/wp-content/uploads/Dynamic-program-analysis_-LF-Mentorship.pdf) [slides] [[video](https://www.youtube.com/watch?v=ufcyOkgFZ2Q)]

[2020: "UBITect: A Precise and Scalable Method to Detect Use-before-Initialization Bugs in Linux Kernel"](https://dl.acm.org/doi/pdf/10.1145/3368089.3409686) [paper]

[2020: "RetroWrite: Statically Instrumenting COTS Binaries for Fuzzing and Sanitization"](https://nebelwelt.net/files/20Oakland.pdf) [paper] [[tool](https://github.com/HexHive/RetroWrite)]

[2020: "Fuzzing a Pixel 3a Kernel with Syzkaller" by senyuuri](https://blog.senyuuri.info/2020/04/16/fuzzing-a-pixel-3a-kernel-with-syzkaller/) [article]

[2020: "Fuzzing the Berkeley Packet Filter" by Benjamin Curt Nilsen](https://search.proquest.com/openview/feeeac2f4c7f767740986bdbf9d51785/1?pq-origsite=gscholar&cbl=44156) [thesis]

[2020: "syzkaller: Adventures in Continuous Coverage-guided Kernel Fuzzing" by Dmitry Vyukov at BlueHat IL](https://docs.google.com/presentation/d/e/2PACX-1vRWjOOL45BclKsCPMzdWmvH12hu-Ld1cU5MbB1tqcBhjVIr1M_qxZRE-ObKcVmqpCyqRAO62Sxm0_aW/pub?start=false&loop=false&delayms=3000&slide=id.p) [[video](https://www.youtube.com/watch?v=YwX4UyXnhz0)]

[2020: "syzkaller / sanitizers: status update" by Dmitry Vyukov at Linux Plumbers](https://linuxplumbersconf.org/event/7/contributions/716/attachments/645/1181/syzkaller_LPC2020.pdf) [slides] [[video](https://www.youtube.com/watch?v=y9Glc90WUN0&t=234)]

[2020: "Fuzzing for eBPF JIT bugs in the Linux kernel" by Simon Scannell](https://scannell.io/posts/ebpf-fuzzing/) [article]

[2020: "Specification and verification in the field: Applying formal methods to BPF just-in-time compilers in the Linux kernel"](https://unsat.cs.washington.edu/papers/nelson-jitterbug.pdf) [paper]

[2020: "Eliminating bugs in BPF JITs using automated formal verification" by Luke Nelson](https://homes.cs.washington.edu/~lukenels/slides/2020-08-28-lpc.pdf) [[video](https://www.youtube.com/watch?v=dZ_1HgUbni0&t=188s)] [slides]

[2020: "Fuzzing the Linux kernel (x86) entry code, Part 1 of 3" by Vegard Nossum](https://blogs.oracle.com/linux/fuzzing-the-linux-kernel-x86-entry-code%2c-part-1-of-3) [article]

[2020: "Fuzzing the Linux kernel (x86) entry code, Part 2 of 3" by Vegard Nossum](https://blogs.oracle.com/linux/fuzzing-the-linux-kernel-x86-entry-code%2c-part-2-of-3) [article]

[2020: "Fuzzing the Linux kernel (x86) entry code, Part 3 of 3" by Vegard Nossum](https://blogs.oracle.com/linux/fuzzing-the-linux-kernel-x86-entry-code%2c-part-3-of-3) [article]

[2020: "Data-race detection in the Linux kernel" by Marco Elver at Linux Plumbers](https://linuxplumbersconf.org/event/7/contributions/647/attachments/549/972/LPC2020-KCSAN.pdf) [slides] [[video](https://www.youtube.com/watch?v=gJRBmunG47w&t=7141)]

[2020: "harbian-qa: State-based target directed fuzzer based on syzkaller"](https://github.com/hardenedlinux/harbian-qa/blob/master/syzkaller/design_inplementation_intro.md) [article]

[2020: "Agamotto: Accelerating Kernel Driver Fuzzing with Lightweight Virtual Machine Checkpoints"](https://www.usenix.org/system/files/sec20-song.pdf) [paper] [[slides](https://www.usenix.org/system/files/sec20_slides_song.pdf)] [[video](https://www.youtube.com/watch?v=Swo6jSkjviA)] [[code](https://github.com/securesystemslab/agamotto)]

[2020: "Using syzkaller, part 1: Fuzzing the Linux kernel" by Andre Almeida](https://www.collabora.com/news-and-blog/blog/2020/03/26/syzkaller-fuzzing-the-kernel/) [article]

[2020: "Using syzkaller, part 2: Detecting programming bugs in the Linux kernel" by Andre Almeida](https://www.collabora.com/news-and-blog/blog/2020/04/17/using-syzkaller-to-detect-programming-bugs-in-linux/) [article]

[2020: "Using syzkaller, part 3: Fuzzing your changes" by Andre Almeida](https://www.collabora.com/news-and-blog/blog/2020/05/12/using-syzkaller-fuzzing-your-changes/) [article]

[2020: "Using syzkaller, part 4: Driver fuzzing" by Andre Almeida](https://www.collabora.com/news-and-blog/blog/2020/06/26/using-syzkaller-part-4-driver-fuzzing/) [article]

[2020: "Effective Detection of Sleep-in-atomic-context Bugs in the Linux Kernel"](https://dl.acm.org/doi/pdf/10.1145/3381990) [paper]

[2020: "KRACE: Data Race Fuzzing for Kernel File Systems"](https://www.cc.gatech.edu/~mxu80/pubs/xu:krace.pdf) [paper] [[video](https://www.youtube.com/watch?v=8m2fMxvRtgg)]

[2020: "USBFuzz: A Framework for Fuzzing USB Drivers by Device Emulation" by Hui Peng and Mathias Payer](https://nebelwelt.net/publications/files/20SEC3.pdf) [paper]

[2020: "HFL: Hybrid Fuzzing on the Linux Kernel"](https://www.ndss-symposium.org/wp-content/uploads/2020/02/24018.pdf) [paper]

[2020: "KOOBE: Towards Facilitating Exploit Generation of Kernel Out-Of-Bounds Write Vulnerabilities"](https://www.usenix.org/system/files/sec20summer_chen-weiteng_prepub.pdf) [paper]

[2020: "Analyzing the Linux Kernel in Userland with AFL and KLEE"](https://blog.grimm-co.com/post/analyzing-the-linux-kernel-in-userland-with-afl-and-klee/) [article]

[2020: "Precisely Characterizing Security Impact in a Flood of Patches via Symbolic Rule Comparison"](https://www.ndss-symposium.org/wp-content/uploads/2020/02/24419-paper.pdf) [paper] [[slides](https://www.ndss-symposium.org/wp-content/uploads/24419-slides.pdf)] [[video](https://www.youtube.com/watch?v=fpkXkvwKbZw)]

[2020: "Finding Race Conditions in Kernels: from Fuzzing to Symbolic Execution" by Meng Xu](https://gts3.org/assets/papers/2020/xu:thesis.pdf) [thesis]

[2020: "A Hybrid Interface Recovery Method for Android Kernels Fuzzing"](https://qrs20.techconf.org/QRS2020_FULL/pdfs/QRS2020-4LGdOos7NAbR8M2s6S6ezE/891300a335/891300a335.pdf) [paper]

[2019: "perf fuzzer: Exposing Kernel Bugs by Detailed Fuzzing of a Specific System Call (2019 Update)" by Vincent M. Weaver and Dave Jones](http://web.eece.maine.edu/~vweaver/projects/perf_events/fuzzer/2019_perf_fuzzer_tr.pdf) [paper]

[2019: "Industry Practice of Coverage-Guided Enterprise Linux Kernel Fuzzing"](http://wingtecher.com/themes/WingTecherResearch/assets/papers/fse19-linux-kernel.pdf) [paper]

[2019: "Effective Static Analysis of Concurrency Use-After-Free Bugs in Linux Device Drivers"](https://hal.inria.fr/hal-02182516/document) [paper]

[2019: "A gentle introduction to Linux Kernel fuzzing" by Marek Majkowski](https://blog.cloudflare.com/a-gentle-introduction-to-linux-kernel-fuzzing/) [article]

[2019: "Unicorefuzz: On the Viability of Emulation for Kernelspace Fuzzing"](https://www.usenix.org/system/files/woot19-paper_maier.pdf) [paper]

[2019: "Case study: Searching for a vulnerability pattern in the Linux kernel" by Alexander Popov](https://a13xp0p0v.github.io/2019/08/10/cfu.html) [article]

[2019: "Razzer: Finding Kernel Race Bugs through Fuzzing"](https://www.youtube.com/watch?v=9UszCIxc0r0) [video] [[paper](https://lifeasageek.github.io/papers/jeong:razzer.pdf)]

[2019: "Fuzzing File Systems via Two-Dimensional Input Space Exploration"](https://taesoo.kim/pubs/2019/xu:janus.pdf) [paper] [[fuzzer](https://github.com/sslab-gatech/janus)]

[2019: "PeriScope: An Effective Probing and Fuzzing Framework for the Hardware-OS Boundary"](https://www.ndss-symposium.org/wp-content/uploads/2019/02/ndss2019_04A-1_Song_paper.pdf) [paper]

[2019: "Hourglass Fuzz: A Quick Bug Hunting Method"](https://conference.hitb.org/hitbsecconf2019ams/materials/D1T2%20-%20Hourglass%20Fuzz%20-%20A%20Quick%20Bug%20Hunting%20Method%20-%20Moony%20Li,%20Todd%20Han,%20Lance%20Jiang%20&%20Lilang%20Wu.pdf) [slides]

[2019: "Detecting Missing-Check Bugs via Semantic- and Context-Aware Criticalness and Constraints Inferences"](https://www.usenix.org/system/files/sec19-lu.pdf) [paper] [[slides](https://www.usenix.org/sites/default/files/conference/protected-files/sec19_slides_lu.pdf)]

[2019: "Automatically Identifying Security Checks for Detecting Kernel Semantic Bugs"](https://github.com/QiushiWu/QiushiWu.github.io/blob/main/papers/cheq.pdf) [paper]

[2018: "FastSyzkaller: Improving Fuzz Efficiency for Linux Kernel Fuzzing"](https://iopscience.iop.org/article/10.1088/1742-6596/1176/2/022013/pdf) [paper]

[2018: "Writing the worlds worst Android fuzzer, and then improving it" by Brandon Falk](https://gamozolabs.github.io/fuzzing/2018/10/18/terrible_android_fuzzer.html) [article]

[2018: "From Thousands of Hours to a Couple of Minutes: Towards Automating Exploit Generation for Arbitrary Types of Kernel Vulnerabilities"](http://i.blackhat.com/us-18/Thu-August-9/us-18-Wu-Towards-Automating-Exploit-Generation-For-Arbitrary-Types-of-Kernel-Vulnerabilities.pdf) [slides] [[paper](http://i.blackhat.com/us-18/Thu-August-9/us-18-Wu-Towards-Automating-Exploit-Generation-For-Arbitrary-Types-of-Kernel-Vulnerabilities-wp.pdf)]

[2018: "MoonShine: Optimizing OS Fuzzer Seed Selection with Trace Distillation"](http://www.cs.columbia.edu/~suman/docs/moonshine.pdf) [paper] [[code](https://github.com/shankarapailoor/moonshine)]

[2018: "Detecting Kernel Memory Disclosure with x86 Emulation and Taint Tracking" by Mateusz Jurczyk](https://j00ru.vexillium.org/papers/2018/bochspwn_reloaded.pdf) [paper]

[2018: "New Compat Vulnerabilities In Linux Device Drivers" at BlackHat](https://www.blackhat.com/docs/asia-18/asia-18-Ding-New-Compat-Vulnerabilities-In-Linux-Device-Drivers.pdf) [slides]

[2018: "Precise and Scalable Detection of Double-Fetch Bugs in OS Kernels"](http://www-users.cs.umn.edu/~kjlu/papers/deadline.pdf) [paper]

[2018: "Concolic Testing for Kernel Fuzzing and Vulnerability Discovery" by Vitaly Nikolenko at OffensiveCon](https://www.youtube.com/watch?v=mpfKN1URqdQ) [video]

[2018: "K-Miner: Uncovering Memory Corruption in Linux"](http://lib.21h.io/library/XHEQU6AX/download/SLDEJFQG/2018_K-Miner_-_Uncovering_Memory_Corruption_in_Linux_Internet_Society.pdf) [paper]

[2017: "KernelMemorySanitizer (KMSAN)" by Alexander Potapenko](https://blog.linuxplumbersconf.org/2017/ocw/system/presentations/4825/original/KMSAN%20presentation%20for%20LPC%202017.pdf) [slides]

[2017: "The android vulnerability discovery in SoC" by Yu Pan and Yang Dai](http://powerofcommunity.net/poc2017/yu.pdf) [slides]

[2017: "Evolutionary Kernel Fuzzing" by Richard Johnson at Black Hat USA](https://moflow.org/Presentations/Evolutionary%20Kernel%20Fuzzing-BH2017-rjohnson-FINAL.pdf) [slides]

[2017: "DIFUZE: Interface Aware Fuzzing for Kernel Drivers"](https://www.blackhat.com/docs/eu-17/materials/eu-17-Corina-Difuzzing-Android-Kernel-Drivers.pdf) [slides] [[paper](https://www.blackhat.com/docs/eu-17/materials/eu-17-Corina-Difuzzing-Android-Kernel-Drivers-wp.pdf)]

[2017: "SemFuzz: Semantics-based Automatic Generation of Proof-of-Concept Exploits" at CCS](https://acmccs.github.io/papers/p2139-youA.pdf) [paper]

[2017: "kAFL: Hardware-Assisted Feedback Fuzzing for OS Kernels" at USENIX](https://www.usenix.org/system/files/conference/usenixsecurity17/sec17-schumilo.pdf) [paper]

[2017: "How Double-Fetch Situations turn into DoubleFetch Vulnerabilities: A Study of Double Fetches in the Linux Kernel" at USENIX](https://www.usenix.org/system/files/conference/usenixsecurity17/sec17-wang.pdf) [paper]

[2017: "DR. CHECKER: A Soundy Analysis for Linux Kernel Drivers" at USENIX](https://www.usenix.org/system/files/conference/usenixsecurity17/sec17-machiry.pdf) [paper]

[2016: "Using Static Checking To Find Security Vulnerabilities In The Linux Kernel" by Vaishali Thakkar](http://events17.linuxfoundation.org/sites/events/files/slides/Using%20static%20checking%20to%20find%20security%20vulnerabilities%20in%20the%20Linux%20Kernel.pdf) [slides]

[2016: "UniSan: Proactive Kernel Memory Initialization to Eliminate Data Leakages"](https://gts3.org/assets/papers/2016/lu:unisan.pdf) [paper]

[2016: "An Analysis on the Impact and Detection of Kernel Stack Infoleaks"](https://www.researchgate.net/publication/298313650_An_Analysis_on_the_Impact_and_Detection_of_Kernel_Stack_Infoleaks) [paper]

[2016: "Syzkaller, Future Developement" by Dmitry Vyukov at Linux Plumbers](https://docs.google.com/presentation/d/1iAuTvzt_xvDzS2misXwlYko_VDvpvCmDevMOq2rXIcA/edit#slide=id.p) [slides]

[2016: "Coverage-guided kernel fuzzing with syzkaller"](https://lwn.net/Articles/677764/) [article]

[2016: "Filesystem Fuzzing with American Fuzzy Lop" by Vegard Nossum and Quentin Casasnovas](https://events.linuxfoundation.org/sites/events/files/slides/AFL%20filesystem%20fuzzing%2C%20Vault%202016_0.pdf) [slides]

[2016: "Project Triforce: AFL + QEMU + kernel = CVEs! (or) How to use AFL to fuzz arbitrary VMs" at ToorCon](https://github.com/nccgroup/TriforceAFL/blob/master/slides/ToorCon16_TriforceAFL.pdf) [slides]

[2015: "KernelAddressSanitizer (KASan): a fast memory error detector for the Linux kernel" by Andrey Konovalov at LinuxCon North America](http://events.linuxfoundation.org/sites/events/files/slides/LinuxCon%20North%20America%202015%20KernelAddressSanitizer.pdf) [slides]

[2015: "Introduction to USB and Fuzzing" by Matt DuHarte at DEF CON](https://www.youtube.com/watch?v=KWOTXypBt4E) [video]

[2015: "Don't Trust Your USB! How to Find Bugs in USB Device Drivers" by Sergej Schumilo, Ralf Spenneberg, and Hendrik Schwartke at Black Hat](https://www.youtube.com/watch?v=OAbzN8k6Am4) [video]

[2012: "Comprehensive Kernel Instrumentation via Dynamic Binary Translation"](http://www.cs.toronto.edu/~peter/feiner_asplos_2012.pdf) [paper]

[2010: "Automatic Bug-finding Techniques for Linux Kernel" by Jiri Slaby](https://www.fi.muni.cz/~xslaby/sklad/teze.pdf) [paper]

[2009: "Opensource Kernel Auditing and Exploitation" by Silvio Cesare at DEF CON](https://www.youtube.com/watch?v=sNh2TD6Tf9Q&feature=youtu.be) [video]


## Defensive

["Linux Kernel Defence Map" by Alexander Popov](https://github.com/a13xp0p0v/linux-kernel-defence-map)

[2024: "On Kernel's Safety in the Spectre Era (And KASLR is Formally Dead)" by Davide Davoli et al.](https://arxiv.org/pdf/2406.07278) [paper]

[2024: "Challenges and innovations towards safer flexible arrays in the Linux Kernel" by Gustavo A. R. Silva](https://embeddedor.com/slides/2024/llc/llc2024.pdf) [slides]

[2024: "Mitigating Integer Overflow in C" by Kees Cook](https://outflux.net/slides/2024/lss-na/) [slides] [[video](https://www.youtube.com/watch?v=PLcZkgHCk90)]

[2024: "Gaining bounds-checking on trailing arrays in the Upstream Linux Kernel" by Gustavo A. R. Silva](https://embeddedor.com/slides/2024/eo/eo2024.pdf) [slides]

[2024: "A Hybrid Alias Analysis Framework and Its Application to Protecting the Linux Kernel" by Guoren Li](https://www.youtube.com/watch?v=F4L2mBqnh30) [video]

[2024: "Hardening the kernel against heap-spraying attacks" by Jonathan Corbet](https://lwn.net/Articles/965837/) [article]

[2024: "Notes on the 'slab: Introduce dedicated bucket allocator' series" by Julien Voisin](https://dustri.org/b/notes-on-the-slab-introduce-dedicated-bucket-allocator-series.html) [article]

[2023: "Exploring Linux's New Random Kmalloc Caches" by sam4k](https://sam4k.com/exploring-linux-random-kmalloc-caches/) [article]

[2023: "Toolchain security features status update"](https://outflux.net/slides/2023/lpc/features.pdf) [slides] [[video](https://www.youtube.com/watch?v=OEFFqhP5sts)]

[2023: "Enable MTE on Pixel 8" by Kees Cook](https://outflux.net/blog/archives/2023/10/26/enable-mte-on-pixel-8/) [article]

[2023: "Gaining bounds-checking on trailing arrays in the Upstream Linux Kernel" by Gustavo A. R. Silva](https://speakerdeck.com/ennael/gaining-bounds-checking-on-trailing-arrays-in-the-upstream-linux-kernel) [slides] [[video](https://www.youtube.com/watch?v=bfKrLH7pLBQ)]

[2023: "CONSTIFY: Fast Defenses for New Exploits" by Mathias Krause](https://grsecurity.net/constify_fast_defenses_for_new_exploits) [article]

[2023: "Mitigating Security Risks in Linux with KLAUS: A Method for Evaluating Patch Correctness"](https://www.usenix.org/system/files/usenixsecurity23-wu-yuhang.pdf) [paper] [[slides](https://www.usenix.org/system/files/sec23_slides_wu-yuhang.pdf)]

[2023: "Progress On Bounds Checking in C and the Linux Kernel" by Kees Cook & Gustavo A. R. Silva](https://outflux.net/slides/2023/lss-na/bounds-checking.pdf) [slides] [[video](https://www.youtube.com/watch?v=V2kzptQG5_A)]

[2023: "Mobile Exploitation - The past, present, and the future" by Ki Chan Ahn](https://github.com/externalist/presentations/blob/master/2023%20Zer0con/Mobile%20Exploitation%2C%20the%20past%2C%20present%2C%20and%20future.pdf) [slides]

[2023: "Bounded Flexible Arrays in C" by Kees Cook](https://people.kernel.org/kees/bounded-flexible-arrays-in-c) [article]

[2022: "Survey of security mitigations and architectures, December 2022" by Saar Amar](https://saaramar.github.io/memory_safety_blogpost_2022/) [article]

[2022: "Canary in the Kernel Mine: Exploiting and Defending Against Same-Type Object Reuse" by Mathias Krause](https://grsecurity.net/exploiting_and_defending_against_same_type_object_reuse) [article] [[reference exploits](https://github.com/opensrcsec/same_type_object_reuse_exploits)]

[2022: "Making Linux Kernel Exploit Cooking Harder"](https://security.googleblog.com/2022/08/making-linux-kernel-exploit-cooking.html) [article] [[reference exploits](https://docs.google.com/document/d/1a9uUAISBzw3ur1aLQqKc5JOQLaJYiOP5pe_B4xCT1KA/edit?usp=sharing)] [[proposed mitigations](https://github.com/thejh/linux/blob/slub-virtual/MITIGATION_README)]

[2022: "Where are we on security features?"](https://lpc.events/event/16/contributions/1173/attachments/1099/2108/LPC22%20-%20Where%20are%20we%20on%20security%20features%3F.pdf) [slides] [[video](https://www.youtube.com/watch?v=tQwv79i02ks)]

[2022: "Control-Flow Integrity Kernel Support"](https://lpc.events/event/16/contributions/1315/attachments/1067/2169/cfi.pdf) [slides] [[video](https://www.youtube.com/watch?v=bmv6blX_F_g)]

[2022: "HotBPF - An On-demand and On-the-fly Memory Protection for the Linux Kernel"](https://www.youtube.com/watch?v=1KSLTsgxaSU) [video]

[2022: "Mind The Gap - The Linux Ecosystem Kernel Patch Gap" by Jakob Lell & Regina Biro](https://www.youtube.com/watch?v=WkJQImkOkNk) [video]

[2022: "The exploit recon 'msg_msg' and its mitigation in VED"](https://hardenedvault.net/blog/2022-11-13-msg_msg-recon-mitigation-ved/) [article]

[2022: "Return to sender: Detecting kernel exploits with eBPF" by Guillaume Fournier at Black Hat USA](https://i.blackhat.com/USA-22/Wednesday/US-22-Fournier-Return-To-Sender.pdf) [slides] [[code](https://github.com/Gui774ume/krie)]

[2022: "Meaningful Bounds Checking in the Linux Kernel" by Kees Cook](https://outflux.net/slides/2022/lss-na/) [slides]

[2022: "Compilers: The Old New Security Frontier" by Brad Spengler](https://grsecurity.net/Compilers_The_Old_New_Security_Frontier_BlueHat_IL_2022.pdf) [slides]

[2022: "In-Kernel Control-Flow Integrity on Commodity OSes using ARM Pointer Authentication"](https://www.usenix.org/system/files/sec22fall_yoo.pdf) [paper] [[slides](https://www.usenix.org/system/files/sec22_slides-yoo.pdf)]

[2022: "Preventing Kernel Hacks with HAKC"](https://nebelwelt.net/files/22NDSS2.pdf) [paper]

[2022: "Mitigating Processor Vulnerabilities by Restructuring the Kernel Address Space" by Sebastian Eydam](https://fosdem.org/2022/schedule/event/seydam/attachments/slides/4837/export/events/attachments/seydam/slides/4837/fosdem_pres_seydam.pdf) [slides]

[2022: "Meaningful Bounds Checking in the Linux Kernel" by Kees Cook at Linux Conf AU](https://outflux.net/slides/2022/lca/) [slides] [[video](https://www.youtube.com/watch?v=17Nqwl30Ch0)]

[2022: "Mitigating kernel risks on 32-bit ARM" by Ard Biesheuvel](https://security.googleblog.com/2022/02/mitigating-kernel-risks-on-32-bit-arm.html) [article]

[2022: "Kernel Hardening for 32-bit Arm Processors" by Keith Packard at Linux Conf AU](https://www.youtube.com/watch?v=kmMGdSVDVuQ) [video]

[2021: "Mitigating Linux kernel memory corruptions with Arm Memory Tagging" by Andrey Konovalov](https://docs.google.com/presentation/d/1IpICtHR1T3oHka858cx1dSNRu2XcT79-RCRPgzCuiRk/edit?usp=sharing) [slides] [[video](https://www.youtube.com/watch?v=UwMt0e_dC_Q)]

[2021: "Attack surface analysis of the Linux kernel based on complexity metrics" by Stefan Bavendiek](https://www.researchgate.net/profile/Stefan-Bavendiek/publication/365872100_Attack_surface_analysis_of_the_Linux_kernel_based_on_complexity_metrics/links/638786d9bbdef30dc9877e26/Attack-surface-analysis-of-the-Linux-kernel-based-on-complexity-metrics.pdf) [thesis]

[2021: "Midas: Systematic Kernel TOCTTOU Protection" at USENIX](https://www.usenix.org/system/files/sec22summer_bhattacharyya.pdf) [paper] [[slides](https://www.usenix.org/system/files/sec22_slides-bhattacharyya.pdf)]

[2021: "Undo Workarounds for Kernel Bugs" at USENIX](https://www.usenix.org/system/files/sec21-talebi.pdf) [paper] [[slides](https://www.usenix.org/system/files/sec21_slides_talebi.pdf)] [[video](https://www.youtube.com/watch?v=4QwMMCjAll8)]

[2021: "SHARD: Fine-Grained Kernel Specialization with Context-Aware Hardening" at USENIX](https://www.usenix.org/system/files/sec21-abubakar.pdf) [[slides](https://www.usenix.org/system/files/sec21_slides_abubakar.pdf)] [[video](https://www.youtube.com/watch?v=ts3MQPTtFkg)]

[2021: "Mitigation of Kernel Memory Corruption Using Multiple Kernel Memory Mechanism"](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9502080) [paper]

[2021: "Hardware-Assisted Fine-Grained Control-Flow Integrity: Adding Lasers to Intel's CET/IBT" by Joao Moreira](https://static.sched.com/hosted_files/lssna2021/8f/LSS_FINEIBT_JOAOMOREIRA.pdf) [slides] [[video](https://www.youtube.com/watch?v=FzGIM1218Ok)]

[2021: "Kernel Self-Protection Project" by Kees Cook](https://outflux.net/slides/2021/lss/kspp.pdf) [slides] [[video](https://www.youtube.com/watch?v=-Binxid8t_8)]

[2021: "Compiler Features for Kernel Security" by Kees Cook](https://linuxplumbersconf.org/event/11/contributions/1026/attachments/884/1692/compiler-features-for-kernel-security.pdf) [slides] [[video](https://www.youtube.com/watch?v=txIgZ31-RHI&t=13238s)]

[2021: "A proof-carrying approach to building correct and flexible in-kernel verifiers"](https://linuxplumbersconf.org/event/11/contributions/944/attachments/893/1707/2021-09-23-lpc21.pdf) [slides] [[video](https://www.youtube.com/watch?v=WjxHKvwX8RY&t=11588s)]

[2021: "How AUTOSLAB Changes the Memory Unsafety Game" by Zhenpeng Lin](https://grsecurity.net/how_autoslab_changes_the_memory_unsafety_game) [article]

[2021: "security things in Linux vX.X" by Kees Cook](https://outflux.net/blog/archives/2021/02/08/security-things-in-linux-v5-8/) [articles]

[2021: "Undo Workarounds for Kernel Bugs"](https://www.usenix.org/system/files/sec21fall-talebi.pdf) [paper]

[2020: "Kernel Integrity Enforcement with HLAT In a Virtual Machine" by Chao Gao](https://static.sched.com/hosted_files/osseu2020/ce/LSSEU20_kernel%20integrity%20enforcement%20with%20HLAT%20in%20a%20virtual%20machine_v3.pdf) [slides] [[video](https://www.youtube.com/watch?v=N8avvE_neV0)]

[2020: "Linux kernel heap quarantine versus use-after-free exploits" by Alexander Popov](https://a13xp0p0v.github.io/2020/11/30/slab-quarantine.html) [article]

[2020: "State of Linux kernel security" by Dmitry Vyukov](https://github.com/ossf/wg-securing-critical-projects/blob/main/presentations/The_state_of_the_Linux_kernel_security.pdf) [slides] [[video](https://www.youtube.com/watch?v=PGwFyzh2KTA&t=1233)]

[2020: "LKRG IN A NUTSHELL" by Adam Zabrocki at OSTconf](https://www.openwall.com/presentations/OSTconf2020-LKRG-In-A-Nutshell/OSTconf2020-LKRG-In-A-Nutshell.pdf) [slides]

[2020: "Following the Linux Kernel Defence Map" by Alexander Popov at Linux Plumbers](https://linuxplumbersconf.org/event/7/contributions/775/attachments/610/1096/Following_the_Linux_Kernel_Defence_Map.pdf) [slides] [[video](https://www.youtube.com/watch?v=4c01jjbQmBc&t=8555)]

[2020: "Memory Tagging for the Kernel: Tag-Based KASAN" by Andrey Konovalov](https://docs.google.com/presentation/d/10V_msbtEap9dNerKvTrRAzvfzYdrQFC8e2NYHCZYJDE/edit?usp=sharing) [slides] [[video](https://www.youtube.com/watch?v=f-Rm7JFsJGI)]

[2020: "10 Years of Linux Security - A Report Card" by Bradley Spengler](https://grsecurity.net/10_years_of_linux_security.pdf) [slides] [[video](https://www.youtube.com/watch?v=F_Kza6fdkSU)]

[2020: "Control Flow Integrity in the Linux Kernel" by Kees Cook at linux.conf.au](https://outflux.net/slides/2020/lca/cfi.pdf) [slides] [[video](https://www.youtube.com/watch?v=0Bj6W7qrOOI)]

[2020: "Identification of Kernel Memory Corruption Using Kernel Memory Secret Observation Mechanism"](https://www.jstage.jst.go.jp/article/transinf/E103.D/7/E103.D_2019ICP0011/_pdf/-char/en) [paper]

[2019: "Camouflage: Hardware-assisted CFI for the ARM Linux kernel"](https://arxiv.org/pdf/1912.04145v1.pdf) [paper]

[2019: "A New Proposal for Protecting Kernel Data Memory" by Igor Stoppa at Linux Security Summit EU](https://www.youtube.com/watch?v=nPH2sQAD6RY) [video]

[2019: "Control-Flow Integrity for the Linux kernel: A Security Evaluation" by Federico Manuel Bento](http://www.alunos.dcc.fc.up.pt/~up201407890/Thesis.pdf) [thesis]

[2019: "Kernel Self-Protection Project" by Kees Cook](https://outflux.net/slides/2019/lss/kspp.pdf) [slides]

[2019: "Touch but don’t look - Running the Kernel in Execute-only memory" by Rick Edgecombe](https://linuxplumbersconf.org/event/4/contributions/283/attachments/357/588/Touch_but_dont_look__Running_the_kernel_in_execute_only_memory-presented.pdf) [slides]

[2019: "Breaking and Protecting Linux Kernel Stack" by Elena Reshetova](https://www.youtube.com/watch?v=FacpjoQbMhU) [video]

[2019: "Making C Less Dangerous in the Linux Kernel" by Kees Cook](https://outflux.net/slides/2019/lca/danger.pdf) [slides]

[2019: "Mitigation for the Kernel Space Mirroring Attack (内核镜像攻击的缓解措施)"](http://c0reteam.org/2019/01/02/ksma) [article]

[2018: "The State of Kernel Self Protection" by Kees Cook](https://outflux.net/slides/2018/lss/kspp.pdf) [slides]

[2018: "Android Kernel Control Flow Integrity Analysis (分析)"](http://c0reteam.org/2018/09/17/kcfi) [article]

[2018: "Overview and Recent Developments: Kernel Self-Protection Project" by Kees Cook](https://outflux.net/slides/2018/lss-eu/kspp.pdf) [slides]

[2018: "The Last Man Standing: The Only Practical, Lightweight and Hypervisor-Based Kernel Protector Struggling with the Real World Alone" by Seunghun Han at beVX](https://github.com/kkamagui/papers/blob/master/bevx-2018/presentation.pdf) [video]

[2018: "Linux Kernel Runtime Guard (LKRG) under the hood" by Adam Zabrocki at CONFidence](https://www.openwall.com/presentations/CONFidence2018-LKRG-Under-The-Hood/CONFidence2018-LKRG-Under-The-Hood.pdf) [slides, [video](https://www.youtube.com/watch?v=tOiPM692DOM)]

[2018: "GuardION: Practical Mitigation of DMA-based Rowhammer Attacks on ARM"](https://vvdveen.com/publications/dimva2018.pdf) [paper]

[2018: "kR^X: Comprehensive Kernel Protection Against Just-In-Time Code Reuse" at BlackHat](https://www.youtube.com/watch?v=L-3eCmZ8s3A) [video]

[2018: "KASR: A Reliable and Practical Approach to Attack Surface Reduction of Commodity OS Kernels"](https://arxiv.org/pdf/1802.07062.pdf) [paper]

[2018: "The State of Kernel Self Protection" by Kees Cook at Linux Conf AU](https://outflux.net/slides/2018/lca/kspp.pdf) [slides]

[2017: "kR^X: Comprehensive Kernel Protection against Just-In-Time Code Reuse"](https://cs.brown.edu/~vpk/papers/krx.eurosys17.pdf) [paper]

[2017: "How STACKLEAK improves Linux kernel security" by Alexander Popov at Linux Piter](https://linuxpiter.com/system/attachments/files/000/001/376/original/Alexander_Popov_LinuxPiter2017.pdf) [slides]

[2017: "Shadow-Box: The Practical and Omnipotent Sandbox" by Seunghun Han at HitB](http://conference.hitb.org/hitbsecconf2017ams/materials/D1T2%20-%20Seunghun%20Han%20-%20Shadow-Box%20-%20The%20Practical%20and%20Omnipotent%20Sandbox.pdf) [slides]

[2017: "Towards Linux Kernel Memory Safety"](https://arxiv.org/pdf/1710.06175.pdf) [paper]

[2017: "Proposal of a Method to Prevent Privilege Escalation Attacks for Linux Kernel"](https://events.linuxfoundation.org/sites/events/files/slides/nakamura_20170831_1.pdf) [slides]

[2017: "Linux Kernel Self Protection Project" by Kees Cook](https://outflux.net/slides/2017/lss/kspp.pdf) [slides]

[2017: "PT-Rand: Practical Mitigation of Data-only Attacks against Page Tables"](https://www.internetsociety.org/sites/default/files/ndss2017_05B-4_Davi_paper.pdf) [paper] [[slides](https://www.ndss-symposium.org/wp-content/uploads/2017/09/ndss2017-05B-4-liebchen_slides.pdf)] [[video](https://www.youtube.com/watch?v=l-ou5LqOOy4)]

[2017: "KASLR is Dead: Long Live KASLR"](https://gruss.cc/files/kaiser.pdf) [paper]

[2017: "Honey, I shrunk the attack surface – Adventures in Android security hardening" by Nick Kralevich](https://www.youtube.com/watch?v=ITL6VHOFQj8) [video]

[2017: "Fine Grained Control-Flow Integrity for The Linux Kernel" by Sandro Rigo, Michalis Polychronakis, Vasileios Kemerlis](https://www.blackhat.com/docs/asia-17/materials/asia-17-Moreira-Drop-The-Rop-Fine-Grained-Control-Flow-Integrity-For-The-Linux-Kernel.pdf) [slides]

[2016: "Thwarting unknown bugs: hardening features in the mainline Linux kernel" by Mark Rutland](https://events.static.linuxfound.org/sites/events/files/slides/slides_21.pdf) [slides]

[2016: "Emerging Defense in Android Kernel" by James Fang](http://keenlab.tencent.com/en/2016/06/01/Emerging-Defense-in-Android-Kernel/) [article]

[2016: "Randomizing the Linux kernel heap freelists" by Thomas Garnier](https://medium.com/@mxatone/randomizing-the-linux-kernel-heap-freelists-b899bb99c767#.3csq8t23s) [article]

[2015: "RAP: RIP ROP"](https://pax.grsecurity.net/docs/PaXTeam-H2HC15-RAP-RIP-ROP.pdf) [slides]

[2015: "Protecting Commodity Operating Systems through Strong Kernel Isolation" by Vasileios Kemerlis](http://www.cs.columbia.edu/~angelos/Papers/theses/vpk_thesis.pdf) [paper]

[2014: "Kernel Self-Protection through Quantified Attack Surface Reduction" by Anil Kurmus](https://publikationsserver.tu-braunschweig.de/servlets/MCRFileNodeServlet/digibib_derivate_00036154/Diss_Kurmus_Anil.pdf) [paper]

[2014: "A Tale of Two Kernels: Towards Ending Kernel Hardening Wars with Split Kernel" by Anil Kurmus and Robby Zippel](http://static.securegoose.org/papers/ccs14.pdf) [paper]

[2013: "KASLR: An Exercise in Cargo Cult Security" by Brad Spengler](https://forums.grsecurity.net/viewtopic.php?f=7&t=3367) [article]

[2012: "How do I mitigate against NULL pointer dereference vulnerabilities?" by RedHat](https://access.redhat.com/articles/20484) [article]

[2011: "Linux kernel vulnerabilities: State-of-the-art defenses and open problems"](https://pdos.csail.mit.edu/papers/chen-kbugs.pdf) [paper]

[2009: "Linux Kernel Heap Tampering Detection" by Larry Highsmith](http://phrack.org/archives/issues/66/15.txt) [article]


## Exploits

[Project Zero bug reports](https://bugs.chromium.org/p/project-zero/issues/list?can=1&q=linux%20kernel&colspec=ID%20Type%20Status%20Priority%20Milestone%20Owner%20Summary&cells=ids&sort=-id)

https://github.com/bsauce/kernel-exploit-factory

https://www.exploit-db.com/search/?action=search&description=linux+kernel

https://github.com/offensive-security/exploit-database/tree/master/platforms/linux/local

http://vulnfactory.org/exploits/ [2010-2011]

https://github.com/dirtycow/dirtycow.github.io/wiki/PoCs

https://github.com/ScottyBauer/Android_Kernel_CVE_POCs

https://github.com/f47h3r/hackingteam_exploits

https://github.com/xairy/kernel-exploits

https://github.com/milabs/kernel-exploits/blob/master/CVE-2017-1000112/poc.c (CVE-2017-1000112 exploit with LKRG bypass)

https://github.com/Kabot/Unix-Privilege-Escalation-Exploits-Pack

https://github.com/SecWiki/linux-kernel-exploits

https://grsecurity.net/~spender/exploits/

https://github.com/jiayy/android_vuln_poc-exp

https://github.com/marsyy/littl_tools/tree/master/bluetooth

https://github.com/nongiach/CVE/tree/master/CVE-2017-5123

http://seclists.org/fulldisclosure/2010/Sep/268

https://github.com/hardenedlinux/offensive_poc

https://github.com/brl/grlh

https://github.com/externalist/exploit_playground

https://github.com/ww9210/Linux_kernel_exploits [FUZE]

https://github.com/ww9210/kepler-cfhp [KEPLER]

https://github.com/yzimhao/godpock

https://github.com/packetforger/localroot

http://www.cs.columbia.edu/~vpk/research/ret2dir/

https://github.com/w0lfzhang/kernel_exploit

https://github.com/jinb-park/linux-exploit

https://github.com/bcoles/kernel-exploits

https://github.com/jollheef/lpe

https://github.com/tangsilian/android-vuln

https://github.com/grant-h/qu1ckr00t

https://github.com/kangtastic/cve-2019-2215

https://github.com/QuestEscape/exploit

https://github.com/duasynt/xfrm_poc

https://github.com/snorez/exploits/

https://github.com/saelo/cve-2014-0038

https://github.com/bluefrostsecurity/CVE-2020-0041/

https://github.com/chompie1337/s8_2019_2215_poc/

https://github.com/c3r34lk1ll3r/CVE-2017-5123

https://haxx.in/blasty-vs-ebpf.c

https://github.com/scannells/exploits/tree/master/CVE-2020-27194

https://github.com/lntrx/CVE-2021-28663

https://haxx.in/files/dirtypipez.c

https://github.com/Arinerron/CVE-2022-0847-DirtyPipe-Exploit

https://github.com/polygraphene/DirtyPipe-Android

https://github.com/Bonfee/CVE-2022-25636

https://github.com/Bonfee/CVE-2022-0995

https://github.com/tr3ee/CVE-2022-23222

https://github.com/tr3ee/CVE-2021-4204

[Linux Kernel SCTP FORWARD-TSN Chunk Memory Corruption Remote Exploit](https://subreption.com/offensive-security/exploits/sctp_thermite/) [CVE-2009-0065]

https://github.com/xkaneiki/CVE-2023-0386

https://www.openwall.com/lists/oss-security/2023/05/08/3 [CVE-2023-2598]

https://www.openwall.com/lists/oss-security/2023/05/15/5 [CVE-2023-32233]

https://github.com/Liuk3r/CVE-2023-32233

https://github.com/lanleft/CVE2023-1829

https://github.com/TurtleARM/CVE-2023-3338-DECPwn

https://github.com/kungfulon/nf-tables-lpe

https://github.com/ysanatomic/io_uring_LPE-CVE-2024-0582

https://github.com/YuriiCrimson/ExploitGSM/ [[notes](https://mastodon.social/@gabe_k/112251322421680553)] [[discussion](https://www.openwall.com/lists/oss-security/2024/04/10/18)]

https://github.com/roddux/germy

https://github.com/renorobert/tagbleedvmm


## Tools

### Fuzzers

https://github.com/google/syzkaller

https://github.com/kernelslacker/trinity

http://web.eece.maine.edu/~vweaver/projects/perf_events/fuzzer/

https://github.com/nccgroup/TriforceLinuxSyscallFuzzer

https://github.com/oracle/kernel-fuzzing

https://github.com/rgbkrk/iknowthis

https://github.com/schumilo/vUSBf

https://github.com/ucsb-seclab/difuze

https://github.com/compsec-snu/razzer [race-condition]

https://github.com/fgsect/unicorefuzz

https://github.com/SunHao-0/healer

https://github.com/atrosinenko/kbdysch

https://github.com/intel/kernel-fuzzer-for-xen-project

https://github.com/IntelLabs/kAFL/

https://github.com/snorez/ebpf-fuzzer

https://github.com/SmoothHacker/LateRegistration

https://github.com/sslab-gatech/janus

https://github.com/google/buzzer

https://github.com/h0mbre/Lucid


### Assorted

https://github.com/jonoberheide/ksymhunter

https://github.com/jonoberheide/kstructhunter

https://github.com/ngalongc/AutoLocalPrivilegeEscalation

https://github.com/PenturaLabs/Linux_Exploit_Suggester

https://github.com/jondonas/linux-exploit-suggester-2

https://github.com/mzet-/linux-exploit-suggester

https://github.com/spencerdodd/kernelpop

https://github.com/vnik5287/kaslr_tsx_bypass

http://www.openwall.com/lkrg/

https://github.com/IAIK/meltdown

https://github.com/nforest/droidimg

https://github.com/a13xp0p0v/kconfig-hardened-check

https://github.com/PaoloMonti42/salt

https://github.com/jollheef/out-of-tree

https://github.com/elfmaster/kdress

https://github.com/mephi42/ida-kallsyms/

[Kernel Address Space Layout Derandomization (KASLD)](https://github.com/bcoles/kasld)

https://github.com/duasynt/gdb_scripts/

https://github.com/evdenis/cvehound

https://github.com/redplait/lkcd

https://github.com/Kyle-Kyle/pwning-toolset/blob/main/linux-kernel/fgkaslr_gadgets.py

https://github.com/vusec/kasper

https://github.com/martinradev/gdb-pt-dump

https://github.com/chompie1337/kernel_obj_finder

https://github.com/marin-m/vmlinux-to-elf

https://github.com/nccgroup/libslub

https://github.com/a13xp0p0v/kernel-hardening-checker

https://github.com/heki-linux

https://github.com/oswalpalash/linux-kernel-regression-tests

https://github.com/google/security-research/blob/master/analysis/kernel/heap-exploitation/README.md [CodeQL] [[dashboard](https://lookerstudio.google.com/reporting/68b02863-4f5c-4d85-b3c1-992af89c855c/page/n92nD)]

https://github.com/milabs/kiddy

https://github.com/androidoffsec/art-kernel-toolkit

https://github.com/notselwyn/get-sig

https://github.com/gsingh93/linux-exploit-dev-env


## Practice

### Workshops

[2021: "Linux kernel exploit development"](https://breaking-bits.gitbook.io/breaking-bits/exploit-development/linux-kernel-exploit-development) [workshop]

[2020: "pwn.college: Module: Kernel Security"](https://pwn.college/modules/kernel) [workshop]

[2020: "Android Kernel Exploitation" by Ashfaq Ansari](https://github.com/cloudfuzz/android-kernel-exploitation) [workshop] [[video](https://www.youtube.com/watch?v=8ySHpVCYcbk)]


### CTF Tasks

[github.com/smallkirby/kernelpwn](https://github.com/smallkirby/kernelpwn)

[github.com/MaherAzzouzi/LinuxKernelExploitation](https://github.com/MaherAzzouzi/LinuxKernelExploitation)

[github.com/AravGarg/kernel-hacking/ctf-challs](https://github.com/AravGarg/kernel-hacking/tree/master/ctf-challs)

HackTheBox (knote): [writeup](https://pwning.tech/knote/)

RWCTF 2024 (RIPTC): [source](https://github.com/chaitin/Real-World-CTF-6th-Challenges/tree/main/RIPTC), [writeup](https://aslr.io/2024/02/04/rwctf-6th-riptc-write-up/), [writeup 2](https://github.com/N1ghtu/RWCTF6th-RIPTC)

Imaginary CTF 2023 (Windows of Opportunity): [writeup 1](https://francescolucarini.github.io/Windows-of-Opportunity/), [writeup 2](https://ctftime.org/writeup/37670)

corCTF 2023 (sysruption): [writeup](https://www.willsroot.io/2023/08/sysruption.html)

corCTF 2023 (zeroday, kcipher): [writeup](https://blog.libh0ps.so/2023/08/02/corCTF2023.html)

hxp CTF 2022 (one_byte): [writeup](https://hxp.io/blog/99/hxp-CTF-2022-one_byte-writeup/)

BFS Ekoparty 2022 (blunder): [writeup](https://klecko.github.io/posts/bfs-ekoparty-2022/)

D^3CTF 2022 (d3bpf): [writeup](https://stdnoerr.github.io/writeup/2022/08/21/eBPF-exploitation-(ft.-D-3CTF-d3bpf).html), [writeup 2](https://github.com/chujDK/d3ctf2022-pwn-d3bpf-and-v2)

zer0pts CTF 2022 (kRCE): [writeup](https://www.willsroot.io/2022/03/zer0pts-ctf-2022-krce-writeup.html)

HITCON CTF 2022 (fourchain-kernel): [writeup and exploit](https://org.anize.rs/HITCON-2022/pwn/fourchain-kernel)

VULNCON CTF 2021 (IPS): [writeup](https://kileak.github.io/ctf/2021/vulncon-ips/), [writeup 2](https://blog.kylebot.net/2022/01/10/VULNCON-2021-IPS/)

N1 CTF 2021 (baby-guess): [source](https://github.com/sajjadium/ctf-archives/tree/main/N1CTF/2021/pwn/baby_guess), [writeup](https://kileak.github.io/ctf/2021/n1ctf21-babyguess/)

Balsn CTF 2021 (futex): [source](https://github.com/sajjadium/ctf-archives/tree/main/Balsn/2021/pwn/futex), [writeup](https://gist.github.com/st424204/e6395bdbed43b1bf308a4de2ba9d6ba0)

TSG CTF 2021 (lkgit): [writeup](https://kileak.github.io/ctf/2021/tsg-lkgit/), [writeup 2](https://smallkirby.hatenablog.com/entry/2021/10/03/171804), [writeup 3](https://ptr-yudai.hatenablog.com/entry/2021/10/03/225325#pwn-322pts-lkgit-7-solves)

Midnightsun Quals 2021 (BroHammer): [writeup](https://www.willsroot.io/2021/04/midnightsunquals-2021-brohammer-single.html)

0ctf2021 (kernote): [source, exploit, and writeup](https://github.com/YZloser/My-CTF-Challenges/tree/master/0ctf-2021-final/kernote), [writeup 2](https://org.anize.rs/0CTF-2021-finals/pwn/kernote)

corCTF 2021 (fire-of-salvation): [source](https://github.com/Crusaders-of-Rust/corCTF-2021-public-challenge-archive/tree/main/pwn/fire-of-salvation), [writeup](https://www.willsroot.io/2021/08/corctf-2021-fire-of-salvation-writeup.html)

corCTF 2021 (wall-of-perdition): [source](https://github.com/Crusaders-of-Rust/corCTF-2021-public-challenge-archive/tree/main/pwn/wall-of-perdition), [writeup](https://syst3mfailure.io/wall-of-perdition)

Google CTF 2021 (pwn-fullchain): [source](https://github.com/google/google-ctf/tree/master/2021/quals/pwn-fullchain), [writeup](https://ptr-yudai.hatenablog.com/entry/2021/07/26/225308)

Google CTF 2021 (pwn-ebpf): [source](https://github.com/google/google-ctf/tree/master/2021/quals/pwn-ebpf), [writeup](https://mem2019.github.io/jekyll/update/2021/07/19/GCTF2021-eBPF.html)

3kCTF 2021 (echo): [source and exploit](https://github.com/MaherAzzouzi/3k21-pwn/tree/main/echo)

3kCTF 2021 (klibrary): [source](https://github.com/MaherAzzouzi/3k21-pwn/tree/main/klibrary), [writeup](https://meowmeowxw.gitlab.io/ctf/3k-2021-klibrary/)

DEF CON CTF Qualifier 2021 (pza999): [source and exploit](https://github.com/o-o-overflow/dc2021q-pza999-public)

DiceCTF 2021 (HashBrown): [writeup](https://www.willsroot.io/2021/02/dicectf-2021-hashbrown-writeup-from.html)

hxp CTF 2020 (pfoten): [source](https://github.com/BrieflyX/ctf-pwns/blob/master/kernel/pfoten/pfoten-c3c4a46948257e62.tar.xz), [writeup](https://mem2019.github.io/jekyll/update/2020/12/21/hxp2020-pfoten.html)

hxp CTF 2020 (kernel-rop): [writeup](https://blog.wohin.me/posts/linux-kernel-pwn-01/)

CUCTF 2020 (Hotrod): [writeup](https://syst3mfailure.io/hotrod)

SpamAndFlags 2020 (Secstore): [writeup](https://pwnfirstsear.ch/2020/05/10/spamandhexctf2020-secstore.html#secstore-1)

BSidesTLV CTF 2020 (Kapara): [writeup and exploit](https://jctf.team/BSidesTLV-2020/Kapara/), [video writeup](https://media.handmade-seattle.com/linux-kernel-adventures/)

HITCON CTF 2020 (spark): [source and exploit #1](https://github.com/david942j/ctf-writeups/tree/master/hitcon-2020/spark), [writeup and exploit #2](https://github.com/BrieflyX/ctf-pwns/tree/master/kernel/spark), [exploit #3](https://gist.github.com/sampritipanda/9fb8f1f92aef6591246e74ed5847c910)

HITCON CTF 2020 (atoms): [source and exploit](https://github.com/david942j/ctf-writeups/tree/master/hitcon-2020/atoms)

N1 CTF 2020 (W2L): [writeup](https://github.com/Nu1LCTF/n1ctf-2020/blob/main/N1CTF2020%20Writeup%20By%20Nu1L.pdf)

Seccon Online 2020 (Kstack): [source, exploit, and writeup](https://github.com/BrieflyX/ctf-pwns/tree/master/kernel/kstack)

TokyoWesterns CTF 2020 (EEBPF): [source](https://github.com/BrieflyX/ctf-pwns/tree/master/kernel/eebpf), [writeup](https://github.com/leesh3288/CTF/blob/master/2020/TWCTF_2020/eebpf/writeup.md)

r2con CTF 2020: [source](https://github.com/esanfelix/r2con2020-ctf-kernel), [exploit](https://github.com/dialluvioso/box/blob/master/r2con2020-ctf-kernel/exploit.c)

ASIS CTF 2020 (Shared House): [writeup](https://ptr-yudai.hatenablog.com/entry/2020/07/06/000622#354pts-Shared-House-7-solves)

DEF CON CTF Qualifier 2020 (fungez): [source](https://github.com/o-o-overflow/dc2020q-fungez-public), [exploit and writeup](https://github.com/BrieflyX/ctf-pwns/tree/master/kernel/fungez)

DEF CON CTF Qualifier 2020 (keml): [source](https://github.com/o-o-overflow/dc2020q-keml-public), [exploit](https://gist.github.com/LYoungJoo/4d225668991c6812701b1fcad6e18646)

zer0pts CTF 2020 (meow): [writeup](https://pr0cf5.github.io/ctf/2020/03/09/the-plight-of-tty-in-the-linux-kernel.html)

De1CTF 2019 (Race): [writeup and exploit](https://github.com/De1ta-team/De1CTF2019/tree/master/writeup/pwn/Race)

r2con CTF 2019: [source, exploit, and writeup](https://github.com/esanfelix/r2con2019-ctf-kernel)

HITCON CTF Quals 2019 (PoE): [source and exploit](https://github.com/david942j/ctf-writeups/tree/master/hitcon-quals-2019/PoE)

Balsn CTF 2019 (KrazyNote): [exploit](https://github.com/Mem2019/Mem2019.github.io/blob/master/codes/krazynote.c), [writeup](https://pr0cf5.github.io/ctf/2019/10/10/balsn-ctf-krazynote.html)

TokyoWesterns CTF 2019 (gnote): [writeup](https://rpis.ec/blog/tokyowesterns-2019-gnote/), video [part 1](https://www.youtube.com/watch?v=n7osrud3PMI), [part 2](https://www.youtube.com/watch?v=i8gZ85VC2Mw)

Security Fest 2019 (brainfuck64): [writeup](https://kileak.github.io/ctf/2019/secfest-brainfuck64/)

Insomni'hack teaser 2019 (1118daysober): [writeup 1](https://ctftime.org/writeup/12919), [writeup 2](https://github.com/EmpireCTF/empirectf/blob/master/writeups/2019-01-19-Insomni-Hack-Teaser/README.md#1118daysober)

hxp CTF 2018 (Green Computing): [writeup](http://s3.eurecom.fr/nops/2018-12-10-hxp-ctf-2018-green-computing.html)

WCTF 2018 (cpf): [source, writeup, and exploit](https://github.com/cykorteam/cykor_belluminar_2018/tree/master/cpf)

SECT CTF 2018 (Gh0st): [writeup](http://mslc.ctf.su/wp/sect-ctf-2018-gh0st/)

TWCTF 2018 (ReadableKernelModule): [writeup](http://r3ka.eu/2018/09/twctf-2018-rkm-readablekernelmodule-writeup/)

NCSTISC 2018 (babydriver): [writeup](http://f0r1st.me/2018/03/28/ROP-in-Linux-Kernel/), [source and exploit](https://github.com/w0lfzhang/kernel_exploit/tree/master/2017-ncstisc-babydriver)

Sharif CTF 2018 (kdb): [writeup](https://changochen.github.io/2018-02-07-sharif8.html), [source and exploit](https://github.com/Changochen/CTF/tree/master/2018/SharifCTF/kdb)

N1CTF 2018: [writeup](http://r3ka.eu/2018/03/n1ctf-2018-network-card-writeup/)

Blaze2018 (blazeme): [source and exploit 1](https://github.com/vakzz/ctfs/tree/master/Blaze2018/blazeme), [soure and exploit 2](https://github.com/wangray/ctf_dump/tree/master/Blaze2018/blazeme)

QWB2018 (solid_core): [writeup](http://f0r1st.me/2018/04/02/QWB2018-solid-core-Write-Up/), [exploit 1](https://github.com/w0lfzhang/kernel_exploit/tree/master/2018-qwb-core), [exploit 2](https://github.com/sixstars/ctf/tree/master/2018/qiangwangbei/core), [exploit 3](https://github.com/o0xmuhe/PwnableLog/blob/master/CTFWP/qwb2018/core/exp.c)

0ctf2018: [writeup 1](http://blog.eadom.net/writeups/0ctf-2018-zerofs-writeup/), [writeup 2](http://ddaa.tw/0ctf_pwnable_478_zer0fs.html)

TCTF 2017 (cred_jar): [writeup](http://ww9210.cn/2017/06/08/tctf-2017-final-cred_jar-linux-kernel-driver-pwn-write-up/)

0ctf2017: [source and exploit 1](https://github.com/lovelydream/0ctf2017_kernel_pwn), [source and exploit 2](https://github.com/yifengyou/CTF/tree/master/2017/0ctf/pwn/knote)

0ctf2016: [writeup](http://dragonsector.pl/docs/0ctf2016_writeups.pdf), [exploit](https://gist.github.com/anonymous/83f96600c5ae851940d6)

Insomni’hack finals 2015: [writeup](https://blog.scrt.ch/2015/03/24/insomnihack-finals-sh1tty-writeup/), [source and exploit](https://github.com/Insomnihack/Insomnihack-2015/tree/master/exploit/sh1tty)

CSAW CTF 2015: [writeup 1](https://poppopret.org/2015/11/16/csaw-ctf-2015-kernel-exploitation-challenge/), [writeup 2](http://itszn.com/blog/?p=21), [source and exploit](https://github.com/mncoppola/StringIPC)

CSAW CTF 2014: [source and exploit](https://github.com/mncoppola/suckerusu)

CSAW CTF 2013: [writeup](https://poppopret.org/2013/11/20/csaw-ctf-2013-kernel-exploitation-challenge/), [source and exploit](https://github.com/mncoppola/Brad-Oberberg)

PlaidCTF 2013 (Servr): [writeup](http://blog.frizn.fr/plaidctf-2013/pwn-400-servr), [source](http://blog.frizn.fr/fil3z/pctf-2013/servr.tar.bz2)

CSAW CTF 2011: [writeup](https://jon.oberheide.org/blog/2011/11/27/csaw-ctf-2011-kernel-exploitation-challenge/), [source](https://jon.oberheide.org/files/SqueamishOssifrage.c)

rwth2011 CTF (ps3game): [writeup](http://mslc.ctf.su/wp/rwth2011-ctf-ps3game/)

CSAW CTF 2010: [writeup](https://jon.oberheide.org/blog/2010/11/02/csaw-ctf-kernel-exploitation-challenge/), [source](https://jon.oberheide.org/files/csaw.c), [source and exploit](https://github.com/0x3f97/pwn/tree/master/kernel/csaw-ctf-2010-kernel-exploitation-challenge)


### Other tasks

["Pawnyable: Linux Kernel Exploitation" by ptr-yudai](https://pawnyable.cafe/linux-kernel/index.html) [articles] [[Holstein v3 writeup](https://h0mbre.github.io/PAWNYABLE_UAF_Walkthrough/)]

[pwnable.kr tasks](http://pwnable.kr/play.php) (syscall, rootkit, softmmu, towelroot, kcrc, exynos)

https://github.com/ReverseLab/kernel-pwn-challenge

https://github.com/R3x/How2Kernel

[OffensiveCon 2023: bfsmatrix](https://static.bluefrostsecurity.de/files/lab/bfsmatrix_offensivecon2023.tgz) [task] [[exploit](https://gist.github.com/arget13/d4006af981356cdfb0316a722a0c90e3)]

[Ekoparty 2022: blunder](https://static.bluefrostsecurity.de/files/lab/module.tar.gz) [task] [[writeup 1](https://klecko.github.io/posts/bfs-ekoparty-2022/)] [[writeup 2](https://soez.github.io/posts/Bluefrost-challenge-EKOPARTY_2022/)]


### Playgrounds

https://github.com/Fuzion24/AndroidKernelExploitationPlayground

https://github.com/djrbliss/libplayground

https://github.com/a13xp0p0v/kernel-hack-drill

https://github.com/pr0cf5/kernel-exploit-practice

https://github.com/hardik05/Damn_Vulnerable_Kernel_Module

[Kernel Read Write eXecute (KRWX)](https://github.com/hacktivesec/KRWX) [[slides](https://www.nohat.it/presentations/KRWX_agroppo.pdf)] [[playground](https://github.com/hacktivesec/beginner-kernel-exploitation-setup)]


### Infrastructure

https://github.com/mncoppola/Linux-Kernel-CTF

https://github.com/crowell/old_blog/blob/source/source/_posts/2014-11-24-hosting-a-local-kernel-ctf-challenge.markdown


## Other lists

[grsecurity/PaX Citations in Academic Research](https://grsecurity.net/research.php)

https://github.com/0xricksanchez/paper_collection

https://github.com/NetKingJ/awesome-android-security

https://github.com/0xor0ne/awesome-list/


## Misc

[2024: "silent syscall hooking on arm64 linux via patching svc handler"](https://tmpout.sh/3/23.html) [article]

[2024: "CVE-2021-4440: A Linux CNA Case Study" by Brad Spengler](https://grsecurity.net/cve-2021-4440_linux_cna_case_study) [article]

[2024: "Make your own backdoor: CFLAGS code injection, Makefile injection, pkg-config" by Vegard Nossum](https://www.openwall.com/lists/oss-security/2024/04/17/3) [article]

[2024: "Demo showing Claude Opus does not find CVE-2023-0266" by Sean Heelan](https://github.com/SeanHeelan/claude_opus_cve_2023_0266) [article]

[2024: "Linux is a CNA" by Greg Kroah-Hartman](http://www.kroah.com/log/blog/2024/02/13/linux-is-a-cna/) [article]

[2024: "An Investigation of Patch Porting Practices of the Linux Kernel Ecosystem"](https://arxiv.org/pdf/2402.05212.pdf) [paper]

[2023: "Syzbot: 7 years of continuous kernel fuzzing" by Aleksandr Nogikh](https://lpc.events/event/17/contributions/1521/attachments/1272/2698/LPC'23_%20Syzbot_%207%20years%20of%20continuous%20kernel%20fuzzing.pdf) [slides] [[video](https://www.youtube.com/watch?v=sDMNEBoTtrI)]

[2023: "Operating system security: how to get into the subject" by Alexander Popov](https://www.youtube.com/watch?v=pq-0JKKNZVQ) [video]

[2023: "Demystifying the Linux kernel security process" by Greg Kroah-Hartman](https://speakerdeck.com/ennael/demystifying-the-linux-kernel-security-process) [slides] [[video](https://www.youtube.com/watch?v=2TZe5EROFhE)]

[2023: "Rustproofing Linux" by Domen Puncer Kugler](https://research.nccgroup.com/2023/02/06/rustproofing-linux-part-1-4-leaking-addresses/) [article] [[part 2](https://research.nccgroup.com/2023/02/08/rustproofing-linux-part-2-4-race-conditions/)] [[part 3](https://research.nccgroup.com/2023/02/14/rustproofing-linux-part-3-4-integer-overflows/)] [[part 4](https://research.nccgroup.com/2023/02/16/rustproofing-linux-part-4-4-shared-memory/)]

[2023: "What is a 'good' Linux Kernel bug?" by Ben Hawkes](https://blog.isosceles.com/what-is-a-good-linux-kernel-bug/) [article]

[2023: "Analysing Linux Kernel Commits"](https://sam4k.com/analysing-linux-kernel-commits/) [article]

[2022: "Mind the Gap" by Ian Beer](https://googleprojectzero.blogspot.com/2022/11/mind-the-gap.html) [article]

[2022: "Designing subsystems for FUZZ-ability" by Dmitry Vyukov](https://lpc.events/event/16/contributions/1309/attachments/988/1979/Designing%20subsystems%20for%20testability_fuzzing%20%28PDF%20version%29.pdf) [slides] [[video](https://www.youtube.com/watch?v=zmF_AswbVbQ)]

[2022: "Making syzbot reports more developer-friendly" by Aleksandr Nogikh](https://lpc.events/event/16/contributions/1311/attachments/1013/1951/Making%20syzbot%20reports%20more%20developer-friendly.pdf) [slides] [[video](https://www.youtube.com/watch?v=ePldLzdAArg)]

[2022: "Peeking into the BPF verifier" by Shung-Hsi Yu](https://docs.google.com/presentation/d/1abYBW7L8kAupgG9YkFPRGayZSXm9hGv_Dvp7ADBkfyg/edit?usp=sharing) [slides]

[2022: "So You Wanna Pwn The Kernel?" by Samuel Page](https://sam4k.com/so-you-wanna-pwn-the-kernel/) [article]

[2022: "Automated RE of Kernel Configurations" by zznop](https://zznop.com/2022/01/02/automated-re-of-kernel-build-configs/) [article]

[2021: "An Investigation of the Android Kernel Patch Ecosystem" at USENIX](https://www.usenix.org/system/files/sec21-zhang-zheng.pdf) [paper] [[slides](https://www.usenix.org/system/files/sec21_slides_zhang-zheng.pdf)] [[video](https://www.youtube.com/watch?v=sx2unUrsQhc)]

[2021: "The Complicated History of a Simple Linux Kernel API"](https://www.grsecurity.net/complicated_history_simple_linux_kernel_api) [article]

[2021: "On the Feasibility of Stealthily Introducing Vulnerabilities in Open-Source Software via Hypocrite Commit"](https://github.com/QiushiWu/QiushiWu.github.io/blob/main/papers/OpenSourceInsecurity.pdf) [paper]

[2020: "Checklist for when you get stuck with a Kernel Exploit"](https://ptr-yudai.hatenablog.com/entry/2020/03/11/125818) [article]

[2020: "Android / Linux SLUB aliasing for general- and special-purpose caches" by Vitaly Nikolenko](https://www.youtube.com/watch?v=5-eRsA0l8Pg) [video]

[grsecurity CVE-Dataset](https://docs.google.com/spreadsheets/u/0/d/1JO43UfT7Vjun9ytSWNdI17xmnzZMg19Tii-rKw94Rvw/htmlview#gid=0) [spreadsheet]

[Syzkaller Coverage Dashboard](https://lookerstudio.google.com/reporting/41ae4a20-9826-4f7f-be14-a934a04686fe/page/4EOpD)

[kernel vulns missing stable backports](https://docs.google.com/spreadsheets/d/1JzRy4amgEn98KvyNs1yB4H_R08TovFZH0nutWx2tvZg/view#gid=0) [[source](https://twitter.com/sirdarckcat/status/1779894891608220052)]

https://github.com/nccgroup/exploit_mitigations

https://github.com/bsauce/kernel-security-learning

https://github.com/hackedteam

https://forums.grsecurity.net/viewforum.php?f=7

https://github.com/jameshilliard/linux-grsec/

https://www.youtube.com/c/dayzerosec/videos

https://github.com/milabs/lkrg-bypass

https://github.com/V4bel/kernel-exploit-technique

https://github.com/mudongliang/reproduce_kernel_bugs

https://github.com/bata24/gef

https://github.com/PaoloMonti42/salt

https://github.com/davidmalcolm/antipatterns.ko

https://kernel.dance/

https://github.com/0xricksanchez/like-dbg

https://github.com/ameetsaahu/Kernel-exploitation

https://github.com/cmu-pasta/linux-kernel-enriched-corpus

https://github.com/niveb/NoCrypt

https://github.com/heki-linux

https://twitter.com/sirdarckcat/status/1681924752800366592

https://github.com/hardenedvault/ved-ebpf

https://github.com/thebabush/linux-russian-roulette
