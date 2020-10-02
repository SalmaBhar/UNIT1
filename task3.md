### Question 1: Describe four roles of the Operating systems in a computer. <br>
1. Augmenting the repetitive manual task of loading programs by hand into computers. Operating systems are even faster since they do batch processing of the programs. <br>
2. Acting as an intermediate between hardware peripherals and software programs in a computer through device drivers. <br>
3. Running several programs simultaneously on a single CPU using smart scheduling. <br>
4. Memory management using virtual memory which makes programs always assume that their memory starts from 0. 

### Question 2: What did you find surprising from the video about the Operating systems (#1) Describe below your point:
I found it surprising how hard programming was before operating systems. As “ignorant” as it may seem, I thought that operating systems only had the role of an interface and linker between hardware and software. However, it seems like operating systems are more than just fancy interfaces. The video mentions that programmers would have to load one program by hand and rush into the office to get the next program. Which must have been very inconvenient and time-consuming. In addition, they also had to read entire manuals for peripherals to work on computers and then “plug and pray”.

### Question 3: Watch the video showing the market share for the most popular Operating Systems during the last years (#2). Describe the trends shown in the graph.
The video starts in 2004 with Win2000 and WinXP in the same level, then we notice that WinXP gets very far ahead of any other software up until 2011, when it gets surpassed by Windows 7. <br>
In May of the same year, we noticed the rise of Mac OS in 3rd position at 8.5% while Win7 stays in 1st position. <br>
In 2016, although Win8 was released, we notice that it stays in 2nd position and it does not surpass its older version Win7. <br>
The video ends in 2019 with the newest version of Windows 10 (59%) in 1st position, preceded by Windows 7 (17.8%) (which still receives a lot of attention until this day) while Mac OS (10.2%) sticks in 3rd position. At the bottom of the leaderboard we observe Linux, Win8 and Chrome OS with smaller percentages of popularity.

### Question 4: Identify the original creators of the Operating Systems in video #2. Add the citations for your sources.
All versions of Windows: Bill Gates (Microsoft) [1] <br>
Linux: Linus Torvalds [2] <br>
Mac OS: Steve Jobs (Apple) [3] <br>
Chrome OS: Google developers [4] <br>

[1] Gibbs, Samuel. “From Windows 1 to Windows 10: 29 Years of Windows Evolution.” The Guardian, Guardian News and Media, 2 Oct. 2014, www.theguardian.com/technology/2014/oct/02/from-windows-1-to-windows-10-29-years-of-windows-evolution. 

[2] “Linux.” Wikipedia, Wikimedia Foundation, 27 Sept. 2020, en.wikipedia.org/wiki/Linux. 

[3] “MacOS.” Wikipedia, Wikimedia Foundation, 27 Sept. 2020, en.wikipedia.org/wiki/MacOS. 

[4] “Chrome OS.” Wikipedia, Wikimedia Foundation, 30 Sept. 2020, en.wikipedia.org/wiki/Chrome_OS. 

### Question 5: The list below states some of the least known open source operating systems. Research what they are mainly used for, what graphical interface system they use and what are the minimal specifications of the computer needed to run them. 
1. Red Hat mainly provides  open source software products to enterprises. RHEL 8, for example, comes in two main flavors, Server without GUI and Workstation with GUI pre-installed as default. For RHEL 8, the minimum specifications are 4 GB RAM, 20 GB unallocated disk space and 64-bit x86 or ARM System. <br>
2. CentOS is mainly used for web hosting. For example CentOS 7 uses the GUI GNOME.  For CentOS 8, the minimum specifications are 2 GB RAM, 2 GHz or Higher Processor, 20 GB Hard Disk and 64-bit x86 System. <br>
3. SUSE is used for servers, mainframes, and workstations. The K Desktop Environment (KDE) is the default GUI for SLES 9. It requires a minimum of 1024 MB of total RAM or a minimum of 512 MB of RAM per CPU core. <br>
4. Linux Mint is mainly used for individual purposes. Its GUI is GNOME or Cinnamon. Linux Mint 32-bit works on both 32-bit and 64-bit processors, 512 MB RAM, 5 GB of disk space and Graphics card capable of 800×600 resolution. <br>
5. Fedora is an easy to use operating system for laptop and desktop computers, with a complete set of tools for developers and makers of all kinds. It doesn't come with any graphical user interface by default so the GUI has to be installed from Linux. Fedora will install on PCs with Intel and AMD 32- and 64-bit processors, a minimum of 256 MB of memory, 7 GB of disk space, and a processor speed of 400 MHz. <br>
6. Knoppix can be used to copy files easily from hard drives with inaccessible operating systems. Its GUI is Adriane. Its system requirements are Intel/AMD-compatible CPU (i486 and up), RAM 200 MB, a bootable CD-ROM/DVD drive (IDE/ATAPI/SATA, Firewire, USB), or USB flash disk and a standard SVGA-compatible graphics chipset. <br>
7. Manjaro is used for domestic use by beginners or by professionals. Its GUI is Calamares. Its minimum requirements are 1 GB RAM,1 GHz CPU, 30 GB hard disk size and bootable media. <br>
8. Kali is a Linux distribution aimed at advanced Penetration Testing and Security Auditing. It uses GNOME as a GUI by default. Kali Version 2020.2 requires at least 3.6GB and a minimum of 257MB RAM for i386 and AMD64 architectures. <br>

### Extra: programming task: Create a program that prints n numbers of the Fibonacci Series, where n is an integer entered by the user.
```.py
#This program shows the 1st n numbers of the Fibonacci sequence
n_terms=int(input("Enter your number of terms "))
n1, n2=1, 1
count=0
while n_terms<0 or n_terms==0:
    n_terms=int(input("Please enter a positive number "))
if n_terms==1:
    print("Fibonacci sequence: {}".format(n1))
else:
    print("Fibonacci sequence: ")
    while count<n_terms:
        print(n1)
        nth=n1+n2
        n1=n2
        n2=nth
        count+=1
```
