[&lt; back](..)

# perftest--without-liburing-file-4k-1-1

2026-11-20 11:26:39

refs/heads/main

[e17954e](https://github.com/rawstor/librawstor/commit/e17954e199dd27edbf1c0dcbd8c13c5fdf2d58fc)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16456: Fri Nov 20 11:25:55 2026
  read: IOPS=546k, BW=2133MiB/s (2237MB/s)(20.8GiB/10001msec)
    slat (nsec): min=189, max=101851, avg=298.12, stdev=262.49
    clat (nsec): min=848, max=112593, avg=1398.77, stdev=611.31
     lat (nsec): min=1060, max=112865, avg=1696.89, stdev=684.69
    clat percentiles (nsec):
     |  1.00th=[ 1048],  5.00th=[ 1128], 10.00th=[ 1176], 20.00th=[ 1256],
     | 30.00th=[ 1304], 40.00th=[ 1336], 50.00th=[ 1384], 60.00th=[ 1416],
     | 70.00th=[ 1448], 80.00th=[ 1496], 90.00th=[ 1544], 95.00th=[ 1608],
     | 99.00th=[ 1784], 99.50th=[ 1992], 99.90th=[15680], 99.95th=[16512],
     | 99.99th=[17280]
   bw (  MiB/s): min= 2084, max= 2167, per=100.00%, avg=2134.65, stdev=24.39, samples=20
   iops        : min=533642, max=554765, avg=546470.15, stdev=6244.56, samples=20
  lat (nsec)   : 1000=0.26%
  lat (usec)   : 2=99.24%, 4=0.31%, 10=0.05%, 20=0.14%, 50=0.01%
  lat (usec)   : 100=0.01%, 250=0.01%
  cpu          : usr=51.12%, sys=48.86%, ctx=59, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=5461236,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16459: Fri Nov 20 11:25:55 2026
  write: IOPS=4799, BW=18.7MiB/s (19.7MB/s)(188MiB/10001msec); 0 zone resets
    slat (nsec): min=871, max=24902, avg=1332.35, stdev=1003.83
    clat (usec): min=118, max=4725, avg=206.42, stdev=90.66
     lat (usec): min=119, max=4731, avg=207.75, stdev=90.79
    clat percentiles (usec):
     |  1.00th=[  141],  5.00th=[  149], 10.00th=[  153], 20.00th=[  161],
     | 30.00th=[  169], 40.00th=[  178], 50.00th=[  186], 60.00th=[  196],
     | 70.00th=[  208], 80.00th=[  229], 90.00th=[  273], 95.00th=[  330],
     | 99.00th=[  562], 99.50th=[  635], 99.90th=[  848], 99.95th=[ 1004],
     | 99.99th=[ 3523]
   bw (  KiB/s): min=13976, max=24648, per=100.00%, avg=19209.45, stdev=3047.92, samples=20
   iops        : min= 3494, max= 6162, avg=4802.30, stdev=761.97, samples=20
  lat (usec)   : 250=86.12%, 500=12.33%, 750=1.35%, 1000=0.15%
  lat (msec)   : 2=0.03%, 4=0.02%, 10=0.01%
  cpu          : usr=2.64%, sys=10.47%, ctx=97189, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,48001,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=2133MiB/s (2237MB/s), 2133MiB/s-2133MiB/s (2237MB/s-2237MB/s), io=20.8GiB (22.4GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=18.7MiB/s (19.7MB/s), 18.7MiB/s-18.7MiB/s (19.7MB/s-19.7MB/s), io=188MiB (197MB), run=10001-10001msec

Disk stats (read/write):
    dm-0: ios=0/420342, sectors=0/3362736, merge=0/0, ticks=0/198313, in_queue=198313, util=34.02%, aggrios=0/116527, aggsectors=0/1954256, aggrmerge=0/127754, aggrticks=0/9654, aggrin_queue=9654, aggrutil=30.88%
  nvme0n1: ios=0/0, sectors=0/0, merge=0/0, ticks=0/0, in_queue=0, util=0.00%
  nvme1n1: ios=0/233055, sectors=0/3908512, merge=0/255509, ticks=0/19309, in_queue=19309, util=30.88%
```
