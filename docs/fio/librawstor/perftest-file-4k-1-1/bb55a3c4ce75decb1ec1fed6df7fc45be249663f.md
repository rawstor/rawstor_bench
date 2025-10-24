[&lt; back](..)

# perftest-file-4k-1-1

2025-10-24 06:47:48

refs/heads/ci/packages

[bb55a3c](https://github.com/rawstor/librawstor/commit/bb55a3c4ce75decb1ec1fed6df7fc45be249663f)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10914: Fri Oct 24 06:47:46 2025
  read: IOPS=32.2k, BW=126MiB/s (132MB/s)(1258MiB/10000msec)
    slat (nsec): min=9, max=14687, avg=44.24, stdev=76.78
    clat (nsec): min=1342, max=113973, avg=3268.48, stdev=2743.73
     lat (nsec): min=1372, max=114013, avg=3312.72, stdev=2750.45
    clat percentiles (nsec):
     |  1.00th=[ 1688],  5.00th=[ 1768], 10.00th=[ 1816], 20.00th=[ 1880],
     | 30.00th=[ 2008], 40.00th=[ 2224], 50.00th=[ 2352], 60.00th=[ 2544],
     | 70.00th=[ 3216], 80.00th=[ 4192], 90.00th=[ 5408], 95.00th=[ 7456],
     | 99.00th=[14912], 99.50th=[18816], 99.90th=[26240], 99.95th=[30592],
     | 99.99th=[70144]
   bw (  KiB/s): min=107992, max=142792, per=99.45%, avg=128140.63, stdev=9936.04, samples=19
   iops        : min=26998, max=35698, avg=32035.16, stdev=2484.01, samples=19
  write: IOPS=32.2k, BW=126MiB/s (132MB/s)(1258MiB/10000msec); 0 zone resets
    slat (nsec): min=29, max=17372, avg=73.55, stdev=113.80
    clat (usec): min=6, max=700, avg=26.82, stdev= 4.25
     lat (usec): min=6, max=700, avg=26.90, stdev= 4.26
    clat percentiles (nsec):
     |  1.00th=[21120],  5.00th=[22144], 10.00th=[22912], 20.00th=[23936],
     | 30.00th=[24704], 40.00th=[25472], 50.00th=[26240], 60.00th=[26752],
     | 70.00th=[27520], 80.00th=[29056], 90.00th=[31872], 95.00th=[33536],
     | 99.00th=[40192], 99.50th=[43776], 99.90th=[49920], 99.95th=[53504],
     | 99.99th=[86528]
   bw (  KiB/s): min=108632, max=141424, per=99.45%, avg=128071.16, stdev=9721.54, samples=19
   iops        : min=27158, max=35356, avg=32017.79, stdev=2430.38, samples=19
  lat (usec)   : 2=14.95%, 4=24.47%, 10=9.32%, 20=1.31%, 50=49.88%
  lat (usec)   : 100=0.06%, 250=0.01%, 500=0.01%, 750=0.01%
  cpu          : usr=9.79%, sys=38.58%, ctx=321656, majf=0, minf=23
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=322131,321935,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=126MiB/s (132MB/s), 126MiB/s-126MiB/s (132MB/s-132MB/s), io=1258MiB (1319MB), run=10000-10000msec
  WRITE: bw=126MiB/s (132MB/s), 126MiB/s-126MiB/s (132MB/s-132MB/s), io=1258MiB (1319MB), run=10000-10000msec

Disk stats (read/write):
  sda: ios=0/131, sectors=0/13472, merge=0/171, ticks=0/91, in_queue=91, util=0.05%
```
