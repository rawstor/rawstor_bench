[&lt; back](..)

# perftest-file-4k-2-1

2025-10-24 07:30:51

refs/heads/ci/packages

[dbbc9bc](https://github.com/rawstor/librawstor/commit/dbbc9bcbb4cccdc4988920db56d816ba41b49be3)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10915: Fri Oct 24 07:30:48 2025
  read: IOPS=68.5k, BW=267MiB/s (280MB/s)(2674MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10104, avg=5458.31, stdev=2846.48
     lat (nsec): min=1442, max=163215, avg=5512.37, stdev=3994.10
    clat percentiles (msec):
     |  1.00th=[  232],  5.00th=[  760], 10.00th=[ 1401], 20.00th=[ 2601],
     | 30.00th=[ 3608], 40.00th=[ 4597], 50.00th=[ 5537], 60.00th=[ 6544],
     | 70.00th=[ 7550], 80.00th=[ 8423], 90.00th=[ 9329], 95.00th=[ 9731],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=211960, max=326744, per=98.88%, avg=270730.95, stdev=36751.18, samples=19
   iops        : min=52990, max=81686, avg=67682.74, stdev=9187.79, samples=19
  write: IOPS=68.4k, BW=267MiB/s (280MB/s)(2671MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10104, avg=5457.24, stdev=2846.22
     lat (usec): min=3, max=369, avg=22.76, stdev= 6.90
    clat percentiles (msec):
     |  1.00th=[  232],  5.00th=[  760], 10.00th=[ 1401], 20.00th=[ 2601],
     | 30.00th=[ 3608], 40.00th=[ 4597], 50.00th=[ 5537], 60.00th=[ 6544],
     | 70.00th=[ 7550], 80.00th=[ 8423], 90.00th=[ 9329], 95.00th=[ 9731],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=211736, max=327912, per=98.95%, avg=270582.32, stdev=36638.33, samples=19
   iops        : min=52934, max=81978, avg=67645.58, stdev=9159.58, samples=19
  lat (msec)   : 250=1.15%, 500=1.94%, 750=1.84%, 1000=2.05%, 2000=8.09%
  lat (msec)   : >=2000=84.93%
  cpu          : usr=19.26%, sys=49.73%, ctx=280372, majf=0, minf=22
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=684580,683714,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=267MiB/s (280MB/s), 267MiB/s-267MiB/s (280MB/s-280MB/s), io=2674MiB (2804MB), run=10001-10001msec
  WRITE: bw=267MiB/s (280MB/s), 267MiB/s-267MiB/s (280MB/s-280MB/s), io=2671MiB (2800MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/410, sectors=0/148248, merge=0/1045, ticks=0/664, in_queue=665, util=0.31%
```
