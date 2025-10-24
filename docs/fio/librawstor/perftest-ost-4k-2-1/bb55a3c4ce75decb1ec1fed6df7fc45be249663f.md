[&lt; back](..)

# perftest-ost-4k-2-1

2025-10-24 06:48:26

refs/heads/ci/packages

[bb55a3c](https://github.com/rawstor/librawstor/commit/bb55a3c4ce75decb1ec1fed6df7fc45be249663f)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11886: Fri Oct 24 06:48:24 2025
  read: IOPS=10.7k, BW=41.7MiB/s (43.7MB/s)(417MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=106, max=10105, avg=5044.50, stdev=2907.77
     lat (usec): min=27, max=32320, avg=79.56, stdev=249.05
    clat percentiles (msec):
     |  1.00th=[  215],  5.00th=[  592], 10.00th=[ 1036], 20.00th=[ 1989],
     | 30.00th=[ 2970], 40.00th=[ 4010], 50.00th=[ 5067], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=39816, max=48088, per=100.00%, avg=42688.84, stdev=2221.30, samples=19
   iops        : min= 9954, max=12022, avg=10672.21, stdev=555.32, samples=19
  write: IOPS=10.6k, BW=41.6MiB/s (43.6MB/s)(416MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=106, max=10105, avg=5049.42, stdev=2911.86
     lat (usec): min=41, max=35648, avg=105.40, stdev=365.02
    clat percentiles (msec):
     |  1.00th=[  211],  5.00th=[  584], 10.00th=[ 1036], 20.00th=[ 1972],
     | 30.00th=[ 2970], 40.00th=[ 4010], 50.00th=[ 5067], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=39976, max=47616, per=100.00%, avg=42612.63, stdev=2041.78, samples=19
   iops        : min= 9994, max=11904, avg=10653.16, stdev=510.44, samples=19
  lat (msec)   : 250=1.37%, 500=2.64%, 750=2.81%, 1000=2.77%, 2000=10.65%
  lat (msec)   : >=2000=79.76%
  cpu          : usr=11.06%, sys=50.07%, ctx=137655, majf=0, minf=42
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=106722,106477,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=41.7MiB/s (43.7MB/s), 41.7MiB/s-41.7MiB/s (43.7MB/s-43.7MB/s), io=417MiB (437MB), run=10001-10001msec
  WRITE: bw=41.6MiB/s (43.6MB/s), 41.6MiB/s-41.6MiB/s (43.6MB/s-43.6MB/s), io=416MiB (436MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/126, sectors=0/36640, merge=0/1073, ticks=0/244, in_queue=251, util=0.15%
```
