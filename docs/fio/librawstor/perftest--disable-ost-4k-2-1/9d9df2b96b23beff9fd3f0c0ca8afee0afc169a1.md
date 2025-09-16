[&lt; back](..)

# perftest--disable-ost-4k-2-1

2025-09-16 21:09:40

refs/heads/main

[9d9df2b](https://github.com/rawstor/librawstor/commit/9d9df2b96b23beff9fd3f0c0ca8afee0afc169a1)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10412: Tue Sep 16 21:09:38 2025
  read: IOPS=73.7k, BW=288MiB/s (302MB/s)(2879MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=104, max=10104, avg=5371.17, stdev=2821.38
     lat (nsec): min=1322, max=186319, avg=4856.21, stdev=3596.36
    clat percentiles (msec):
     |  1.00th=[  230],  5.00th=[  718], 10.00th=[ 1334], 20.00th=[ 2534],
     | 30.00th=[ 3540], 40.00th=[ 4463], 50.00th=[ 5470], 60.00th=[ 6409],
     | 70.00th=[ 7349], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=220944, max=342592, per=100.00%, avg=294815.20, stdev=35604.73, samples=20
   iops        : min=55236, max=85648, avg=73703.80, stdev=8901.18, samples=20
  write: IOPS=73.6k, BW=287MiB/s (301MB/s)(2874MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=104, max=10104, avg=5368.78, stdev=2820.45
     lat (usec): min=3, max=928, avg=21.35, stdev= 6.76
    clat percentiles (msec):
     |  1.00th=[  230],  5.00th=[  718], 10.00th=[ 1334], 20.00th=[ 2534],
     | 30.00th=[ 3540], 40.00th=[ 4463], 50.00th=[ 5470], 60.00th=[ 6409],
     | 70.00th=[ 7349], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=220056, max=341424, per=100.00%, avg=294344.40, stdev=35378.18, samples=20
   iops        : min=55014, max=85356, avg=73586.10, stdev=8844.54, samples=20
  lat (msec)   : 250=1.14%, 500=1.90%, 750=2.26%, 1000=1.89%, 2000=7.79%
  lat (msec)   : >=2000=85.02%
  cpu          : usr=16.81%, sys=51.32%, ctx=302224, majf=0, minf=28
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=737038,735861,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=288MiB/s (302MB/s), 288MiB/s-288MiB/s (302MB/s-302MB/s), io=2879MiB (3019MB), run=10001-10001msec
  WRITE: bw=287MiB/s (301MB/s), 287MiB/s-287MiB/s (301MB/s-301MB/s), io=2874MiB (3014MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/44, sectors=0/968, merge=0/2, ticks=0/10, in_queue=11, util=0.01%
```
