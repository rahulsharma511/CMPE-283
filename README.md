# CMPE-283 Assignment 2
## Things to achieve in the assignment
  For CPUID with input in eax as 0x4FFFFFFF:
    print the total number of exits by writing it back in the eax register
  For CPUID with input in eax as 0x4FFFFFFE:
    Print the total time spent processing all exits by returning the high 32 bits in ebx register and low 32 bits in the ecx register
    
Rahul Sharma(SJSU Id-015963649)
  Built the linux kernal in assignment 1
  compiled and built the kvm module after editing the cpuid.c and vmx.c file 
    using the make module command followed by the make INSTALL_MOD_STRIP=1 modules_install && make install for packaging
  loaded the module into the linux kernal by modprobe
  created nested ubuntu vm and executed the test files for getting the output
  Debugged error while running the test file due to syntax errors in the script
  
Bhargav Shah(SJSU ID-)
  researched on what all edits must be done in vmx file for getting the cpu cycles
  used the atomic variables for getting the errors solved 
  created the test scripts for grabbing the output and printing the data
  
##Steps to complete the assignment 
  Edit the cpuid.c and the vmx.c file for adding the required functnality for undifined leaf nodes after 4x0000000
  compile and load the modules 
  After the kernal code has been modified with the functnality added in kvm install nested vm
  then run cpuid command in the nested vm for getting the output
  
