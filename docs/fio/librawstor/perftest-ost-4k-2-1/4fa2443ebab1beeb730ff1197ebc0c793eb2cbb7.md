[&lt; back](..)

# perftest-ost-4k-2-1

2025-10-27 07:30:56

refs/heads/releases/v0.0

[4fa2443](https://github.com/rawstor/librawstor/commit/4fa2443ebab1beeb730ff1197ebc0c793eb2cbb7)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11958: Mon Oct 27 07:30:54 2025
  read: IOPS=10.4k, BW=40.7MiB/s (42.7MB/s)(407MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=106, max=10105, avg=5064.39, stdev=2910.21
     lat (usec): min=24, max=36443, avg=81.63, stdev=296.28
    clat percentiles (msec):
     |  1.00th=[  213],  5.00th=[  592], 10.00th=[ 1045], 20.00th=[ 1989],
     | 30.00th=[ 3004], 40.00th=[ 4044], 50.00th=[ 5067], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=38840, max=46416, per=100.00%, avg=41661.60, stdev=2024.03, samples=20
   iops        : min= 9710, max=11604, avg=10415.40, stdev=506.01, samples=20
  write: IOPS=10.4k, BW=40.6MiB/s (42.6MB/s)(406MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=106, max=10105, avg=5073.05, stdev=2916.91
     lat (usec): min=47, max=35089, avg=107.81, stdev=380.43
    clat percentiles (msec):
     |  1.00th=[  209],  5.00th=[  584], 10.00th=[ 1045], 20.00th=[ 1989],
     | 30.00th=[ 2970], 40.00th=[ 4044], 50.00th=[ 5067], 60.00th=[ 6074],
     | 70.00th=[ 7148], 80.00th=[ 8154], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=38264, max=45888, per=100.00%, avg=41593.20, stdev=1947.47, samples=20
   iops        : min= 9566, max=11472, avg=10398.30, stdev=486.87, samples=20
  lat (msec)   : 250=1.39%, 500=2.70%, 750=2.77%, 1000=2.67%, 2000=10.63%
  lat (msec)   : >=2000=79.85%
  cpu          : usr=10.62%, sys=50.09%, ctx=136598, majf=0, minf=41
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=104154,103983,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=40.7MiB/s (42.7MB/s), 40.7MiB/s-40.7MiB/s (42.7MB/s-42.7MB/s), io=407MiB (427MB), run=10001-10001msec
  WRITE: bw=40.6MiB/s (42.6MB/s), 40.6MiB/s-40.6MiB/s (42.6MB/s-42.6MB/s), io=406MiB (426MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/263, sectors=0/42328, merge=0/1308, ticks=0/342, in_queue=348, util=0.25%
```
