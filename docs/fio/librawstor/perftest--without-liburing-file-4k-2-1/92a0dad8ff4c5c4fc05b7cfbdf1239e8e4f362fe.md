[&lt; back](..)

# perftest--without-liburing-file-4k-2-1

2026-09-14 09:59:18

refs/heads/releases/v0.2.11

[92a0dad](https://github.com/rawstor/librawstor/commit/92a0dad8ff4c5c4fc05b7cfbdf1239e8e4f362fe)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=14034: Mon Sep 14 09:58:21 2026
  read: IOPS=314k, BW=1228MiB/s (1288MB/s)(12.0GiB/10001msec)
    slat (nsec): min=160, max=83024, avg=204.70, stdev=202.30
    clat (usec): min=4, max=169, avg= 5.89, stdev= 1.12
     lat (usec): min=4, max=170, avg= 6.10, stdev= 1.14
    clat percentiles (nsec):
     |  1.00th=[ 5344],  5.00th=[ 5472], 10.00th=[ 5536], 20.00th=[ 5600],
     | 30.00th=[ 5728], 40.00th=[ 5728], 50.00th=[ 5792], 60.00th=[ 5856],
     | 70.00th=[ 5920], 80.00th=[ 5984], 90.00th=[ 6048], 95.00th=[ 6176],
     | 99.00th=[ 7456], 99.50th=[15936], 99.90th=[19072], 99.95th=[23424],
     | 99.99th=[38144]
   bw (  MiB/s): min= 1188, max= 1255, per=100.00%, avg=1229.34, stdev=13.63, samples=20
   iops        : min=304322, max=321480, avg=314712.05, stdev=3488.20, samples=20
  lat (usec)   : 10=99.33%, 20=0.59%, 50=0.08%, 100=0.01%, 250=0.01%
  cpu          : usr=33.32%, sys=66.66%, ctx=70, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=3145090,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=14036: Mon Sep 14 09:58:21 2026
  write: IOPS=255k, BW=994MiB/s (1043MB/s)(9945MiB/10001msec); 0 zone resets
    slat (nsec): min=240, max=155001, avg=292.75, stdev=227.60
    clat (usec): min=6, max=165, avg= 7.29, stdev= 1.22
     lat (usec): min=6, max=165, avg= 7.59, stdev= 1.25
    clat percentiles (nsec):
     |  1.00th=[ 6688],  5.00th=[ 6816], 10.00th=[ 6880], 20.00th=[ 7008],
     | 30.00th=[ 7072], 40.00th=[ 7072], 50.00th=[ 7136], 60.00th=[ 7200],
     | 70.00th=[ 7264], 80.00th=[ 7328], 90.00th=[ 7520], 95.00th=[ 7712],
     | 99.00th=[ 9792], 99.50th=[18816], 99.90th=[21376], 99.95th=[24960],
     | 99.99th=[33536]
   bw (  KiB/s): min=  400, max=1033000, per=95.30%, avg=970411.52, stdev=222519.98, samples=21
   iops        : min=  100, max=258250, avg=242602.67, stdev=55629.94, samples=21
  lat (usec)   : 10=99.06%, 20=0.75%, 50=0.18%, 100=0.01%, 250=0.01%
  cpu          : usr=32.18%, sys=67.78%, ctx=304, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,2545801,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=1228MiB/s (1288MB/s), 1228MiB/s-1228MiB/s (1288MB/s-1288MB/s), io=12.0GiB (12.9GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=994MiB/s (1043MB/s), 994MiB/s-994MiB/s (1043MB/s-1043MB/s), io=9945MiB (10.4GB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=1/282, sectors=248/362848, merge=0/717, ticks=0/434, in_queue=434, util=0.16%
```
