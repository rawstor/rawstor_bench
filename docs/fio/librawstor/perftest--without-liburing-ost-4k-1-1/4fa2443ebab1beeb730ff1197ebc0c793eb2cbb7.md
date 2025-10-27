[&lt; back](..)

# perftest--without-liburing-ost-4k-1-1

2025-10-27 07:30:49

refs/heads/releases/v0.0

[4fa2443](https://github.com/rawstor/librawstor/commit/4fa2443ebab1beeb730ff1197ebc0c793eb2cbb7)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=12130: Mon Oct 27 07:30:47 2025
  read: IOPS=5948, BW=23.2MiB/s (24.4MB/s)(232MiB/10001msec)
    slat (nsec): min=40, max=17933, avg=169.91, stdev=229.49
    clat (usec): min=43, max=24399, avg=70.83, stdev=185.14
     lat (usec): min=44, max=24399, avg=71.00, stdev=185.14
    clat percentiles (usec):
     |  1.00th=[   53],  5.00th=[   57], 10.00th=[   58], 20.00th=[   62],
     | 30.00th=[   64], 40.00th=[   67], 50.00th=[   69], 60.00th=[   71],
     | 70.00th=[   73], 80.00th=[   76], 90.00th=[   82], 95.00th=[   88],
     | 99.00th=[  102], 99.50th=[  111], 99.90th=[  145], 99.95th=[  293],
     | 99.99th=[ 1729]
   bw (  KiB/s): min=21992, max=25072, per=100.00%, avg=23854.74, stdev=949.00, samples=19
   iops        : min= 5498, max= 6268, avg=5963.68, stdev=237.25, samples=19
  write: IOPS=5933, BW=23.2MiB/s (24.3MB/s)(232MiB/10001msec); 0 zone resets
    slat (nsec): min=80, max=20659, avg=260.71, stdev=244.37
    clat (usec): min=55, max=25434, avg=93.93, stdev=185.96
     lat (usec): min=55, max=25434, avg=94.19, stdev=185.96
    clat percentiles (usec):
     |  1.00th=[   74],  5.00th=[   79], 10.00th=[   82], 20.00th=[   84],
     | 30.00th=[   87], 40.00th=[   89], 50.00th=[   92], 60.00th=[   94],
     | 70.00th=[   96], 80.00th=[   99], 90.00th=[  105], 95.00th=[  112],
     | 99.00th=[  125], 99.50th=[  135], 99.90th=[  190], 99.95th=[  355],
     | 99.99th=[ 1385]
   bw (  KiB/s): min=21936, max=25448, per=100.00%, avg=23743.16, stdev=898.14, samples=19
   iops        : min= 5484, max= 6362, avg=5935.79, stdev=224.54, samples=19
  lat (usec)   : 50=0.12%, 100=90.47%, 250=9.35%, 500=0.04%, 750=0.01%
  lat (usec)   : 1000=0.01%
  lat (msec)   : 2=0.01%, 4=0.01%, 10=0.01%, 20=0.01%, 50=0.01%
  cpu          : usr=9.93%, sys=31.35%, ctx=118938, majf=0, minf=44
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=59495,59345,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=23.2MiB/s (24.4MB/s), 23.2MiB/s-23.2MiB/s (24.4MB/s-24.4MB/s), io=232MiB (244MB), run=10001-10001msec
  WRITE: bw=23.2MiB/s (24.3MB/s), 23.2MiB/s-23.2MiB/s (24.3MB/s-24.3MB/s), io=232MiB (243MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/144, sectors=0/54656, merge=0/1115, ticks=0/275, in_queue=281, util=0.16%
```
