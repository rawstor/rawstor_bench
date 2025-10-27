[&lt; back](..)

# perftest--without-liburing-file-4k-1-1

2025-10-27 07:30:50

refs/heads/releases/v0.0

[4fa2443](https://github.com/rawstor/librawstor/commit/4fa2443ebab1beeb730ff1197ebc0c793eb2cbb7)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11119: Mon Oct 27 07:30:47 2025
  read: IOPS=161k, BW=628MiB/s (658MB/s)(6276MiB/10001msec)
    slat (nsec): min=9, max=24276, avg=30.75, stdev=68.29
    clat (nsec): min=1663, max=111620, avg=2464.94, stdev=1309.23
     lat (nsec): min=1693, max=111681, avg=2495.69, stdev=1312.22
    clat percentiles (nsec):
     |  1.00th=[ 1976],  5.00th=[ 2064], 10.00th=[ 2096], 20.00th=[ 2128],
     | 30.00th=[ 2160], 40.00th=[ 2192], 50.00th=[ 2224], 60.00th=[ 2256],
     | 70.00th=[ 2320], 80.00th=[ 2384], 90.00th=[ 2608], 95.00th=[ 3632],
     | 99.00th=[ 7392], 99.50th=[11584], 99.90th=[18304], 99.95th=[21632],
     | 99.99th=[30336]
   bw (  KiB/s): min=359992, max=727200, per=99.33%, avg=638336.84, stdev=117558.96, samples=19
   iops        : min=89998, max=181800, avg=159584.21, stdev=29389.73, samples=19
  write: IOPS=161k, BW=627MiB/s (657MB/s)(6271MiB/10001msec); 0 zone resets
    slat (nsec): min=29, max=28123, avg=43.25, stdev=66.99
    clat (usec): min=2, max=109, avg= 3.17, stdev= 1.32
     lat (usec): min=2, max=109, avg= 3.22, stdev= 1.33
    clat percentiles (nsec):
     |  1.00th=[ 2416],  5.00th=[ 2480], 10.00th=[ 2512], 20.00th=[ 2576],
     | 30.00th=[ 2608], 40.00th=[ 2640], 50.00th=[ 2672], 60.00th=[ 2736],
     | 70.00th=[ 2800], 80.00th=[ 3024], 90.00th=[ 5152], 95.00th=[ 5600],
     | 99.00th=[ 6944], 99.50th=[ 8384], 99.90th=[15168], 99.95th=[17280],
     | 99.99th=[25728]
   bw (  KiB/s): min=360000, max=724952, per=99.30%, avg=637524.63, stdev=117215.55, samples=19
   iops        : min=90000, max=181238, avg=159381.16, stdev=29303.89, samples=19
  lat (usec)   : 2=0.74%, 4=89.19%, 10=9.57%, 20=0.45%, 50=0.04%
  lat (usec)   : 100=0.01%, 250=0.01%
  cpu          : usr=28.63%, sys=71.34%, ctx=60, majf=0, minf=37
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=1606692,1605280,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=628MiB/s (658MB/s), 628MiB/s-628MiB/s (658MB/s-658MB/s), io=6276MiB (6581MB), run=10001-10001msec
  WRITE: bw=627MiB/s (657MB/s), 627MiB/s-627MiB/s (657MB/s-657MB/s), io=6271MiB (6575MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/29, sectors=0/5848, merge=0/43, ticks=0/26, in_queue=26, util=0.03%
```
