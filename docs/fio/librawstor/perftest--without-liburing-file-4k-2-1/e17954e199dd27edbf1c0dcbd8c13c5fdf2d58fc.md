[&lt; back](..)

# perftest--without-liburing-file-4k-2-1

2026-11-20 11:26:39

refs/heads/main

[e17954e](https://github.com/rawstor/librawstor/commit/e17954e199dd27edbf1c0dcbd8c13c5fdf2d58fc)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16330: Fri Nov 20 11:25:25 2026
  read: IOPS=384k, BW=1501MiB/s (1574MB/s)(14.7GiB/10001msec)
    slat (nsec): min=200, max=28913, avg=312.53, stdev=176.95
    clat (nsec): min=2654, max=88221, avg=4699.61, stdev=1289.87
     lat (nsec): min=2944, max=88502, avg=5012.14, stdev=1288.55
    clat percentiles (nsec):
     |  1.00th=[ 2960],  5.00th=[ 3216], 10.00th=[ 3440], 20.00th=[ 3984],
     | 30.00th=[ 4256], 40.00th=[ 4448], 50.00th=[ 4512], 60.00th=[ 4576],
     | 70.00th=[ 4704], 80.00th=[ 4896], 90.00th=[ 6432], 95.00th=[ 7520],
     | 99.00th=[ 7968], 99.50th=[10048], 99.90th=[15680], 99.95th=[17024],
     | 99.99th=[21888]
   bw (  MiB/s): min= 1488, max= 1511, per=100.00%, avg=1502.22, stdev= 7.63, samples=20
   iops        : min=381018, max=386816, avg=384568.75, stdev=1953.41, samples=20
  lat (usec)   : 4=20.42%, 10=79.08%, 20=0.48%, 50=0.02%, 100=0.01%
  cpu          : usr=42.54%, sys=57.44%, ctx=63, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=3843876,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=16332: Fri Nov 20 11:25:25 2026
  write: IOPS=1717, BW=6872KiB/s (7037kB/s)(67.1MiB/10001msec); 0 zone resets
    slat (nsec): min=400, max=27541, avg=1238.22, stdev=895.49
    clat (usec): min=179, max=217756, avg=1171.66, stdev=8824.10
     lat (usec): min=180, max=217757, avg=1172.89, stdev=8824.13
    clat percentiles (usec):
     |  1.00th=[   212],  5.00th=[   269], 10.00th=[   334], 20.00th=[   465],
     | 30.00th=[   494], 40.00th=[   515], 50.00th=[   537], 60.00th=[   553],
     | 70.00th=[   578], 80.00th=[   627], 90.00th=[   799], 95.00th=[   898],
     | 99.00th=[  7242], 99.50th=[ 20841], 99.90th=[177210], 99.95th=[198181],
     | 99.99th=[217056]
   bw (  KiB/s): min= 1552, max=12136, per=100.00%, avg=6873.70, stdev=3338.74, samples=20
   iops        : min=  388, max= 3034, avg=1718.35, stdev=834.66, samples=20
  lat (usec)   : 250=3.38%, 500=29.49%, 750=54.23%, 1000=9.22%
  lat (msec)   : 2=1.86%, 4=0.52%, 10=0.51%, 20=0.29%, 50=0.13%
  lat (msec)   : 100=0.13%, 250=0.25%
  cpu          : usr=0.75%, sys=3.67%, ctx=34481, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,17180,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=1501MiB/s (1574MB/s), 1501MiB/s-1501MiB/s (1574MB/s-1574MB/s), io=14.7GiB (15.7GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=6872KiB/s (7037kB/s), 6872KiB/s-6872KiB/s (7037kB/s-7037kB/s), io=67.1MiB (70.4MB), run=10001-10001msec

Disk stats (read/write):
  nvme0n1: ios=3/47160, sectors=48/1670968, merge=0/69751, ticks=28/131164, in_queue=131193, util=48.41%
```
