[&lt; back](..)

# perftest-file-4k-2-1

2025-10-27 07:30:50

refs/heads/releases/v0.0

[4fa2443](https://github.com/rawstor/librawstor/commit/4fa2443ebab1beeb730ff1197ebc0c793eb2cbb7)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11011: Mon Oct 27 07:30:47 2025
  read: IOPS=67.6k, BW=264MiB/s (277MB/s)(2642MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10104, avg=5409.58, stdev=2802.83
     lat (nsec): min=1403, max=251237, avg=5445.66, stdev=4217.39
    clat percentiles (msec):
     |  1.00th=[  232],  5.00th=[  735], 10.00th=[ 1385], 20.00th=[ 2635],
     | 30.00th=[ 3608], 40.00th=[ 4530], 50.00th=[ 5537], 60.00th=[ 6409],
     | 70.00th=[ 7349], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9731],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=194056, max=315928, per=99.39%, avg=268922.53, stdev=37138.98, samples=19
   iops        : min=48514, max=78982, avg=67230.63, stdev=9284.74, samples=19
  write: IOPS=67.6k, BW=264MiB/s (277MB/s)(2639MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10104, avg=5408.61, stdev=2802.44
     lat (usec): min=3, max=824, avg=23.22, stdev= 8.71
    clat percentiles (msec):
     |  1.00th=[  230],  5.00th=[  726], 10.00th=[ 1385], 20.00th=[ 2635],
     | 30.00th=[ 3608], 40.00th=[ 4530], 50.00th=[ 5537], 60.00th=[ 6409],
     | 70.00th=[ 7349], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=193048, max=315376, per=99.45%, avg=268729.68, stdev=37179.45, samples=19
   iops        : min=48262, max=78844, avg=67182.42, stdev=9294.86, samples=19
  lat (msec)   : 250=1.15%, 500=2.05%, 750=1.97%, 1000=2.02%, 2000=7.24%
  lat (msec)   : >=2000=85.58%
  cpu          : usr=18.34%, sys=48.96%, ctx=280133, majf=0, minf=22
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=676472,675631,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=264MiB/s (277MB/s), 264MiB/s-264MiB/s (277MB/s-277MB/s), io=2642MiB (2771MB), run=10001-10001msec
  WRITE: bw=264MiB/s (277MB/s), 264MiB/s-264MiB/s (277MB/s-277MB/s), io=2639MiB (2767MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/19, sectors=0/2048, merge=0/36, ticks=0/9, in_queue=8, util=0.01%
```
