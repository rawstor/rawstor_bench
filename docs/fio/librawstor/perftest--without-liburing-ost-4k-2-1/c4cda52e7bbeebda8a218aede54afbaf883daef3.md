[&lt; back](..)

# perftest--without-liburing-ost-4k-2-1

2025-10-19 09:56:50

refs/heads/feat/ci

[c4cda52](https://github.com/rawstor/librawstor/commit/c4cda52e7bbeebda8a218aede54afbaf883daef3)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11763: Sun Oct 19 09:56:48 2025
  read: IOPS=9546, BW=37.3MiB/s (39.1MB/s)(373MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=111, max=10111, avg=5068.50, stdev=2890.97
     lat (usec): min=28, max=28402, avg=97.60, stdev=269.59
    clat percentiles (msec):
     |  1.00th=[  226],  5.00th=[  609], 10.00th=[ 1045], 20.00th=[ 2072],
     | 30.00th=[ 3071], 40.00th=[ 4077], 50.00th=[ 5000], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=35568, max=43608, per=100.00%, avg=38190.80, stdev=1951.52, samples=20
   iops        : min= 8892, max=10902, avg=9547.70, stdev=487.88, samples=20
  write: IOPS=9528, BW=37.2MiB/s (39.0MB/s)(372MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=112, max=10111, avg=5077.09, stdev=2900.39
     lat (usec): min=46, max=28416, avg=109.62, stdev=227.33
    clat percentiles (msec):
     |  1.00th=[  220],  5.00th=[  600], 10.00th=[ 1045], 20.00th=[ 2056],
     | 30.00th=[ 3071], 40.00th=[ 4077], 50.00th=[ 5067], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10134], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=35736, max=42880, per=100.00%, avg=38116.00, stdev=1701.58, samples=20
   iops        : min= 8934, max=10720, avg=9529.00, stdev=425.40, samples=20
  lat (msec)   : 250=1.27%, 500=2.57%, 750=2.80%, 1000=2.91%, 2000=10.08%
  lat (msec)   : >=2000=80.38%
  cpu          : usr=11.78%, sys=36.75%, ctx=100793, majf=0, minf=42
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=95477,95290,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=37.3MiB/s (39.1MB/s), 37.3MiB/s-37.3MiB/s (39.1MB/s-39.1MB/s), io=373MiB (391MB), run=10001-10001msec
  WRITE: bw=37.2MiB/s (39.0MB/s), 37.2MiB/s-37.2MiB/s (39.0MB/s-39.0MB/s), io=372MiB (390MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/336, sectors=0/42688, merge=0/1398, ticks=0/185, in_queue=191, util=0.26%
```
