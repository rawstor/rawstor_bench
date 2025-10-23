[&lt; back](..)

# perftest--without-liburing-file-4k-1-1

2025-10-23 21:01:35

refs/heads/ci/packages

[2a80f1a](https://github.com/rawstor/librawstor/commit/2a80f1a23bf5dca2fcbe4d8b4066d8bea57c41bc)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10949: Thu Oct 23 21:01:32 2025
  read: IOPS=171k, BW=667MiB/s (700MB/s)(6675MiB/10001msec)
    slat (nsec): min=9, max=32721, avg=27.13, stdev=56.80
    clat (nsec): min=1663, max=746464, avg=2320.58, stdev=1379.69
     lat (nsec): min=1683, max=746504, avg=2347.71, stdev=1381.90
    clat percentiles (nsec):
     |  1.00th=[ 1944],  5.00th=[ 1992], 10.00th=[ 2008], 20.00th=[ 2040],
     | 30.00th=[ 2064], 40.00th=[ 2096], 50.00th=[ 2128], 60.00th=[ 2128],
     | 70.00th=[ 2160], 80.00th=[ 2224], 90.00th=[ 2384], 95.00th=[ 3472],
     | 99.00th=[ 6816], 99.50th=[10816], 99.90th=[17024], 99.95th=[20352],
     | 99.99th=[31104]
   bw (  KiB/s): min=376008, max=757320, per=100.00%, avg=683513.20, stdev=117342.59, samples=20
   iops        : min=94002, max=189330, avg=170878.30, stdev=29335.65, samples=20
  write: IOPS=171k, BW=667MiB/s (699MB/s)(6670MiB/10001msec); 0 zone resets
    slat (nsec): min=29, max=30066, avg=41.09, stdev=77.50
    clat (usec): min=2, max=178, avg= 2.96, stdev= 1.19
     lat (usec): min=2, max=178, avg= 3.00, stdev= 1.19
    clat percentiles (nsec):
     |  1.00th=[ 2384],  5.00th=[ 2416], 10.00th=[ 2448], 20.00th=[ 2480],
     | 30.00th=[ 2512], 40.00th=[ 2512], 50.00th=[ 2544], 60.00th=[ 2576],
     | 70.00th=[ 2608], 80.00th=[ 2800], 90.00th=[ 4704], 95.00th=[ 5088],
     | 99.00th=[ 6112], 99.50th=[ 7840], 99.90th=[14272], 99.95th=[16064],
     | 99.99th=[23168]
   bw (  KiB/s): min=376304, max=759176, per=100.00%, avg=682994.40, stdev=117301.64, samples=20
   iops        : min=94076, max=189794, avg=170748.60, stdev=29325.41, samples=20
  lat (usec)   : 2=3.78%, 4=87.13%, 10=8.66%, 20=0.40%, 50=0.03%
  lat (usec)   : 100=0.01%, 250=0.01%, 750=0.01%
  cpu          : usr=29.52%, sys=70.45%, ctx=76, majf=0, minf=37
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=1708783,1707486,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=667MiB/s (700MB/s), 667MiB/s-667MiB/s (700MB/s-700MB/s), io=6675MiB (6999MB), run=10001-10001msec
  WRITE: bw=667MiB/s (699MB/s), 667MiB/s-667MiB/s (699MB/s-699MB/s), io=6670MiB (6994MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/74, sectors=0/137384, merge=0/34, ticks=0/681, in_queue=681, util=0.16%
```
