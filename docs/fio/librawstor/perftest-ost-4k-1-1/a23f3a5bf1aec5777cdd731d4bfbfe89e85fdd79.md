[&lt; back](..)

# perftest-ost-4k-1-1

2026-11-20 10:30:46

refs/heads/add/list-by-location

[a23f3a5](https://github.com/rawstor/librawstor/commit/a23f3a5bf1aec5777cdd731d4bfbfe89e85fdd79)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16333: Fri Nov 20 10:29:38 2026
  read: IOPS=28.5k, BW=111MiB/s (117MB/s)(1114MiB/10001msec)
    slat (nsec): min=881, max=26760, avg=1030.54, stdev=350.73
    clat (usec): min=27, max=635, avg=33.80, stdev= 4.07
     lat (usec): min=28, max=637, avg=34.83, stdev= 4.12
    clat percentiles (nsec):
     |  1.00th=[30080],  5.00th=[30592], 10.00th=[30592], 20.00th=[31104],
     | 30.00th=[31360], 40.00th=[32128], 50.00th=[33024], 60.00th=[33536],
     | 70.00th=[34560], 80.00th=[35584], 90.00th=[37632], 95.00th=[40704],
     | 99.00th=[48896], 99.50th=[51456], 99.90th=[59648], 99.95th=[66048],
     | 99.99th=[90624]
   bw (  KiB/s): min=104528, max=121472, per=100.00%, avg=114161.75, stdev=5036.25, samples=20
   iops        : min=26132, max=30368, avg=28540.45, stdev=1259.09, samples=20
  lat (usec)   : 50=99.29%, 100=0.71%, 250=0.01%, 500=0.01%, 750=0.01%
  cpu          : usr=13.53%, sys=34.43%, ctx=285286, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=285276,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16338: Fri Nov 20 10:29:38 2026
  write: IOPS=3123, BW=12.2MiB/s (12.8MB/s)(122MiB/10001msec); 0 zone resets
    slat (nsec): min=1923, max=131469, avg=2649.25, stdev=1155.13
    clat (usec): min=236, max=12333, avg=317.17, stdev=99.54
     lat (usec): min=238, max=12336, avg=319.82, stdev=99.63
    clat percentiles (usec):
     |  1.00th=[  260],  5.00th=[  269], 10.00th=[  277], 20.00th=[  285],
     | 30.00th=[  297], 40.00th=[  310], 50.00th=[  318], 60.00th=[  322],
     | 70.00th=[  326], 80.00th=[  334], 90.00th=[  347], 95.00th=[  359],
     | 99.00th=[  486], 99.50th=[  578], 99.90th=[ 1156], 99.95th=[ 1827],
     | 99.99th=[ 2933]
   bw (  KiB/s): min=11312, max=12920, per=100.00%, avg=12499.70, stdev=369.56, samples=20
   iops        : min= 2828, max= 3230, avg=3124.90, stdev=92.38, samples=20
  lat (usec)   : 250=0.07%, 500=99.01%, 750=0.66%, 1000=0.12%
  lat (msec)   : 2=0.10%, 4=0.03%, 10=0.01%, 20=0.01%
  cpu          : usr=2.03%, sys=4.22%, ctx=31240, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,31238,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=111MiB/s (117MB/s), 111MiB/s-111MiB/s (117MB/s-117MB/s), io=1114MiB (1168MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=12.2MiB/s (12.8MB/s), 12.2MiB/s-12.2MiB/s (12.8MB/s-12.8MB/s), io=122MiB (128MB), run=10001-10001msec

Disk stats (read/write):
  nvme0n1: ios=1/80338, sectors=8/1795568, merge=0/120944, ticks=0/13356, in_queue=13358, util=34.57%
```
