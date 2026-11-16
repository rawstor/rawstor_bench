[&lt; back](..)

# perftest--without-liburing-file-4k-1-1

2026-11-16 21:04:41

refs/heads/add/security-authorization

[bad7dc5](https://github.com/rawstor/librawstor/commit/bad7dc5e9daf991dedda6e426d6eb5ed774ca05d)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16358: Mon Nov 16 21:04:00 2026
  read: IOPS=320k, BW=1249MiB/s (1309MB/s)(12.2GiB/10001msec)
    slat (nsec): min=320, max=40002, avg=428.67, stdev=224.45
    clat (nsec): min=1743, max=71604, avg=2443.62, stdev=578.22
     lat (nsec): min=2113, max=72045, avg=2872.29, stdev=637.48
    clat percentiles (nsec):
     |  1.00th=[ 1960],  5.00th=[ 2024], 10.00th=[ 2064], 20.00th=[ 2192],
     | 30.00th=[ 2384], 40.00th=[ 2416], 50.00th=[ 2448], 60.00th=[ 2480],
     | 70.00th=[ 2512], 80.00th=[ 2544], 90.00th=[ 2640], 95.00th=[ 2704],
     | 99.00th=[ 3152], 99.50th=[ 3984], 99.90th=[11584], 99.95th=[12352],
     | 99.99th=[19072]
   bw (  MiB/s): min= 1231, max= 1262, per=100.00%, avg=1249.65, stdev= 8.48, samples=20
   iops        : min=315380, max=323106, avg=319909.85, stdev=2170.35, samples=20
  lat (usec)   : 2=2.93%, 4=96.58%, 10=0.24%, 20=0.24%, 50=0.01%
  lat (usec)   : 100=0.01%
  cpu          : usr=53.66%, sys=46.32%, ctx=55, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=3197336,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16362: Mon Nov 16 21:04:00 2026
  write: IOPS=3094, BW=12.1MiB/s (12.7MB/s)(121MiB/10001msec); 0 zone resets
    slat (nsec): min=1352, max=27671, avg=2564.29, stdev=894.22
    clat (usec): min=187, max=11134, avg=319.13, stdev=274.53
     lat (usec): min=189, max=11136, avg=321.70, stdev=274.54
    clat percentiles (usec):
     |  1.00th=[  202],  5.00th=[  225], 10.00th=[  239], 20.00th=[  253],
     | 30.00th=[  269], 40.00th=[  289], 50.00th=[  297], 60.00th=[  310],
     | 70.00th=[  322], 80.00th=[  343], 90.00th=[  375], 95.00th=[  424],
     | 99.00th=[  611], 99.50th=[  799], 99.90th=[ 3884], 99.95th=[ 7439],
     | 99.99th=[ 9896]
   bw (  KiB/s): min=11328, max=13048, per=100.00%, avg=12382.00, stdev=442.48, samples=20
   iops        : min= 2832, max= 3262, avg=3095.45, stdev=110.67, samples=20
  lat (usec)   : 250=17.71%, 500=79.95%, 750=1.77%, 1000=0.19%
  lat (msec)   : 2=0.08%, 4=0.21%, 10=0.08%, 20=0.01%
  cpu          : usr=2.83%, sys=11.22%, ctx=62268, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,30944,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=1249MiB/s (1309MB/s), 1249MiB/s-1249MiB/s (1309MB/s-1309MB/s), io=12.2GiB (13.1GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=12.1MiB/s (12.7MB/s), 12.1MiB/s-12.1MiB/s (12.7MB/s-12.7MB/s), io=121MiB (127MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=1/79132, sectors=8/2322096, merge=0/119852, ticks=6/11391, in_queue=11398, util=37.22%
```
