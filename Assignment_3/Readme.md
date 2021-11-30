Work Done by Rahul :-
•	Created leaf node %eax= 0x4FFFFFFC
•	Made required changes in cpuid.c and vmx.c
•	Tested and Verified results
•	Documented the steps and results.

Work Done by Bhargav :-
•	Created leaf node %eax= 0x4FFFFFFD
•	Made required changes in cpuid.c and vmx.c
•	Tested and Verified results
•	Documented the steps and results.

Prerequisites:-
Need a working assignment 1

Steps:-
1.sudo apt install vim build-essential libncurses-dev bison flex libssl-dev libelf-dev
2.cd linux
3.uname -a
4.cp -v /boot/config-$(uname -r) .config && make oldconfig && make -j 6 && make -j 6 modules
5.sudo bash
6.make modules_install && make install
after changes
sudo make && sudo make modules_install && sudo make install
Case I :
cpuid -l 0x4FFFFFFC
dmesg for kernel message output
Case II :
cpuid -l 0x4FFFFFFD -s 12
dmesg for kernel message output


Questions:-
Q1. Comment on the frequency of exits – does the number of exits increase at a stable rate? Or are there more exits performed during certain VM operations? Approximately how many exits does a full VM boot entail?

The number of exits keep on increasing after boot and does not increase at a stable rate.
if some activities are performed on the vm then the number of some exits shoot up.

Q2. Of the exit types defined in the SDM, which are the most frequent? Least?
The most frequent exits that we saw were
Exit number 48 (EPT violation)

When it comes to least number of exits there were some exit codes with zero 
Exit number 29 - (MOV DR)
Exit number 54-55 (WBINVD-XSETBV)

