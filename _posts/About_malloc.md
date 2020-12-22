# Writeups
- https://sourceware.org/glibc/wiki/MallocInternals
- https://sploitfun.wordpress.com/2015/02/10/understanding-glibc-malloc/

# History
dlmalloc forked into ptmalloc2 and then threading support was added and then merged to glibc source code.

# Source code and other allocators:
- https://code.woboq.org/userspace/glibc/malloc/malloc.c.html
- https://sources.debian.org/src/glibc/2.28-10/malloc/malloc.c/
- https://opensource.apple.com/source/libmalloc/libmalloc-53.1.1/src/malloc.c.auto.html
- tcmalloc from Google
- https://github.com/microsoft/mimalloc
- http://mirror.fsf.org/pmon2000/2.x/src/lib/libc/malloc.c
- https://medium.com/@andrestc/implementing-malloc-and-free-ba7e7704a473
- http://mirror.fsf.org/pmon2000/2.x/src/lib/libc/malloc.c
- https://chromium.googlesource.com/chromium/src/base/+/master/allocator


# Systems calls used in Linux:
- brk
- mmap

ptmalloc2 maintains a seperate heap segment per thread, so does not require locking.

# Malloc lab from educational institutions:
- https://www.cs.cmu.edu/afs/cs/academic/class/15213-f10/www/labs/malloclab-writeup.pdf
