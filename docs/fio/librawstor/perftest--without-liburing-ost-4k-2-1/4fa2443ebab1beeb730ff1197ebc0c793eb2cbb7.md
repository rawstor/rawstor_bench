[&lt; back](..)

# perftest--without-liburing-ost-4k-2-1

2025-10-27 07:30:39

refs/heads/releases/v0.0

[4fa2443](https://github.com/rawstor/librawstor/commit/4fa2443ebab1beeb730ff1197ebc0c793eb2cbb7)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=12066: Mon Oct 27 07:30:36 2025
  read: IOPS=9934, BW=38.8MiB/s (40.7MB/s)(388MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10105, avg=5042.58, stdev=2914.05
     lat (usec): min=29, max=29694, avg=92.98, stdev=243.93
    clat percentiles (msec):
     |  1.00th=[  199],  5.00th=[  558], 10.00th=[ 1020], 20.00th=[ 1989],
     | 30.00th=[ 3004], 40.00th=[ 4010], 50.00th=[ 5000], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=37040, max=44728, per=100.00%, avg=39848.42, stdev=2091.98, samples=19
   iops        : min= 9260, max=11182, avg=9962.11, stdev=522.99, samples=19
  write: IOPS=9923, BW=38.8MiB/s (40.6MB/s)(388MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=106, max=10105, avg=5054.29, stdev=2923.99
     lat (usec): min=49, max=30133, avg=105.98, stdev=311.05
    clat percentiles (msec):
     |  1.00th=[  194],  5.00th=[  550], 10.00th=[ 1020], 20.00th=[ 1989],
     | 30.00th=[ 3004], 40.00th=[ 4010], 50.00th=[ 5067], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=36936, max=45000, per=100.00%, avg=39731.37, stdev=2270.66, samples=19
   iops        : min= 9234, max=11250, avg=9932.84, stdev=567.66, samples=19
  lat (msec)   : 250=1.59%, 500=2.81%, 750=2.78%, 1000=2.60%, 2000=10.31%
  lat (msec)   : >=2000=79.90%
  cpu          : usr=12.49%, sys=36.49%, ctx=103433, majf=0, minf=43
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=99359,99240,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=38.8MiB/s (40.7MB/s), 38.8MiB/s-38.8MiB/s (40.7MB/s-40.7MB/s), io=388MiB (407MB), run=10001-10001msec
  WRITE: bw=38.8MiB/s (40.6MB/s), 38.8MiB/s-38.8MiB/s (40.6MB/s-40.6MB/s), io=388MiB (406MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=15/147, sectors=744/38048, merge=0/1041, ticks=5/243, in_queue=253, util=0.23%
```
