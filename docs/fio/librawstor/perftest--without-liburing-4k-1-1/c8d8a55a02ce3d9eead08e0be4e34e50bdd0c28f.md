[&lt; back](..)

# perftest--without-liburing-4k-1-1

2025-09-22 11:51:35

refs/heads/add/cppost

[c8d8a55](https://github.com/rawstor/librawstor/commit/c8d8a55a02ce3d9eead08e0be4e34e50bdd0c28f)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11387: Mon Sep 22 11:51:33 2025
  read: IOPS=5937, BW=23.2MiB/s (24.3MB/s)(232MiB/10001msec)
    slat (nsec): min=40, max=18535, avg=161.68, stdev=170.06
    clat (usec): min=41, max=29838, avg=70.54, stdev=202.03
     lat (usec): min=41, max=29838, avg=70.71, stdev=202.03
    clat percentiles (usec):
     |  1.00th=[   52],  5.00th=[   56], 10.00th=[   58], 20.00th=[   61],
     | 30.00th=[   64], 40.00th=[   66], 50.00th=[   68], 60.00th=[   70],
     | 70.00th=[   73], 80.00th=[   76], 90.00th=[   82], 95.00th=[   89],
     | 99.00th=[  104], 99.50th=[  113], 99.90th=[  139], 99.95th=[  174],
     | 99.99th=[ 2638]
   bw (  KiB/s): min=22064, max=25504, per=100.00%, avg=23751.20, stdev=958.64, samples=20
   iops        : min= 5516, max= 6376, avg=5937.80, stdev=239.66, samples=20
  write: IOPS=5921, BW=23.1MiB/s (24.3MB/s)(231MiB/10001msec); 0 zone resets
    slat (nsec): min=90, max=17312, avg=236.85, stdev=235.53
    clat (usec): min=54, max=31190, avg=94.46, stdev=224.74
     lat (usec): min=54, max=31190, avg=94.70, stdev=224.74
    clat percentiles (usec):
     |  1.00th=[   74],  5.00th=[   78], 10.00th=[   81], 20.00th=[   84],
     | 30.00th=[   87], 40.00th=[   89], 50.00th=[   92], 60.00th=[   94],
     | 70.00th=[   96], 80.00th=[  100], 90.00th=[  106], 95.00th=[  113],
     | 99.00th=[  129], 99.50th=[  139], 99.90th=[  172], 99.95th=[  200],
     | 99.99th=[ 4080]
   bw (  KiB/s): min=21840, max=25944, per=100.00%, avg=23686.80, stdev=1013.49, samples=20
   iops        : min= 5460, max= 6486, avg=5921.70, stdev=253.37, samples=20
  lat (usec)   : 50=0.17%, 100=89.48%, 250=10.32%, 500=0.02%, 750=0.01%
  lat (msec)   : 4=0.01%, 10=0.01%, 20=0.01%, 50=0.01%
  cpu          : usr=8.32%, sys=31.45%, ctx=118680, majf=0, minf=295
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=59378,59217,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=23.2MiB/s (24.3MB/s), 23.2MiB/s-23.2MiB/s (24.3MB/s-24.3MB/s), io=232MiB (243MB), run=10001-10001msec
  WRITE: bw=23.1MiB/s (24.3MB/s), 23.1MiB/s-23.1MiB/s (24.3MB/s-24.3MB/s), io=231MiB (243MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/127, sectors=0/37984, merge=0/993, ticks=0/242, in_queue=249, util=0.19%
```
