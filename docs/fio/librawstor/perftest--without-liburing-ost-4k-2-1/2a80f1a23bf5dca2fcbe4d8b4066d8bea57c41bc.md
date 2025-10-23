[&lt; back](..)

# perftest--without-liburing-ost-4k-2-1

2025-10-23 21:01:59

refs/heads/ci/packages

[2a80f1a](https://github.com/rawstor/librawstor/commit/2a80f1a23bf5dca2fcbe4d8b4066d8bea57c41bc)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11933: Thu Oct 23 21:01:57 2025
  read: IOPS=9920, BW=38.8MiB/s (40.6MB/s)(388MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10104, avg=5052.96, stdev=2899.67
     lat (usec): min=31, max=29596, avg=94.10, stdev=264.06
    clat percentiles (msec):
     |  1.00th=[  213],  5.00th=[  584], 10.00th=[ 1083], 20.00th=[ 2022],
     | 30.00th=[ 3004], 40.00th=[ 3977], 50.00th=[ 5000], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=36448, max=44296, per=100.00%, avg=39685.20, stdev=1696.72, samples=20
   iops        : min= 9112, max=11074, avg=9921.30, stdev=424.18, samples=20
  write: IOPS=9907, BW=38.7MiB/s (40.6MB/s)(387MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10104, avg=5064.40, stdev=2909.56
     lat (usec): min=49, max=29462, avg=105.10, stdev=184.52
    clat percentiles (msec):
     |  1.00th=[  207],  5.00th=[  584], 10.00th=[ 1083], 20.00th=[ 2005],
     | 30.00th=[ 3004], 40.00th=[ 4010], 50.00th=[ 5067], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=36920, max=44672, per=100.00%, avg=39634.40, stdev=1771.36, samples=20
   iops        : min= 9230, max=11168, avg=9908.60, stdev=442.84, samples=20
  lat (msec)   : 250=1.38%, 500=2.70%, 750=2.01%, 1000=2.90%, 2000=10.88%
  lat (msec)   : >=2000=80.14%
  cpu          : usr=12.14%, sys=36.88%, ctx=102751, majf=0, minf=43
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=99213,99086,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=38.8MiB/s (40.6MB/s), 38.8MiB/s-38.8MiB/s (40.6MB/s-40.6MB/s), io=388MiB (406MB), run=10001-10001msec
  WRITE: bw=38.7MiB/s (40.6MB/s), 38.7MiB/s-38.7MiB/s (40.6MB/s-40.6MB/s), io=387MiB (406MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/186, sectors=0/38000, merge=0/1183, ticks=0/614, in_queue=621, util=0.17%
```
