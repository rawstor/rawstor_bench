[&lt; back](..)

# perftest--without-liburing-4k-2-1

2025-09-22 11:50:56

refs/heads/add/cppost

[c8d8a55](https://github.com/rawstor/librawstor/commit/c8d8a55a02ce3d9eead08e0be4e34e50bdd0c28f)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11375: Mon Sep 22 11:50:54 2025
  read: IOPS=9643, BW=37.7MiB/s (39.5MB/s)(377MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=106, max=10105, avg=5032.11, stdev=2905.02
     lat (usec): min=30, max=34833, avg=96.30, stdev=281.98
    clat percentiles (msec):
     |  1.00th=[  213],  5.00th=[  567], 10.00th=[  995], 20.00th=[ 2005],
     | 30.00th=[ 3004], 40.00th=[ 4010], 50.00th=[ 5000], 60.00th=[ 6007],
     | 70.00th=[ 7013], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=35624, max=45256, per=100.00%, avg=38577.60, stdev=2223.76, samples=20
   iops        : min= 8906, max=11314, avg=9644.40, stdev=555.94, samples=20
  write: IOPS=9627, BW=37.6MiB/s (39.4MB/s)(376MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=107, max=10105, avg=5041.86, stdev=2914.77
     lat (usec): min=50, max=34815, avg=108.79, stdev=285.28
    clat percentiles (msec):
     |  1.00th=[  209],  5.00th=[  558], 10.00th=[  995], 20.00th=[ 2005],
     | 30.00th=[ 3004], 40.00th=[ 4010], 50.00th=[ 5000], 60.00th=[ 6007],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=36080, max=44536, per=100.00%, avg=38512.00, stdev=2016.34, samples=20
   iops        : min= 9020, max=11134, avg=9628.00, stdev=504.09, samples=20
  lat (msec)   : 250=1.45%, 500=2.84%, 750=2.84%, 1000=2.94%, 2000=9.87%
  lat (msec)   : >=2000=80.05%
  cpu          : usr=10.23%, sys=37.22%, ctx=100631, majf=0, minf=296
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=96444,96280,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=37.7MiB/s (39.5MB/s), 37.7MiB/s-37.7MiB/s (39.5MB/s-39.5MB/s), io=377MiB (395MB), run=10001-10001msec
  WRITE: bw=37.6MiB/s (39.4MB/s), 37.6MiB/s-37.6MiB/s (39.4MB/s-39.4MB/s), io=376MiB (394MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/388, sectors=0/241224, merge=0/1784, ticks=0/2562, in_queue=2569, util=0.39%
```
