[&lt; back](..)

# perftest--without-liburing-file-4k-1-1

2025-10-24 07:31:01

refs/heads/ci/packages

[dbbc9bc](https://github.com/rawstor/librawstor/commit/dbbc9bcbb4cccdc4988920db56d816ba41b49be3)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11065: Fri Oct 24 07:30:59 2025
  read: IOPS=166k, BW=650MiB/s (682MB/s)(6503MiB/10001msec)
    slat (nsec): min=9, max=14938, avg=28.59, stdev=52.66
    clat (nsec): min=1673, max=128890, avg=2369.74, stdev=1279.75
     lat (nsec): min=1703, max=128920, avg=2398.33, stdev=1281.94
    clat percentiles (nsec):
     |  1.00th=[ 1960],  5.00th=[ 2008], 10.00th=[ 2040], 20.00th=[ 2096],
     | 30.00th=[ 2096], 40.00th=[ 2128], 50.00th=[ 2160], 60.00th=[ 2160],
     | 70.00th=[ 2224], 80.00th=[ 2256], 90.00th=[ 2448], 95.00th=[ 3504],
     | 99.00th=[ 7008], 99.50th=[11072], 99.90th=[17536], 99.95th=[21120],
     | 99.99th=[30080]
   bw (  KiB/s): min=367232, max=736976, per=99.52%, avg=662672.42, stdev=116350.70, samples=19
   iops        : min=91808, max=184244, avg=165668.11, stdev=29087.68, samples=19
  write: IOPS=166k, BW=650MiB/s (681MB/s)(6498MiB/10001msec); 0 zone resets
    slat (nsec): min=29, max=25247, avg=42.60, stdev=71.23
    clat (usec): min=2, max=112, avg= 3.04, stdev= 1.21
     lat (usec): min=2, max=112, avg= 3.08, stdev= 1.21
    clat percentiles (nsec):
     |  1.00th=[ 2416],  5.00th=[ 2480], 10.00th=[ 2480], 20.00th=[ 2512],
     | 30.00th=[ 2544], 40.00th=[ 2576], 50.00th=[ 2608], 60.00th=[ 2640],
     | 70.00th=[ 2672], 80.00th=[ 2864], 90.00th=[ 4832], 95.00th=[ 5216],
     | 99.00th=[ 6368], 99.50th=[ 8032], 99.90th=[14528], 99.95th=[16512],
     | 99.99th=[25472]
   bw (  KiB/s): min=367984, max=736128, per=99.48%, avg=661935.16, stdev=116098.33, samples=19
   iops        : min=91996, max=184032, avg=165483.79, stdev=29024.58, samples=19
  lat (usec)   : 2=1.65%, 4=88.87%, 10=9.03%, 20=0.41%, 50=0.04%
  lat (usec)   : 100=0.01%, 250=0.01%
  cpu          : usr=30.02%, sys=69.96%, ctx=87, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=1664825,1663602,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=650MiB/s (682MB/s), 650MiB/s-650MiB/s (682MB/s-682MB/s), io=6503MiB (6819MB), run=10001-10001msec
  WRITE: bw=650MiB/s (681MB/s), 650MiB/s-650MiB/s (681MB/s-681MB/s), io=6498MiB (6814MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/2, sectors=0/16, merge=0/0, ticks=0/1, in_queue=0, util=0.00%
```
