[&lt; back](..)

# perftest--disable-ost-4k-1-1

2025-09-28 20:09:23

refs/heads/add/socket

[5dded36](https://github.com/rawstor/librawstor/commit/5dded36e9d4baaed3055c2d7bddf2e03e51fd1da)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10631: Sun Sep 28 20:09:20 2025
  read: IOPS=32.2k, BW=126MiB/s (132MB/s)(1258MiB/10001msec)
    slat (nsec): min=20, max=17873, avg=37.60, stdev=75.85
    clat (nsec): min=1272, max=141475, avg=3251.53, stdev=2940.56
     lat (nsec): min=1302, max=141525, avg=3289.13, stdev=2945.94
    clat percentiles (nsec):
     |  1.00th=[ 1640],  5.00th=[ 1720], 10.00th=[ 1768], 20.00th=[ 1832],
     | 30.00th=[ 1944], 40.00th=[ 2128], 50.00th=[ 2224], 60.00th=[ 2416],
     | 70.00th=[ 3152], 80.00th=[ 4192], 90.00th=[ 5600], 95.00th=[ 7776],
     | 99.00th=[15424], 99.50th=[19072], 99.90th=[26752], 99.95th=[31360],
     | 99.99th=[84480]
   bw (  KiB/s): min=105304, max=145792, per=99.48%, avg=128152.42, stdev=13663.07, samples=19
   iops        : min=26326, max=36448, avg=32038.21, stdev=3415.86, samples=19
  write: IOPS=32.2k, BW=126MiB/s (132MB/s)(1257MiB/10001msec); 0 zone resets
    slat (nsec): min=40, max=38142, avg=70.13, stdev=149.90
    clat (usec): min=7, max=399, avg=26.90, stdev= 4.88
     lat (usec): min=8, max=399, avg=26.97, stdev= 4.90
    clat percentiles (nsec):
     |  1.00th=[20608],  5.00th=[21888], 10.00th=[22656], 20.00th=[23424],
     | 30.00th=[24192], 40.00th=[25216], 50.00th=[25984], 60.00th=[26496],
     | 70.00th=[27520], 80.00th=[30080], 90.00th=[32640], 95.00th=[35072],
     | 99.00th=[44288], 99.50th=[48384], 99.90th=[58112], 99.95th=[66048],
     | 99.99th=[97792]
   bw (  KiB/s): min=106904, max=144864, per=99.49%, avg=128082.95, stdev=13586.02, samples=19
   iops        : min=26726, max=36216, avg=32020.74, stdev=3396.51, samples=19
  lat (usec)   : 2=16.17%, 4=23.15%, 10=9.30%, 20=1.59%, 50=49.61%
  lat (usec)   : 100=0.18%, 250=0.01%, 500=0.01%
  cpu          : usr=8.96%, sys=38.40%, ctx=321628, majf=0, minf=32
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=322071,321863,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=126MiB/s (132MB/s), 126MiB/s-126MiB/s (132MB/s-132MB/s), io=1258MiB (1319MB), run=10001-10001msec
  WRITE: bw=126MiB/s (132MB/s), 126MiB/s-126MiB/s (132MB/s-132MB/s), io=1257MiB (1318MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/7, sectors=0/1824, merge=0/38, ticks=0/5, in_queue=4, util=0.01%
```
