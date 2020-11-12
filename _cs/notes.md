
## Common memory related errors in unmanaged languages like C:
- Memory leaks
- Double frees
- Dangling pointers

## Common memory related errors in managed languages like Java and C#:
- OutOfMemoryException is common as we don't know when and where memory is freed

# The new way:
- Rust

# Windows heap managers
- Windows Heap Manager and CLR Heap Manager
- Both of them go to Virtual Memory Manager (check Memoryapi.h https://docs.microsoft.com/en-us/windows/win32/api/memoryapi/)


# .net Managed heap
- Small object heap
    -- Has a Ephemeral segment
- Large object heap
    -- Doen't do compaction by default, only does a collection i.e, frees unused space but does not move around objects to prevent fragmentation.
    
Server GC vs Workstation GC:
- Server GC has one heap per core and one dedicated GC thread per heap

## SOS commands:
!eeheap -gc
!gcroot <address>
!DumpHeap
!DumpAssembly <assembly address>
!DumpClass <class address>
!DumpDomain [<domain address>] - dumps app domains
!FinalizeQueue [-detail] | [-allReady] [-short]

## SOSEX commands:
!gcgen <address>

## PSSCOR2/4:
- Superset of SOS but focuses on IIS

GC roots are determined using the followign components:
- JIT compiler
- Stack walker
- Handle table
- Finalize queue