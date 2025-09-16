[&lt; back](..)

# perftest--without-liburing-4k-1-1

2025-09-16 21:10:46

refs/heads/main

[9d9df2b](https://github.com/rawstor/librawstor/commit/9d9df2b96b23beff9fd3f0c0ca8afee0afc169a1)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11448: Tue Sep 16 21:10:45 2025
  read: IOPS=5047, BW=19.7MiB/s (20.7MB/s)(197MiB/10001msec)
    slat (nsec): min=50, max=21480, avg=209.33, stdev=249.26
    clat (usec): min=45, max=76856, avg=82.33, stdev=413.79
     lat (usec): min=45, max=76857, avg=82.54, stdev=413.79
    clat percentiles (usec):
     |  1.00th=[   58],  5.00th=[   62], 10.00th=[   67], 20.00th=[   71],
     | 30.00th=[   74], 40.00th=[   76], 50.00th=[   78], 60.00th=[   81],
     | 70.00th=[   83], 80.00th=[   87], 90.00th=[   94], 95.00th=[  101],
     | 99.00th=[  120], 99.50th=[  128], 99.90th=[  159], 99.95th=[  198],
     | 99.99th=[ 2343]
   bw (  KiB/s): min=16544, max=23616, per=100.00%, avg=20200.00, stdev=2034.88, samples=19
   iops        : min= 4136, max= 5904, avg=5050.00, stdev=508.72, samples=19
  write: IOPS=5023, BW=19.6MiB/s (20.6MB/s)(196MiB/10001msec); 0 zone resets
    slat (nsec): min=101, max=28333, avg=307.86, stdev=370.03
    clat (usec): min=61, max=86675, avg=111.93, stdev=639.71
     lat (usec): min=62, max=86675, avg=112.24, stdev=639.71
    clat percentiles (usec):
     |  1.00th=[   82],  5.00th=[   87], 10.00th=[   91], 20.00th=[   96],
     | 30.00th=[   99], 40.00th=[  102], 50.00th=[  104], 60.00th=[  106],
     | 70.00th=[  110], 80.00th=[  114], 90.00th=[  121], 95.00th=[  128],
     | 99.00th=[  145], 99.50th=[  155], 99.90th=[  212], 99.95th=[  392],
     | 99.99th=[11207]
   bw (  KiB/s): min=16808, max=22992, per=99.95%, avg=20082.37, stdev=1872.07, samples=19
   iops        : min= 4202, max= 5748, avg=5020.58, stdev=468.00, samples=19
  lat (usec)   : 50=0.01%, 100=64.41%, 250=35.53%, 500=0.03%, 750=0.01%
  lat (usec)   : 1000=0.01%
  lat (msec)   : 2=0.01%, 4=0.01%, 10=0.01%, 20=0.01%, 50=0.01%
  lat (msec)   : 100=0.01%
  cpu          : usr=8.63%, sys=30.02%, ctx=100819, majf=0, minf=293
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=50482,50236,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=19.7MiB/s (20.7MB/s), 19.7MiB/s-19.7MiB/s (20.7MB/s-20.7MB/s), io=197MiB (207MB), run=10001-10001msec
  WRITE: bw=19.6MiB/s (20.6MB/s), 19.6MiB/s-19.6MiB/s (20.6MB/s-20.6MB/s), io=196MiB (206MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/191, sectors=0/36472, merge=0/828, ticks=0/465, in_queue=465, util=0.06%
```
