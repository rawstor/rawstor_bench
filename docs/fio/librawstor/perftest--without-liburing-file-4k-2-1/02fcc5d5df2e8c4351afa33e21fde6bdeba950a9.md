[&lt; back](..)

# perftest--without-liburing-file-4k-2-1

2026-11-19 18:17:11

refs/heads/add/location-list

[02fcc5d](https://github.com/rawstor/librawstor/commit/02fcc5d5df2e8c4351afa33e21fde6bdeba950a9)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16486: Thu Nov 19 18:16:10 2026
  read: IOPS=373k, BW=1456MiB/s (1526MB/s)(14.2GiB/10001msec)
    slat (nsec): min=290, max=45936, avg=404.17, stdev=229.30
    clat (nsec): min=2826, max=90459, avg=4734.07, stdev=1395.67
     lat (nsec): min=3186, max=90830, avg=5138.24, stdev=1406.54
    clat percentiles (nsec):
     |  1.00th=[ 3056],  5.00th=[ 3280], 10.00th=[ 3440], 20.00th=[ 3952],
     | 30.00th=[ 4320], 40.00th=[ 4448], 50.00th=[ 4512], 60.00th=[ 4640],
     | 70.00th=[ 4768], 80.00th=[ 4960], 90.00th=[ 6496], 95.00th=[ 7584],
     | 99.00th=[ 8160], 99.50th=[12224], 99.90th=[17024], 99.95th=[20864],
     | 99.99th=[26496]
   bw (  MiB/s): min= 1416, max= 1472, per=100.00%, avg=1456.40, stdev=13.51, samples=20
   iops        : min=362557, max=376911, avg=372838.90, stdev=3458.12, samples=20
  lat (usec)   : 4=21.13%, 10=78.27%, 20=0.53%, 50=0.06%, 100=0.01%
  cpu          : usr=52.40%, sys=47.58%, ctx=58, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=3726531,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=16490: Thu Nov 19 18:16:10 2026
  write: IOPS=3156, BW=12.3MiB/s (12.9MB/s)(123MiB/10001msec); 0 zone resets
    slat (nsec): min=561, max=22883, avg=2048.98, stdev=1277.08
    clat (usec): min=223, max=17549, avg=630.49, stdev=301.75
     lat (usec): min=226, max=17550, avg=632.54, stdev=301.54
    clat percentiles (usec):
     |  1.00th=[  249],  5.00th=[  302], 10.00th=[  400], 20.00th=[  529],
     | 30.00th=[  562], 40.00th=[  578], 50.00th=[  603], 60.00th=[  627],
     | 70.00th=[  652], 80.00th=[  701], 90.00th=[  865], 95.00th=[  955],
     | 99.00th=[ 1254], 99.50th=[ 2008], 99.90th=[ 3392], 99.95th=[ 5145],
     | 99.99th=[10290]
   bw (  KiB/s): min=11888, max=13282, per=100.00%, avg=12632.20, stdev=458.46, samples=20
   iops        : min= 2972, max= 3320, avg=3158.00, stdev=114.56, samples=20
  lat (usec)   : 250=1.08%, 500=12.66%, 750=70.31%, 1000=12.72%
  lat (msec)   : 2=2.73%, 4=0.42%, 10=0.07%, 20=0.01%
  cpu          : usr=2.05%, sys=11.40%, ctx=63447, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,31570,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=1456MiB/s (1526MB/s), 1456MiB/s-1456MiB/s (1526MB/s-1526MB/s), io=14.2GiB (15.3GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=12.3MiB/s (12.9MB/s), 12.3MiB/s-12.3MiB/s (12.9MB/s-12.9MB/s), io=123MiB (129MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=2/80559, sectors=16/2372280, merge=0/122080, ticks=8/15349, in_queue=15357, util=38.27%
```
