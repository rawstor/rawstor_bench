[&lt; back](..)

# perftest-4k-1-1

2025-09-22 11:51:00

refs/heads/add/cppost

[c8d8a55](https://github.com/rawstor/librawstor/commit/c8d8a55a02ce3d9eead08e0be4e34e50bdd0c28f)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11375: Mon Sep 22 11:50:58 2025
  read: IOPS=5604, BW=21.9MiB/s (23.0MB/s)(219MiB/10001msec)
    slat (nsec): min=49, max=21670, avg=183.82, stdev=223.87
    clat (usec): min=41, max=30964, avg=75.25, stdev=202.27
     lat (usec): min=41, max=30965, avg=75.43, stdev=202.27
    clat percentiles (usec):
     |  1.00th=[   55],  5.00th=[   60], 10.00th=[   62], 20.00th=[   66],
     | 30.00th=[   69], 40.00th=[   71], 50.00th=[   73], 60.00th=[   75],
     | 70.00th=[   78], 80.00th=[   81], 90.00th=[   87], 95.00th=[   93],
     | 99.00th=[  108], 99.50th=[  114], 99.90th=[  137], 99.95th=[  180],
     | 99.99th=[ 2999]
   bw (  KiB/s): min=20688, max=25688, per=100.00%, avg=22418.40, stdev=1384.16, samples=20
   iops        : min= 5172, max= 6422, avg=5604.60, stdev=346.04, samples=20
  write: IOPS=5577, BW=21.8MiB/s (22.8MB/s)(218MiB/10001msec); 0 zone resets
    slat (nsec): min=80, max=18084, avg=255.99, stdev=218.11
    clat (usec): min=54, max=28321, avg=99.61, stdev=194.29
     lat (usec): min=54, max=28321, avg=99.87, stdev=194.29
    clat percentiles (usec):
     |  1.00th=[   77],  5.00th=[   82], 10.00th=[   85], 20.00th=[   89],
     | 30.00th=[   92], 40.00th=[   95], 50.00th=[   97], 60.00th=[   99],
     | 70.00th=[  102], 80.00th=[  105], 90.00th=[  112], 95.00th=[  118],
     | 99.00th=[  133], 99.50th=[  141], 99.90th=[  174], 99.95th=[  231],
     | 99.99th=[ 2802]
   bw (  KiB/s): min=20440, max=25368, per=100.00%, avg=22314.00, stdev=1442.82, samples=20
   iops        : min= 5110, max= 6342, avg=5578.50, stdev=360.71, samples=20
  lat (usec)   : 50=0.11%, 100=80.29%, 250=19.57%, 500=0.01%, 750=0.01%
  lat (msec)   : 2=0.01%, 4=0.01%, 20=0.01%, 50=0.01%
  cpu          : usr=6.88%, sys=33.10%, ctx=111930, majf=0, minf=294
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=56046,55785,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=21.9MiB/s (23.0MB/s), 21.9MiB/s-21.9MiB/s (23.0MB/s-23.0MB/s), io=219MiB (230MB), run=10001-10001msec
  WRITE: bw=21.8MiB/s (22.8MB/s), 21.8MiB/s-21.8MiB/s (22.8MB/s-22.8MB/s), io=218MiB (228MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/227, sectors=0/40704, merge=0/1167, ticks=0/476, in_queue=481, util=0.17%
```
