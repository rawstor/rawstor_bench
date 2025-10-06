[&lt; back](..)

# perftest-ost-4k-1-1

2025-10-06 09:57:00

refs/heads/add/uri

[7d5ccdc](https://github.com/rawstor/librawstor/commit/7d5ccdce3ba82ca4a4ebd0dd1adf6e8799c84a40)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11829: Mon Oct  6 09:56:58 2025
  read: IOPS=5665, BW=22.1MiB/s (23.2MB/s)(221MiB/10001msec)
    slat (nsec): min=70, max=21029, avg=205.49, stdev=265.80
    clat (usec): min=37, max=26080, avg=73.88, stdev=183.87
     lat (usec): min=38, max=26081, avg=74.08, stdev=183.87
    clat percentiles (usec):
     |  1.00th=[   56],  5.00th=[   60], 10.00th=[   62], 20.00th=[   65],
     | 30.00th=[   68], 40.00th=[   70], 50.00th=[   71], 60.00th=[   74],
     | 70.00th=[   76], 80.00th=[   79], 90.00th=[   85], 95.00th=[   90],
     | 99.00th=[  103], 99.50th=[  111], 99.90th=[  137], 99.95th=[  163],
     | 99.99th=[ 2114]
   bw (  KiB/s): min=21152, max=24168, per=100.00%, avg=22666.00, stdev=705.45, samples=20
   iops        : min= 5288, max= 6042, avg=5666.50, stdev=176.36, samples=20
  write: IOPS=5640, BW=22.0MiB/s (23.1MB/s)(220MiB/10001msec); 0 zone resets
    slat (nsec): min=120, max=17894, avg=284.04, stdev=246.65
    clat (usec): min=55, max=29009, avg=99.10, stdev=176.79
     lat (usec): min=55, max=29009, avg=99.39, stdev=176.79
    clat percentiles (usec):
     |  1.00th=[   80],  5.00th=[   84], 10.00th=[   87], 20.00th=[   90],
     | 30.00th=[   92], 40.00th=[   95], 50.00th=[   97], 60.00th=[   99],
     | 70.00th=[  101], 80.00th=[  104], 90.00th=[  111], 95.00th=[  117],
     | 99.00th=[  129], 99.50th=[  137], 99.90th=[  172], 99.95th=[  217],
     | 99.99th=[ 1516]
   bw (  KiB/s): min=21272, max=23936, per=100.00%, avg=22565.20, stdev=810.99, samples=20
   iops        : min= 5318, max= 5984, avg=5641.30, stdev=202.75, samples=20
  lat (usec)   : 50=0.06%, 100=82.09%, 250=17.81%, 500=0.02%, 750=0.01%
  lat (usec)   : 1000=0.01%
  lat (msec)   : 2=0.01%, 4=0.01%, 20=0.01%, 50=0.01%
  cpu          : usr=7.31%, sys=33.42%, ctx=113151, majf=0, minf=293
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=56665,56413,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=22.1MiB/s (23.2MB/s), 22.1MiB/s-22.1MiB/s (23.2MB/s-23.2MB/s), io=221MiB (232MB), run=10001-10001msec
  WRITE: bw=22.0MiB/s (23.1MB/s), 22.0MiB/s-22.0MiB/s (23.1MB/s-23.1MB/s), io=220MiB (231MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/88, sectors=0/30304, merge=0/979, ticks=0/205, in_queue=211, util=0.15%
```
