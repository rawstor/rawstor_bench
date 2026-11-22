[&lt; back](..)

# perftest--without-liburing-ost-4k-1-1

2026-11-22 13:26:06

refs/heads/releases/v0.3

[fba59c4](https://github.com/rawstor/librawstor/commit/fba59c4e9eafea1009c7fb6fd0dd9076edea69ff)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16460: Sun Nov 22 13:25:27 2026
  read: IOPS=23.7k, BW=92.6MiB/s (97.1MB/s)(926MiB/10001msec)
    slat (nsec): min=973, max=35494, avg=1288.81, stdev=723.20
    clat (usec): min=20, max=1075, avg=40.66, stdev=14.90
     lat (usec): min=21, max=1077, avg=41.95, stdev=14.95
    clat percentiles (usec):
     |  1.00th=[   21],  5.00th=[   22], 10.00th=[   22], 20.00th=[   23],
     | 30.00th=[   28], 40.00th=[   46], 50.00th=[   46], 60.00th=[   47],
     | 70.00th=[   48], 80.00th=[   50], 90.00th=[   54], 95.00th=[   58],
     | 99.00th=[   69], 99.50th=[   72], 99.90th=[  113], 99.95th=[  239],
     | 99.99th=[  363]
   bw (  KiB/s): min=80352, max=119472, per=100.00%, avg=94862.95, stdev=12684.99, samples=20
   iops        : min=20088, max=29868, avg=23715.65, stdev=3171.29, samples=20
  lat (usec)   : 50=81.64%, 100=18.24%, 250=0.07%, 500=0.04%, 750=0.01%
  lat (usec)   : 1000=0.01%
  lat (msec)   : 2=0.01%
  cpu          : usr=15.41%, sys=25.55%, ctx=237039, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=237035,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16464: Sun Nov 22 13:25:27 2026
  write: IOPS=4495, BW=17.6MiB/s (18.4MB/s)(176MiB/10001msec); 0 zone resets
    slat (nsec): min=1794, max=75847, avg=3461.95, stdev=2374.89
    clat (usec): min=145, max=1738, avg=218.45, stdev=33.85
     lat (usec): min=148, max=1741, avg=221.91, stdev=33.94
    clat percentiles (usec):
     |  1.00th=[  174],  5.00th=[  182], 10.00th=[  188], 20.00th=[  196],
     | 30.00th=[  202], 40.00th=[  208], 50.00th=[  215], 60.00th=[  223],
     | 70.00th=[  231], 80.00th=[  237], 90.00th=[  247], 95.00th=[  258],
     | 99.00th=[  347], 99.50th=[  412], 99.90th=[  510], 99.95th=[  570],
     | 99.99th=[  775]
   bw (  KiB/s): min=16960, max=19368, per=100.00%, avg=17991.25, stdev=655.63, samples=20
   iops        : min= 4240, max= 4842, avg=4497.70, stdev=163.94, samples=20
  lat (usec)   : 250=92.50%, 500=7.39%, 750=0.10%, 1000=0.01%
  lat (msec)   : 2=0.01%
  cpu          : usr=5.40%, sys=5.14%, ctx=44962, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,44958,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=92.6MiB/s (97.1MB/s), 92.6MiB/s-92.6MiB/s (97.1MB/s-97.1MB/s), io=926MiB (971MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=17.6MiB/s (18.4MB/s), 17.6MiB/s-17.6MiB/s (18.4MB/s-18.4MB/s), io=176MiB (184MB), run=10001-10001msec

Disk stats (read/write):
    dm-0: ios=0/320808, sectors=0/2566464, merge=0/0, ticks=0/55635, in_queue=55635, util=23.83%, aggrios=0/105333, aggsectors=0/1530716, aggrmerge=0/86006, aggrticks=0/3721, aggrin_queue=3721, aggrutil=20.88%
  nvme0n1: ios=0/0, sectors=0/0, merge=0/0, ticks=0/0, in_queue=0, util=0.00%
  nvme1n1: ios=0/210667, sectors=0/3061432, merge=0/172012, ticks=0/7443, in_queue=7443, util=20.88%
```
