[&lt; back](..)

# perftest-ost-4k-2-1

2025-10-24 07:15:15

refs/heads/ci/packages

[cdec14c](https://github.com/rawstor/librawstor/commit/cdec14c0f1cf5df283d6f4d7ca9b9c8cfe1400b4)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11916: Fri Oct 24 07:15:12 2025
  read: IOPS=16.1k, BW=62.9MiB/s (65.9MB/s)(629MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=106, max=10105, avg=5152.71, stdev=2919.85
     lat (usec): min=17, max=45907, avg=53.71, stdev=360.97
    clat percentiles (msec):
     |  1.00th=[  222],  5.00th=[  625], 10.00th=[ 1070], 20.00th=[ 2089],
     | 30.00th=[ 3104], 40.00th=[ 4144], 50.00th=[ 5134], 60.00th=[ 6208],
     | 70.00th=[ 7215], 80.00th=[ 8221], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=58080, max=75440, per=100.00%, avg=64485.47, stdev=4259.36, samples=19
   iops        : min=14520, max=18860, avg=16121.37, stdev=1064.84, samples=19
  write: IOPS=16.1k, BW=62.9MiB/s (65.9MB/s)(629MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=107, max=10105, avg=5159.45, stdev=2917.48
     lat (usec): min=23, max=45955, avg=68.90, stdev=419.30
    clat percentiles (msec):
     |  1.00th=[  218],  5.00th=[  617], 10.00th=[ 1070], 20.00th=[ 2072],
     | 30.00th=[ 3104], 40.00th=[ 4144], 50.00th=[ 5134], 60.00th=[ 6208],
     | 70.00th=[ 7282], 80.00th=[ 8221], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=57976, max=75200, per=100.00%, avg=64544.84, stdev=4541.26, samples=19
   iops        : min=14494, max=18800, avg=16136.21, stdev=1135.31, samples=19
  lat (msec)   : 250=1.29%, 500=2.56%, 750=2.61%, 1000=2.77%, 2000=9.89%
  lat (msec)   : >=2000=80.90%
  cpu          : usr=11.79%, sys=39.35%, ctx=218788, majf=0, minf=43
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=160976,160956,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=62.9MiB/s (65.9MB/s), 62.9MiB/s-62.9MiB/s (65.9MB/s-65.9MB/s), io=629MiB (659MB), run=10001-10001msec
  WRITE: bw=62.9MiB/s (65.9MB/s), 62.9MiB/s-62.9MiB/s (65.9MB/s-65.9MB/s), io=629MiB (659MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=1/149, sectors=160/42032, merge=0/1039, ticks=0/133, in_queue=138, util=0.18%
```
