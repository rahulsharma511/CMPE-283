Question_3: What did you learn from the count of exits? Was the count what you expected? If not, why not?

=> The count of exits increased when nested paging was disabled(i.e. ept=0). 
So when using shadow paging the number of exits increases because exits could occur if VM attempts to execute CR0, CR3, CR4 or any exits which are related to paging such as a page fault.

Q4) What changed between the two runs (ept vs no-ept)?
When ept is disabled, the exit counts are higher than when it is enabled, which is what we would expect. 
Exit codes 0 and 3 have much more exits when ept is disabled. This makes sense because each code corresponds to the move to CR0 and move to CR3 instructions, respectively. 