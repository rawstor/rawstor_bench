[&lt; back](..)

# perftest--without-liburing-ost-4k-2-1

2025-10-24 07:31:19

refs/heads/ci/packages

[dbbc9bc](https://github.com/rawstor/librawstor/commit/dbbc9bcbb4cccdc4988920db56d816ba41b49be3)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=12096: Fri Oct 24 07:31:18 2025
  read: IOPS=14.5k, BW=56.7MiB/s (59.4MB/s)(567MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=106, max=10105, avg=5096.32, stdev=2921.43
     lat (usec): min=18, max=57933, avg=63.50, stdev=458.20
    clat percentiles (msec):
     |  1.00th=[  213],  5.00th=[  575], 10.00th=[ 1036], 20.00th=[ 2039],
     | 30.00th=[ 3037], 40.00th=[ 4077], 50.00th=[ 5067], 60.00th=[ 6141],
     | 70.00th=[ 7148], 80.00th=[ 8154], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10134], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=53088, max=62864, per=99.81%, avg=57932.21, stdev=2810.05, samples=19
   iops        : min=13272, max=15716, avg=14483.05, stdev=702.51, samples=19
  write: IOPS=14.5k, BW=56.7MiB/s (59.5MB/s)(567MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=107, max=10106, avg=5111.57, stdev=2924.86
     lat (usec): min=25, max=57449, avg=72.75, stdev=431.98
    clat percentiles (msec):
     |  1.00th=[  209],  5.00th=[  575], 10.00th=[ 1045], 20.00th=[ 2039],
     | 30.00th=[ 3037], 40.00th=[ 4077], 50.00th=[ 5134], 60.00th=[ 6141],
     | 70.00th=[ 7148], 80.00th=[ 8154], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10134], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=52968, max=63720, per=99.82%, avg=57996.21, stdev=3309.63, samples=19
   iops        : min=13242, max=15930, avg=14499.05, stdev=827.41, samples=19
  lat (msec)   : 250=1.36%, 500=2.78%, 750=2.67%, 1000=2.70%, 2000=10.11%
  lat (msec)   : >=2000=80.36%
  cpu          : usr=13.14%, sys=29.74%, ctx=158756, majf=0, minf=45
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=145116,145272,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=56.7MiB/s (59.4MB/s), 56.7MiB/s-56.7MiB/s (59.4MB/s-59.4MB/s), io=567MiB (594MB), run=10001-10001msec
  WRITE: bw=56.7MiB/s (59.5MB/s), 56.7MiB/s-56.7MiB/s (59.5MB/s-59.5MB/s), io=567MiB (595MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/214, sectors=0/48560, merge=0/1168, ticks=0/281, in_queue=286, util=0.17%
```
