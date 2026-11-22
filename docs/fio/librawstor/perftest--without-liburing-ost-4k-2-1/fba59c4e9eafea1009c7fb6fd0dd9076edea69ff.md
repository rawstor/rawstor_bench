[&lt; back](..)

# perftest--without-liburing-ost-4k-2-1

2026-11-22 13:26:06

refs/heads/releases/v0.3

[fba59c4](https://github.com/rawstor/librawstor/commit/fba59c4e9eafea1009c7fb6fd0dd9076edea69ff)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16514: Sun Nov 22 13:25:34 2026
  read: IOPS=17.2k, BW=67.1MiB/s (70.4MB/s)(671MiB/10001msec)
    slat (nsec): min=491, max=61324, avg=4826.46, stdev=2278.60
    clat (usec): min=44, max=2651, avg=110.23, stdev=24.30
     lat (usec): min=49, max=2657, avg=115.06, stdev=24.43
    clat percentiles (usec):
     |  1.00th=[   74],  5.00th=[   85], 10.00th=[   90], 20.00th=[   96],
     | 30.00th=[  101], 40.00th=[  105], 50.00th=[  110], 60.00th=[  114],
     | 70.00th=[  118], 80.00th=[  124], 90.00th=[  133], 95.00th=[  141],
     | 99.00th=[  159], 99.50th=[  167], 99.90th=[  198], 99.95th=[  219],
     | 99.99th=[  644]
   bw (  KiB/s): min=65448, max=71872, per=100.00%, avg=68790.95, stdev=1559.13, samples=20
   iops        : min=16362, max=17968, avg=17197.60, stdev=389.71, samples=20
  lat (usec)   : 50=0.02%, 100=28.46%, 250=71.50%, 500=0.01%, 750=0.01%
  lat (usec)   : 1000=0.01%
  lat (msec)   : 2=0.01%, 4=0.01%
  cpu          : usr=34.23%, sys=37.97%, ctx=89925, majf=0, minf=54
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=171896,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=16516: Sun Nov 22 13:25:34 2026
  write: IOPS=3364, BW=13.1MiB/s (13.8MB/s)(131MiB/10001msec); 0 zone resets
    slat (nsec): min=882, max=57777, avg=9602.23, stdev=4085.48
    clat (usec): min=335, max=14322, avg=583.05, stdev=296.41
     lat (usec): min=344, max=14327, avg=592.66, stdev=296.12
    clat percentiles (usec):
     |  1.00th=[  375],  5.00th=[  404], 10.00th=[  420], 20.00th=[  445],
     | 30.00th=[  465], 40.00th=[  490], 50.00th=[  515], 60.00th=[  553],
     | 70.00th=[  635], 80.00th=[  725], 90.00th=[  807], 95.00th=[  873],
     | 99.00th=[ 1090], 99.50th=[ 1565], 99.90th=[ 2638], 99.95th=[ 4752],
     | 99.99th=[12911]
   bw (  KiB/s): min=12376, max=14112, per=100.00%, avg=13464.00, stdev=446.11, samples=20
   iops        : min= 3094, max= 3528, avg=3365.90, stdev=111.49, samples=20
  lat (usec)   : 500=44.64%, 750=39.00%, 1000=14.66%
  lat (msec)   : 2=1.41%, 4=0.23%, 10=0.03%, 20=0.03%
  cpu          : usr=8.95%, sys=10.15%, ctx=28499, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,33648,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=67.1MiB/s (70.4MB/s), 67.1MiB/s-67.1MiB/s (70.4MB/s-70.4MB/s), io=671MiB (704MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=13.1MiB/s (13.8MB/s), 13.1MiB/s-13.1MiB/s (13.8MB/s-13.8MB/s), io=131MiB (138MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=1/80787, sectors=8/1874272, merge=0/130779, ticks=1/11309, in_queue=11310, util=30.11%
```
