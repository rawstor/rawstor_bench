[&lt; back](..)

# perftest--without-liburing-file-4k-1-1

2025-10-19 09:57:01

refs/heads/feat/ci

[c4cda52](https://github.com/rawstor/librawstor/commit/c4cda52e7bbeebda8a218aede54afbaf883daef3)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10773: Sun Oct 19 09:56:59 2025
  read: IOPS=169k, BW=658MiB/s (690MB/s)(6583MiB/10001msec)
    slat (nsec): min=10, max=13486, avg=27.73, stdev=57.82
    clat (nsec): min=1723, max=110345, avg=2365.22, stdev=1204.18
     lat (nsec): min=1743, max=110375, avg=2392.95, stdev=1206.55
    clat percentiles (nsec):
     |  1.00th=[ 1976],  5.00th=[ 2024], 10.00th=[ 2064], 20.00th=[ 2096],
     | 30.00th=[ 2128], 40.00th=[ 2128], 50.00th=[ 2160], 60.00th=[ 2192],
     | 70.00th=[ 2224], 80.00th=[ 2256], 90.00th=[ 2416], 95.00th=[ 3472],
     | 99.00th=[ 6880], 99.50th=[10944], 99.90th=[16768], 99.95th=[20096],
     | 99.99th=[29824]
   bw (  KiB/s): min=367400, max=745744, per=99.54%, avg=670874.53, stdev=118438.96, samples=19
   iops        : min=91850, max=186436, avg=167718.63, stdev=29609.74, samples=19
  write: IOPS=168k, BW=658MiB/s (690MB/s)(6577MiB/10001msec); 0 zone resets
    slat (nsec): min=29, max=13455, avg=39.92, stdev=61.93
    clat (nsec): min=2104, max=80510, avg=2960.08, stdev=1146.65
     lat (nsec): min=2134, max=80550, avg=3000.00, stdev=1150.43
    clat percentiles (nsec):
     |  1.00th=[ 2384],  5.00th=[ 2416], 10.00th=[ 2448], 20.00th=[ 2480],
     | 30.00th=[ 2480], 40.00th=[ 2512], 50.00th=[ 2544], 60.00th=[ 2576],
     | 70.00th=[ 2608], 80.00th=[ 2800], 90.00th=[ 4704], 95.00th=[ 5024],
     | 99.00th=[ 6368], 99.50th=[ 7968], 99.90th=[14272], 99.95th=[15936],
     | 99.99th=[21888]
   bw (  KiB/s): min=368048, max=743920, per=99.52%, avg=670202.95, stdev=118254.42, samples=19
   iops        : min=92012, max=185980, avg=167550.74, stdev=29563.61, samples=19
  lat (usec)   : 2=0.96%, 4=89.95%, 10=8.65%, 20=0.41%, 50=0.03%
  lat (usec)   : 100=0.01%, 250=0.01%
  cpu          : usr=29.59%, sys=70.39%, ctx=75, majf=0, minf=34
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=1685180,1683825,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=658MiB/s (690MB/s), 658MiB/s-658MiB/s (690MB/s-690MB/s), io=6583MiB (6902MB), run=10001-10001msec
  WRITE: bw=658MiB/s (690MB/s), 658MiB/s-658MiB/s (690MB/s-690MB/s), io=6577MiB (6897MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/8, sectors=0/1848, merge=0/32, ticks=0/5, in_queue=5, util=0.02%
```
