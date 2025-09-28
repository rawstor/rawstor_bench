[&lt; back](..)

# perftest--without-liburing-4k-2-1

2025-09-28 20:09:32

refs/heads/add/socket

[5dded36](https://github.com/rawstor/librawstor/commit/5dded36e9d4baaed3055c2d7bddf2e03e51fd1da)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11651: Sun Sep 28 20:09:29 2025
  read: IOPS=14.7k, BW=57.2MiB/s (60.0MB/s)(572MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=107, max=10106, avg=5117.54, stdev=2918.76
     lat (usec): min=19, max=48547, avg=61.13, stdev=312.61
    clat percentiles (msec):
     |  1.00th=[  213],  5.00th=[  584], 10.00th=[ 1028], 20.00th=[ 2056],
     | 30.00th=[ 3071], 40.00th=[ 4077], 50.00th=[ 5134], 60.00th=[ 6141],
     | 70.00th=[ 7215], 80.00th=[ 8154], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=53192, max=64376, per=99.64%, avg=58408.42, stdev=3190.98, samples=19
   iops        : min=13298, max=16094, avg=14602.11, stdev=797.74, samples=19
  write: IOPS=14.7k, BW=57.3MiB/s (60.1MB/s)(573MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=107, max=10106, avg=5132.29, stdev=2921.85
     lat (usec): min=23, max=49054, avg=73.63, stdev=448.22
    clat percentiles (msec):
     |  1.00th=[  209],  5.00th=[  575], 10.00th=[ 1036], 20.00th=[ 2056],
     | 30.00th=[ 3104], 40.00th=[ 4111], 50.00th=[ 5201], 60.00th=[ 6208],
     | 70.00th=[ 7215], 80.00th=[ 8221], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=53544, max=64936, per=99.70%, avg=58501.47, stdev=2989.19, samples=19
   iops        : min=13386, max=16234, avg=14625.37, stdev=747.30, samples=19
  lat (msec)   : 250=1.43%, 500=2.67%, 750=2.75%, 1000=2.80%, 2000=9.85%
  lat (msec)   : >=2000=80.50%
  cpu          : usr=13.09%, sys=30.02%, ctx=157220, majf=0, minf=301
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=146556,146711,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=57.2MiB/s (60.0MB/s), 57.2MiB/s-57.2MiB/s (60.0MB/s-60.0MB/s), io=572MiB (600MB), run=10001-10001msec
  WRITE: bw=57.3MiB/s (60.1MB/s), 57.3MiB/s-57.3MiB/s (60.1MB/s-60.1MB/s), io=573MiB (601MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/121, sectors=0/40592, merge=0/1112, ticks=0/119, in_queue=122, util=0.14%
```
