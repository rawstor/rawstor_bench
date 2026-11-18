[&lt; back](..)

# perftest--without-liburing-file-4k-1-1

2026-11-18 08:46:19

refs/heads/add/object-image-import-export

[1e6eb8f](https://github.com/rawstor/librawstor/commit/1e6eb8f3a6e9ce22bae2b9a79c38c74f00bddfd2)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16418: Wed Nov 18 08:45:37 2026
  read: IOPS=314k, BW=1227MiB/s (1287MB/s)(12.0GiB/10001msec)
    slat (nsec): min=320, max=46948, avg=424.50, stdev=225.34
    clat (nsec): min=1783, max=58440, avg=2506.69, stdev=596.52
     lat (nsec): min=2133, max=58870, avg=2931.18, stdev=652.77
    clat percentiles (nsec):
     |  1.00th=[ 2008],  5.00th=[ 2096], 10.00th=[ 2128], 20.00th=[ 2256],
     | 30.00th=[ 2448], 40.00th=[ 2480], 50.00th=[ 2512], 60.00th=[ 2544],
     | 70.00th=[ 2576], 80.00th=[ 2608], 90.00th=[ 2672], 95.00th=[ 2800],
     | 99.00th=[ 3440], 99.50th=[ 4128], 99.90th=[11712], 99.95th=[12480],
     | 99.99th=[19840]
   bw (  MiB/s): min= 1200, max= 1239, per=100.00%, avg=1228.28, stdev=10.79, samples=20
   iops        : min=307452, max=317268, avg=314438.70, stdev=2762.27, samples=20
  lat (usec)   : 2=0.83%, 4=98.61%, 10=0.30%, 20=0.24%, 50=0.01%
  lat (usec)   : 100=0.01%
  cpu          : usr=51.94%, sys=48.05%, ctx=54, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=3142683,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16420: Wed Nov 18 08:45:37 2026
  write: IOPS=2969, BW=11.6MiB/s (12.2MB/s)(116MiB/10001msec); 0 zone resets
    slat (nsec): min=1523, max=26579, avg=2754.70, stdev=1044.25
    clat (usec): min=219, max=16471, avg=332.57, stdev=210.38
     lat (usec): min=221, max=16474, avg=335.32, stdev=210.41
    clat percentiles (usec):
     |  1.00th=[  231],  5.00th=[  243], 10.00th=[  251], 20.00th=[  269],
     | 30.00th=[  289], 40.00th=[  302], 50.00th=[  314], 60.00th=[  322],
     | 70.00th=[  334], 80.00th=[  351], 90.00th=[  383], 95.00th=[  433],
     | 99.00th=[  742], 99.50th=[ 1450], 99.90th=[ 3097], 99.95th=[ 3490],
     | 99.99th=[ 5997]
   bw (  KiB/s): min=10952, max=12384, per=100.00%, avg=11881.85, stdev=410.44, samples=20
   iops        : min= 2738, max= 3096, avg=2970.40, stdev=102.66, samples=20
  lat (usec)   : 250=9.52%, 500=87.41%, 750=2.10%, 1000=0.29%
  lat (msec)   : 2=0.31%, 4=0.34%, 10=0.02%, 20=0.01%
  cpu          : usr=3.00%, sys=10.60%, ctx=59673, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,29695,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=1227MiB/s (1287MB/s), 1227MiB/s-1227MiB/s (1287MB/s-1287MB/s), io=12.0GiB (12.9GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=11.6MiB/s (12.2MB/s), 11.6MiB/s-11.6MiB/s (12.2MB/s-12.2MB/s), io=116MiB (122MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=1/75441, sectors=8/2249776, merge=0/114376, ticks=7/15867, in_queue=15874, util=38.55%
```
