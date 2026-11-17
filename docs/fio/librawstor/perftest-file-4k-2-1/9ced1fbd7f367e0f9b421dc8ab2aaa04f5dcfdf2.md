[&lt; back](..)

# perftest-file-4k-2-1

2026-11-17 21:13:26

refs/heads/worktree-ref-tenant-to-account

[9ced1fb](https://github.com/rawstor/librawstor/commit/9ced1fbd7f367e0f9b421dc8ab2aaa04f5dcfdf2)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16177: Tue Nov 17 21:08:25 2026
  read: IOPS=578k, BW=2259MiB/s (2369MB/s)(22.1GiB/10001msec)
    slat (nsec): min=150, max=106922, avg=205.47, stdev=216.08
    clat (usec): min=2, max=140, avg= 3.12, stdev= 1.00
     lat (usec): min=2, max=140, avg= 3.33, stdev= 1.03
    clat percentiles (nsec):
     |  1.00th=[ 2704],  5.00th=[ 2800], 10.00th=[ 2832], 20.00th=[ 2896],
     | 30.00th=[ 2960], 40.00th=[ 2992], 50.00th=[ 3056], 60.00th=[ 3120],
     | 70.00th=[ 3152], 80.00th=[ 3248], 90.00th=[ 3344], 95.00th=[ 3472],
     | 99.00th=[ 4080], 99.50th=[ 4640], 99.90th=[11328], 99.95th=[15168],
     | 99.99th=[41216]
   bw (  MiB/s): min= 2165, max= 2338, per=100.00%, avg=2260.70, stdev=52.20, samples=20
   iops        : min=554308, max=598720, avg=578740.25, stdev=13363.37, samples=20
  lat (usec)   : 4=98.86%, 10=0.80%, 20=0.31%, 50=0.02%, 100=0.01%
  lat (usec)   : 250=0.01%
  cpu          : usr=31.99%, sys=67.99%, ctx=71, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=5784312,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=16183: Tue Nov 17 21:08:25 2026
  write: IOPS=3973, BW=15.5MiB/s (16.3MB/s)(155MiB/10001msec); 0 zone resets
    slat (nsec): min=320, max=93843, avg=691.15, stdev=729.39
    clat (usec): min=217, max=190997, avg=502.27, stdev=1730.32
     lat (usec): min=217, max=190998, avg=502.96, stdev=1730.37
    clat percentiles (usec):
     |  1.00th=[   249],  5.00th=[   265], 10.00th=[   281], 20.00th=[   302],
     | 30.00th=[   318], 40.00th=[   338], 50.00th=[   363], 60.00th=[   392],
     | 70.00th=[   429], 80.00th=[   490], 90.00th=[   611], 95.00th=[   742],
     | 99.00th=[  3589], 99.50th=[  4948], 99.90th=[  8848], 99.95th=[ 10159],
     | 99.99th=[124257]
   bw (  KiB/s): min= 6336, max=20592, per=100.00%, avg=15901.50, stdev=3390.00, samples=20
   iops        : min= 1584, max= 5148, avg=3975.25, stdev=847.55, samples=20
  lat (usec)   : 250=1.34%, 500=79.79%, 750=13.97%, 1000=1.28%
  lat (msec)   : 2=1.59%, 4=1.19%, 10=0.80%, 20=0.04%, 50=0.01%
  lat (msec)   : 100=0.01%, 250=0.01%
  cpu          : usr=0.88%, sys=2.62%, ctx=44101, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,39741,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=2259MiB/s (2369MB/s), 2259MiB/s-2259MiB/s (2369MB/s-2369MB/s), io=22.1GiB (23.7GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=15.5MiB/s (16.3MB/s), 15.5MiB/s-15.5MiB/s (16.3MB/s-16.3MB/s), io=155MiB (163MB), run=10001-10001msec

Disk stats (read/write):
  nvme0n1: ios=0/94402, sectors=0/3251208, merge=0/145098, ticks=0/140061, in_queue=140062, util=49.22%
```
