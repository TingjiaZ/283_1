# 283_1

1. Download VMware fusion/workstation from the VMware website and configure the local enviornment of computer.
2. create a vitural machine and download the file "makefile" and "cmpe283-1.c".
3. Implement code in cmpe283-1.c
4. define the controls
  #define IA32_VMX_PINBASED_CTLS 0x481
  #define IA32_VMX_ENTRY_CTLS 0x484
  #define IA32_VMX_EXIT_CTLS 0x483
  #define IA32_VMX_PROCBASED_CTLS 0x482
  #define IA32_VMX_PROCBASED_CTLS2 0x48B
5. define pinbased capabilities
6. define procbased capabilities
  struct capability_info procbased[21] =
  {
    { 2, " Interrupt-window exiting" },
    { 3, "Use TSC offsetting " },
    { 7, "HLT exiting " },
    { 9, "INVLPG exiting " },
    { 10, "MWAIT exiting" },
    { 11, "RDPMC exiting" },
    { 12, "RDTSC exiting" },
    { 15, "CR3-load exiting" },
    { 16, "CR3-store exiting" },
    { 19, "CR8-load exiting" },
    { 20, "CR8-store exiting" },
    { 21, "Use TPR shadow " },
    { 22, "NMI-window exiting" },
    { 23, "MOV-DR exiting" },
    { 24, "Unconditional I/O exiting" },
    { 25, "Use I/O bitmaps " },
    { 27, "Monitor trap flag " },
    { 28, "Use MSR bitmaps" },
    { 29, "MONITOR exiting" },
    { 30, "PAUSE exiting" },
    { 31, "Activate secondary controls" }
  }; 
  7. define secondary procbased capabilities
    struct capability_info secondary_procbased[23] =
  {
    { 0, " Virtualize APIC accesses" },
    { 1, "Enable EPT " },
    { 2, "Descriptor-table exiting " },
    { 3, "Enable RDTSCP " },
    { 4, "Virtualize x2APIC mode" },
    { 5, "Enable VPID" },
    { 6, "WBINVD exiting" },
    { 7, "Unrestricted guest" },
    { 8, "APIC-register virtualization" },
    { 9, "Virtual-interrupt delivery" },
    { 10, "PAUSE-loop exiting" },
    { 11, "RDRAND exiting " },
    { 12, "Enable INVPCID" },
    { 13, "Enable VM functions" },
    { 14, "VMCS shadowing" },
    { 15, "Enable ENCLS exiting " },
    { 16, "RDSEED exiting " },
    { 17, "Enable PML" },
    { 18, "EPT-violation #VE" },
    { 19, "Conceal VMX non-root operation from Intel PT" },
    { 20, "Enable XSAVES/XRSTORS" },
    { 22, "Mode-based execution control for EPT" },
    { 25, "Use TSC scaling" }
  }; 
 8. define entry controls capabilities
 9. define exit controls capabilities
  10. make clean
