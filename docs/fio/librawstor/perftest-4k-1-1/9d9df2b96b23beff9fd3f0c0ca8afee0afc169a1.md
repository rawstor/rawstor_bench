[&lt; back](..)

# perftest-4k-1-1

2025-09-16 21:10:07

refs/heads/main

[9d9df2b](https://github.com/rawstor/librawstor/commit/9d9df2b96b23beff9fd3f0c0ca8afee0afc169a1)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11449: Tue Sep 16 21:10:04 2025
  read: IOPS=6102, BW=23.8MiB/s (25.0MB/s)(238MiB/10001msec)
    slat (nsec): min=40, max=17152, avg=172.87, stdev=203.85
    clat (usec): min=39, max=26218, avg=68.06, stdev=170.98
     lat (usec): min=39, max=26218, avg=68.23, stdev=170.98
    clat percentiles (usec):
     |  1.00th=[   51],  5.00th=[   55], 10.00th=[   57], 20.00th=[   60],
     | 30.00th=[   62], 40.00th=[   63], 50.00th=[   65], 60.00th=[   68],
     | 70.00th=[   71], 80.00th=[   74], 90.00th=[   80], 95.00th=[   86],
     | 99.00th=[  100], 99.50th=[  108], 99.90th=[  135], 99.95th=[  176],
     | 99.99th=[  412]
   bw (  KiB/s): min=22592, max=27544, per=99.88%, avg=24382.32, stdev=1253.49, samples=19
   iops        : min= 5648, max= 6886, avg=6095.58, stdev=313.37, samples=19
  write: IOPS=6084, BW=23.8MiB/s (24.9MB/s)(238MiB/10001msec); 0 zone resets
    slat (nsec): min=80, max=57026, avg=237.99, stdev=336.59
    clat (usec): min=52, max=25079, avg=92.46, stdev=211.18
     lat (usec): min=52, max=25080, avg=92.70, stdev=211.18
    clat percentiles (usec):
     |  1.00th=[   74],  5.00th=[   77], 10.00th=[   80], 20.00th=[   83],
     | 30.00th=[   85], 40.00th=[   87], 50.00th=[   89], 60.00th=[   92],
     | 70.00th=[   94], 80.00th=[   98], 90.00th=[  103], 95.00th=[  110],
     | 99.00th=[  123], 99.50th=[  131], 99.90th=[  161], 99.95th=[  206],
     | 99.99th=[ 2147]
   bw (  KiB/s): min=22776, max=27144, per=99.82%, avg=24292.21, stdev=1217.49, samples=19
   iops        : min= 5694, max= 6786, avg=6073.05, stdev=304.37, samples=19
  lat (usec)   : 50=0.30%, 100=91.84%, 250=7.83%, 500=0.01%, 750=0.01%
  lat (msec)   : 2=0.01%, 4=0.01%, 50=0.01%
  cpu          : usr=6.13%, sys=33.87%, ctx=121974, majf=0, minf=289
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=61034,60848,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=23.8MiB/s (25.0MB/s), 23.8MiB/s-23.8MiB/s (25.0MB/s-25.0MB/s), io=238MiB (250MB), run=10001-10001msec
  WRITE: bw=23.8MiB/s (24.9MB/s), 23.8MiB/s-23.8MiB/s (24.9MB/s-24.9MB/s), io=238MiB (249MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/198, sectors=0/38280, merge=0/1157, ticks=0/309, in_queue=321, util=0.26%
```
