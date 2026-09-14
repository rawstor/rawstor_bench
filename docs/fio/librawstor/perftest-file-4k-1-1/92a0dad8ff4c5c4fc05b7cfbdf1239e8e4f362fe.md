[&lt; back](..)

# perftest-file-4k-1-1

2026-09-14 09:59:18

refs/heads/releases/v0.2.11

[92a0dad](https://github.com/rawstor/librawstor/commit/92a0dad8ff4c5c4fc05b7cfbdf1239e8e4f362fe)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=13924: Mon Sep 14 09:58:17 2026
  read: IOPS=391k, BW=1528MiB/s (1602MB/s)(14.9GiB/10001msec)
    slat (nsec): min=170, max=38532, avg=195.39, stdev=165.47
    clat (nsec): min=1683, max=131915, avg=2112.55, stdev=557.45
     lat (nsec): min=1873, max=132095, avg=2307.94, stdev=584.18
    clat percentiles (nsec):
     |  1.00th=[ 1880],  5.00th=[ 1928], 10.00th=[ 1960], 20.00th=[ 1992],
     | 30.00th=[ 2008], 40.00th=[ 2040], 50.00th=[ 2064], 60.00th=[ 2096],
     | 70.00th=[ 2128], 80.00th=[ 2160], 90.00th=[ 2256], 95.00th=[ 2320],
     | 99.00th=[ 2576], 99.50th=[ 3088], 99.90th=[12608], 99.95th=[12992],
     | 99.99th=[16768]
   bw (  MiB/s): min= 1482, max= 1547, per=100.00%, avg=1528.61, stdev=13.01, samples=20
   iops        : min=379545, max=396110, avg=391323.80, stdev=3331.80, samples=20
  lat (usec)   : 2=22.84%, 4=76.89%, 10=0.06%, 20=0.21%, 50=0.01%
  lat (usec)   : 100=0.01%, 250=0.01%
  cpu          : usr=32.98%, sys=67.00%, ctx=73, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=3911095,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=13927: Mon Sep 14 09:58:17 2026
  write: IOPS=28.4k, BW=111MiB/s (116MB/s)(1110MiB/10001msec); 0 zone resets
    slat (nsec): min=370, max=53990, avg=643.86, stdev=233.08
    clat (usec): min=10, max=3257, avg=33.78, stdev= 9.67
     lat (usec): min=10, max=3258, avg=34.42, stdev= 9.73
    clat percentiles (usec):
     |  1.00th=[   24],  5.00th=[   28], 10.00th=[   29], 20.00th=[   30],
     | 30.00th=[   32], 40.00th=[   32], 50.00th=[   33], 60.00th=[   34],
     | 70.00th=[   38], 80.00th=[   39], 90.00th=[   41], 95.00th=[   42],
     | 99.00th=[   45], 99.50th=[   47], 99.90th=[   57], 99.95th=[   66],
     | 99.99th=[  157]
   bw (  KiB/s): min=  144, max=125595, per=95.31%, avg=108293.48, stdev=25545.95, samples=21
   iops        : min=   36, max=31398, avg=27073.24, stdev=6386.44, samples=21
  lat (usec)   : 20=0.10%, 50=99.61%, 100=0.27%, 250=0.01%, 500=0.01%
  lat (usec)   : 750=0.01%, 1000=0.01%
  lat (msec)   : 2=0.01%, 4=0.01%
  cpu          : usr=18.54%, sys=27.50%, ctx=284090, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,284097,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=1528MiB/s (1602MB/s), 1528MiB/s-1528MiB/s (1602MB/s-1602MB/s), io=14.9GiB (16.0GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=111MiB/s (116MB/s), 111MiB/s-111MiB/s (116MB/s-116MB/s), io=1110MiB (1164MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/407, sectors=0/336952, merge=0/948, ticks=0/540, in_queue=540, util=0.18%
```
