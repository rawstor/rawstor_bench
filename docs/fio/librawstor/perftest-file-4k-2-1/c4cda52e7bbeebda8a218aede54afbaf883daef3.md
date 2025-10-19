[&lt; back](..)

# perftest-file-4k-2-1

2025-10-19 09:56:36

refs/heads/feat/ci

[c4cda52](https://github.com/rawstor/librawstor/commit/c4cda52e7bbeebda8a218aede54afbaf883daef3)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10661: Sun Oct 19 09:56:34 2025
  read: IOPS=61.8k, BW=241MiB/s (253MB/s)(2413MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10104, avg=5412.04, stdev=2812.28
     lat (nsec): min=1432, max=104116, avg=5610.68, stdev=4130.15
    clat percentiles (msec):
     |  1.00th=[  232],  5.00th=[  709], 10.00th=[ 1334], 20.00th=[ 2601],
     | 30.00th=[ 3641], 40.00th=[ 4597], 50.00th=[ 5537], 60.00th=[ 6477],
     | 70.00th=[ 7416], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=188128, max=289672, per=99.93%, avg=246895.16, stdev=33231.28, samples=19
   iops        : min=47032, max=72418, avg=61723.79, stdev=8307.82, samples=19
  write: IOPS=61.7k, BW=241MiB/s (253MB/s)(2410MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10105, avg=5412.09, stdev=2812.70
     lat (usec): min=3, max=1120, avg=25.85, stdev= 8.49
    clat percentiles (msec):
     |  1.00th=[  232],  5.00th=[  709], 10.00th=[ 1334], 20.00th=[ 2601],
     | 30.00th=[ 3641], 40.00th=[ 4597], 50.00th=[ 5537], 60.00th=[ 6477],
     | 70.00th=[ 7416], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=190520, max=288408, per=99.94%, avg=246647.58, stdev=33046.00, samples=19
   iops        : min=47630, max=72102, avg=61661.89, stdev=8261.50, samples=19
  lat (msec)   : 250=1.14%, 500=2.08%, 750=2.08%, 1000=1.96%, 2000=7.83%
  lat (msec)   : >=2000=84.92%
  cpu          : usr=17.23%, sys=48.71%, ctx=262833, majf=0, minf=24
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=617708,617062,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=241MiB/s (253MB/s), 241MiB/s-241MiB/s (253MB/s-253MB/s), io=2413MiB (2530MB), run=10001-10001msec
  WRITE: bw=241MiB/s (253MB/s), 241MiB/s-241MiB/s (253MB/s-253MB/s), io=2410MiB (2527MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/5, sectors=0/696, merge=0/16, ticks=0/3, in_queue=2, util=0.01%
```
