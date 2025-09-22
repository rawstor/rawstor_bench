[&lt; back](..)

# perftest--without-liburing--disable-ost-4k-1-1

2025-09-22 11:50:41

refs/heads/add/cppost

[c8d8a55](https://github.com/rawstor/librawstor/commit/c8d8a55a02ce3d9eead08e0be4e34e50bdd0c28f)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10498: Mon Sep 22 11:50:39 2025
  read: IOPS=178k, BW=697MiB/s (730MB/s)(6966MiB/10000msec)
    slat (nsec): min=9, max=16311, avg=26.51, stdev=57.26
    clat (nsec): min=1593, max=116887, avg=2211.67, stdev=1192.06
     lat (nsec): min=1613, max=116918, avg=2238.18, stdev=1194.48
    clat percentiles (nsec):
     |  1.00th=[ 1864],  5.00th=[ 1896], 10.00th=[ 1928], 20.00th=[ 1944],
     | 30.00th=[ 1960], 40.00th=[ 1992], 50.00th=[ 2008], 60.00th=[ 2040],
     | 70.00th=[ 2064], 80.00th=[ 2128], 90.00th=[ 2256], 95.00th=[ 3312],
     | 99.00th=[ 6624], 99.50th=[10560], 99.90th=[16512], 99.95th=[19584],
     | 99.99th=[28288]
   bw (  KiB/s): min=383960, max=787448, per=99.47%, avg=709550.32, stdev=126731.49, samples=19
   iops        : min=95990, max=196862, avg=177387.58, stdev=31682.87, samples=19
  write: IOPS=178k, BW=696MiB/s (730MB/s)(6958MiB/10000msec); 0 zone resets
    slat (nsec): min=29, max=18505, avg=40.11, stdev=63.34
    clat (usec): min=2, max=123, avg= 2.82, stdev= 1.12
     lat (usec): min=2, max=123, avg= 2.86, stdev= 1.12
    clat percentiles (nsec):
     |  1.00th=[ 2288],  5.00th=[ 2320], 10.00th=[ 2320], 20.00th=[ 2352],
     | 30.00th=[ 2384], 40.00th=[ 2384], 50.00th=[ 2416], 60.00th=[ 2448],
     | 70.00th=[ 2512], 80.00th=[ 2640], 90.00th=[ 4512], 95.00th=[ 4832],
     | 99.00th=[ 5856], 99.50th=[ 7264], 99.90th=[14144], 99.95th=[15680],
     | 99.99th=[20352]
   bw (  KiB/s): min=384616, max=786848, per=99.51%, avg=708979.37, stdev=126633.33, samples=19
   iops        : min=96154, max=196712, avg=177244.84, stdev=31658.33, samples=19
  lat (usec)   : 2=22.58%, 4=69.04%, 10=7.96%, 20=0.38%, 50=0.03%
  lat (usec)   : 100=0.01%, 250=0.01%
  cpu          : usr=28.27%, sys=71.70%, ctx=79, majf=0, minf=34
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=1783283,1781257,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=697MiB/s (730MB/s), 697MiB/s-697MiB/s (730MB/s-730MB/s), io=6966MiB (7304MB), run=10000-10000msec
  WRITE: bw=696MiB/s (730MB/s), 696MiB/s-696MiB/s (730MB/s-730MB/s), io=6958MiB (7296MB), run=10000-10000msec

Disk stats (read/write):
  sdb: ios=0/3, sectors=0/464, merge=0/9, ticks=0/1, in_queue=0, util=0.00%
```
