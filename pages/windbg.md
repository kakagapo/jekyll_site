---
layout: page
title: WinDbg
permalink: /windbg
---


```
0:155> k
 # Child-SP          RetAddr           Call Site
00 0000010a`d8cfabc0 00007ffe`49cf67ae KERNELBASE!RaiseFailFastException+0xae [d:\rs1\minkernel\kernelbase\xcpt.c @ 1106] 
01 0000010a`d8cfb190 00007ffe`49cf6215 FabricRuntime!Common::Assert::DoFailFast+0x1ca [x:\bt\1024265\repo\src\prod\src\common\assertwf.cpp @ 188] 
02 0000010a`d8cfb400 00007ffe`49d0bd5f FabricRuntime!Common::Assert::CodingError+0x59 [x:\bt\1024265\repo\src\prod\src\common\assertwf.cpp @ 199] 
03 0000010a`d8cfb480 00007ffe`66a3c0b0 FabricRuntime!Common::ComUnknownBase::~ComUnknownBase+0x47 [x:\bt\1024265\repo\src\prod\src\common\comunknownbase.cpp @ 17] 
04 0000010a`d8cfb4e0 00007ffe`66a31d6e VCRUNTIME140!_CallSettingFrame+0x20 [f:\dd\vctools\crt\vcruntime\src\eh\amd64\handlers.asm @ 50] 
05 0000010a`d8cfb510 00007ffe`66a3b7fb VCRUNTIME140!__FrameHandler3::FrameUnwindToState+0x196 [f:\dd\vctools\crt\vcruntime\src\eh\frame.cpp @ 1210] 
06 0000010a`d8cfb580 00007ffe`66a323e3 VCRUNTIME140!__FrameHandler3::FrameUnwindToEmptyState+0x57 [f:\dd\vctools\crt\vcruntime\src\eh\risctrnsctrl.cpp @ 246] 
07 0000010a`d8cfb5b0 00007ffe`66a3b882 VCRUNTIME140!__InternalCxxFrameHandler<__FrameHandler3>+0x11f [f:\dd\vctools\crt\vcruntime\src\eh\frame.cpp @ 318] 
08 0000010a`d8cfb610 00007ffe`72a9a60d VCRUNTIME140!__CxxFrameHandler3+0x72 [f:\dd\vctools\crt\vcruntime\src\eh\risctrnsctrl.cpp @ 272] 
09 0000010a`d8cfb660 00007ffe`72a306ba ntdll!RtlpExecuteHandlerForUnwind+0xd [d:\rs1\minkernel\ntos\rtl\amd64\xcptmisc.asm @ 252] 
0a 0000010a`d8cfb690 00007ffe`64672a90 ntdll!RtlUnwindEx+0x38a [d:\rs1\minkernel\ntos\rtl\amd64\exdsptch.c @ 1044] 
0b 0000010a`d8cfbd70 00007ffe`64672a4b clr!ClrUnwindEx+0x40 [f:\dd\ndp\clr\src\vm\exceptionhandling.cpp @ 4288] 
0c 0000010a`d8cfc290 00007ffe`72a9a58d clr!ProcessCLRException+0x2e9 [f:\dd\ndp\clr\src\vm\exceptionhandling.cpp @ 1028] 
0d 0000010a`d8cfc370 00007ffe`72a2fd23 ntdll!RtlpExecuteHandlerForException+0xd [d:\rs1\minkernel\ntos\rtl\amd64\xcptmisc.asm @ 131] 
0e 0000010a`d8cfc3a0 00007ffe`72a31a39 ntdll!RtlDispatchException+0x373 [d:\rs1\minkernel\ntos\rtl\amd64\exdsptch.c @ 546] 
0f 0000010a`d8cfcaa0 00007ffe`6f9b4c48 ntdll!RtlRaiseException+0x2d9 [d:\rs1\minkernel\ntos\rtl\amd64\raise.c @ 160] 
10 0000010a`d8cfd280 00007ffe`66a342cd KERNELBASE!RaiseException+0x68 [d:\rs1\minkernel\kernelbase\xcpt.c @ 904] 
11 0000010a`d8cfd360 00007ffe`4a3862e7 VCRUNTIME140!_CxxThrowException+0xad [f:\dd\vctools\crt\vcruntime\src\eh\throw.cpp @ 133] 
12 0000010a`d8cfd3d0 00007ffe`4a3850cf FabricRuntime!__scrt_throw_std_bad_alloc+0x1f [f:\dd\vctools\crt\vcstartup\src\heap\throw_bad_alloc.cpp @ 33] 
13 0000010a`d8cfd420 00007ffe`49b61833 FabricRuntime!operator new+0x3b [f:\dd\vctools\crt\vcstartup\src\heap\new_scalar.cpp @ 47] 
14 0000010a`d8cfd450 00007ffe`49e88f1b FabricRuntime!std::_Allocate<std::_Default_allocate_traits<1> >+0x3f [o:\.btcxcache\.a\visualcpp.corext.elyyhdt-q2d4auds-s6rva\include\xmemory0 @ 123] 
15 (Inline Function) --------`-------- FabricRuntime!std::allocator<unsigned char>::allocate+0x10 [o:\.btcxcache\.a\visualcpp.corext.elyyhdt-q2d4auds-s6rva\include\xmemory0 @ 1055] 
16 0000010a`d8cfd480 00007ffe`49e89c8b FabricRuntime!std::vector<unsigned char,std::allocator<unsigned char> >::_Resize<<lambda_2b51424039c320f102fd798e073c89b2> >+0x7f [o:\.btcxcache\.a\visualcpp.corext.elyyhdt-q2d4auds-s6rva\include\vector @ 1490] 
17 (Inline Function) --------`-------- FabricRuntime!std::vector<unsigned char,std::allocator<unsigned char> >::resize+0xb [o:\.btcxcache\.a\visualcpp.corext.elyyhdt-q2d4auds-s6rva\include\vector @ 1531] 
18 0000010a`d8cfd4e0 00007ffe`49e89552 FabricRuntime!Reliability::ReplicationComponent::ComManagedOperationData::ComManagedOperationData+0x8b [x:\bt\1024265\repo\src\prod\src\reliability\replication\comreplicator.cpp @ 38] 
19 0000010a`d8cfd540 00007ffe`49e8b072 FabricRuntime!Common::make_com<Reliability::ReplicationComponent::ComManagedOperationData,unsigned long * __ptr64 & __ptr64,unsigned long & __ptr64>+0x56 [x:\bt\1024265\repo\src\prod\src\common\comunknownbase.h @ 66] 
1a 0000010a`d8cfd580 00007ffe`05f3354a FabricRuntime!Reliability::ReplicationComponent::ComReplicator::CreateOperationData+0x42 [x:\bt\1024265\repo\src\prod\src\reliability\replication\comreplicator.cpp @ 1086] 
1b 0000010a`d8cfd5d0 00007ffe`05f3316f Microsoft_Cloud_InstrumentationFramework_Events!DomainBoundILStubClass.IL_STUB_CLRtoCOM(IntPtr, UInt32)+0xda
1c 0000010a`d8cfd6d0 00007ffe`05f32e6f System_Fabric!System.Fabric.Interop.OperationDataFactoryWrapper.CreateNativeOperationData(System.Fabric.IOperationData, UInt32[])+0x8f
1d 0000010a`d8cfd780 00007ffe`05f32baf System_Fabric!System.Fabric.Interop.OperationDataFactoryWrapper.CreateOperationData(System.Fabric.OperationData)+0x14f
1e 0000010a`d8cfd800 00007ffe`64642ef9 Microsoft_Cloud_InstrumentationFramework_Events!DomainBoundILStubClass.IL_STUB_COMtoCLR(IntPtr, IntPtr)+0x4f
1f 0000010a`d8cfd860 00007ffe`647d1a64 clr!COMToCLRDispatchHelper+0x39 [f:\dd\ndp\clr\src\vm\amd64\GenericComCallStubs.asm @ 286] 
20 (Inline Function) --------`-------- clr!InvokeStub+0x1b [f:\dd\ndp\clr\src\vm\comtoclrcall.cpp @ 269] 
21 (Inline Function) --------`-------- clr!COMToCLRInvokeTarget+0x38 [f:\dd\ndp\clr\src\vm\comtoclrcall.cpp @ 451] 
22 (Inline Function) --------`-------- clr!COMToCLRWorkerBody+0xeb [f:\dd\ndp\clr\src\vm\comtoclrcall.cpp @ 629] 
23 0000010a`d8cfd890 00007ffe`64642e57 clr!COMToCLRWorker+0x1b4 [f:\dd\ndp\clr\src\vm\comtoclrcall.cpp @ 880] 
24 0000010a`d8cfd950 00007ffe`49ee5b92 clr!GenericComCallStub+0x57 [f:\dd\ndp\clr\src\vm\amd64\GenericComCallStubs.asm @ 134] 
25 0000010a`d8cfd9e0 00007ffe`49d0f716 FabricRuntime!Reliability::ReplicationComponent::ComProxyAsyncEnumOperationData::GetNextAsyncOperation::EndComAsyncOperation+0x52 [x:\bt\1024265\repo\src\prod\src\reliability\replication\comproxyasyncenumoperation.cpp @ 114] 
26 0000010a`d8cfda30 00007ffe`49d0f985 FabricRuntime!Common::ComProxyAsyncOperation::FinishComAsyncOperation+0x36 [x:\bt\1024265\repo\src\prod\src\common\comproxyasyncoperation.cpp @ 132] 
27 0000010a`d8cfda60 00007ffe`05a477cc FabricRuntime!Common::ComProxyAsyncOperation::OnComAsyncOperationCompleted+0x61 [x:\bt\1024265\repo\src\prod\src\common\comproxyasyncoperation.cpp @ 124] 
28 0000010a`d8cfda90 00007ffe`05a47684 Microsoft_Cloud_InstrumentationFramework_Events!DomainBoundILStubClass.IL_STUB_CLRtoCOM(IFabricAsyncOperationContext)+0xdc
29 0000010a`d8cfdb80 00007ffe`6195f2c6 System_Fabric!System.Fabric.Interop.AsyncTaskCallInAdapter.ProcessNativeCallback()+0x34
2a 0000010a`d8cfdbb0 00007ffe`61915ab3 mscorlib_ni!System.Threading.Tasks.Task.Execute()+0x46 [f:\dd\ndp\clr\src\BCL\system\threading\Tasks\Task.cs @ 2498] 
2b 0000010a`d8cfdbf0 00007ffe`61915944 mscorlib_ni!System.Threading.ExecutionContext.RunInternal(System.Threading.ExecutionContext, System.Threading.ContextCallback, System.Object, Boolean)+0x163 [f:\dd\ndp\clr\src\BCL\system\threading\executioncontext.cs @ 954] 
2c 0000010a`d8cfdcc0 00007ffe`6195f565 mscorlib_ni!System.Threading.ExecutionContext.Run(System.Threading.ExecutionContext, System.Threading.ContextCallback, System.Object, Boolean)+0x14 [f:\dd\ndp\clr\src\BCL\system\threading\executioncontext.cs @ 902] 
2d 0000010a`d8cfdcf0 00007ffe`6195ec93 mscorlib_ni!System.Threading.Tasks.Task.ExecuteWithThreadLocal(System.Threading.Tasks.Task ByRef)+0x215 [f:\dd\ndp\clr\src\BCL\system\threading\Tasks\Task.cs @ 2827] 
2e 0000010a`d8cfdda0 00007ffe`61963011 mscorlib_ni!System.Threading.Tasks.Task.ExecuteEntry(Boolean)+0x73 [f:\dd\ndp\clr\src\BCL\system\threading\Tasks\Task.cs @ 2767] 
2f 0000010a`d8cfdde0 00007ffe`61962eee mscorlib_ni!System.Threading.Tasks.ThreadPoolTaskScheduler.TryExecuteTaskInline(System.Threading.Tasks.Task, Boolean)+0x31 [f:\dd\ndp\clr\src\BCL\system\threading\Tasks\ThreadPoolTaskScheduler.cs @ 92] 
30 0000010a`d8cfde30 00007ffe`61962ba4 mscorlib_ni!System.Threading.Tasks.TaskScheduler.TryRunInline(System.Threading.Tasks.Task, Boolean)+0x19e [f:\dd\ndp\clr\src\BCL\system\threading\Tasks\TaskScheduler.cs @ 219] 
31 0000010a`d8cfded0 00007ffe`618e3ae8 mscorlib_ni!System.Threading.Tasks.TaskContinuation.InlineIfPossibleOrElseQueue(System.Threading.Tasks.Task, Boolean)+0x74 [f:\dd\ndp\clr\src\BCL\system\threading\Tasks\TaskContinuation.cs @ 263] 
32 0000010a`d8cfdf60 00007ffe`6195e873 mscorlib_ni!System.Threading.Tasks.Task.FinishContinuations()+0xf8 [f:\dd\ndp\clr\src\BCL\system\threading\Tasks\Task.cs @ 3642] 
33 0000010a`d8cfdff0 00007ffe`6195f588 mscorlib_ni!System.Threading.Tasks.Task.Finish(Boolean)+0x33 [f:\dd\ndp\clr\src\BCL\system\threading\Tasks\Task.cs @ 2253] 
34 0000010a`d8cfe050 00007ffe`6195ec93 mscorlib_ni!System.Threading.Tasks.Task.ExecuteWithThreadLocal(System.Threading.Tasks.Task ByRef)+0x238 [f:\dd\ndp\clr\src\BCL\system\threading\Tasks\Task.cs @ 2830] 
35 0000010a`d8cfe100 00007ffe`61915ab3 mscorlib_ni!System.Threading.Tasks.Task.ExecuteEntry(Boolean)+0x73 [f:\dd\ndp\clr\src\BCL\system\threading\Tasks\Task.cs @ 2767] 
36 0000010a`d8cfe140 00007ffe`61915944 mscorlib_ni!System.Threading.ExecutionContext.RunInternal(System.Threading.ExecutionContext, System.Threading.ContextCallback, System.Object, Boolean)+0x163 [f:\dd\ndp\clr\src\BCL\system\threading\executioncontext.cs @ 954] 
37 0000010a`d8cfe210 00007ffe`61915912 mscorlib_ni!System.Threading.ExecutionContext.Run(System.Threading.ExecutionContext, System.Threading.ContextCallback, System.Object, Boolean)+0x14 [f:\dd\ndp\clr\src\BCL\system\threading\executioncontext.cs @ 902] 
38 0000010a`d8cfe240 00007ffe`622c4b6c mscorlib_ni!System.Threading.ExecutionContext.Run(System.Threading.ExecutionContext, System.Threading.ContextCallback, System.Object)+0x52 [f:\dd\ndp\clr\src\BCL\system\threading\executioncontext.cs @ 891] 
39 0000010a`d8cfe290 00007ffe`64646ad3 mscorlib_ni!System.Threading.ThreadHelper.ThreadStart(System.Object)+0x5c [f:\dd\ndp\clr\src\BCL\system\threading\thread.cs @ 93] 
3a 0000010a`d8cfe2d0 00007ffe`64646988 clr!CallDescrWorkerInternal+0x83 [f:\dd\ndp\clr\src\vm\amd64\CallDescrWorkerAMD64.asm @ 97] 
3b 0000010a`d8cfe310 00007ffe`6464724d clr!CallDescrWorkerWithHandler+0x4e [f:\dd\ndp\clr\src\vm\callhelpers.cpp @ 89] 
3c 0000010a`d8cfe350 00007ffe`647b8a79 clr!MethodDescCallSite::CallTargetWorker+0xf8 [f:\dd\ndp\clr\src\vm\callhelpers.cpp @ 655] 
3d (Inline Function) --------`-------- clr!MethodDescCallSite::Call+0xc [f:\dd\ndp\clr\src\vm\callhelpers.h @ 423] 
3e 0000010a`d8cfe450 00007ffe`64647a11 clr!ThreadNative::KickOffThread_Worker+0x109 [f:\dd\ndp\clr\src\vm\comsynchronizable.cpp @ 301] 
3f 0000010a`d8cfe6b0 00007ffe`64647980 clr!ManagedThreadBase_DispatchInner+0x39 [f:\dd\ndp\clr\src\vm\threads.cpp @ 10273] 
40 0000010a`d8cfe6f0 00007ffe`646478bd clr!ManagedThreadBase_DispatchMiddle+0x6c [f:\dd\ndp\clr\src\vm\threads.cpp @ 10322] 
41 0000010a`d8cfe7f0 00007ffe`64647a4f clr!ManagedThreadBase_DispatchOuter+0x75 [f:\dd\ndp\clr\src\vm\threads.cpp @ 10577] 
42 0000010a`d8cfe880 00007ffe`647b895b clr!ManagedThreadBase_FullTransitionWithAD+0x2f [f:\dd\ndp\clr\src\vm\threads.cpp @ 10641] 
43 (Inline Function) --------`-------- clr!ManagedThreadBase::KickOff+0x20 [f:\dd\ndp\clr\src\vm\threads.cpp @ 10675] 
44 0000010a`d8cfe8e0 00007ffe`647f128f clr!ThreadNative::KickOffThread+0xdb [f:\dd\ndp\clr\src\vm\comsynchronizable.cpp @ 421] 
45 0000010a`d8cfe9b0 00007ffe`729484d4 clr!Thread::intermediateThreadProc+0x86 [f:\dd\ndp\clr\src\vm\threads.cpp @ 2872] 
46 0000010a`d8cff870 00007ffe`72a5e851 kernel32!BaseThreadInitThunk+0x14 [d:\rs1\base\win32\client\thread.c @ 64] 
47 0000010a`d8cff8a0 00000000`00000000 ntdll!RtlUserThreadStart+0x21 [d:\rs1\minkernel\ntdll\rtlstrt.c @ 997] 
```

```
0:155> !sos.threadpool
CPU utilization: 100%
Worker Thread: Total: 51 Running: 9 Idle: 42 MaxLimit: 32767 MinLimit: 50
Work Request in Queue: 0
--------------------------------------
Number of Timers: 1
--------------------------------------
Completion Port Thread:Total: 50 Free: 48 MaxFree: 8 CurrentLimit: 50 MaxLimit: 1000 MinLimit: 50
```

```
0:155> !address -summary
                                     
Mapping file section regions...
Mapping module regions...
Mapping PEB regions...
Mapping TEB and stack regions...
Mapping heap regions...
Mapping page heap regions...
Mapping other regions...
Mapping stack trace database regions...
Mapping activation context regions...

--- Usage Summary ---------------- RgnCount ----------- Total Size -------- %ofBusy %ofTotal
Free                                    387     7ff6`62f09000 ( 127.962 TB)           99.97%
<unknown>                               650        9`4921c000 (  37.143 GB)  96.59%    0.03%
Stack                                   495        0`26f80000 ( 623.500 MB)   1.58%    0.00%
Heap                                   1665        0`1aa37000 ( 426.215 MB)   1.08%    0.00%
Image                                  1860        0`121fd000 ( 289.988 MB)   0.74%    0.00%
Other                                    14        0`001cc000 (   1.797 MB)   0.00%    0.00%
TEB                                     165        0`0014a000 (   1.289 MB)   0.00%    0.00%
PEB                                       1        0`00001000 (   4.000 kB)   0.00%    0.00%

--- Type Summary (for busy) ------ RgnCount ----------- Total Size -------- %ofBusy %ofTotal
MEM_PRIVATE                            2946        9`8a34d000 (  38.159 GB)  99.23%    0.03%
MEM_IMAGE                              1860        0`121fd000 ( 289.988 MB)   0.74%    0.00%
MEM_MAPPED                               44        0`00b9d000 (  11.613 MB)   0.03%    0.00%

--- State Summary ---------------- RgnCount ----------- Total Size -------- %ofBusy %ofTotal
MEM_FREE                                387     7ff6`62f09000 ( 127.962 TB)           99.97%
MEM_COMMIT                             3953        5`7338f000 (  21.800 GB)  56.69%    0.02%
MEM_RESERVE                             897        4`29d58000 (  16.654 GB)  43.31%    0.01%

--- Protect Summary (for commit) - RgnCount ----------- Total Size -------- %ofBusy %ofTotal
PAGE_READWRITE                         1947        5`6041f000 (  21.504 GB)  55.92%    0.02%
PAGE_EXECUTE_READ                       139        0`0b17d000 ( 177.488 MB)   0.45%    0.00%
PAGE_READONLY                           659        0`05886000 (  88.523 MB)   0.22%    0.00%
PAGE_WRITECOPY                          324        0`01848000 (  24.281 MB)   0.06%    0.00%
PAGE_EXECUTE_READWRITE                   91        0`00608000 (   6.031 MB)   0.02%    0.00%
PAGE_READWRITE|PAGE_GUARD               165        0`00303000 (   3.012 MB)   0.01%    0.00%
PAGE_NOACCESS                           572        0`0023c000 (   2.234 MB)   0.01%    0.00%
PAGE_EXECUTE_WRITECOPY                   56        0`001de000 (   1.867 MB)   0.00%    0.00%

--- Largest Region by Usage ----------- Base Address -------- Region Size ----------
Free                                    1b4`45d20000     7e41`b9ec0000 ( 126.257 TB)
<unknown>                               1aa`9dcc0000        4`0c557000 (  16.193 GB)
Stack                                    5b`28280000        0`003f9000 (   3.973 MB)
Heap                                    1aa`801c2000        0`00801000 (   8.004 MB)
Image                                  7ffe`5b8d6000        0`011b6000 (  17.711 MB)
Other                                   1aa`9d820000        0`00181000 (   1.504 MB)
TEB                                      5b`26804000        0`00002000 (   8.000 kB)
PEB                                      5b`269bd000        0`00001000 (   4.000 kB)
```

```
0:155>  !dumpheap -stat
Statistics:
              MT    Count    TotalSize Class Name
00007ffe62681ec0        1           24 System.Collections.Generic.GenericEqualityComparer`1[[System.Int64, mscorlib]]
00007ffe62678ac8        1           24 System.Threading.Tasks.Task`1+<>c[[System.Boolean, mscorlib]]
00007ffe62675da0        1           24 System.Collections.Generic.GenericEqualityComparer`1[[System.UInt16, mscorlib]]
00007ffe62669ca0        1           24 System.Collections.Generic.GenericEqualityComparer`1[[System.UInt64, mscorlib]]
00007ffe62669720        1           24 System.Collections.Generic.GenericComparer`1[[System.UInt32, mscorlib]]
00007ffe62646640        1           24 System.Collections.Generic.GenericEqualityComparer`1[[System.Boolean, mscorlib]]
00007ffe62644aa8        1           24 System.Collections.Generic.GenericComparer`1[[System.TimeSpan, mscorlib]]
00007ffe62644800        1           24 System.Collections.Generic.GenericEqualityComparer`1[[System.TimeSpan, mscorlib]]
00007ffe6263e5b8        1           24 System.Threading.Tasks.Task`1+<>c[[System.Threading.Tasks.Task, mscorlib]]
00007ffe6263e330        1           24 System.Threading.Tasks.Task`1+<>c[[System.Byte[], mscorlib]]
...
00007ffe61b39808 13812245   1735804192 System.String
000001aa9d43a640 13622497   3554483010      Free
00007ffe61b3eab0 16986172   6824299787 System.Byte[]
Total 206538726 objects
Fragmented blocks larger than 0.5 MB:
            Addr     Size      Followed by
000001b2d922eb98    9.3MB 000001b2d9b72a88 System.Threading.OverlappedData
...
000001aff6ed8fe0  133.1MB 000001afff3fa7c8 System.Byte[]
```

```
0:155> !EEHeap
Loader Heap:
--------------------------------------
System Domain:     00007ffe64f91420
LowFrequencyHeap:  00007ffe04f30000(3000:3000) 00007ffe05360000(10000:10000) 00007ffe05980000(10000:10000) 00007ffe06010000(10000:10000) 00007ffe06840000(10000:1000) Size: 0x34000 (212992) bytes.
HighFrequencyHeap: 00007ffe04f34000(9000:9000) 00007ffe05400000(10000:10000) 00007ffe055d0000(10000:10000) 00007ffe058c0000(10000:10000) 00007ffe05be0000(10000:10000) 00007ffe05d80000(10000:10000) 00007ffe061e0000(10000:10000) 00007ffe06820000(10000:1000) Size: 0x6a000 (434176) bytes.
StubHeap:          00007ffe04f3d000(3000:3000) 00007ffe05430000(10000:6000) Size: 0x9000 (36864) bytes.
Virtual Call Stub Heap:
  IndcellHeap:     00007ffe04fe0000(6000:1000) Size: 0x1000 (4096) bytes.
  LookupHeap:      00007ffe04fec000(4000:1000) Size: 0x1000 (4096) bytes.
  ResolveHeap:     00007ffe05016000(3a000:6000) Size: 0x6000 (24576) bytes.
  DispatchHeap:    00007ffe04ff0000(26000:2000) Size: 0x2000 (8192) bytes.
  CacheEntryHeap:  00007ffe04fe6000(6000:2000) Size: 0x2000 (8192) bytes.
Total size:        Size: 0xb3000 (733184) bytes.
--------------------------------------
Shared Domain:     00007ffe64f90e50
LowFrequencyHeap:  00007ffe04f30000(3000:3000) 00007ffe05360000(10000:10000) 00007ffe05980000(10000:10000) 00007ffe06010000(10000:10000) 00007ffe06840000(10000:1000) Size: 0x34000 (212992) bytes.
HighFrequencyHeap: 00007ffe04f34000(9000:9000) 00007ffe05400000(10000:10000) 00007ffe055d0000(10000:10000) 00007ffe058c0000(10000:10000) 00007ffe05be0000(10000:10000) 00007ffe05d80000(10000:10000) 00007ffe061e0000(10000:10000) 00007ffe06820000(10000:1000) Size: 0x6a000 (434176) bytes.
StubHeap:          00007ffe04f3d000(3000:3000) 00007ffe05430000(10000:6000) Size: 0x9000 (36864) bytes.
Virtual Call Stub Heap:
  IndcellHeap:     00007ffe04fe0000(6000:1000) Size: 0x1000 (4096) bytes.
  LookupHeap:      00007ffe04fec000(4000:1000) Size: 0x1000 (4096) bytes.
  ResolveHeap:     00007ffe05016000(3a000:6000) Size: 0x6000 (24576) bytes.
  DispatchHeap:    00007ffe04ff0000(26000:2000) Size: 0x2000 (8192) bytes.
  CacheEntryHeap:  00007ffe04fe6000(6000:2000) Size: 0x2000 (8192) bytes.
Total size:        Size: 0xb3000 (733184) bytes.
--------------------------------------
Domain 1:          000001aa9d4454f0
LowFrequencyHeap:  00007ffe04f40000(3000:1000) 00007ffe05050000(30000:29000) 00007ffe05080000(10000:10000) 00007ffe05090000(10000:a000) 00007ffe05120000(10000:10000) 00007ffe05130000(10000:10000) 00007ffe05140000(10000:d000) 00007ffe05160000(10000:10000) 00007ffe05170000(10000:10000) 00007ffe05180000(40000:40000) 00007ffe051c0000(10000:10000) ... 00007ffe06410000(10000:10000) 00007ffe06430000(10000:f000) 00007ffe06440000(10000:10000) 00007ffe06450000(10000:10000) 00007ffe06470000(10000:10000) 00007ffe06480000(10000:10000) 00007ffe06490000(10000:10000) 00007ffe064c0000(10000:10000) 00007ffe064e0000(10000:10000) 00007ffe06500000(10000:10000) 00007ffe06520000(10000:10000) 00007ffe06540000(10000:e000) 00007ffe06770000(10000:10000) 00007ffe06780000(10000:10000) 00007ffe067b0000(10000:10000) 00007ffe067d0000(10000:10000) 00007ffe067f0000(10000:10000) 00007ffe06810000(10000:10000) 00007ffe06850000(10000:4000) Size: 0x81f000 (8515584) bytes total, 0x88000 (557056) bytes wasted.
HighFrequencyHeap: 00007ffe04f43000(a000:a000) 00007ffe05150000(10000:10000) 00007ffe05210000(10000:10000) 00007ffe05240000(10000:10000) 00007ffe05260000(10000:10000) 00007ffe05280000(10000:10000) 00007ffe052a0000(10000:10000) 00007ffe052d0000(10000:10000) 00007ffe052f0000(10000:10000) 00007ffe05320000(10000:10000) ... 00007ffe06830000(10000:10000) 00007ffe06860000(10000:3000) Size: 0x6ab000 (6991872) bytes total, 0x2000 (8192) bytes wasted.
StubHeap:          00007ffe04f4d000(3000:3000) 00007ffe054e0000(10000:10000) 00007ffe06070000(10000:e000) Size: 0x21000 (135168) bytes.
Virtual Call Stub Heap:
  IndcellHeap:     00007ffe04f50000(4000:4000) 00007ffe05cf0000(10000:7000) Size: 0xb000 (45056) bytes.
  LookupHeap:      00007ffe04f5b000(2000:2000) 00007ffe05620000(10000:d000) Size: 0xf000 (61440) bytes.
  ResolveHeap:     00007ffe04f8c000(54000:38000) Size: 0x38000 (229376) bytes.
  DispatchHeap:    00007ffe04f5d000(2f000:19000) Size: 0x19000 (102400) bytes.
  CacheEntryHeap:  00007ffe04f54000(7000:7000) 00007ffe05d20000(10000:f000) Size: 0x16000 (90112) bytes.
Total size:        Size: 0xf6c000 (16171008) bytes total, 0x8a000 (565248) bytes wasted.
--------------------------------------
Jit code heap:
HostCodeHeap:      00007ffe067a0000 Size: 0xa000 (40960) bytes.
LoaderCodeHeap:    0000000000000000(0:0) Size: 0x0 (0) bytes.
...
HostCodeHeap:      00007ffe05610000 Size: 0x10000 (65536) bytes.
LoaderCodeHeap:    0000000000000000(0:0) Size: 0x0 (0) bytes.
LoaderCodeHeap:    0000000000000000(0:0) Size: 0x0 (0) bytes.
Total size:        Size: 0x5a000 (368640) bytes.
--------------------------------------
Module Thunk heaps:
Module 00007ffe61411000: Size: 0x0 (0) bytes.
...
Module 00007ffe58241000: Size: 0x0 (0) bytes.
Total size:              Size: 0x0 (0) bytes.
--------------------------------------
Module Lookup Table heaps:
Module 00007ffe61411000: Size: 0x0 (0) bytes.
...
Module 00007ffe583f1000: Size: 0x0 (0) bytes.
Module 00007ffe50311000: Size: 0x0 (0) bytes.
Module 00007ffe49731000: Size: 0x0 (0) bytes.
Module 00007ffe58241000: Size: 0x0 (0) bytes.
Total size:              Size: 0x0 (0) bytes.
--------------------------------------
Total LoaderHeap size:   Size: 0x112c000 (18006016) bytes total, 0x8a000 (565248) bytes wasted.
=======================================
Number of GC Heaps: 4
------------------------------
Heap 0 (000001aa9d4888f0)
generation 0 starts at 0x000001b2d4a52430
generation 1 starts at 0x000001b2d48075a0
generation 2 starts at 0x000001aa9dcc1000
ephemeral segment allocation context: (0x000001b31203e2d8, 0x000001b31203e2f0)
         segment             begin         allocated              size
000001aa9dcc0000  000001aa9dcc1000  000001ab9dcbff48  0xffffef48(4294963016)
000001b2cfdf0000  000001b2cfdf1000  000001b31203e2d8  0x4224d2d8(1109709528)
Large object heap starts at 0x000001ae9dcc1000
         segment             begin         allocated              size
000001ae9dcc0000  000001ae9dcc1000  000001aeaa1f6b18  0xc535b18(206789400)
000001af0d0e0000  000001af0d0e1000  000001af14012eb0  0x6f31eb0(116596400)
000001afaa320000  000001afaa321000  000001afb1741618  0x7420618(121767448)
Heap Size:               Size: 0x15cad4200 (5849825792) bytes.
------------------------------
Heap 1 (000001aa9d4b14a0)
generation 0 starts at 0x000001b0d73e0470
generation 1 starts at 0x000001b0d72ea9c0
generation 2 starts at 0x000001ab9dcc1000
ephemeral segment allocation context: (0x000001b0e7e95a70, 0x000001b0e7e95a88)
         segment             begin         allocated              size
000001ab9dcc0000  000001ab9dcc1000  000001ac9dcbfb60  0xffffeb60(4294962016)
000001b0cfdf0000  000001b0cfdf1000  000001b0e7e95a70  0x180a4a70(403327600)
Large object heap starts at 0x000001aeadcc1000
         segment             begin         allocated              size
000001aeadcc0000  000001aeadcc1000  000001aeb42c5ee8  0x6604ee8(106974952)
000001aa8b160000  000001aa8b161000  000001aa9a1a5f88  0xf044f88(251940744)
000001af3e0b0000  000001af3e0b1000  000001af4a401e30  0xc350e30(204803632)
000001af6e0b0000  000001af6e0b1000  000001af708b1118  0x2800118(41943320)
Heap Size:               Size: 0x13c23e388 (5303952264) bytes.
------------------------------
...
------------------------------
GC Heap Size:            Size: 0x511508f60 (21765328736) bytes.
```