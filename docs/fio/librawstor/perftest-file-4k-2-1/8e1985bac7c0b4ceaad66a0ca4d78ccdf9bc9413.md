[&lt; back](..)

# perftest-file-4k-2-1

2026-11-24 21:37:09

refs/heads/worktree-pki-show-positional

[8e1985b](https://github.com/rawstor/librawstor/commit/8e1985bac7c0b4ceaad66a0ca4d78ccdf9bc9413)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16596: Tue Nov 24 21:36:27 2026
  read: IOPS=799k, BW=3120MiB/s (3272MB/s)(30.5GiB/10001msec)
    slat (nsec): min=180, max=170928, avg=235.44, stdev=294.17
    clat (nsec): min=1530, max=189811, avg=2134.52, stdev=969.74
     lat (nsec): min=1765, max=197446, avg=2369.96, stdev=1034.08
    clat percentiles (nsec):
     |  1.00th=[ 1816],  5.00th=[ 1896], 10.00th=[ 1928], 20.00th=[ 1976],
     | 30.00th=[ 2008], 40.00th=[ 2040], 50.00th=[ 2064], 60.00th=[ 2096],
     | 70.00th=[ 2128], 80.00th=[ 2192], 90.00th=[ 2256], 95.00th=[ 2320],
     | 99.00th=[ 2544], 99.50th=[ 2960], 99.90th=[21888], 99.95th=[23424],
     | 99.99th=[24448]
   bw (  MiB/s): min= 3074, max= 3153, per=100.00%, avg=3121.50, stdev=21.34, samples=20
   iops        : min=786981, max=807216, avg=799104.80, stdev=5463.59, samples=20
  lat (usec)   : 2=26.36%, 4=73.27%, 10=0.10%, 20=0.12%, 50=0.15%
  lat (usec)   : 100=0.01%, 250=0.01%
  cpu          : usr=47.16%, sys=52.82%, ctx=40, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=7987866,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=16600: Tue Nov 24 21:36:27 2026
  write: IOPS=9966, BW=38.9MiB/s (40.8MB/s)(389MiB/10001msec); 0 zone resets
    slat (nsec): min=424, max=36340, avg=1215.03, stdev=1012.16
    clat (usec): min=108, max=6953, avg=198.94, stdev=72.67
     lat (usec): min=109, max=6958, avg=200.16, stdev=72.67
    clat percentiles (usec):
     |  1.00th=[  145],  5.00th=[  155], 10.00th=[  157], 20.00th=[  165],
     | 30.00th=[  169], 40.00th=[  172], 50.00th=[  176], 60.00th=[  184],
     | 70.00th=[  194], 80.00th=[  219], 90.00th=[  302], 95.00th=[  322],
     | 99.00th=[  367], 99.50th=[  383], 99.90th=[  424], 99.95th=[  441],
     | 99.99th=[ 3064]
   bw (  KiB/s): min=37912, max=40777, per=100.00%, avg=39880.80, stdev=628.27, samples=20
   iops        : min= 9478, max=10194, avg=9970.15, stdev=157.04, samples=20
  lat (usec)   : 250=84.41%, 500=15.56%, 750=0.01%, 1000=0.01%
  lat (msec)   : 2=0.01%, 4=0.01%, 10=0.01%
  cpu          : usr=4.07%, sys=3.16%, ctx=100322, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,99673,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=3120MiB/s (3272MB/s), 3120MiB/s-3120MiB/s (3272MB/s-3272MB/s), io=30.5GiB (32.7GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=38.9MiB/s (40.8MB/s), 38.9MiB/s-38.9MiB/s (40.8MB/s-40.8MB/s), io=389MiB (408MB), run=10001-10001msec

Disk stats (read/write):
    dm-0: ios=0/632918, sectors=0/5063344, merge=0/0, ticks=0/216351, in_queue=216351, util=34.60%, aggrios=0/168255, aggsectors=0/2871224, aggrmerge=0/190648, aggrticks=0/7252, aggrin_queue=7252, aggrutil=32.29%
  nvme0n1: ios=0/0, sectors=0/0, merge=0/0, ticks=0/0, in_queue=0, util=0.00%
  nvme1n1: ios=0/336510, sectors=0/5742448, merge=0/381296, ticks=0/14505, in_queue=14504, util=32.29%
```
