[&lt; back](..)

# perftest--without-liburing-file-4k-2-1

2026-11-23 13:30:22

refs/heads/fix/drop-server-error-log-v0.3

[d618cec](https://github.com/rawstor/librawstor/commit/d618cec76b6f4d37dc9c6a8cb6a3a270c0fefafe)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16339: Mon Nov 23 13:23:34 2026
  read: IOPS=556k, BW=2173MiB/s (2279MB/s)(21.2GiB/10001msec)
    slat (nsec): min=150, max=163246, avg=241.28, stdev=200.68
    clat (nsec): min=1742, max=269647, avg=3212.96, stdev=1044.42
     lat (nsec): min=1953, max=269837, avg=3454.24, stdev=1055.26
    clat percentiles (nsec):
     |  1.00th=[ 1976],  5.00th=[ 2160], 10.00th=[ 2320], 20.00th=[ 2704],
     | 30.00th=[ 2896], 40.00th=[ 2992], 50.00th=[ 3056], 60.00th=[ 3152],
     | 70.00th=[ 3248], 80.00th=[ 3408], 90.00th=[ 4448], 95.00th=[ 5152],
     | 99.00th=[ 5600], 99.50th=[ 5856], 99.90th=[11456], 99.95th=[12864],
     | 99.99th=[18560]
   bw (  MiB/s): min= 2066, max= 2283, per=100.00%, avg=2174.41, stdev=51.76, samples=20
   iops        : min=528906, max=584632, avg=556650.25, stdev=13249.92, samples=20
  lat (usec)   : 2=1.26%, 4=87.06%, 10=11.41%, 20=0.26%, 50=0.01%
  lat (usec)   : 100=0.01%, 250=0.01%, 500=0.01%
  cpu          : usr=48.52%, sys=51.46%, ctx=65, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=5564103,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=16342: Mon Nov 23 13:23:34 2026
  write: IOPS=3398, BW=13.3MiB/s (13.9MB/s)(133MiB/10001msec); 0 zone resets
    slat (nsec): min=310, max=15053, avg=553.47, stdev=354.38
    clat (usec): min=200, max=159121, avg=587.56, stdev=1615.24
     lat (usec): min=201, max=159122, avg=588.11, stdev=1615.28
    clat percentiles (usec):
     |  1.00th=[  229],  5.00th=[  273], 10.00th=[  326], 20.00th=[  490],
     | 30.00th=[  510], 40.00th=[  529], 50.00th=[  545], 60.00th=[  562],
     | 70.00th=[  578], 80.00th=[  603], 90.00th=[  758], 95.00th=[  832],
     | 99.00th=[  963], 99.50th=[ 1090], 99.90th=[ 7242], 99.95th=[20317],
     | 99.99th=[79168]
   bw (  KiB/s): min= 2496, max=15184, per=100.00%, avg=13602.75, stdev=2714.55, samples=20
   iops        : min=  624, max= 3796, avg=3400.65, stdev=678.64, samples=20
  lat (usec)   : 250=2.97%, 500=21.80%, 750=64.78%, 1000=9.65%
  lat (msec)   : 2=0.55%, 4=0.10%, 10=0.08%, 20=0.03%, 50=0.03%
  lat (msec)   : 100=0.02%, 250=0.01%
  cpu          : usr=0.85%, sys=5.73%, ctx=68496, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,33993,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=2173MiB/s (2279MB/s), 2173MiB/s-2173MiB/s (2279MB/s-2279MB/s), io=21.2GiB (22.8GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=13.3MiB/s (13.9MB/s), 13.3MiB/s-13.3MiB/s (13.9MB/s-13.9MB/s), io=133MiB (139MB), run=10001-10001msec

Disk stats (read/write):
  nvme0n1: ios=3/88854, sectors=24/2612776, merge=0/132121, ticks=51/104402, in_queue=104453, util=46.86%
```
