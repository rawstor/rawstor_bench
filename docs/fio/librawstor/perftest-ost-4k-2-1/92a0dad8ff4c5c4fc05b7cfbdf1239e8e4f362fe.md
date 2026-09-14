[&lt; back](..)

# perftest-ost-4k-2-1

2026-09-14 09:59:18

refs/heads/releases/v0.2.11

[92a0dad](https://github.com/rawstor/librawstor/commit/92a0dad8ff4c5c4fc05b7cfbdf1239e8e4f362fe)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=14013: Mon Sep 14 09:58:26 2026
  read: IOPS=23.9k, BW=93.4MiB/s (97.9MB/s)(934MiB/10001msec)
    slat (nsec): min=230, max=56196, avg=561.78, stdev=352.67
    clat (usec): min=23, max=574, avg=82.45, stdev=13.20
     lat (usec): min=23, max=574, avg=83.01, stdev=13.26
    clat percentiles (usec):
     |  1.00th=[   70],  5.00th=[   73], 10.00th=[   73], 20.00th=[   74],
     | 30.00th=[   75], 40.00th=[   76], 50.00th=[   78], 60.00th=[   81],
     | 70.00th=[   85], 80.00th=[   95], 90.00th=[   99], 95.00th=[  104],
     | 99.00th=[  117], 99.50th=[  126], 99.90th=[  192], 99.95th=[  247],
     | 99.99th=[  326]
   bw (  KiB/s): min=82128, max=106288, per=100.00%, avg=95658.50, stdev=6968.61, samples=20
   iops        : min=20532, max=26572, avg=23914.50, stdev=1742.14, samples=20
  lat (usec)   : 50=0.06%, 100=90.53%, 250=9.36%, 500=0.04%, 750=0.01%
  cpu          : usr=8.89%, sys=44.65%, ctx=119530, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=239024,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=14015: Mon Sep 14 09:58:26 2026
  write: IOPS=16.4k, BW=64.0MiB/s (67.1MB/s)(640MiB/10001msec); 0 zone resets
    slat (nsec): min=621, max=36559, avg=1271.25, stdev=563.69
    clat (usec): min=67, max=399, avg=119.96, stdev=14.38
     lat (usec): min=68, max=399, avg=121.23, stdev=14.44
    clat percentiles (usec):
     |  1.00th=[  100],  5.00th=[  102], 10.00th=[  104], 20.00th=[  109],
     | 30.00th=[  110], 40.00th=[  112], 50.00th=[  117], 60.00th=[  122],
     | 70.00th=[  128], 80.00th=[  139], 90.00th=[  143], 95.00th=[  145],
     | 99.00th=[  149], 99.50th=[  153], 99.90th=[  167], 99.95th=[  178],
     | 99.99th=[  212]
   bw (  KiB/s): min=   56, max=71470, per=95.29%, avg=62458.57, stdev=15010.39, samples=21
   iops        : min=   14, max=17867, avg=15614.57, stdev=3752.59, samples=21
  lat (usec)   : 100=1.09%, 250=98.90%, 500=0.01%
  cpu          : usr=10.26%, sys=30.90%, ctx=83493, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,163873,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=93.4MiB/s (97.9MB/s), 93.4MiB/s-93.4MiB/s (97.9MB/s-97.9MB/s), io=934MiB (979MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=64.0MiB/s (67.1MB/s), 64.0MiB/s-64.0MiB/s (67.1MB/s-67.1MB/s), io=640MiB (671MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/448, sectors=0/307264, merge=0/1026, ticks=0/1151, in_queue=1151, util=0.19%
```
