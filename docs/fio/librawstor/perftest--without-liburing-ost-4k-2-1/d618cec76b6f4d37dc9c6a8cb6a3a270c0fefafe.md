[&lt; back](..)

# perftest--without-liburing-ost-4k-2-1

2026-11-23 13:30:22

refs/heads/fix/drop-server-error-log-v0.3

[d618cec](https://github.com/rawstor/librawstor/commit/d618cec76b6f4d37dc9c6a8cb6a3a270c0fefafe)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=17069: Mon Nov 23 13:25:34 2026
  read: IOPS=17.6k, BW=68.9MiB/s (72.2MB/s)(689MiB/10001msec)
    slat (nsec): min=471, max=72716, avg=4839.60, stdev=2243.46
    clat (usec): min=41, max=3836, avg=107.30, stdev=35.84
     lat (usec): min=44, max=3844, avg=112.14, stdev=36.22
    clat percentiles (usec):
     |  1.00th=[   60],  5.00th=[   75], 10.00th=[   82], 20.00th=[   89],
     | 30.00th=[   96], 40.00th=[  101], 50.00th=[  106], 60.00th=[  112],
     | 70.00th=[  117], 80.00th=[  124], 90.00th=[  133], 95.00th=[  143],
     | 99.00th=[  165], 99.50th=[  180], 99.90th=[  265], 99.95th=[  545],
     | 99.99th=[ 1156]
   bw (  KiB/s): min=62304, max=78316, per=100.00%, avg=70572.45, stdev=4408.68, samples=20
   iops        : min=15576, max=19579, avg=17643.05, stdev=1102.16, samples=20
  lat (usec)   : 50=0.13%, 100=38.70%, 250=61.06%, 500=0.06%, 750=0.02%
  lat (usec)   : 1000=0.02%
  lat (msec)   : 2=0.01%, 4=0.01%
  cpu          : usr=34.76%, sys=36.77%, ctx=101542, majf=0, minf=49
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=176339,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=17074: Mon Nov 23 13:25:34 2026
  write: IOPS=3576, BW=14.0MiB/s (14.7MB/s)(140MiB/10002msec); 0 zone resets
    slat (nsec): min=912, max=137496, avg=9333.70, stdev=3956.99
    clat (usec): min=332, max=5112, avg=548.08, stdev=239.63
     lat (usec): min=340, max=5121, avg=557.42, stdev=239.35
    clat percentiles (usec):
     |  1.00th=[  367],  5.00th=[  392], 10.00th=[  408], 20.00th=[  429],
     | 30.00th=[  449], 40.00th=[  469], 50.00th=[  490], 60.00th=[  515],
     | 70.00th=[  553], 80.00th=[  635], 90.00th=[  750], 95.00th=[  832],
     | 99.00th=[ 1156], 99.50th=[ 2114], 99.90th=[ 3490], 99.95th=[ 4113],
     | 99.99th=[ 5014]
   bw (  KiB/s): min=13242, max=14928, per=100.00%, avg=14315.60, stdev=514.71, samples=20
   iops        : min= 3310, max= 3732, avg=3578.85, stdev=128.71, samples=20
  lat (usec)   : 500=54.82%, 750=35.08%, 1000=8.34%
  lat (msec)   : 2=1.25%, 4=0.45%, 10=0.06%
  cpu          : usr=9.56%, sys=10.57%, ctx=30711, majf=0, minf=37
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,35776,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=68.9MiB/s (72.2MB/s), 68.9MiB/s-68.9MiB/s (72.2MB/s-72.2MB/s), io=689MiB (722MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=14.0MiB/s (14.7MB/s), 14.0MiB/s-14.0MiB/s (14.7MB/s-14.7MB/s), io=140MiB (147MB), run=10002-10002msec

Disk stats (read/write):
  sda: ios=1/85656, sectors=8/1980208, merge=0/137613, ticks=1/12332, in_queue=12333, util=30.19%
```
