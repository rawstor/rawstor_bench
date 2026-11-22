[&lt; back](..)

# perftest--without-liburing-file-4k-1-1

2026-11-22 13:26:06

refs/heads/releases/v0.3

[fba59c4](https://github.com/rawstor/librawstor/commit/fba59c4e9eafea1009c7fb6fd0dd9076edea69ff)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16350: Sun Nov 22 13:25:00 2026
  read: IOPS=483k, BW=1887MiB/s (1979MB/s)(18.4GiB/10001msec)
    slat (nsec): min=190, max=142054, avg=260.96, stdev=210.24
    clat (nsec): min=1162, max=282344, avg=1660.76, stdev=720.76
     lat (nsec): min=1382, max=282685, avg=1921.72, stdev=753.75
    clat percentiles (nsec):
     |  1.00th=[ 1336],  5.00th=[ 1400], 10.00th=[ 1448], 20.00th=[ 1528],
     | 30.00th=[ 1576], 40.00th=[ 1608], 50.00th=[ 1640], 60.00th=[ 1656],
     | 70.00th=[ 1704], 80.00th=[ 1752], 90.00th=[ 1816], 95.00th=[ 1896],
     | 99.00th=[ 2064], 99.50th=[ 2192], 99.90th=[ 8768], 99.95th=[ 9280],
     | 99.99th=[18816]
   bw (  MiB/s): min= 1772, max= 1961, per=100.00%, avg=1888.17, stdev=52.79, samples=20
   iops        : min=453760, max=502136, avg=483372.50, stdev=13514.62, samples=20
  lat (usec)   : 2=98.17%, 4=1.63%, 10=0.16%, 20=0.03%, 50=0.01%
  lat (usec)   : 100=0.01%, 250=0.01%, 500=0.01%
  cpu          : usr=48.82%, sys=51.16%, ctx=75, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=4831495,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16353: Sun Nov 22 13:25:00 2026
  write: IOPS=3508, BW=13.7MiB/s (14.4MB/s)(137MiB/10001msec); 0 zone resets
    slat (nsec): min=360, max=16725, avg=592.92, stdev=366.92
    clat (usec): min=190, max=129801, avg=284.08, stdev=1112.33
     lat (usec): min=190, max=129815, avg=284.67, stdev=1112.46
    clat percentiles (usec):
     |  1.00th=[  206],  5.00th=[  217], 10.00th=[  223], 20.00th=[  235],
     | 30.00th=[  249], 40.00th=[  260], 50.00th=[  265], 60.00th=[  273],
     | 70.00th=[  281], 80.00th=[  289], 90.00th=[  310], 95.00th=[  326],
     | 99.00th=[  478], 99.50th=[  562], 99.90th=[ 1188], 99.95th=[ 1844],
     | 99.99th=[82314]
   bw (  KiB/s): min= 6036, max=15440, per=100.00%, avg=14040.75, stdev=2267.14, samples=20
   iops        : min= 1509, max= 3860, avg=3510.15, stdev=566.78, samples=20
  lat (usec)   : 250=31.59%, 500=67.58%, 750=0.57%, 1000=0.10%
  lat (msec)   : 2=0.11%, 4=0.01%, 10=0.01%, 50=0.01%, 100=0.01%
  lat (msec)   : 250=0.01%
  cpu          : usr=0.81%, sys=6.33%, ctx=70659, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,35091,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=1887MiB/s (1979MB/s), 1887MiB/s-1887MiB/s (1979MB/s-1979MB/s), io=18.4GiB (19.8GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=13.7MiB/s (14.4MB/s), 13.7MiB/s-13.7MiB/s (14.4MB/s-14.4MB/s), io=137MiB (144MB), run=10001-10001msec

Disk stats (read/write):
  nvme0n1: ios=1/91966, sectors=8/2660104, merge=0/136977, ticks=1/97240, in_queue=97242, util=46.05%
```
