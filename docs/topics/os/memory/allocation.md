### 内存分配

#### 进程内存分配的几种形式

- 分区式管理：最简单直观的方式，在内存中分配一个区，将整个进程放入这个区。缺点是会产生外碎片，即时间长了会在分区之间产生难以被利用的小空间。

- 分页式管理：将内存分成固定大小的页，分配若干页将整个进程载入。页面可以不连续是其重要优点，不会产生外碎片，更有效地利用了内存，不过会产生一些内碎片，即分配给进程的最后一个页往往不能正好用完，不过在页面大小不是很大的时候可以接受。

- 分段式管理：将程序分为若干个段，如数据段和代码段，加以不同的保护。施加保护是分段式的优点，但其仍是向分区式管理一样的连续分配。

- 段页式管理：同样将程序分段，加以不同的保护，但是各段不再连续分配，而采用分页式离散分配。