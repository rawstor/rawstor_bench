[&lt; back](..)

# perftest--without-liburing-ost-4k-2-1

2025-10-24 07:15:18

refs/heads/ci/packages

[cdec14c](https://github.com/rawstor/librawstor/commit/cdec14c0f1cf5df283d6f4d7ca9b9c8cfe1400b4)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=12036: Fri Oct 24 07:15:16 2025
  read: IOPS=9818, BW=38.4MiB/s (40.2MB/s)(384MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10104, avg=5062.21, stdev=2900.99
     lat (usec): min=31, max=33542, avg=94.37, stdev=257.03
    clat percentiles (msec):
     |  1.00th=[  215],  5.00th=[  575], 10.00th=[ 1003], 20.00th=[ 2039],
     | 30.00th=[ 3037], 40.00th=[ 4077], 50.00th=[ 5067], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=36112, max=45448, per=100.00%, avg=39279.20, stdev=1951.06, samples=20
   iops        : min= 9028, max=11362, avg=9819.80, stdev=487.76, samples=20
  write: IOPS=9800, BW=38.3MiB/s (40.1MB/s)(383MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10105, avg=5070.87, stdev=2909.65
     lat (usec): min=45, max=33538, avg=106.99, stdev=286.70
    clat percentiles (msec):
     |  1.00th=[  209],  5.00th=[  567], 10.00th=[ 1003], 20.00th=[ 2022],
     | 30.00th=[ 3037], 40.00th=[ 4077], 50.00th=[ 5067], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=36240, max=44688, per=100.00%, avg=39206.80, stdev=1914.01, samples=20
   iops        : min= 9060, max=11172, avg=9801.70, stdev=478.50, samples=20
  lat (msec)   : 250=1.38%, 500=2.87%, 750=2.87%, 1000=2.85%, 2000=9.76%
  lat (msec)   : >=2000=80.26%
  cpu          : usr=12.78%, sys=36.18%, ctx=101741, majf=0, minf=43
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=98198,98017,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=38.4MiB/s (40.2MB/s), 38.4MiB/s-38.4MiB/s (40.2MB/s-40.2MB/s), io=384MiB (402MB), run=10001-10001msec
  WRITE: bw=38.3MiB/s (40.1MB/s), 38.3MiB/s-38.3MiB/s (40.1MB/s-40.1MB/s), io=383MiB (401MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/296, sectors=0/48688, merge=0/1436, ticks=0/1163, in_queue=1170, util=0.19%
```
