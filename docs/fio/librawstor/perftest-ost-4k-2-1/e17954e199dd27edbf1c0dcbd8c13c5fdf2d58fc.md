[&lt; back](..)

# perftest-ost-4k-2-1

2026-11-20 11:26:39

refs/heads/main

[e17954e](https://github.com/rawstor/librawstor/commit/e17954e199dd27edbf1c0dcbd8c13c5fdf2d58fc)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16502: Fri Nov 20 11:26:17 2026
  read: IOPS=47.8k, BW=187MiB/s (196MB/s)(1869MiB/10001msec)
    slat (nsec): min=290, max=310064, avg=1232.16, stdev=788.13
    clat (usec): min=15, max=2634, avg=40.33, stdev=16.87
     lat (usec): min=16, max=2635, avg=41.56, stdev=16.64
    clat percentiles (usec):
     |  1.00th=[   19],  5.00th=[   19], 10.00th=[   19], 20.00th=[   22],
     | 30.00th=[   24], 40.00th=[   46], 50.00th=[   50], 60.00th=[   51],
     | 70.00th=[   52], 80.00th=[   52], 90.00th=[   55], 95.00th=[   58],
     | 99.00th=[   68], 99.50th=[   72], 99.90th=[   86], 99.95th=[   92],
     | 99.99th=[  159]
   bw (  KiB/s): min=148192, max=326565, per=100.00%, avg=191473.20, stdev=43290.83, samples=20
   iops        : min=37048, max=81641, avg=47868.15, stdev=10822.65, samples=20
  lat (usec)   : 20=15.25%, 50=36.97%, 100=47.75%, 250=0.03%, 500=0.01%
  lat (msec)   : 4=0.01%
  cpu          : usr=31.33%, sys=30.86%, ctx=199290, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=478513,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=16509: Fri Nov 20 11:26:17 2026
  write: IOPS=7693, BW=30.1MiB/s (31.5MB/s)(301MiB/10001msec); 0 zone resets
    slat (nsec): min=665, max=41048, avg=5640.44, stdev=3749.09
    clat (usec): min=132, max=1878, avg=253.63, stdev=53.04
     lat (usec): min=136, max=1881, avg=259.27, stdev=52.78
    clat percentiles (usec):
     |  1.00th=[  178],  5.00th=[  192], 10.00th=[  200], 20.00th=[  212],
     | 30.00th=[  221], 40.00th=[  231], 50.00th=[  241], 60.00th=[  253],
     | 70.00th=[  273], 80.00th=[  293], 90.00th=[  330], 95.00th=[  355],
     | 99.00th=[  404], 99.50th=[  424], 99.90th=[  478], 99.95th=[  523],
     | 99.99th=[ 1139]
   bw (  KiB/s): min=30352, max=31222, per=100.00%, avg=30786.40, stdev=290.69, samples=20
   iops        : min= 7588, max= 7805, avg=7696.55, stdev=72.62, samples=20
  lat (usec)   : 250=57.35%, 500=42.59%, 750=0.03%, 1000=0.01%
  lat (msec)   : 2=0.02%
  cpu          : usr=10.96%, sys=8.09%, ctx=69677, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,76945,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=187MiB/s (196MB/s), 187MiB/s-187MiB/s (196MB/s-196MB/s), io=1869MiB (1960MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=30.1MiB/s (31.5MB/s), 30.1MiB/s-30.1MiB/s (31.5MB/s-31.5MB/s), io=301MiB (315MB), run=10001-10001msec

Disk stats (read/write):
    dm-0: ios=0/495996, sectors=0/3967968, merge=0/0, ticks=0/60758, in_queue=60758, util=31.73%, aggrios=0/158713, aggsectors=0/2358692, aggrmerge=0/136123, aggrticks=0/4988, aggrin_queue=4988, aggrutil=27.06%
  nvme0n1: ios=0/0, sectors=0/0, merge=0/0, ticks=0/0, in_queue=0, util=0.00%
  nvme1n1: ios=0/317426, sectors=0/4717384, merge=0/272247, ticks=0/9976, in_queue=9976, util=27.06%
```
