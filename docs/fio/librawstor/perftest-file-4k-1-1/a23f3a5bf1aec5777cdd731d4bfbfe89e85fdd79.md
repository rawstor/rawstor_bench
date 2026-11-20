[&lt; back](..)

# perftest-file-4k-1-1

2026-11-20 10:30:46

refs/heads/add/list-by-location

[a23f3a5](https://github.com/rawstor/librawstor/commit/a23f3a5bf1aec5777cdd731d4bfbfe89e85fdd79)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16523: Fri Nov 20 10:29:54 2026
  read: IOPS=348k, BW=1359MiB/s (1425MB/s)(13.3GiB/10001msec)
    slat (nsec): min=310, max=43572, avg=352.76, stdev=225.56
    clat (nsec): min=1793, max=75283, avg=2267.89, stdev=601.79
     lat (nsec): min=2133, max=75884, avg=2620.65, stdev=651.26
    clat percentiles (nsec):
     |  1.00th=[ 1992],  5.00th=[ 2040], 10.00th=[ 2096], 20.00th=[ 2128],
     | 30.00th=[ 2160], 40.00th=[ 2192], 50.00th=[ 2224], 60.00th=[ 2256],
     | 70.00th=[ 2288], 80.00th=[ 2320], 90.00th=[ 2416], 95.00th=[ 2512],
     | 99.00th=[ 3024], 99.50th=[ 3472], 99.90th=[11840], 99.95th=[13376],
     | 99.99th=[21120]
   bw (  MiB/s): min= 1341, max= 1384, per=100.00%, avg=1359.60, stdev=12.62, samples=20
   iops        : min=343392, max=354516, avg=348058.30, stdev=3231.31, samples=20
  lat (usec)   : 2=1.34%, 4=98.34%, 10=0.08%, 20=0.22%, 50=0.01%
  lat (usec)   : 100=0.01%
  cpu          : usr=36.58%, sys=63.40%, ctx=60, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=3478504,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16537: Fri Nov 20 10:29:54 2026
  write: IOPS=2932, BW=11.5MiB/s (12.0MB/s)(115MiB/10001msec); 0 zone resets
    slat (nsec): min=972, max=24947, avg=2167.44, stdev=930.73
    clat (usec): min=211, max=14363, avg=337.36, stdev=198.06
     lat (usec): min=213, max=14366, avg=339.53, stdev=198.09
    clat percentiles (usec):
     |  1.00th=[  247],  5.00th=[  262], 10.00th=[  269], 20.00th=[  285],
     | 30.00th=[  306], 40.00th=[  318], 50.00th=[  326], 60.00th=[  338],
     | 70.00th=[  351], 80.00th=[  363], 90.00th=[  392], 95.00th=[  429],
     | 99.00th=[  570], 99.50th=[  668], 99.90th=[ 1319], 99.95th=[ 3228],
     | 99.99th=[12518]
   bw (  KiB/s): min=11070, max=12392, per=100.00%, avg=11736.15, stdev=350.89, samples=20
   iops        : min= 2767, max= 3098, avg=2933.95, stdev=87.78, samples=20
  lat (usec)   : 250=1.58%, 500=96.55%, 750=1.52%, 1000=0.14%
  lat (msec)   : 2=0.15%, 4=0.02%, 10=0.02%, 20=0.01%
  cpu          : usr=2.34%, sys=2.62%, ctx=29330, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,29330,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=1359MiB/s (1425MB/s), 1359MiB/s-1359MiB/s (1425MB/s-1425MB/s), io=13.3GiB (14.2GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=11.5MiB/s (12.0MB/s), 11.5MiB/s-11.5MiB/s (12.0MB/s-12.0MB/s), io=115MiB (120MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=24/74680, sectors=1208/2220920, merge=29/113360, ticks=13/15740, in_queue=15754, util=35.29%
```
