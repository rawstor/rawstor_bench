[&lt; back](..)

# perftest--without-liburing--disable-ost-4k-2-1

2025-09-22 11:50:49

refs/heads/add/cppost

[c8d8a55](https://github.com/rawstor/librawstor/commit/c8d8a55a02ce3d9eead08e0be4e34e50bdd0c28f)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10385: Mon Sep 22 11:50:47 2025
  read: IOPS=169k, BW=660MiB/s (692MB/s)(6600MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=104, max=10104, avg=5495.16, stdev=2740.29
     lat (nsec): min=1643, max=109113, avg=2369.55, stdev=1234.32
    clat percentiles (msec):
     |  1.00th=[  271],  5.00th=[  978], 10.00th=[ 1670], 20.00th=[ 2735],
     | 30.00th=[ 3742], 40.00th=[ 4665], 50.00th=[ 5604], 60.00th=[ 6477],
     | 70.00th=[ 7416], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=372880, max=752784, per=99.50%, avg=672443.53, stdev=118978.84, samples=19
   iops        : min=93220, max=188196, avg=168110.84, stdev=29744.80, samples=19
  write: IOPS=169k, BW=659MiB/s (692MB/s)(6596MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=104, max=10104, avg=5496.69, stdev=2740.91
     lat (usec): min=4, max=134, avg= 8.96, stdev= 4.68
    clat percentiles (msec):
     |  1.00th=[  271],  5.00th=[  978], 10.00th=[ 1670], 20.00th=[ 2735],
     | 30.00th=[ 3742], 40.00th=[ 4665], 50.00th=[ 5604], 60.00th=[ 6477],
     | 70.00th=[ 7416], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=373320, max=753568, per=99.49%, avg=671858.11, stdev=118935.51, samples=19
   iops        : min=93330, max=188392, avg=167964.53, stdev=29733.88, samples=19
  lat (msec)   : 250=0.89%, 500=1.48%, 750=1.41%, 1000=1.35%, 2000=7.90%
  lat (msec)   : >=2000=86.96%
  cpu          : usr=26.59%, sys=73.39%, ctx=66, majf=0, minf=35
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=1689719,1688459,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=660MiB/s (692MB/s), 660MiB/s-660MiB/s (692MB/s-692MB/s), io=6600MiB (6921MB), run=10001-10001msec
  WRITE: bw=659MiB/s (692MB/s), 659MiB/s-659MiB/s (692MB/s-692MB/s), io=6596MiB (6916MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/105, sectors=0/151016, merge=0/50, ticks=0/211, in_queue=211, util=0.13%
```
