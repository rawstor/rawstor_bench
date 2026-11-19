[&lt; back](..)

# perftest--without-liburing-ost-4k-2-1

2026-11-19 18:17:11

refs/heads/add/location-list

[02fcc5d](https://github.com/rawstor/librawstor/commit/02fcc5d5df2e8c4351afa33e21fde6bdeba950a9)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16305: Thu Nov 19 18:16:08 2026
  read: IOPS=29.8k, BW=116MiB/s (122MB/s)(1164MiB/10001msec)
    slat (nsec): min=330, max=51728, avg=2105.65, stdev=956.53
    clat (usec): min=32, max=2878, avg=64.45, stdev=17.54
     lat (usec): min=34, max=2879, avg=66.56, stdev=17.65
    clat percentiles (usec):
     |  1.00th=[   42],  5.00th=[   47], 10.00th=[   51], 20.00th=[   55],
     | 30.00th=[   58], 40.00th=[   61], 50.00th=[   64], 60.00th=[   67],
     | 70.00th=[   70], 80.00th=[   74], 90.00th=[   80], 95.00th=[   85],
     | 99.00th=[   98], 99.50th=[  103], 99.90th=[  121], 99.95th=[  135],
     | 99.99th=[  379]
   bw (  KiB/s): min=112240, max=124432, per=100.00%, avg=119273.20, stdev=3888.51, samples=20
   iops        : min=28060, max=31108, avg=29818.25, stdev=972.10, samples=20
  lat (usec)   : 50=9.26%, 100=90.00%, 250=0.73%, 500=0.01%, 750=0.01%
  lat (usec)   : 1000=0.01%
  lat (msec)   : 2=0.01%, 4=0.01%
  cpu          : usr=28.31%, sys=41.59%, ctx=172008, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=298036,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=16309: Thu Nov 19 18:16:08 2026
  write: IOPS=3055, BW=11.9MiB/s (12.5MB/s)(120MiB/10022msec); 0 zone resets
    slat (nsec): min=781, max=48804, avg=6297.91, stdev=2391.21
    clat (usec): min=252, max=208500, avg=647.28, stdev=2884.76
     lat (usec): min=257, max=208508, avg=653.57, stdev=2884.75
    clat percentiles (usec):
     |  1.00th=[   285],  5.00th=[   314], 10.00th=[   334], 20.00th=[   363],
     | 30.00th=[   400], 40.00th=[   457], 50.00th=[   529], 60.00th=[   562],
     | 70.00th=[   594], 80.00th=[   627], 90.00th=[   685], 95.00th=[   766],
     | 99.00th=[  2114], 99.50th=[  5145], 99.90th=[ 28967], 99.95th=[ 49546],
     | 99.99th=[149947]
   bw (  KiB/s): min= 3879, max=15224, per=100.00%, avg=12252.20, stdev=2603.38, samples=20
   iops        : min=  969, max= 3806, avg=3062.90, stdev=650.95, samples=20
  lat (usec)   : 500=44.85%, 750=49.74%, 1000=2.82%
  lat (msec)   : 2=1.55%, 4=0.42%, 10=0.29%, 20=0.20%, 50=0.08%
  lat (msec)   : 100=0.02%, 250=0.03%
  cpu          : usr=5.21%, sys=5.69%, ctx=26928, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,30618,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=116MiB/s (122MB/s), 116MiB/s-116MiB/s (122MB/s-122MB/s), io=1164MiB (1221MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=11.9MiB/s (12.5MB/s), 11.9MiB/s-11.9MiB/s (12.5MB/s-12.5MB/s), io=120MiB (125MB), run=10022-10022msec

Disk stats (read/write):
  nvme0n1: ios=2/71388, sectors=16/1632080, merge=0/108662, ticks=3/29020, in_queue=29023, util=38.07%
```
